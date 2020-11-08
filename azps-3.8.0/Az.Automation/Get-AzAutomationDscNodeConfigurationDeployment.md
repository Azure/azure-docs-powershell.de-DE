---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 449d539b767883bb075bcf333695b3285e047a9c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997402"
---
# <span data-ttu-id="b388d-101">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="b388d-101">Get-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="b388d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b388d-102">SYNOPSIS</span></span>
<span data-ttu-id="b388d-103">Ruft die Konfigurations Bereitstellungen für DSC-Knoten in der Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="b388d-103">Gets DSC Node configuration deployments in Automation.</span></span>

## <span data-ttu-id="b388d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b388d-104">SYNTAX</span></span>

### <span data-ttu-id="b388d-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="b388d-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b388d-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="b388d-106">ByJobId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b388d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b388d-107">DESCRIPTION</span></span>
<span data-ttu-id="b388d-108">Mit dem Cmdlet **Get-AzAutomationDscNodeConfigurationDeployment** wird eine APS-Knoten Konfiguration (Desired State Configuration, DSC) in Azure Automation bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b388d-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="b388d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b388d-109">EXAMPLES</span></span>

### <span data-ttu-id="b388d-110">Beispiel 1: Abrufen einer Knoten Konfigurations Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="b388d-110">Example 1: Get a node configuration deployment</span></span>
```
PS C:\> $deployment = Get-AzAutomationDscNodeConfigurationDeployment `
                         -JobId 35b14eb4-52b7-4a1d-ad62-8e9f84adc657 `
                         -AutomationAccountName "Contoso01"  `
                         -ResourceGroupName "ResourceGroup01" `
            
ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : Running
NodeStatus            : {System.Collections.Generic.Dictionary`2[System.String,System.String], System.Collections.Generic.Dictionary`2[System.String,System.String]}
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000

PS C:\> $deployment | Select -expand nodeStatus

Key        Value
---        -----
WebServer  Pending
WebServer2 Pending
WebServer3 Compliant
```

<span data-ttu-id="b388d-111">Der obige Befehl stellt die Konfiguration des DSC-Knotens mit dem Namen "Config01. Node1" für das angegebene zweidimensionale Array von Knotennamen bereit.</span><span class="sxs-lookup"><span data-stu-id="b388d-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="b388d-112">Die Bereitstellung erfolgt in einer stufenweisen Weise.</span><span class="sxs-lookup"><span data-stu-id="b388d-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="b388d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b388d-113">PARAMETERS</span></span>

### <span data-ttu-id="b388d-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b388d-114">-AutomationAccountName</span></span>
<span data-ttu-id="b388d-115">Gibt den Namen des Automatisierungs Kontos an, das die DSC-Konfiguration enthält, die von diesem Cmdlet kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="b388d-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="b388d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b388d-116">-DefaultProfile</span></span>
<span data-ttu-id="b388d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b388d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b388d-118">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b388d-118">-EndTime</span></span>
<span data-ttu-id="b388d-119">Endzeit Filter.</span><span class="sxs-lookup"><span data-stu-id="b388d-119">End time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b388d-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="b388d-120">-JobId</span></span>
<span data-ttu-id="b388d-121">Gibt die Auftrags-ID eines vorhandenen Bereitstellungsauftrags an.</span><span class="sxs-lookup"><span data-stu-id="b388d-121">Specifies the Job id of an existing deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b388d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b388d-122">-ResourceGroupName</span></span>
<span data-ttu-id="b388d-123">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet eine Konfiguration kompiliert.</span><span class="sxs-lookup"><span data-stu-id="b388d-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="b388d-124">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="b388d-124">-StartTime</span></span>
<span data-ttu-id="b388d-125">Start Zeitfilter</span><span class="sxs-lookup"><span data-stu-id="b388d-125">Start time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b388d-126">-Status</span><span class="sxs-lookup"><span data-stu-id="b388d-126">-Status</span></span>
<span data-ttu-id="b388d-127">Status des Auftrags Filters</span><span class="sxs-lookup"><span data-stu-id="b388d-127">Status of the Job filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b388d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b388d-128">CommonParameters</span></span>
<span data-ttu-id="b388d-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b388d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b388d-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b388d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b388d-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b388d-131">INPUTS</span></span>

### <span data-ttu-id="b388d-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b388d-132">System.Guid</span></span>

### <span data-ttu-id="b388d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b388d-133">System.String</span></span>

## <span data-ttu-id="b388d-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b388d-134">OUTPUTS</span></span>

### <span data-ttu-id="b388d-135">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="b388d-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="b388d-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="b388d-136">NOTES</span></span>

## <span data-ttu-id="b388d-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b388d-137">RELATED LINKS</span></span>

[<span data-ttu-id="b388d-138">Anfang-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="b388d-138">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="b388d-139">Importieren-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="b388d-139">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="b388d-140">Anfang-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="b388d-140">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="b388d-141">Stopp-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="b388d-141">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="b388d-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="b388d-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
