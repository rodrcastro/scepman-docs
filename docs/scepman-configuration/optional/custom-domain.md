# Custom Domain

## Custom Domain Configuration

If you want to create your own custom domain for your **App Service** URL, follow these steps:

1. Choose your **App Service,** on the left select **Custom domain**.&#x20;
2. Click **Add custom domain.**&#x20;
3. Enter your custom domain (**1**) and click **Validate\***.&#x20;
4. If **CNAME** is set correct (**2**) domain ownership is validated (**3**).

![](<../../../.gitbook/assets/scepman\_cname1 (1) (1) (1) (1) (1) (1).png>)

\*if you don't have a custom domain yet follow the steps:

1. Go to TLS/SSL settings
2. Click on Private Key Certificates (.pfx)
3. Create App Service Managed Certificate

![](<../../../.gitbook/assets/image (35).png>)

More information about configure SSL Certificate [click here](https://docs.microsoft.com/en-us/azure/app-service/configure-ssl-certificate)

### SSL Binding

1. Click **Add custom domain** to finish this configuration.
2. When the domain is added, create a SSL binding.
3. Click **Add binding** on the custom domain screen.

![](<../../../.gitbook/assets/scepman\_cname2 (1) (1).png>)

1. On the TLS/SSL Binding submenu click **Upload PFX Certificate.**
2. After uploading select your certificate and the binding type.
3. Next click **Add binding.**

![](<../../../.gitbook/assets/scepman\_cname3 (1) (2) (2) (2) (2) (2) (4) (4) (4) (4) (4) (3).png>)

1. After completing these steps, **Application settings** needs to be updated
2. Choose app service and click **Configuration**
3. Then click **Application Settings** and edit the setting **AppConfig:BaseUrl**
4. Enter your custom domain and click **OK**.

![](../../../.gitbook/assets/scepman\_cname4\_1.png)

1. Finally click **Save**.

### Microsoft Documentation and Managed Certificates

Add custom domain to an App Service:\
[https://docs.microsoft.com/en-us/azure/app-service/app-service-web-tutorial-custom-domain](https://docs.microsoft.com/en-us/azure/app-service/app-service-web-tutorial-custom-domain)

Add and manage TLS/SSL certificates in App Service:\
[https://docs.microsoft.com/en-us/azure/app-service/configure-ssl-certificate](https://docs.microsoft.com/en-us/azure/app-service/configure-ssl-certificate)

Create a free certificate:\
[https://docs.microsoft.com/en-us/azure/app-service/configure-ssl-certificate#create-a-free-certificate-preview](https://docs.microsoft.com/en-us/azure/app-service/configure-ssl-certificate#create-a-free-certificate-preview)

| Back to Trial Guide | [Back to Community Guide](../../scepman-deployment/community-guide.md#step-4-configure-a-custom-domain-and-ssl-certificate) | ​[Back to Enterprise Guide​](../../scepman-deployment/enterprise-guide.md#step-4-configure-a-custom-domain-and-ssl-certificate) |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
