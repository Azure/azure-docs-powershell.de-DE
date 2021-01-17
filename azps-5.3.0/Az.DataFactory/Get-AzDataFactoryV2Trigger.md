---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d315ae997a468abc3cd5f4e33601c1c9e770a40a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472674"
---
# <span data-ttu-id="97371-101">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="97371-101">Get-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="97371-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97371-102">SYNOPSIS</span></span>
<span data-ttu-id="97371-103">Ruft Informationen zu Triggern in einer Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="97371-103">Gets information about triggers in a data factory.</span></span>

## <span data-ttu-id="97371-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97371-104">SYNTAX</span></span>

### <span data-ttu-id="97371-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="97371-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97371-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="97371-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97371-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="97371-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97371-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97371-108">DESCRIPTION</span></span>
<span data-ttu-id="97371-109">Das **Cmdlet "Get-AzDataFactoryV2Trigger"** ruft Informationen zu Triggern in einer Datenfactory ab.</span><span class="sxs-lookup"><span data-stu-id="97371-109">The **Get-AzDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="97371-110">Wenn Sie den Namen eines Triggers angeben, ruft das Cmdlet Informationen zu diesem Trigger ab.</span><span class="sxs-lookup"><span data-stu-id="97371-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="97371-111">Wenn Sie keinen Namen angeben, ruft das Cmdlet Informationen zu allen Triggern in der Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="97371-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="97371-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="97371-112">EXAMPLES</span></span>

### <span data-ttu-id="97371-113">Beispiel 1: Informationen zu allen Triggern</span><span class="sxs-lookup"><span data-stu-id="97371-113">Example 1: Get information about all triggers</span></span>
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

<span data-ttu-id="97371-114">Ruft eine Liste aller Trigger ab, die in der Daten factory "WikiADF" erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="97371-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="97371-115">Beispiel 2: Erhalten von Informationen zu einem bestimmten Trigger</span><span class="sxs-lookup"><span data-stu-id="97371-115">Example 2: Get information about a specific trigger</span></span>
```
Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="97371-116">Ruft einen einzelnen Trigger namens "ScheduledTrigger" in der Daten factory "WikiADF" ab.</span><span class="sxs-lookup"><span data-stu-id="97371-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="97371-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97371-117">PARAMETERS</span></span>

### <span data-ttu-id="97371-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="97371-118">-DataFactory</span></span>
<span data-ttu-id="97371-119">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="97371-119">The data factory object.</span></span>

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

### <span data-ttu-id="97371-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="97371-120">-DataFactoryName</span></span>
<span data-ttu-id="97371-121">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="97371-121">The data factory name.</span></span>

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

### <span data-ttu-id="97371-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97371-122">-DefaultProfile</span></span>
<span data-ttu-id="97371-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97371-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97371-124">-Name</span><span class="sxs-lookup"><span data-stu-id="97371-124">-Name</span></span>
<span data-ttu-id="97371-125">Der Auslösername.</span><span class="sxs-lookup"><span data-stu-id="97371-125">The trigger name.</span></span>

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

### <span data-ttu-id="97371-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97371-126">-ResourceGroupName</span></span>
<span data-ttu-id="97371-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="97371-127">The resource group name.</span></span>

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

### <span data-ttu-id="97371-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97371-128">-ResourceId</span></span>
<span data-ttu-id="97371-129">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="97371-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="97371-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97371-130">CommonParameters</span></span>
<span data-ttu-id="97371-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97371-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97371-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97371-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97371-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="97371-133">INPUTS</span></span>

### <span data-ttu-id="97371-134">System.String</span><span class="sxs-lookup"><span data-stu-id="97371-134">System.String</span></span>

### <span data-ttu-id="97371-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="97371-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="97371-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="97371-136">OUTPUTS</span></span>

### <span data-ttu-id="97371-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="97371-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="97371-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="97371-138">NOTES</span></span>

## <span data-ttu-id="97371-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="97371-139">RELATED LINKS</span></span>

[<span data-ttu-id="97371-140">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="97371-140">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="97371-141">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="97371-141">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="97371-142">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="97371-142">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="97371-143">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="97371-143">Remove-AzDataFactoryV2Trigger</span></span>]()
