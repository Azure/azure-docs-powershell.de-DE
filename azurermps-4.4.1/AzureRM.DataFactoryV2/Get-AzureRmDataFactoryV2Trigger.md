---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: bc60bbb5b48c4022e7db6a95e26a1f43ef891ae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505086"
---
# <span data-ttu-id="6ccf9-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6ccf9-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="6ccf9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6ccf9-102">SYNOPSIS</span></span>
<span data-ttu-id="6ccf9-103">Ruft Informationen zu Triggern in einer Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ccf9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ccf9-104">SYNTAX</span></span>

### <span data-ttu-id="6ccf9-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6ccf9-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="6ccf9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6ccf9-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="6ccf9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ccf9-107">DESCRIPTION</span></span>
<span data-ttu-id="6ccf9-108">Das Cmdlet " **Get-AzureRmDataFactoryV2Trigger** " Ruft Informationen zu Triggern in einer Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-108">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="6ccf9-109">Wenn Sie den Namen eines Triggers angeben, ruft das Cmdlet Informationen zu diesem Trigger ab.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="6ccf9-110">Wenn Sie keinen Namen angeben, ruft das Cmdlet Informationen zu allen Triggern in der Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-110">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>


## <span data-ttu-id="6ccf9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6ccf9-111">EXAMPLES</span></span>

### <span data-ttu-id="6ccf9-112">Beispiel 1: Abrufen von Informationen zu einem bestimmten Trigger</span><span class="sxs-lookup"><span data-stu-id="6ccf9-112">Example 1: Get information about a specific trigger</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

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

<span data-ttu-id="6ccf9-113">Ruft eine Liste aller Trigger ab, die in der Data Factory "WikiADF" erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-113">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="6ccf9-114">Beispiel 2: Abrufen von Informationen zu allen Triggern</span><span class="sxs-lookup"><span data-stu-id="6ccf9-114">Example 2: Get information about all triggers</span></span>

```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="6ccf9-115">Ruft einen einzelnen Trigger mit dem Namen "ScheduledTrigger" in der Data Factory "WikiADF" ab.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-115">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="6ccf9-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ccf9-116">PARAMETERS</span></span>

### <span data-ttu-id="6ccf9-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6ccf9-117">-DataFactory</span></span>
<span data-ttu-id="6ccf9-118">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-118">The data factory object.</span></span>

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

### <span data-ttu-id="6ccf9-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="6ccf9-119">-DataFactoryName</span></span>
<span data-ttu-id="6ccf9-120">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-120">The data factory name.</span></span>

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

### <span data-ttu-id="6ccf9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6ccf9-121">-Name</span></span>
<span data-ttu-id="6ccf9-122">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ccf9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ccf9-123">-ResourceGroupName</span></span>
<span data-ttu-id="6ccf9-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-124">The resource group name.</span></span>

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

## <span data-ttu-id="6ccf9-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6ccf9-125">INPUTS</span></span>

### <span data-ttu-id="6ccf9-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6ccf9-126">System.String</span></span>
<span data-ttu-id="6ccf9-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6ccf9-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="6ccf9-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6ccf9-128">OUTPUTS</span></span>

### <span data-ttu-id="6ccf9-129">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6ccf9-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="6ccf9-130">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="6ccf9-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="6ccf9-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="6ccf9-131">NOTES</span></span>

## <span data-ttu-id="6ccf9-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6ccf9-132">RELATED LINKS</span></span>
[<span data-ttu-id="6ccf9-133">Satz-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6ccf9-133">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6ccf9-134">Anfang-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6ccf9-134">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6ccf9-135">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6ccf9-135">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6ccf9-136">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6ccf9-136">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
