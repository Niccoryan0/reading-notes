# 401-29 Readings

## Policies
[Link](https://docs.microsoft.com/en-us/aspnet/core/security/authorization/policies?view=aspnetcore-2.1)
- Policies can be used to set Authorization rules for different pages or routes on a site. 
- They can be applied to both MVC Controller routes as well as whole Razor Pages.
- Authorization can be done in an Authorization Handler as well, which can allow for rules that aren't based on role, the example given in the link provided is a policy which sets an age restriction on a page.
- Handlers don't return anything, and they don't need to handle failures usually either.
- Failure can be gauranteed even if the other handlers success by calling context.Fail.
- Handlers can have multiple requirements assigned to them, which is useful if evaluation should happen on an OR basis.

## Custom Policy Providers
[Link](https://docs.microsoft.com/en-us/aspnet/core/security/authorization/iauthorizationpolicyprovider?view=aspnetcore-2.1)
- Some policies that are required for a site cannot be registered by calling AuthorizationOptions.AddPolicy(). For these types we need to make a custom IAuthorizationPolicyProvider. These are useful when:
  - Using an external service to provide policy evaluation.
  - Using a large range of policies (for different room numbers or ages, for example), so it doesn't make sense to add each individual authorization policy with an AuthorizationOptions.AddPolicy call.
  - Creating policies at runtime based on information in an external data source (like a database) or determining authorization requirements dynamically through another mechanism.
- Policy retrieval can also be customized via the IAuthorizationPolicyProvider.
- "In addition to providing named authorization policies, a custom IAuthorizationPolicyProvider needs to implement GetDefaultPolicyAsync to provide an authorization policy for [Authorize] attributes without a policy name specified."