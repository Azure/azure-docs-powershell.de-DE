---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: ba9ea38f5915f5a89326c806e11a055ec6aeed75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930176"
---
# <span data-ttu-id="5f995-101">Get-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="5f995-101">Get-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="5f995-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f995-102">SYNOPSIS</span></span>
<span data-ttu-id="5f995-103">Gibt Informationen zu Triggerläufen zurück.</span><span class="sxs-lookup"><span data-stu-id="5f995-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="5f995-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f995-104">SYNTAX</span></span>

### <span data-ttu-id="5f995-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5f995-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f995-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5f995-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f995-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f995-107">DESCRIPTION</span></span>
<span data-ttu-id="5f995-108">Der **Befehl Get-AzDataFactoryV2TriggerRun** gibt detaillierte Informationen zu Triggerläufen für den angegebenen Trigger im angegebenen Zeitrahmen zurück.</span><span class="sxs-lookup"><span data-stu-id="5f995-108">The **Get-AzDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="5f995-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5f995-109">EXAMPLES</span></span>

### <span data-ttu-id="5f995-110">Beispiel 1: Informationen zur Triggerauslösung erhalten</span><span class="sxs-lookup"><span data-stu-id="5f995-110">Example 1: Get information about trigger run</span></span>
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

<span data-ttu-id="5f995-111">Dieser Befehl zeigt Informationen zu den Ausgeführt für "WikiTrigger" in der Factory "WikiADF", die zwischen "2017-09-01" und "2019-09-30" gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="5f995-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="5f995-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5f995-112">PARAMETERS</span></span>

### <span data-ttu-id="5f995-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5f995-113">-DataFactory</span></span>
<span data-ttu-id="5f995-114">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5f995-114">The data factory object.</span></span>

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

### <span data-ttu-id="5f995-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5f995-115">-DataFactoryName</span></span>
<span data-ttu-id="5f995-116">Der Name der Datenfabrik.</span><span class="sxs-lookup"><span data-stu-id="5f995-116">The data factory name.</span></span>

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

### <span data-ttu-id="5f995-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f995-117">-DefaultProfile</span></span>
<span data-ttu-id="5f995-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f995-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f995-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5f995-119">-Name</span></span>
<span data-ttu-id="5f995-120">Der Triggername.</span><span class="sxs-lookup"><span data-stu-id="5f995-120">The trigger name.</span></span>

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

### <span data-ttu-id="5f995-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f995-121">-ResourceGroupName</span></span>
<span data-ttu-id="5f995-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5f995-122">The resource group name.</span></span>

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

### <span data-ttu-id="5f995-123">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="5f995-123">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="5f995-124">Die Zeit, zu der oder nach der die Ausführung des Triggers im ISO8601-Format gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="5f995-124">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="5f995-125">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="5f995-125">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="5f995-126">Die Zeit, zu der oder vor der die Ausführung des Triggers im ISO8601-Format gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="5f995-126">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="5f995-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f995-127">CommonParameters</span></span>
<span data-ttu-id="5f995-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f995-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f995-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f995-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f995-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5f995-130">INPUTS</span></span>

### <span data-ttu-id="5f995-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5f995-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="5f995-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5f995-132">System.String</span></span>

## <span data-ttu-id="5f995-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5f995-133">OUTPUTS</span></span>

### <span data-ttu-id="5f995-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="5f995-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="5f995-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5f995-135">NOTES</span></span>

## <span data-ttu-id="5f995-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5f995-136">RELATED LINKS</span></span>

[<span data-ttu-id="5f995-137">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5f995-137">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5f995-138">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5f995-138">Stop-AzDataFactoryV2Trigger</span></span>]()

