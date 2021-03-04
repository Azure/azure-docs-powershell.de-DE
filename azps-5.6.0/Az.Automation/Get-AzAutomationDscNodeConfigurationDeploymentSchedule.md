---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeploymentschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
ms.openlocfilehash: 3bb0f095550394991bb74065e8d1c34c346b0c4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920064"
---
# <span data-ttu-id="ca643-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="ca643-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="ca643-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca643-102">SYNOPSIS</span></span>
<span data-ttu-id="ca643-103">Ruft einen Zeitplan für die Bereitstellung der DSC-Knotenkonfiguration in automation ab.</span><span class="sxs-lookup"><span data-stu-id="ca643-103">Gets a DSC Node configuration deployment job schedule in Automation.</span></span>

## <span data-ttu-id="ca643-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca643-104">SYNTAX</span></span>

### <span data-ttu-id="ca643-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="ca643-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca643-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="ca643-106">ByJobScheduleId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca643-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ca643-107">DESCRIPTION</span></span>
<span data-ttu-id="ca643-108">Das **Cmdlet Get-AzAutomationDscNodeConfigurationDeployment** stellt eine APS Desired State Configuration (DSC)-Knotenkonfiguration in Azure Automation bereit.</span><span class="sxs-lookup"><span data-stu-id="ca643-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="ca643-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ca643-109">EXAMPLES</span></span>

### <span data-ttu-id="ca643-110">Beispiel 1: Alle Bereitstellungszeitpläne erhalten</span><span class="sxs-lookup"><span data-stu-id="ca643-110">Example 1: Get all the deployment schedules</span></span>
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

### <span data-ttu-id="ca643-111">Beispiel 2: Erstellen eines Bereitstellungszeitplans</span><span class="sxs-lookup"><span data-stu-id="ca643-111">Example 2: Get a deployment schedule</span></span>
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

<span data-ttu-id="ca643-112">Mit dem obigen Befehl wird die KONFIGURATION des DSC-Knotens mit dem Namen "Config01.Node1" für das angegebene zweidimensionale Array von Knotennamen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ca643-112">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="ca643-113">Die Bereitstellung erfolgt in einer mehrstufigen Weise.</span><span class="sxs-lookup"><span data-stu-id="ca643-113">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="ca643-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ca643-114">PARAMETERS</span></span>

### <span data-ttu-id="ca643-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ca643-115">-AutomationAccountName</span></span>
<span data-ttu-id="ca643-116">Gibt den Namen des Automatisierungskontos an, das die VON diesem Cmdlet kompilierte DSC-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="ca643-116">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="ca643-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca643-117">-DefaultProfile</span></span>
<span data-ttu-id="ca643-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ca643-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca643-119">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="ca643-119">-JobScheduleId</span></span>
<span data-ttu-id="ca643-120">Gibt die Auftragsplan-ID eines vorhandenen geplanten Bereitstellungsauftrags an.</span><span class="sxs-lookup"><span data-stu-id="ca643-120">Specifies the Job Schedule id of an existing scheduled deployment job.</span></span>

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

### <span data-ttu-id="ca643-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca643-121">-ResourceGroupName</span></span>
<span data-ttu-id="ca643-122">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet eine Konfiguration kompiliert.</span><span class="sxs-lookup"><span data-stu-id="ca643-122">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="ca643-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca643-123">CommonParameters</span></span>
<span data-ttu-id="ca643-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca643-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca643-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca643-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca643-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ca643-126">INPUTS</span></span>

### <span data-ttu-id="ca643-127">System.Guid</span><span class="sxs-lookup"><span data-stu-id="ca643-127">System.Guid</span></span>

### <span data-ttu-id="ca643-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ca643-128">System.String</span></span>

## <span data-ttu-id="ca643-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ca643-129">OUTPUTS</span></span>

### <span data-ttu-id="ca643-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="ca643-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="ca643-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ca643-131">NOTES</span></span>

## <span data-ttu-id="ca643-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ca643-132">RELATED LINKS</span></span>

[<span data-ttu-id="ca643-133">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="ca643-133">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="ca643-134">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca643-134">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="ca643-135">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ca643-135">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="ca643-136">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ca643-136">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="ca643-137">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ca643-137">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)
