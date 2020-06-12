**`Since Microsoft has certified and distributes Industrial App Store
Connector there is no need to use this option. Please get in touch to
discuss if you still feel the need for it.` **

Follow
[these](https://docs.microsoft.com/en-us/data-integration/gateway/service-gateway-install)
instructions to install an on-premises data gateway.

Once the gateway is set up, follow
[these](https://docs.microsoft.com/en-us/power-bi/service-gateway-custom-connectors)
quick steps to install Intelligent Plant Industrial App Store Connector.
You will need to [contact](https://www.intelligentplant.com/contactus)
Intelligent Plant in order to obtain the custom connector file.

**Setting up the gateway with IndustrilAppStore Connector**

Before reading through the steps below please make sure that your
gateway version is at least **October 2019 R2** or higher. Here are the
steps to configure gateway side of things (this assumes that you have
installed it):

1.  Create a directory that the user which is used to run the gateway
    service can access (READ). I'll use C:/Documents/Connectors/ as an
    example for further steps. 
2.  Put the issued IndustrialAppStore.mez file into
    C:/Documents/Connectors/.
3.  In gateway application, click Connectors option and navigate to
    C:/Documents/Connectors/.
4.  Give it a split second and the Industrial AppStore connector should
    appear in the box above the path. If it hasn't - try restarting the
    service, if that won't help make sure you have permissions set
    correctly. There are log files for more information in the gateway
    installation directory.
5.  If above worked, that's it\! Navigate
    to <https://app.powerbi.com/> and configure background data
    refresh using gateway option (Make sure *Allow user's custom data
    connectors to refresh through this gateway cluster* option is
    ticked, you can find more info
    [here](https://docs.microsoft.com/en-us/power-bi/service-gateway-custom-connectors)).

*Nore to IP developers
[here](http://trac.intelligentplant.com/svn-TrendTool/ticket/1610).*
