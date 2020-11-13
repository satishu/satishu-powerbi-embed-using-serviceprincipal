### Embed Test of Power BI

**Using ServicePrincipal**

1. Create an APP registration
2. Create Client Secret
3. Create an AD Group and add the Service Principal to it
4. Enable Allow Service Principals to use Power BI APIs under Power BI Admin Portal -> Tenant Settings -> Developer Settings
5. Under Apply to -> Add the AD group created in Step 3
6. Setup a separate workspace where the report is to be published. Grant access to the Service Principal (not the AD group) with Admin privilidges to the Workspace.
7. Publish the Report to the Workspace from Power BI Desktop
8. Grab values for Tenant ID, Application ID and Client Secret from the App Registration page in Azure AD
9. Grab values for Workspace ID and Report ID from Power BI. This can be obtained from the URL. Value after "groups" is Workspace ID and value after "Reports" is the Report ID
10. Update these values in the App Settings file
11. Hit F5 to run


**References**

https://docs.microsoft.com/en-us/power-bi/developer/embedded/embed-service-principal

**Sample code**

https://github.com/guyinacube/PowerBI-Developer-Samples

Using the .Net Core - Embed for your customers project available at: https://github.com/guyinacube/PowerBI-Developer-Samples/tree/master/.NET%20Core/Embed%20for%20your%20customers