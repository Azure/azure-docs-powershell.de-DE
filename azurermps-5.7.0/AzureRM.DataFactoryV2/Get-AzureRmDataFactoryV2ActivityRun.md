---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
ms.openlocfilehash: 300aad37f2dede64a4adebc4f1a9d9eb9cc43743
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478518"
---
# <span data-ttu-id="60218-101">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="60218-101">Get-AzureRmDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="60218-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60218-102">SYNOPSIS</span></span>
<span data-ttu-id="60218-103">Ruft Informationen zu Aktivitäts Läufen für eine Pipelineausführung ab.</span><span class="sxs-lookup"><span data-stu-id="60218-103">Gets information about activity runs for a pipeline run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60218-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60218-104">SYNTAX</span></span>

### <span data-ttu-id="60218-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="60218-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [[-LinkedServiceName] <String>]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="60218-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="60218-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [[-LinkedServiceName] <String>]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60218-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60218-107">DESCRIPTION</span></span>
<span data-ttu-id="60218-108">Das Cmdlet " **Get-AzureRmDataFactoryV2ActivityRun** " Ruft Informationen zu ausgeführten Ausführungen in Azure Data Factory für den angegebenen Pipeline Durchlauf ab, der im angegebenen Zeitrahmen stattgefunden hat.</span><span class="sxs-lookup"><span data-stu-id="60218-108">The **Get-AzureRmDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="60218-109">Darüber hinaus können Sie Filter für den Aktivitätsnamen, den Namen des verknüpften Diensts und den Ausführungsstatus angeben.</span><span class="sxs-lookup"><span data-stu-id="60218-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="60218-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60218-110">EXAMPLES</span></span>

### <span data-ttu-id="60218-111">Beispiel 1: Abrufen aller Aktivitäts Läufe für eine Pipelineausführung</span><span class="sxs-lookup"><span data-stu-id="60218-111">Example 1: Get all activity runs for a pipeline run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2ActivityRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter "2017-09-01" -RunStartedBefore "2017-09-30"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    ActivityName      : MyWebActivity
    PipelineRunId     : f288712d-fb08-4cb8-96ef-82d3b9b30621
    PipelineName      : DPWikisample
    Input             : {method, url, headers, body...}
    Output            : {operationstatus}
    LinkedServiceName :
    ActivityRunStart  : 9/14/2017 12:20:57 AM
    ActivityRunEnd    : 9/14/2017 12:21:00 AM
    DurationInMs      : 2768
    Status            : Succeeded
    Error             : {errorCode, message, failureType, target}
```

<span data-ttu-id="60218-112">Dieser Befehl ruft Details zu allen Aktivitäten ab, die in der Pipeline ausgeführt werden, mit der ID "f288712d-fb08-4cb8-96ef-82d3b9b30621", die zwischen "2017-09-01" und "2017-09-30" stattgefunden hat.</span><span class="sxs-lookup"><span data-stu-id="60218-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="60218-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="60218-113">PARAMETERS</span></span>

### <span data-ttu-id="60218-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="60218-114">-ActivityName</span></span>
<span data-ttu-id="60218-115">Der Name der Aktivität.</span><span class="sxs-lookup"><span data-stu-id="60218-115">The name of the activity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60218-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="60218-116">-DataFactory</span></span>
<span data-ttu-id="60218-117">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="60218-117">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60218-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="60218-118">-DataFactoryName</span></span>
<span data-ttu-id="60218-119">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="60218-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60218-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60218-120">-DefaultProfile</span></span>
<span data-ttu-id="60218-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="60218-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60218-122">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="60218-122">-LinkedServiceName</span></span>
<span data-ttu-id="60218-123">Der Name des verknüpften Diensts.</span><span class="sxs-lookup"><span data-stu-id="60218-123">The linked service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60218-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="60218-124">-PipelineRunId</span></span>
<span data-ttu-id="60218-125">Die Ausführungs-ID der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="60218-125">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60218-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60218-126">-ResourceGroupName</span></span>
<span data-ttu-id="60218-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="60218-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60218-128">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="60218-128">-RunStartedAfter</span></span>
<span data-ttu-id="60218-129">Die Zeit, zu der oder nach der die Ausführung der Pipeline gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="60218-129">The time at or after which the pipeline run started to execute.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60218-130">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="60218-130">-RunStartedBefore</span></span>
<span data-ttu-id="60218-131">Die Zeit, zu der oder vor dem die Ausführung der Pipeline ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="60218-131">The time at or before which the pipeline run started to execute.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60218-132">-Status</span><span class="sxs-lookup"><span data-stu-id="60218-132">-Status</span></span>
<span data-ttu-id="60218-133">Der Status der Pipelineausführung.</span><span class="sxs-lookup"><span data-stu-id="60218-133">The status of the pipeline run.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60218-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60218-134">CommonParameters</span></span>
<span data-ttu-id="60218-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60218-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60218-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60218-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60218-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60218-137">INPUTS</span></span>

### <span data-ttu-id="60218-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="60218-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="60218-139">System. String</span><span class="sxs-lookup"><span data-stu-id="60218-139">System.String</span></span>

## <span data-ttu-id="60218-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60218-140">OUTPUTS</span></span>

### <span data-ttu-id="60218-141">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSActivityRun, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="60218-141">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="60218-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="60218-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="60218-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="60218-143">NOTES</span></span>

## <span data-ttu-id="60218-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60218-144">RELATED LINKS</span></span>

[<span data-ttu-id="60218-145">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="60218-145">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="60218-146">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="60218-146">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

