This is a step-by-step descriptions on how I manipulated the Excel data. 

# 1. To create my “Figure 1: Average Individual Income for Immigrants and U.S. Natives in Baltimore”, I first combine two datasets downloaded from the Opportunity Atlas Data, "baltimore_cty_kir_imm _rP_gP_pall" and "baltimore_cty_kir_ native_rP_gP_pall” and form a new excel table named “baltimore_cty_kir_imm_and_native_rP_gP_pall”. 

In the resultant file, I insert a new column in the front named “Imm/Native” to represent if one row belongs to Immigrants or US Native. 
Then, I use the PivotTable, setting ‘Imm/Native’ as CATEGORIES, and “Average of Individual Income for Immigrants” and “Average of Individual Income for Native” as VALUES. 



# 2. To generat4e "Figure3: Average Individual Income Relative to Parent Income for Immigrants in Baltimore": 
For the “imm_parent_child_income_comparisoin” excel book, I download the individual income data from the Opportunity Atlas Data, calculate the average income for different races and different parent income level. 
 
Then, I insert a 2-D line graph and select multiple regions as different Series to draw multiple lines in the same line graph. 
