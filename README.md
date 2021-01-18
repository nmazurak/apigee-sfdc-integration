# Apigee-Salesforce integration 

## To recreate this proxy follow next steps:

### Create Connected App in your Salesforce account
  1. Login to your sfdc developer account
  2. Go to Setup -> Apps -> App Manager -> New Connected Apps 
  3. Fill in all the required fields
  4. Enable Oauth Settings
  5. In OAuth scope select "Access and manage your data" and "Perform requests on your behalf at any time"
  6. Click Save

### Create Key-Value Map in Apigee
  1. Login to your Apigee account
  2. Go to Admin -> Environments -> Key Value Maps
  3. Select test environment and create KVM with name "sfdc_creds"
  4. Select encrypted 
  5. Populate KVM with the following parameters: 
       * username (your sfdc username)
       * password (sfdc password)
       * client_id (could be found in Apps-> App-> Manager -> Your App -> View -> Consumer Key)
       * client_secret (...-> View -> Consumer Secret )
  
### Import proxy 
  1. Clone and zip this project 
  2. Go to Develop -> Proxies -> import proxy from bundle 
  3. Select previously saved zip file
  4. Change {your-org-name} in target URL to your sfdc org name 
  
  
