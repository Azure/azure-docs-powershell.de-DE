---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
ms.openlocfilehash: 7d3f1ca73712753ad38b46c186a51bd7aa159b46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662478"
---
# <span data-ttu-id="c71b9-101">Get-AzureRmDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="c71b9-101">Get-AzureRmDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="c71b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c71b9-102">SYNOPSIS</span></span>
<span data-ttu-id="c71b9-103">Gibt Informationen zu Trigger-Läufen zurück.</span><span class="sxs-lookup"><span data-stu-id="c71b9-103">Returns information about trigger runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c71b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c71b9-104">SYNTAX</span></span>

### <span data-ttu-id="c71b9-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c71b9-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c71b9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c71b9-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c71b9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c71b9-107">DESCRIPTION</span></span>
<span data-ttu-id="c71b9-108">Der Befehl " **Get-AzureRmDataFactoryV2TriggerRun** " gibt detaillierte Informationen zu Trigger-Läufen für den angegebenen Trigger im angegebenen Zeitrahmen zurück.</span><span class="sxs-lookup"><span data-stu-id="c71b9-108">The **Get-AzureRmDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="c71b9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c71b9-109">EXAMPLES</span></span>

### <span data-ttu-id="c71b9-110">Beispiel 1: Abrufen von Informationen zur Trigger-Ausführung</span><span class="sxs-lookup"><span data-stu-id="c71b9-110">Example 1: Get information about trigger run</span></span>
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

<span data-ttu-id="c71b9-111">Dieser Befehl zeigt Informationen zu den Läufen für "WikiTrigger" in der Factory "WikiADF" an, die zwischen "2017-09-01" und "2019-09-30" gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="c71b9-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="c71b9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c71b9-112">PARAMETERS</span></span>

### <span data-ttu-id="c71b9-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c71b9-113">-DataFactory</span></span>
<span data-ttu-id="c71b9-114">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c71b9-114">The data factory object.</span></span>

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

### <span data-ttu-id="c71b9-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="c71b9-115">-DataFactoryName</span></span>
<span data-ttu-id="c71b9-116">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="c71b9-116">The data factory name.</span></span>

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

### <span data-ttu-id="c71b9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c71b9-117">-Name</span></span>
<span data-ttu-id="c71b9-118">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="c71b9-118">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c71b9-119">-ResourceGroupName</span></span>
<span data-ttu-id="c71b9-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c71b9-120">The resource group name.</span></span>

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

### <span data-ttu-id="c71b9-121">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="c71b9-121">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="c71b9-122">Die Zeit, zu der oder nach der der Trigger gestartet wurde, um im ISO8601-Format ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="c71b9-122">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="c71b9-123">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="c71b9-123">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="c71b9-124">Die Zeitspanne, zu der der Trigger gestartet wurde, um im ISO8601-Format ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="c71b9-124">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c71b9-125">-DefaultProfile</span></span>
<span data-ttu-id="c71b9-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c71b9-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71b9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c71b9-127">CommonParameters</span></span>
<span data-ttu-id="c71b9-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c71b9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c71b9-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c71b9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c71b9-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c71b9-130">INPUTS</span></span>

### <span data-ttu-id="c71b9-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c71b9-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="c71b9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c71b9-132">System.String</span></span>

## <span data-ttu-id="c71b9-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c71b9-133">OUTPUTS</span></span>

### <span data-ttu-id="c71b9-134">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerRun, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c71b9-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="c71b9-135">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="c71b9-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="c71b9-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="c71b9-136">NOTES</span></span>

## <span data-ttu-id="c71b9-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c71b9-137">RELATED LINKS</span></span>

[<span data-ttu-id="c71b9-138">Anfang-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c71b9-138">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="c71b9-139">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c71b9-139">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

