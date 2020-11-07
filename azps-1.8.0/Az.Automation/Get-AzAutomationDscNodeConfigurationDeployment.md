---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 74966351f50be86f19441edc254af227f2e17fab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661831"
---
# <span data-ttu-id="48fad-101">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="48fad-101">Get-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="48fad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="48fad-102">SYNOPSIS</span></span>
<span data-ttu-id="48fad-103">Ruft die Konfigurations Bereitstellungen für DSC-Knoten in der Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="48fad-103">Gets DSC Node configuration deployments in Automation.</span></span>

## <span data-ttu-id="48fad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="48fad-104">SYNTAX</span></span>

### <span data-ttu-id="48fad-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="48fad-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48fad-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="48fad-106">ByJobId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48fad-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48fad-107">DESCRIPTION</span></span>
<span data-ttu-id="48fad-108">Mit dem Cmdlet **Get-AzAutomationDscNodeConfigurationDeployment** wird eine APS-Knoten Konfiguration (Desired State Configuration, DSC) in Azure Automation bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="48fad-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deployes an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="48fad-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="48fad-109">EXAMPLES</span></span>

### <span data-ttu-id="48fad-110">Beispiel 1: Abrufen einer Knoten Konfigurations Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="48fad-110">Example 1: Get a node configuration deployment</span></span>
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

<span data-ttu-id="48fad-111">Der obige Befehl stellt die Konfiguration des DSC-Knotens mit dem Namen "Config01. Node1" für das angegebene zweidimensionale Array von Knotennamen bereit.</span><span class="sxs-lookup"><span data-stu-id="48fad-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="48fad-112">Die Bereitstellung erfolgt in einer stufenweisen Weise.</span><span class="sxs-lookup"><span data-stu-id="48fad-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="48fad-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="48fad-113">PARAMETERS</span></span>

### <span data-ttu-id="48fad-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="48fad-114">-AutomationAccountName</span></span>
<span data-ttu-id="48fad-115">Gibt den Namen des Automatisierungs Kontos an, das die DSC-Konfiguration enthält, die von diesem Cmdlet kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="48fad-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="48fad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48fad-116">-DefaultProfile</span></span>
<span data-ttu-id="48fad-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="48fad-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48fad-118">-EndTime</span><span class="sxs-lookup"><span data-stu-id="48fad-118">-EndTime</span></span>
<span data-ttu-id="48fad-119">Endzeit Filter.</span><span class="sxs-lookup"><span data-stu-id="48fad-119">End time filter.</span></span>

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

### <span data-ttu-id="48fad-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="48fad-120">-JobId</span></span>
<span data-ttu-id="48fad-121">Gibt die Auftrags-ID eines vorhandenen Bereitstellungsauftrags an.</span><span class="sxs-lookup"><span data-stu-id="48fad-121">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="48fad-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48fad-122">-ResourceGroupName</span></span>
<span data-ttu-id="48fad-123">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet eine Konfiguration kompiliert.</span><span class="sxs-lookup"><span data-stu-id="48fad-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="48fad-124">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="48fad-124">-StartTime</span></span>
<span data-ttu-id="48fad-125">Start Zeitfilter</span><span class="sxs-lookup"><span data-stu-id="48fad-125">Start time filter.</span></span>

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

### <span data-ttu-id="48fad-126">-Status</span><span class="sxs-lookup"><span data-stu-id="48fad-126">-Status</span></span>
<span data-ttu-id="48fad-127">Status des Auftrags Filters</span><span class="sxs-lookup"><span data-stu-id="48fad-127">Status of the Job filter.</span></span>

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

### <span data-ttu-id="48fad-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48fad-128">CommonParameters</span></span>
<span data-ttu-id="48fad-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48fad-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48fad-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48fad-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48fad-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="48fad-131">INPUTS</span></span>

### <span data-ttu-id="48fad-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="48fad-132">System.Guid</span></span>

### <span data-ttu-id="48fad-133">System. String</span><span class="sxs-lookup"><span data-stu-id="48fad-133">System.String</span></span>

## <span data-ttu-id="48fad-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="48fad-134">OUTPUTS</span></span>

### <span data-ttu-id="48fad-135">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="48fad-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="48fad-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="48fad-136">NOTES</span></span>

## <span data-ttu-id="48fad-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="48fad-137">RELATED LINKS</span></span>

[<span data-ttu-id="48fad-138">Anfang-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="48fad-138">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="48fad-139">Importieren-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="48fad-139">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="48fad-140">Anfang-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="48fad-140">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="48fad-141">Stopp-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="48fad-141">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="48fad-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="48fad-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
