# 401-33 Readings

## OAUTH MSFT Docs
[Link](https://docs.microsoft.com/en-us/aspnet/core/security/authentication/social/?view=aspnetcore-2.1&tabs=visual-studio)
- If an app is deployed behind a proxy server or load balancer then some of the original request info will be forwarded in request headers. This information oftne includes the secure request scheme (https), as well as host and client IP address. Losting the secure scheme results in the app generating incorrect insecure redirect URLs.
- SecretManager is used to store the Id and Secret Tokens, more secure than appsettings.

## OAUTH
[Link](https://www.jerriepelser.com/blog/authenticate-oauth-aspnet-core-2/)
- The Authorization endpoint will usually have the path /authorize, /authenticate, /auth or something similar. The Token endpoint will typically have the path /access_token or /token, so look out for those.
- ![OAUTH 2 Flow](https://d33wubrfki0l68.cloudfront.net/89a626ba4f5a2ba44fbf8f2c08bc83fd6f29716b/8a476/static/1bbb72105e640cd3502b28d932e62f06/f96db/oauth-flow.png)
- Required Authentication services must be registered in Startup.
- Rest of article is a step by step for setting up GitHub OAUTH, useful for reference.