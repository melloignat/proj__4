## **Project description**

A prototype of a machine learning model for company X. The company develops solutions for the efficient operation of industrial enterprises.
The model must predict the gold recovery rate from gold-bearing ore. You have data on mining and refining parameters.
The model will help optimize production allowing not to launch unprofitable business.

Project is made with **Python** and in **Jupyter Notebook** format.

<hr>

### **Main task**

Prepare the data. Conduct exploratory data analysis. Build and train the model.
Use sMAPE as the final metric. The symmetric mean absolute percentage error (SMAPE or sMAPE) is an accuracy measure based on percentage (or relative) errors.

### **Data description**

* <i>gold_industry_train.csv</i> — training sample;
* <i>gold_industry_test.csv</i> — test sample;
* <i>gold_industry_full.csv</i> — original data.

#### Technological process
<ul>
<li><i>Rougher feed</i> - feedstock</li>
<li><i>Rougher additions (or reagent additions)</i> - flotation reagents: Xanthate, Sulphate, Depressant</li>
<ul>
<li><i>Xanthate</i> — xanthate (promoter, or activator of flotation)</li>
<li><i>Sulphate</i> — sulfate (in this production sodium sulfide)</li>
<li><i>Depressant</i> — depressant (sodium silicate)</li>
</ul>
<li><i>Rougher process</i> — flotation</li>
<li><i>Rougher tails</i> — final tailings</li>
<li><i>Float banks</i> — flotation unit</li>
<li><i>Cleaner process</i> — cleaning</li>
<li><i>Rougher Au</i> — rough gold concentrate</li>
<li><i>Final Au</i> — final gold concentrate</li>
</ul>

#### Stage parameters

<ul>
<li><i>air amount</i> — air volume</li>
<li><i>fluid levels</i> — liquid level</li>
<li><i>feed size</i> — raw material granule size</li>
<li><i>feed rate</i> — feed rate</li>
</ul>

### **Feature name**

Feature name should be as follows:
[stage].[parameter_type].[parameter_name]
Example: rougher.input.feed_ag

#### Possible values ​​for the [stage] block:

<ul>
<li><i>rougher</i> - flotation</li>
<li><i>rougher</i> — flotation</li>
<li><i>primary_cleaner</i> — primary cleaning</li>
<li><i>secondary_cleaner</i> — secondary cleaning</li>
<li><i>final</i> — final characteristics</li>
</ul>

#### Possible values ​​for the [parameter_type] block:

<ul>
<li><i>input</i> — raw material parameters</li>
<li><i>output</i> — product parameters</li>
<li><i>state</i> — parameters characterizing the current state of the stage</li>
<li><i>calculation</i> — calculated characteristics</li>
</ul>
  
### **Project timeline:**

* Prepare the data. Open the files and explore them.
* Check that the enrichment efficiency is calculated correctly. Calculate it on the training set for the rougher.output.recovery feature. Find the MAE between your calculations and the feature value.
* Analyze the features not available in the test dataset.
* Preprocess the data.
* Analyze the data. See how the concentration of metals (Au, Ag, Pb) changes at different stages: in the feedstock, in the rough concentrate, in the concentrate after the first cleaning, and in the final concentrate.
* Compare the distributions of the grain sizes of the feedstock on the training and test sets. If the distributions differ greatly from each other, the model estimate will be incorrect.
* Study the total concentration of metals at different stages: in the feedstock, in the rough concentrate, in the concentrate after the first cleaning, and in the final concentrate.
* Build models.
* Write a function to calculate the final sMAPE metric.
* Train different models and evaluate their quality using cross-validation. Choose the best model and test it on the test set.

<hr>
