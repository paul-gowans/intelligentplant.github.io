# Write an App in Visual Studio

We provide an extension for Visual Studio 2015 and Visual Studio 2017
that makes it easy to create an App Store application. You can download
the extension
[here](https://appstore.intelligentplant.com/nuget/downloads/IP%20App%20Store%20Tools.vsix).
(Edge users note, the VSIX file may download as a ZIP in which case
rename the archive back to .VSIX)

Here is a video that takes you through the whole process

<https://www.youtube.com/watch?v=NgcSOyOEIWA>

Once installed, you can create an App Store web application by selecting
*File \> New \> Project* in Visual Studio, choosing .NET Framework 4.5.2
or greater, and navigating to *Visual C\# \> Web* from the project
template browser:

![](/dev/image002.png)

Once Visual Studio creates the new project, you'll find a readme file in
your new project that contains instructions for registering an
application with the App Store.

Your new application is an [ASP.NET MVC](https://www.asp.net/mvc)
application with [Web API](https://www.asp.net/web-api) and
[SignalR](https://www.asp.net/signalr) pre-configured, containing
out-of-the-box functionality that demonstrates how to request available
data sources, find tags on the data sources, and subscribe to receive
updates to tag values in real time. Make sure you have a look around the
project to see how these components are used\!

**Important:** If you have not yet registered as an App Store developer,
you can do so
[here](https://appstore.intelligentplant.com/Developer/RegisterDeveloper).
