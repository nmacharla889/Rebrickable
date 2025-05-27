# Rebrickable
Microsoft Azure Data Engineering Project 1

Task:
This project focuses on ingesting data into Azure Data Lake Storage Gen 2 to make it available for further tasks for the customer.

Data Sources:
1. Rebrickable Downloads - https://rebrickable.com/downloads/- This link has the Lego Catalog Database available in zipped csv format which is updated everyday. 
2. Rebrickable API - https://rebrickable.com/api/ - This link has Lego Catalog Database as well as User Lego Collection. We are only using the User Lego Collection as our ingestion data.

Important points:
1. Use two environments i.e 2 resource groups - Dev & PROD and follow CI/CD process via Azure DevOps. Dev as LRS and PROD as GRS.
2. Use life cycle management policy.
3. Use suitable access tiers
4. Inside ADLSG2, use directories as raw->rebrickable->lego->dataset1->year->month->day->files and so on
5. Use Key valut to store secrets.
6. Use Managed Identity + Entra groups + RBAC overall.
7. Schedule it to run once a day.
8. Error Handling - send email if something fails.
9. Parameterise wherever encessary.
10. Restricted Access - Best Security principles.
11. Create Azure Data Factory instances for Ingestion process
