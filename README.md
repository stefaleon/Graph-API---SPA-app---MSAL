
## [Javascript SPA guided setup for JS-SPA-Graph-MSAL](https://apps.dev.microsoft.com/portal/guided-setup/introduction?appType=singlePageApp&appTech=javascriptSpa&appId=ce501538-bbcc-495e-bd28-f5e05ed2aac4)

My applications -> JS-SPA-Graph-MSAL -> Guided setup -> Javascript SPA


## Call the Microsoft Graph API from a JavaScript Single Page Application (SPA)

This guide demonstrates how a JavaScript Single Page Application (SPA) can sign in personal, work and school accounts, get an access token, and call the Microsoft Graph API or other APIs that require access tokens from the Azure Active Directory v2 endpoint.


* The sample application created by this guide enables a JavaScript SPA to query the Microsoft Graph API or a Web API that accepts tokens from Azure Active Directory v2 endpoint. For this scenario, after a user signs-in, an access token is requested and added to HTTP requests via the authorization header. Token acquisition and renewal are handled by the Microsoft Authentication Library (MSAL).


## Create your project

### Option 1: Visual Studio

* If you are using Visual Studio and are creating a new project, follow the steps below to create a new Visual Studio solution:
    1. In Visual Studio: File > New > Project
    2. Under Visual C#\Web, select ASP.NET Web Application (.NET Framework)
    3. Name your application and click OK
    4. Under New ASP.NET Web Application, select Empty

