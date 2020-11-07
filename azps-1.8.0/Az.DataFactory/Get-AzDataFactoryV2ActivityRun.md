---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
ms.openlocfilehash: 5f6c56fac892e2c3e9c1546dac226c5d81ddb99e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661365"
---
# <span data-ttu-id="e1fcd-101">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="e1fcd-101">Get-AzDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="e1fcd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1fcd-102">SYNOPSIS</span></span>
<span data-ttu-id="e1fcd-103">Ruft Informationen zu Aktivitäts Läufen für eine Pipelineausführung ab.</span><span class="sxs-lookup"><span data-stu-id="e1fcd-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="e1fcd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1fcd-104">SYNTAX</span></span>

### <span data-ttu-id="e1fcd-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e1fcd-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1fcd-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e1fcd-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1fcd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1fcd-107">DESCRIPTION</span></span>
<span data-ttu-id="e1fcd-108">Das Cmdlet " **Get-AzDataFactoryV2ActivityRun** " Ruft Informationen zu ausgeführten Ausführungen in Azure Data Factory für den angegebenen Pipeline Durchlauf ab, der im angegebenen Zeitrahmen stattgefunden hat.</span><span class="sxs-lookup"><span data-stu-id="e1fcd-108">The **Get-AzDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="e1fcd-109">Darüber hinaus können Sie Filter für den Aktivitätsnamen, den Namen des verknüpften Diensts und den Ausführungsstatus angeben.</span><span class="sxs-lookup"><span data-stu-id="e1fcd-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="e1fcd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1fcd-110">EXAMPLES</span></span>

### <span data-ttu-id="e1fcd-111">Beispiel 1: Abrufen aller Aktivitäts Läufe für eine Pipelineausführung</span><span class="sxs-lookup"><span data-stu-id="e1fcd-111">Example 1: Get all activity runs for a pipeline run</span></span>
```
PS C:\> Get-AzDataFactoryV2ActivityRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter "2017-09-01" -RunStartedBefore "2017-09-30"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    ActivityName      : MyWebActivity
    PipelineRunId     : f288712d-fb08-4cb8-96ef-82d3b9b30621
    PipelineName      : DPWikisample
    Input             : {method, url, headers, body...}
    Output            : {operationstatus}
    ActivityRunStart  : 9/14/2017 12:20:57 AM
    ActivityRunEnd    : 9/14/2017 12:21:00 AM
    DurationInMs      : 2768
    Status            : Succeeded
    Error             : {errorCode, message, failureType, target}
```

<span data-ttu-id="e1fcd-112">Dieser Befehl ruft Details zu allen Aktivitäten ab, die in der Pipeline ausgeführt werden, mit der ID "f288712d-fb08-4cb8-96ef-82d3b9b30621", die zwischen "2017-09-01" und "2017-09-30" stattgefunden hat.</span><span class="sxs-lookup"><span data-stu-id="e1fcd-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="e1fcd-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1fcd-113">PARAMETERS</span></span>

### <span data-ttu-id="e1fcd-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="e1fcd-114">-ActivityName</span></span>
<span data-ttu-id="e1fcd-115">Der Name der Aktivität.</span><span class="sxs-lookup"><span data-stu-id="e1fcd-115">The name of the activity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1fcd-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e1fcd-116">-DataFactory</span></span>
<span data-ttu-id="e1fcd-117">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e1fcd-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1fcd-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e1fcd-118">-DataFactoryName</span></span>
<span data-ttu-id="e1fcd-119">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="e1fcd-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1fcd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1fcd-120">-DefaultProfile</span></span>
<span data-ttu-id="e1fcd-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e1fcd-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1fcd-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="e1fcd-122">-PipelineRunId</span></span>
<span data-ttu-id="e1fcd-123">Die Ausführungs-ID der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e1fcd-123">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1fcd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1fcd-124">-ResourceGroupName</span></span>
<span data-ttu-id="e1fcd-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e1fcd-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1fcd-126">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="e1fcd-126">-RunStartedAfter</span></span>
<span data-ttu-id="e1fcd-127">Die Zeit, zu der oder nach der die Ausführung der Pipeline gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="e1fcd-127">The time at or after which the pipeline run started to execute.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1fcd-128">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="e1fcd-128">-RunStartedBefore</span></span>
<span data-ttu-id="e1fcd-129">Die Zeit, zu der oder vor dem die Ausführung der Pipeline ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="e1fcd-129">The time at or before which the pipeline run started to execute.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1fcd-130">-Status</span><span class="sxs-lookup"><span data-stu-id="e1fcd-130">-Status</span></span>
<span data-ttu-id="e1fcd-131">Der Status der Pipelineausführung.</span><span class="sxs-lookup"><span data-stu-id="e1fcd-131">The status of the pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1fcd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1fcd-132">CommonParameters</span></span>
<span data-ttu-id="e1fcd-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1fcd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1fcd-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1fcd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1fcd-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1fcd-135">INPUTS</span></span>

### <span data-ttu-id="e1fcd-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e1fcd-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="e1fcd-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e1fcd-137">System.String</span></span>

## <span data-ttu-id="e1fcd-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1fcd-138">OUTPUTS</span></span>

### <span data-ttu-id="e1fcd-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="e1fcd-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="e1fcd-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1fcd-140">NOTES</span></span>

## <span data-ttu-id="e1fcd-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1fcd-141">RELATED LINKS</span></span>

[<span data-ttu-id="e1fcd-142">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e1fcd-142">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="e1fcd-143">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="e1fcd-143">Get-AzDataFactoryV2PipelineRun</span></span>]()

