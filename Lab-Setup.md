[**Back to main**](./README.md)

 <br/>

 **_NOTE:_**  This document is under development.

 <br/>

## Requirements
1. [Microsoft 365 subscription](https://www.microsoft.com/en-us/microsoft-365/) or [Microsoft 365 free 30 days trial](https://www.microsoft.com/en-us/microsoft-365/try) or [Microsoft 365 Developer Program](https://developer.microsoft.com/en-us/microsoft-365/dev-program)
1. [Microsoft Power Apps free 30 days trial](https://powerapps.microsoft.com/) or [Dynamics 365 Sales free 30 days trial](https://dynamics.microsoft.com/en-us/dynamics-365-free-trial/)
   - Note: [Power Apps Developer Plan ](https://powerapps.microsoft.com/en-us/developerplan/) have some limitations
1. [Microsoft Azure subscription](https://azure.microsoft.com/en-us/pricing/purchase-options/pay-as-you-go/) or [Microsoft Azure free trial](https://azure.microsoft.com/en-us/free/)
1. [Microsoft Azure DevOps account](https://dev.azure.com)

 <br/>


## Software

| Software Type |   Description | Download | 
|:---: | ---|---|
| SDK  | .NET Framework 4.6.2 Developer Pack | [URL here](https://dotnet.microsoft.com/en-us/download/dotnet-framework/net462)|
| SDK  | .NET Framework 4.8 Developer Pack   | [URL here](https://dotnet.microsoft.com/en-us/download/dotnet-framework/net48)|
| SDK  | .NET 6 Developer Pack               | [URL here](https://dotnet.microsoft.com/en-us/download/dotnet/6.0)|
| SDK  | Dynamics 365 SDK Tools              | [It is recommended to use the PowerShell script available here ](https://docs.microsoft.com/en-us/dynamics365/customerengagement/on-premises/developer/download-tools-nuget?view=op-9-1#download-tools-using-powershell) **OR** [By CDS.Tools here](https://xrm.tools/SDK) |
| Developer CLI | Microsoft Power Platform CLI | [Download here](https://aka.ms/PowerAppsCLI) **OR** [Overview here](https://docs.microsoft.com/en-us/powerapps/developer/data-platform/powerapps-cli) <br> **- Note:** To update to the latest capabilities use: ```pac install latest```|
| Runtime       | .Net Framework 4.6.2 | [URL here](https://dotnet.microsoft.com/en-us/download/dotnet-framework/net462)|
| Runtime       | .Net Framework 4.8   | [URL here](https://dotnet.microsoft.com/en-us/download/dotnet-framework/net48)|
| Runtime       | Node JS              | [URL here](https://nodejs.org/)|
| API platform  | Postman              | [URL here](https://www.postman.com/downloads)|
| IDE           | Visual Studio        | [URL here](https://visualstudio.microsoft.com/downloads/)|
| IDE           | Visual Studio Code   | [URL here](https://code.visualstudio.com/)|


 <br/>

## Visual Studio Code Extensions

| Extension | Publisher | Description | Install using command prompt |
| --- | --- | ---- | ---- |
| [Azure Tools](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-node-azure-pack) | Microsoft | Get web site hosting, SQL and MongoDB data, Docker Containers, Serve | ```code --install-extension ms-vscode.vscode-node-azure-pack ```|  
| [C#](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp) | Microsoft | C# for Visual Studio Code (powered by OmniSharp). | ```code --install-extension ms-dotnettools.csharp``` |
|[Power Platform Tools](https://docs.microsoft.com/en-us/powerapps/maker/portals/power-apps-cli) | Microsoft | Tooling to create Power Platform solutions & packages, manage Power Platform environments and edit Power Apps Portals | ```code --install-extension microsoft-IsvExpTools.powerplatform-vscode``` |

 <br/>
 
 
 ## Community tools for Microsoft Dataverse
 
| Tool | 	Description |
| --- | --- |
|[Attribute Manager](https://www.xrmtoolbox.com/plugins/DLaB.Xrm.AttributeManager/) |	Used to rename/delete/or change the type of the column.|
|[Chromium Metadata Browser](https://community.dynamicslabs.io/feed/metadata-browser) | Lets you browse metadata such as tables, columns, relationships, choices of Dataverse environments.|
|[Early Bound Generator](https://www.xrmtoolbox.com/plugins/DLaB.Xrm.EarlyBoundGenerator/) | Generates Early Bound Tables/Choices/Actions. Uses CrmSvcUtil from the SDK, and shows command line used to create the classes.|
|[Export to Excel](https://www.xrmtoolbox.com/plugins/Ryr.XrmToolBox.ExportToExcel/) |	Easily export records from the selected view/fetchxml to Excel.|
|[FetchXML Builder](https://www.xrmtoolbox.com/plugins/Cinteros.Xrm.FetchXmlBuilder/)|	Create and test FetchXml Queries|
|[Metadata Browser](https://www.xrmtoolbox.com/plugins/MsCrmTools.MetadataBrowser/)  |	Browse metadata from your Dataverse environment|
|[Plugin Trace Viewer](https://www.xrmtoolbox.com/plugins/Cinteros.XrmToolBox.PluginTraceViewer/) | Investigate the Plug-in Trace Log with easy filtering and display possibilities|
|[User Settings Utility](https://www.xrmtoolbox.com/plugins/MsCrmTools.UserSettingsUtility/) | Manage users personal settings in bulk|
|[XrmToolBox](https://www.xrmtoolbox.com/) ***Recommended*** | XrmToolBox is a Windows application that connects to Microsoft Dataverse. |

---

[**Back to main**](./README.md)
