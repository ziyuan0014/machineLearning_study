# assignment03

### dataset：Cystic Fibrosis RNA-seq
RNA-seq is a technology that allows us to determine the abundance of a gene by capturing the RNA in the tissue and sequencing all the molecules. Genes that have been transcribed more often would have many more molecules to be sequenced. Given the data set used, complete the following tasks：
### assignment：

**Task 1**: Importing Data

1. Load the file 'RNASeqData.xlsx' and save it as a pandas dataframe called data_df.

2. Filter the dataframe to only contain the 60 columns. Call it raw_data.
   Save the "ID" as gene_ids.

**Task 2**: Normalization

1. Calculate the sum of each columns and call this list raw_cols_sums.
2. For each gene, divide it by its corresponding raw_cols_sum.Then multiply it by 1,000,000.
3. Save it as a pandas dataframe called norm_cpm_df.

**Task 3**: Top 10 genes

Let's pretend the top 10 genes are :
top10_ci_genes = ['LOC105372578','MCEMP1','MMP9','SOCS3','ANXA3','G0S2','IL1R2','PFKFB3','OSM','SEMA6B']

1. Filter norm_cpm_df to contain only genes listed above.Call this norm_cpm_df_top10.
   The columns of the dataframe are labeled as such:
   •any column name that has the term HC is a Health Control.
   •any column with Base is a patient with CF but no Treatment.
   •any column with V2 is a CF patient with treatment.
2. Split norm_cpm_df_top10 into 2 different dataframes
   •one with just healthy values , call it hc_top10.
   •one with just CF (Base) values , call it cf_top10.
3. Transpose both dataframes so that the gene ids will now be columns. Call it hc_top10_t and cf_top10_t.
   •Add a new column filled with 0 to hc_top10_t call it Y
   •Add a new column filled with 1 to cf_top10_t call it Y
   （Y is going to be our label）

4. Merge hc_top10_t and cf_top10_t.Call this hc_cf_top10.

**Task 4**: Machine Learning

1. Split hc_cf_top10 into X and Y. Perform SVM using the cross validation function.
   Perform 5x cross validation Try:
   •	different values for C ( less than 1, 1, and greater than 1)
   •	different kernels (linear and radial)
2. Report best combination.
3. Explain how the score that is reported is calculated.

### package：

- numpy
- pandas
- matplotlib
- sklearn
