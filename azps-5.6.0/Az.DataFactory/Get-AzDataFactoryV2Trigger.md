---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 5940d362b3c06ede714568daa2ecce8bd829581d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930179"
---
# <span data-ttu-id="bd16c-101">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="bd16c-101">Get-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="bd16c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd16c-102">SYNOPSIS</span></span>
<span data-ttu-id="bd16c-103">Ruft Informationen zu Triggern in einer Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="bd16c-103">Gets information about triggers in a data factory.</span></span>

## <span data-ttu-id="bd16c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd16c-104">SYNTAX</span></span>

### <span data-ttu-id="bd16c-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="bd16c-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd16c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bd16c-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd16c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bd16c-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd16c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd16c-108">DESCRIPTION</span></span>
<span data-ttu-id="bd16c-109">Das **Get-AzDataFactoryV2Trigger-Cmdlet** ruft Informationen zu Triggern in einer Datenfactory ab.</span><span class="sxs-lookup"><span data-stu-id="bd16c-109">The **Get-AzDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="bd16c-110">Wenn Sie den Namen eines Triggers angeben, ruft das Cmdlet Informationen zu diesem Trigger ab.</span><span class="sxs-lookup"><span data-stu-id="bd16c-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="bd16c-111">Wenn Sie keinen Namen angeben, ruft das Cmdlet Informationen zu allen Triggern in der Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="bd16c-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="bd16c-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bd16c-112">EXAMPLES</span></span>

### <span data-ttu-id="bd16c-113">Beispiel 1: Informationen zu allen Triggern</span><span class="sxs-lookup"><span data-stu-id="bd16c-113">Example 1: Get information about all triggers</span></span>
```
PS C:\> Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped

    TriggerName       : ScheduledTrigger2
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="bd16c-114">Ruft eine Liste aller Trigger ab, die in der Daten factory "WikiADF" erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="bd16c-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="bd16c-115">Beispiel 2: Informationen zu einem bestimmten Trigger erhalten</span><span class="sxs-lookup"><span data-stu-id="bd16c-115">Example 2: Get information about a specific trigger</span></span>
```
Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="bd16c-116">Ruft einen einzelnen Trigger mit dem Namen "ScheduledTrigger" in der Daten factory "WikiADF" ab.</span><span class="sxs-lookup"><span data-stu-id="bd16c-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="bd16c-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bd16c-117">PARAMETERS</span></span>

### <span data-ttu-id="bd16c-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="bd16c-118">-DataFactory</span></span>
<span data-ttu-id="bd16c-119">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="bd16c-119">The data factory object.</span></span>

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

### <span data-ttu-id="bd16c-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bd16c-120">-DataFactoryName</span></span>
<span data-ttu-id="bd16c-121">Der Name der Datenfabrik.</span><span class="sxs-lookup"><span data-stu-id="bd16c-121">The data factory name.</span></span>

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

### <span data-ttu-id="bd16c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd16c-122">-DefaultProfile</span></span>
<span data-ttu-id="bd16c-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bd16c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd16c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="bd16c-124">-Name</span></span>
<span data-ttu-id="bd16c-125">Der Triggername.</span><span class="sxs-lookup"><span data-stu-id="bd16c-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd16c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd16c-126">-ResourceGroupName</span></span>
<span data-ttu-id="bd16c-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bd16c-127">The resource group name.</span></span>

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

### <span data-ttu-id="bd16c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd16c-128">-ResourceId</span></span>
<span data-ttu-id="bd16c-129">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="bd16c-129">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd16c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd16c-130">CommonParameters</span></span>
<span data-ttu-id="bd16c-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd16c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd16c-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd16c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd16c-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bd16c-133">INPUTS</span></span>

### <span data-ttu-id="bd16c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="bd16c-134">System.String</span></span>

### <span data-ttu-id="bd16c-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bd16c-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="bd16c-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bd16c-136">OUTPUTS</span></span>

### <span data-ttu-id="bd16c-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="bd16c-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="bd16c-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bd16c-138">NOTES</span></span>

## <span data-ttu-id="bd16c-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bd16c-139">RELATED LINKS</span></span>

[<span data-ttu-id="bd16c-140">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="bd16c-140">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="bd16c-141">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="bd16c-141">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="bd16c-142">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="bd16c-142">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="bd16c-143">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="bd16c-143">Remove-AzDataFactoryV2Trigger</span></span>]()
