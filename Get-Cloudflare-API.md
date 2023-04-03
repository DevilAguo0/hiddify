1.  From the [Cloudflare dashboardExternal link icon Open external link](https://dash.cloudflare.com/profile/api-tokens/) , go to **My Profile** > **API Tokens**.
    
2.  Select **Create Token**.
    
3.  Select a template from the available [API token templates](/fundamentals/api/reference/template/) or create a custom token. We use the **Edit zone DNS** template in the following examples.
    
4.  Add or edit the token name to describe why or how the token is used. Templates are prefilled with a token name and permissions.
   
![Token template overview screen](https://user-images.githubusercontent.com/114227601/229591958-adc4e813-1e04-4de0-9bbb-29b94df4b4d9.png)

    
5.  Modify the token’s permissions. After selecting a permissions group (_Account_, _User_, or _Zone_), choose what level of access to grant the token. Most groups offer `Edit` or `Read` options. `Edit` is full CRUDL (create, read, update, delete, list) access, while `Read` is the read permission and list where appropriate. Refer to the [available token permissions](/fundamentals/api/reference/permissions/) for more information.
    
6.  Select which resources the token is authorized to access. For example, granting `Zone DNS Read` access to a zone `example.com` will allow the token to read DNS records only for that specific zone. Any other zone will return an error for DNS record reads operations. Any other operation on that zone will also return an error.
    
    
8.  Select **Continue to summary**.
    
![Token summary screen displaying the resources and permissions selected](https://user-images.githubusercontent.com/114227601/229592071-3faf93c3-b246-4a08-823b-4680a3a4cf5e.png)

    
10.  Select **Create Token** to generate the token’s secret.
    
11.  Copy the secret to a secure place.

![image](https://user-images.githubusercontent.com/114227601/229592139-25482e17-ddef-48b5-9926-265d073669e9.png)
