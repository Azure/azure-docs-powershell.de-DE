---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: d5ea2dee1f6023b9505c38a58d364b7aa92591db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664281"
---
# <span data-ttu-id="c5e50-101">Get-AzureRmDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="c5e50-101">Get-AzureRmDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="c5e50-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c5e50-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e50-103">Gibt Informationen zu Trigger-Läufen zurück.</span><span class="sxs-lookup"><span data-stu-id="c5e50-103">Returns information about trigger runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5e50-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5e50-104">SYNTAX</span></span>

### <span data-ttu-id="c5e50-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c5e50-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="c5e50-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c5e50-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="c5e50-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5e50-107">DESCRIPTION</span></span>
<span data-ttu-id="c5e50-108">Der Befehl " **Get-AzureRmDataFactoryV2TriggerRun** " gibt detaillierte Informationen zu Trigger-Läufen für den angegebenen Trigger im angegebenen Zeitrahmen zurück.</span><span class="sxs-lookup"><span data-stu-id="c5e50-108">The **Get-AzureRmDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="c5e50-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5e50-109">EXAMPLES</span></span>

### <span data-ttu-id="c5e50-110">Beispiel 1: Abrufen von Informationen zur Trigger-Ausführung</span><span class="sxs-lookup"><span data-stu-id="c5e50-110">Example 1: Get information about trigger run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "WikiTrigger" -TriggerRunStartedAfter "2017-09-01" -TriggerRunStartedBefore "2019-09-30"

    ResourceGroupName   : ADF
    DataFactoryName     : WikiADF
    TriggerName         : WikiTrigger
    TriggerRunId        : 08586958400454144995526033731
    TriggerType         : ScheduleTrigger
    TriggerRunTimestamp : 9/18/2017 8:34:00 PM
    Status              : Succeeded

```

<span data-ttu-id="c5e50-111">Dieser Befehl zeigt Informationen zu den Läufen für "WikiTrigger" in der Factory "WikiADF" an, die zwischen "2017-09-01" und "2019-09-30" gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="c5e50-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="c5e50-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5e50-112">PARAMETERS</span></span>

### <span data-ttu-id="c5e50-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c5e50-113">-DataFactory</span></span>
<span data-ttu-id="c5e50-114">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c5e50-114">The data factory object.</span></span>

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

### <span data-ttu-id="c5e50-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="c5e50-115">-DataFactoryName</span></span>
<span data-ttu-id="c5e50-116">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="c5e50-116">The data factory name.</span></span>

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

### <span data-ttu-id="c5e50-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c5e50-117">-Name</span></span>
<span data-ttu-id="c5e50-118">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="c5e50-118">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e50-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5e50-119">-ResourceGroupName</span></span>
<span data-ttu-id="c5e50-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c5e50-120">The resource group name.</span></span>

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

### <span data-ttu-id="c5e50-121">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="c5e50-121">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="c5e50-122">Die Zeit, zu der oder nach der der Trigger gestartet wurde, um im ISO8601-Format ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="c5e50-122">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="c5e50-123">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="c5e50-123">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="c5e50-124">Die Zeitspanne, zu der der Trigger gestartet wurde, um im ISO8601-Format ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="c5e50-124">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="c5e50-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c5e50-125">INPUTS</span></span>

### <span data-ttu-id="c5e50-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c5e50-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="c5e50-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c5e50-127">System.String</span></span>


## <span data-ttu-id="c5e50-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c5e50-128">OUTPUTS</span></span>

### <span data-ttu-id="c5e50-129">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerRun, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c5e50-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="c5e50-130">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="c5e50-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>


## <span data-ttu-id="c5e50-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="c5e50-131">NOTES</span></span>

## <span data-ttu-id="c5e50-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c5e50-132">RELATED LINKS</span></span>
[<span data-ttu-id="c5e50-133">Anfang-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c5e50-133">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="c5e50-134">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c5e50-134">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

