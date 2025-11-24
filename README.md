# Batch-Processing-to-Streaming-Processing

There are times that building a new batch pipeline anticipated a strong possibility of needing to process data in real time in the future. In this case have to choose the most performant batch processing engine, as that will make it easier to adapt to streaming later. This project demonstrates batch and streaming data processing using PySpark. 
1. **Word Count**
   - Batch: "batch_word_count.ipynb"
   - Text files for batch word count
     
2. **Invoice Processing**
   - Streaming: "streaming_invoice.ipynb"
   - JSON files for streaming customers invoice datasets

## ETL Workflow

The project follows a **three-step ETL process**:

1. **Load raw files into landing zone**
   - Input data is stored in a "data/landing/" folder before processing.
2. **Processing and transformation**
   - Data is cleaned, transformed, and aggregated using PySpark.
3. **Upload final output tables**
   - Final Delta tables are stored in Databricks DBFS for further analytics.

## Development, Test and Production Environments

- **Development Environment**: VS Code
  - All scripts were initially developed and tested locally using VS Code.
  - Linting, debugging were handled in VS Code.
  - Version control were handeled in Git, Github

- **Production and Testing Environment**: Databricks
  - Scripts were tested and run on Databricks clusters to simulate real-world streaming and batch workloads.(a test script was created to automate and test streaming process)
  - Data processing pipelines were validated on Databricks using small sample datasets before scaling.
