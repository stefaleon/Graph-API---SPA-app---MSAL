
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




## Create your single page application’s UI


1. Create an index.html file for your JavaScript SPA. If you are using Visual Studio, select the project (project root folder), right click and select: Add > New Item > HTML page and name it index.html
2. Add the following code to your page:

```
<!DOCTYPE html>
<html>
<head>
    <!-- bootstrap reference used for styling the page -->
    <link href="//maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" rel="stylesheet">
    <title>JavaScript SPA Guided Setup</title>
</head>
<body style="margin: 40px">
    <button id="callGraphButton" type="button" class="btn btn-primary" onclick="callGraphApi()">Call Microsoft Graph API</button>
    <div id="errorMessage" class="text-danger"></div>
    <div class="hidden">
        <h3>Graph API Call Response</h3>
        <pre class="well" id="graphResponse"></pre>
    </div>
    <div class="hidden">
        <h3>Access Token</h3>
        <pre class="well" id="accessToken"></pre>
    </div>
    <div class="hidden">
        <h3>ID Token Claims</h3>
        <pre class="well" id="userInfo"></pre>
    </div>
    <button id="signOutButton" type="button" class="btn btn-primary hidden" onclick="signOut()">Sign out</button>

    <!-- This app uses cdn to reference msal.js (recommended). 
         You can also download it from: https://github.com/AzureAD/microsoft-authentication-library-for-js -->
    <script src="https://secure.aadcdn.microsoftonline-p.com/lib/0.1.3/js/msal.min.js"></script>

    <!-- The 'bluebird' and 'fetch' references below are required if you need to run this application on Internet Explorer -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/bluebird/3.3.4/bluebird.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/fetch/2.0.3/fetch.min.js"></script>

    <script type="text/javascript" src="msalconfig.js"></script>
    <script type="text/javascript" src="app.js"></script>
</body>
</html>
```