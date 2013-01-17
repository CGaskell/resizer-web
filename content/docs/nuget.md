
# Installing the ImageResizer via NuGet

[NuGet](http://nuget.org) is a package manager for .NET, and a pretty good one. It's easy to set up, and friendly to use.

The ImageResizer is published as a NuGet package, as are nearly all of the plugins. If you have [NuGet](http://nuget.org) installed, you can right-click on your project and choose "Add Library Package Refrence". Search for "ImageResizer", and you should see a [list of packages](http://www.nuget.org/List/Search?searchTerm=author%3A%20Nathanael%20Jones). Click Install, and you're done. You can install plugins with similar ease, but it's always good to check the [plugin's documentation](/plugins) to see if additional steps are required for activation.

## ImageResizer or ImageResizer.WebConfig ?

If you want to manually add the required settings to Web.Config (as [shown on the home page](/)), install the **ImageResizer** package. Otherwise, you can install the **ImageResizer.WebConfig** package, which will install **ImageResizer**, then add the HttpModule and ConfigurationSection registration elements to Web.Config. 

The WebConfig package never deletes anything from your Web.config file, but it may duplicate elements if you have already installed the changes in a slightly different manner.

The WebConfig package is used by most of the sample packages.

If you're using ASP.NET MVC, you can install **ImageResizer.MvcWebConfig** to get [everything working](/docs/mvc) in one step. 

**Don't worry! All packages can be safely combined!** 


## Full list of available packages

The following is a list of NuGet packages available for V3.1. 

Click [here for the list on nuget.org that may be more up-to-date](http://www.nuget.org/List/Search?searchTerm=author%3A%20Nathanael%20Jones)

Please note, that with the exception of the Logging and PdfRenderer plugin, all packages starting with "ImageResizer.Plugins" [require a paid license for production-server use](/plugins)

* ImageResizer
* ImageResizer.WebConfig
* ImageResizer.Mvc
* ImageResizer.MvcWebConfig
* ImageResizer.Plugins.AdvancedFilters
* ImageResizer.Plugins.AnimatedGifs
* ImageResizer.Plugins.BatchZipper
* ImageResizer.Plugins.CloudFront
* ImageResizer.Plugins.DiskCache
* ImageResizer.Plugins.Logging
* ImageResizer.Plugins.MongoReader
* ImageResizer.Plugins.PrettyGifs
* ImageResizer.Plugins.PsdReader
* ImageResizer.Plugins.PdfRenderer
* ImageResizer.Plugins.RemoteReader
* ImageResizer.Plugins.S3Reader
* ImageResizer.Plugins.SeamCarving
* ImageResizer.Plugins.SimpleFilters
* ImageResizer.Plugins.SqlReader
* ImageResizer.Plugins.Watermark
* ImageResizer.Plugins.WhitespaceTrimmer
* ImageResizer.Plugins.Wic
* ImageResizer.Samples.Jcrop