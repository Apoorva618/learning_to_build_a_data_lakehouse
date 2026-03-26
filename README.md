
# Databricks for Analysis
The goal was to get comfortable with the interface and write some basic queries to get a hold of the workspace

## ER diagram
![drawSQL-image-export-2026-03-16](https://github.com/user-attachments/assets/8661c2c1-f669-42dd-9586-da3a7a64e141)

## Sales Dashboard
<img width="1738" height="703" alt="Screenshot 2026-03-16 190655" src="https://github.com/user-attachments/assets/0cbf0c8c-e5ea-426f-9856-c9b865ced97e" />

## Customer Dashboard
<img width="1347" height="571" alt="Screenshot 2026-03-22 170639" src="https://github.com/user-attachments/assets/fe7b9cd9-9546-4742-8882-ac92e3f9d6bd" />

## Key Concepts learnt
- How to browse the structure of my data in catalog and how to write queries inside the SQL editor
- How to turn queries into visuals
- How to build dashboards based on user requirements
- How to chat with my data using AI Genie

# Databricks to Design a Lakehouse
The goal was to create a production style lakehouse and implement the medallion architecture on a toy dataset. 

## How did I start? 
Step 1 : Visualize the schema and the possible relationships between the tables 
<img width="743" height="601" alt="image" src="https://github.com/user-attachments/assets/d3bb173c-9405-4795-a841-b12b8f3e81ec" />

Step 2 : Ingest into the Bronze layer

Step 3 : Go through each table and think of transformations that makes the table clean, reliable and ready for business use 

Step 4 : Write (babysit) some pySpark code to make those changes 

Step 5 : Write into the Silver layer once happy

<img width="1229" height="302" alt="silver_data_transformation drawio (1)" src="https://github.com/user-attachments/assets/9515be1c-2fc0-4ed0-b469-9ea47d4b8b77" />

Step 6 : Make the joins to implement a STAR schema
<img width="651" height="431" alt="gold drawio" src="https://github.com/user-attachments/assets/a9959368-b864-41d3-9740-bfeacae0a23f" />

Step 7 : Orchestrate the pipeline and watch your baby go 

## What can business users do with it? 

Stalk their customers 
- Figure out if there's a correlation between variables ( gender, marital status, country, age) and sales
- Adjust their marketing strategy

Look within
- Which products have the highest profit margins? Can we discontinue some SKUs based on demand and sales? 
- Is there a latency in their supply chain? What's their average order fulfillment time? Can they make it faster?
- How price sensitive are their customers? Run an experiment: increase the price of a product by a little in one market and monitor how it affects sales

  ## What can I improve in the pipeline?

- make a function for data quality checks ( nulls, duplicates, row counts)
- make a config file for business rules ( which columns can be connected, what does it mean if a KPI is null or 0 and can it be removed from the final dataset)
- write descriptions for each table and columns so that the AI works better 
