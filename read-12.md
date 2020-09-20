## OAuth 2 Simplified
### This post describes OAuth 2.0 in a simplified format to help developers and service providers implement the protocol.

### The OAuth 2 spec can be a bit confusing to read, so I've written this post to help describe the terminology in a simplified format. The core spec leaves many decisions up to the implementer, often based on security tradeoffs of the implementation. Instead of describing all possible decisions that need to be made to successfully implement OAuth 2, this post makes decisions that are appropriate for most implementations.



## Build a Simple REST API with Node and OAuth
### JavaScript is used everywhere on the web - nearly every web page will include at least some JavaScript, and even if it doesn’t, your browser probably has some sort of extension that injects bits of JavaScript code on to the page anyway. It’s hard to avoid in 2018.

### JavaScript can also be used outside the context of a browser, for anything from hosting a web server to controlling an RC car or running a full-fledged operating system. Sometimes you want a couple of servers to talk to each other, whether on a local network or over the internet.

### Today, I’ll show you how to create a REST API using Node.js, and secure it with OAuth 2.0 to prevent unwarranted requests. REST APIs are all over the web, but without the proper tools require a ton of boilerplate code. I’ll show you how to use a couple of amazing tools that make it all a breeze, including Okta to implement the Client Credentials Flow, which securely connects two machines together without the context of a user.


## Roles
### The Third-Party Application: "Client"
### The client is the application that is attempting to get access to the user's account. It needs to get permission from the user before it can do so.

### The API: "Resource Server"
### The resource server is the API server used to access the user's information.

### The Authorization Server
### This is the server that presents the interface where the user approves or denies the request. In smaller implementations, this may be the same server as the API server, but larger scale deployments will often build this as a separate component.

### The User: "Resource Owner"
### The resource owner is the person who is giving access to some portion of their account.

### Creating an App
### Before you can begin the OAuth process, you must first register a new app with the service. When registering a new app, you usually register basic information such as application name, website, a logo, etc. In addition, you must register a redirect URI to be used for redirecting users to for web server, browser-based, or mobile apps.

### Redirect URIs
### The service will only redirect users to a registered URI, which helps prevent some attacks. Any HTTP redirect URIs must be served via HTTPS. This helps prevent tokens from being intercepted during the authorization process. Native apps may register a redirect URI with a custom URL scheme for the application, which may look like demoapp://redirect.

### Client ID and Secret
### After registering your app, you will receive a client ID and optionally a client secret. The client ID is considered public information, and is used to build login URLs, or included in Javascript source code on a page. The client secret must be kept confidential. If a deployed app cannot keep the secret confidential, such as single-page Javascript apps or native apps, then the secret is not used, and ideally the service shouldn't issue a secret to these types of apps in the first place.

