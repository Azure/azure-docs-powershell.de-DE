---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 3f98ff38d5e74b7b167dc3a168a1cc05a42a7a23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661354"
---
# <span data-ttu-id="60c90-101">Get-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="60c90-101">Get-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="60c90-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60c90-102">SYNOPSIS</span></span>
<span data-ttu-id="60c90-103">Gibt Informationen zu Trigger-Läufen zurück.</span><span class="sxs-lookup"><span data-stu-id="60c90-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="60c90-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60c90-104">SYNTAX</span></span>

### <span data-ttu-id="60c90-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="60c90-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60c90-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="60c90-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60c90-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60c90-107">DESCRIPTION</span></span>
<span data-ttu-id="60c90-108">Der Befehl " **Get-AzDataFactoryV2TriggerRun** " gibt detaillierte Informationen zu Trigger-Läufen für den angegebenen Trigger im angegebenen Zeitrahmen zurück.</span><span class="sxs-lookup"><span data-stu-id="60c90-108">The **Get-AzDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="60c90-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60c90-109">EXAMPLES</span></span>

### <span data-ttu-id="60c90-110">Beispiel 1: Abrufen von Informationen zur Trigger-Ausführung</span><span class="sxs-lookup"><span data-stu-id="60c90-110">Example 1: Get information about trigger run</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "WikiTrigger" -TriggerRunStartedAfter "2017-09-01" -TriggerRunStartedBefore "2019-09-30"

    ResourceGroupName   : ADF
    DataFactoryName     : WikiADF
    TriggerName         : WikiTrigger
    TriggerRunId        : 08586958400454144995526033731
    TriggerType         : ScheduleTrigger
    TriggerRunTimestamp : 9/18/2017 8:34:00 PM
    Status              : Succeeded
```

<span data-ttu-id="60c90-111">Dieser Befehl zeigt Informationen zu den Läufen für "WikiTrigger" in der Factory "WikiADF" an, die zwischen "2017-09-01" und "2019-09-30" gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="60c90-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="60c90-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="60c90-112">PARAMETERS</span></span>

### <span data-ttu-id="60c90-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="60c90-113">-DataFactory</span></span>
<span data-ttu-id="60c90-114">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="60c90-114">The data factory object.</span></span>

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

### <span data-ttu-id="60c90-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="60c90-115">-DataFactoryName</span></span>
<span data-ttu-id="60c90-116">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="60c90-116">The data factory name.</span></span>

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

### <span data-ttu-id="60c90-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60c90-117">-DefaultProfile</span></span>
<span data-ttu-id="60c90-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="60c90-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60c90-119">-Name</span><span class="sxs-lookup"><span data-stu-id="60c90-119">-Name</span></span>
<span data-ttu-id="60c90-120">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="60c90-120">The trigger name.</span></span>

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

### <span data-ttu-id="60c90-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60c90-121">-ResourceGroupName</span></span>
<span data-ttu-id="60c90-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="60c90-122">The resource group name.</span></span>

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

### <span data-ttu-id="60c90-123">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="60c90-123">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="60c90-124">Die Zeit, zu der oder nach der der Trigger gestartet wurde, um im ISO8601-Format ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="60c90-124">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="60c90-125">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="60c90-125">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="60c90-126">Die Zeitspanne, zu der der Trigger gestartet wurde, um im ISO8601-Format ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="60c90-126">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="60c90-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60c90-127">CommonParameters</span></span>
<span data-ttu-id="60c90-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60c90-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60c90-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60c90-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60c90-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60c90-130">INPUTS</span></span>

### <span data-ttu-id="60c90-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="60c90-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="60c90-132">System. String</span><span class="sxs-lookup"><span data-stu-id="60c90-132">System.String</span></span>

## <span data-ttu-id="60c90-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60c90-133">OUTPUTS</span></span>

### <span data-ttu-id="60c90-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="60c90-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="60c90-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="60c90-135">NOTES</span></span>

## <span data-ttu-id="60c90-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60c90-136">RELATED LINKS</span></span>

[<span data-ttu-id="60c90-137">Anfang-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="60c90-137">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="60c90-138">Stopp-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="60c90-138">Stop-AzDataFactoryV2Trigger</span></span>]()

