---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeploymentschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
ms.openlocfilehash: bc98d8ed8773e49eab594a4d715bef3f93862e83
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997404"
---
# <span data-ttu-id="19a87-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="19a87-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="19a87-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19a87-102">SYNOPSIS</span></span>
<span data-ttu-id="19a87-103">Ruft einen Auftragszeitplan für die Bereitstellung einer DSC-Knoten Konfiguration in der Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="19a87-103">Gets a DSC Node configuration deployment job schedule in Automation.</span></span>

## <span data-ttu-id="19a87-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19a87-104">SYNTAX</span></span>

### <span data-ttu-id="19a87-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="19a87-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19a87-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="19a87-106">ByJobScheduleId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19a87-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19a87-107">DESCRIPTION</span></span>
<span data-ttu-id="19a87-108">Mit dem Cmdlet **Get-AzAutomationDscNodeConfigurationDeployment** wird eine APS-Knoten Konfiguration (Desired State Configuration, DSC) in Azure Automation bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="19a87-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="19a87-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19a87-109">EXAMPLES</span></span>

### <span data-ttu-id="19a87-110">Beispiel 1: Abrufen aller Bereitstellungs Zeitpläne</span><span class="sxs-lookup"><span data-stu-id="19a87-110">Example 1: Get all the deployment schedules</span></span>
```
PS C:\> Get-AzAutomationDscNodeConfigurationDeploymentSchedule `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01"

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : e347dfc4-62fe-4ed6-adfb-55518c57b558
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1
```

### <span data-ttu-id="19a87-111">Beispiel 2: Abrufen eines Bereitstellungszeitplans</span><span class="sxs-lookup"><span data-stu-id="19a87-111">Example 2: Get a deployment schedule</span></span>
```
PS C:\> $js= Get-AzAutomationDscNodeConfigurationDeploymentSchedule `
                 -AutomationAccountName "Contoso01" `
                 -ResourceGroupName "ResourceGroup01" `
                 -JobScheduleId 2b1d7738-093d-4ff7-b87b-e4b2321319e5

PS C:\> $js

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSche
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1

PS C:\> $js.JobSchedule

ResourceGroupName     : ResourceGroup01
RunOn                 :
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1
ScheduleName          : TestScheduleName
Parameters            : {AutomationAccountName, NodeConfigurationName, ResourceGroupName, ListOfNodeNames}
HybridWorker          :
```

<span data-ttu-id="19a87-112">Der obige Befehl stellt die Konfiguration des DSC-Knotens mit dem Namen "Config01. Node1" für das angegebene zweidimensionale Array von Knotennamen bereit.</span><span class="sxs-lookup"><span data-stu-id="19a87-112">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="19a87-113">Die Bereitstellung erfolgt in einer stufenweisen Weise.</span><span class="sxs-lookup"><span data-stu-id="19a87-113">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="19a87-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="19a87-114">PARAMETERS</span></span>

### <span data-ttu-id="19a87-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="19a87-115">-AutomationAccountName</span></span>
<span data-ttu-id="19a87-116">Gibt den Namen des Automatisierungs Kontos an, das die DSC-Konfiguration enthält, die von diesem Cmdlet kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="19a87-116">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19a87-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19a87-117">-DefaultProfile</span></span>
<span data-ttu-id="19a87-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="19a87-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19a87-119">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="19a87-119">-JobScheduleId</span></span>
<span data-ttu-id="19a87-120">Gibt die ID des Auftragszeitplans für einen vorhandenen geplanten Bereitstellungsauftrag an.</span><span class="sxs-lookup"><span data-stu-id="19a87-120">Specifies the Job Schedule id of an existing scheduled deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19a87-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19a87-121">-ResourceGroupName</span></span>
<span data-ttu-id="19a87-122">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet eine Konfiguration kompiliert.</span><span class="sxs-lookup"><span data-stu-id="19a87-122">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19a87-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19a87-123">CommonParameters</span></span>
<span data-ttu-id="19a87-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19a87-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19a87-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19a87-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19a87-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19a87-126">INPUTS</span></span>

### <span data-ttu-id="19a87-127">System. GUID</span><span class="sxs-lookup"><span data-stu-id="19a87-127">System.Guid</span></span>

### <span data-ttu-id="19a87-128">System. String</span><span class="sxs-lookup"><span data-stu-id="19a87-128">System.String</span></span>

## <span data-ttu-id="19a87-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19a87-129">OUTPUTS</span></span>

### <span data-ttu-id="19a87-130">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="19a87-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="19a87-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="19a87-131">NOTES</span></span>

## <span data-ttu-id="19a87-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19a87-132">RELATED LINKS</span></span>

[<span data-ttu-id="19a87-133">Anfang-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="19a87-133">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="19a87-134">Importieren-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="19a87-134">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="19a87-135">Anfang-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="19a87-135">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="19a87-136">Stopp-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="19a87-136">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="19a87-137">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="19a87-137">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)
