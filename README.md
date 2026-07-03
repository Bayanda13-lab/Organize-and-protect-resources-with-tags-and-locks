# Organize-and-protect-resources-with-tags-and-locks
# explanation
Organize and protect cloud assets by applying metadata tags for cost tracking and categorization, and setting up CanNotDelete or ReadOnly resource locks. These steps prevent accidental deletions or unauthorized modifications without interfering with the underlying functionality of your infrastructure
# step 1 Prepare the environment 
-In Microsoft Azure portal search bar, search for resource groups

-select "+create" .name resource group "xxxxx" then choose preferred region and select "review+create"
# step 2 Create  a test storage account
- Portal search bar, search storage account
- select '+create'
- On basics tab ensure your step 1 resource group is selected as default resource group
- Name storage account xxxxx
- same region as resource group
- for preferred storage type I used 'Azure Blob storage or Data lake storage'
- for performance, select standard
- for redundacy ,Local rendundant storage(cheapest)
- review+ create
- when finished deployment ,select go to resource
  # step 3 Tag the resouce
  - In search bar ,search resource group
  - select resource group thats was created (step 1)
  - left menu select "Tags"
  - Add tags name:department value:development
  - add 2nd name:environment value: test
  - select apply and verify tags appear
    # step 4 tag storage accounts
    - open storage account
    - left menu select tags then create the  same tags in the previous step
    # step 5 create a 2nd storage accoun with different resource tag
    - To create storage account  Step 2
    -  to tag is step 4 <img width="1201" height="788" alt="Screenshot (25)" src="https://github.com/user-attachments/assets/7e5adf7a-d11d-468d-a6f3-bea8a62c438b" />

    # step 6 filter resources by Tags
    - search resource group
    - select the created resouce group
    - add filters
    - filter dropdown select Tags , tags dropdwown select department  then select development
    - observe the first tag corresponds with the first storage account
    - do the same thing but seelect different tag and  observe which storage account it corresponds with
      # step 7 Apply a delete lock to storage account
      - <img width="1600" height="900" alt="Screenshot (27)" src="https://github.com/user-attachments/assets/06444ecc-1ecd-45cf-92be-ffb14d7ec4fa" />
      # step 8 test read only lock on the resource group
      <img width="1600" height="900" alt="Screenshot (28)" src="https://github.com/user-attachments/assets/32e30599-dd1a-41e7-9381-e19c8a66da0b" />


