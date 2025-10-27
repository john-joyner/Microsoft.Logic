# Integrate Azure Monitor alerts with your ITSM Solution
Author: John Joyner

This solution is a bi-directional connector between Azure Monitor and any ITSM with a REST API HTTP interface. The solution will create tickets in your ITSM system when Azure Monitor alerts fire, update the ITSM as alert status changes, and write ITSM ticket data back to the Azure Monitor alert history to keep alerts and tickets in sync. The solution respects suppression alert processing rules and securely stores the ITSM service principal secrets in Azure Key vault.

There are two (2) Logic apps that are part of this solution:

1. <b>Azure-Monitor-Alert-ITSM-HTTP-API</b> (Configured as an Azure Monitor Alert Action Group action, launched every time an Azure Monitor alert condition changes.) Consumption plan Logic App has one (1) trigger and 58 actions.

2. <b>Azure-Monitor-Close-ITSM-HTTP-API</b> (Configured as a webhook destination, called by the ITSM when an Azure Monitor alert-sourced ticket is closed in the ITSM.) Consumption plan Logic App has one (1) trigger and six (6) actions.

### Click to Deploy Azure-Monitor-Alert-ITSM-HTTP-API to Azure

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fjohn-joyner%2FMicrosoft.Logic%2Frefs%2Fheads%2Fmain%2FIntegrate-Azure-Monitor-alerts-with-your-ITSM-Solution%2FAzure-Monitor-Alert-ITSM-HTTP-API.json" target="_blank">
    <img src="https://aka.ms/deploytoazurebutton"/>
</a>

<a href="https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fjohn-joyner%2FMicrosoft.Logic%2Frefs%2Fheads%2Fmain%2FIntegrate-Azure-Monitor-alerts-with-your-ITSM-Solution%2FAzure-Monitor-Alert-ITSM-HTTP-API.json" target="_blank">
<img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.png"/>
</a>

### Click to Deploy Azure-Monitor-Close-ITSM-HTTP-API to Azure

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fjohn-joyner%2FMicrosoft.Logic%2Frefs%2Fheads%2Fmain%2FIntegrate-Azure-Monitor-alerts-with-your-ITSM-Solution%2FAzure-Monitor-Close-ITSM-HTTP-API.json" target="_blank">
    <img src="https://aka.ms/deploytoazurebutton"/>
</a>

<a href="https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fjohn-joyner%2FMicrosoft.Logic%2Frefs%2Fheads%2Fmain%2FIntegrate-Azure-Monitor-alerts-with-your-ITSM-Solution%2FAzure-Monitor-Close-ITSM-HTTP-API.json" target="_blank">
<img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.png"/>
</a>

### IMPORTANT POST DEPLOYMENT STEPS

<b>Extensive customization of this Logic app may be required before it will work in your environment.</b> 

Read the detailed step-by-step instruction at this link: https://blog.johnjoyner.net/integrate-azure-monitor-alerts-from-servers-with-your-itsm-system/

<b>Solution Overview</b>

![1-SolutionOverview](https://github.com/john-joyner/Microsoft.Logic/blob/main/Integrate-Azure-Monitor-alerts-with-your-ITSM-Solution/images/Azure-Monitor-ITSM-HTTP-API%20SolutionOverview.jpg)

<b>Azure-Monitor-Alert-ITSM-HTTP-API Functional Diagram</b>

![2-AlertFunctionalDiagram](https://github.com/john-joyner/Microsoft.Logic/blob/main/Integrate-Azure-Monitor-alerts-with-your-ITSM-Solution/images/Azure-Monitor-Alert-ITSM-HTTP-API%20Functional%20Diagram.jpg)

<b>Azure-Monitor-Close-ITSM-HTTP-API Functional Diagram</b>

![3-CloseFunctionalDiagram](https://github.com/john-joyner/Microsoft.Logic/blob/main/Integrate-Azure-Monitor-alerts-with-your-ITSM-Solution/images/Azure-Monitor-Close-ITSM-HTTP-API%20Functional%20Diagram.jpg)


