# streamset
Building  Data Collector (with streamset data 
collector)  pipelines based on the Basic and Extended
Tutorials .

Basic Tutorial

The basic tutorial creates a pipeline that reads a file from a directory, processes the data in two branches, and writes all data to a file system. You'll use data preview to help configure the pipeline, and you'll create a data alert and run the pipeline.

Here are high level steps for building and running the basic pipeline:
Configure pipeline properties, primarily error handling.
Add a Directory origin to represent the data to be processed.
Preview source data to determine the field-level details needed for the pipeline.
Use a Stream Selector to route credit card transactions to the primary branch and cash transactions to the secondary branch. We'll define a required field to discard records without a payment type.
Configure a Jython Evaluator to perform custom processing that determines the credit card type based on the credit card number.
Add a Field Masker to mask credit card numbers. Use a required field to discard records without credit card numbers.
Connect both branches to a Local FS destination.
In the secondary branch, use an Expression Evaluator to add fields to the cash records to match the credit card records. Use data preview to verify the fields to add.
Add a data rule to raise an alert if too many credit card payments are missing credit card numbers.
Start the pipeline and monitor the results.

![image](https://user-images.githubusercontent.com/75900861/201968255-89d25efc-c7a3-4702-8e32-52263d5ad38f.png)

Extended Tutorial

The extended tutorial builds on the basic tutorial, using an additional set of stages to perform some data transformations and write to the Trash development destination. We'll also use data preview to test stage configuration.

You can write to a real destination instead of the Trash destination. The Trash destination allows you to run the pipeline without writing to a real destination system.

The extended tutorial continues with the following steps:
Configure a Field Type Converter to convert field types.
Manipulate data with the Expression Evaluator.
Use data preview to test and update pipeline configuration.
Complete the pipeline with the placeholder Trash destination.
Reset the origin and run the extended pipeline.
![image](https://user-images.githubusercontent.com/75900861/201968618-cc2cc564-bfba-4fd5-b046-8debfd1f210e.png)



Installation: https://docs.streamsets.com/portal/datacollector/3.22.x/help/datacollector/UserGuide/Installation/InstallationAndConfig.html...
Installation requirements: https://docs.streamsets.com/portal/datacollector/3.22.x/help/datacollector/UserGuide/Installation/InstallationAndConfig.html#concept_vzg_n2p_kq
Tutorial overview: https://docs.streamsets.com/portal/datacollector/3.22.x/help/datacollector/UserGuide/Tutorial/Overview.html
Before you begin (please see the link below for the sample data): https://docs.streamsets.com/portal/datacollector/3.22.x/help/datacollector/UserGuide/Tutorial/BeforeYouBegin.html...
You can download sample data via the following link: https://www.streamsets.com/documentation/datacollector/sample_data/tutorial/nyc_taxi_data.csv
Basic tutorial: https://docs.streamsets.com/portal/datacollector/3.22.x/help/datacollector/UserGuide/Tutorial/BasicTutorial.html
Extended tutorial: https://docs.streamsets.com/portal/datacollector/3.22.x/help/datacollector/UserGuide/Tutorial/ExtendedTutorial.html
