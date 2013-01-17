Tags: plugin
Bundle: free

#Diagnostics plugin

The `/resizer.debug` page is provided by this plugin (which is installed by default)

If you're not using IIS Integrated mode, you will need to access it via /resizer.debug.ashx

## Diagnostics page not working?

By default, the Diagnostics plugin uses the same setting as [customErrors](http://msdn.microsoft.com/en-us/library/h0hfz6fc.aspx) (which defaults to Localhost). Thus, if you can see ASP.NET error messages, you will also be able to get the diagnostics page. This ensures that the diagnostics page never exposes data to a host that doesn't already have access to detailed error messages. 

To override, add one of the following to the &lt;resizer&gt; section.

	<diagnostics enableFor="AllHosts" />
	<diagnostics enableFor="Localhost" />
	<diagnostics enableFor="None" />
	


I think they are pretty obvious.


### ASP.NET MVC notes

If you can't access the diagnostics page, your routes may be interfering. 

Either (a) install the [MvcRoutingShim plugin](/plugins/mvcroutingshim), or (b) make the following code change.

In Global.asax.cs, in RegisterRoutes, add the line of code displayed below. 

	public static void RegisterRoutes(RouteCollection routes) {
		routes.IgnoreRoute("resizer.debug");
		routes.IgnoreRoute("resizer.debug.ashx");
	}
