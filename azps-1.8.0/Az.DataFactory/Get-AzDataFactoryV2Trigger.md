---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
ms.openlocfilehash: e5afbdd389d1ee9e1b74895743ed47ceed0b4ae9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820403"
---
# <span data-ttu-id="856c3-101">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="856c3-101">Get-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="856c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="856c3-102">SYNOPSIS</span></span>
<span data-ttu-id="856c3-103">Ruft Informationen zu Triggern in einer Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="856c3-103">Gets information about triggers in a data factory.</span></span>

## <span data-ttu-id="856c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="856c3-104">SYNTAX</span></span>

### <span data-ttu-id="856c3-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="856c3-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="856c3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="856c3-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="856c3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="856c3-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="856c3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="856c3-108">DESCRIPTION</span></span>
<span data-ttu-id="856c3-109">Das Cmdlet " **Get-AzDataFactoryV2Trigger** " Ruft Informationen zu Triggern in einer Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="856c3-109">The **Get-AzDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="856c3-110">Wenn Sie den Namen eines Triggers angeben, ruft das Cmdlet Informationen zu diesem Trigger ab.</span><span class="sxs-lookup"><span data-stu-id="856c3-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="856c3-111">Wenn Sie keinen Namen angeben, ruft das Cmdlet Informationen zu allen Triggern in der Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="856c3-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="856c3-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="856c3-112">EXAMPLES</span></span>

### <span data-ttu-id="856c3-113">Beispiel 1: Abrufen von Informationen zu einem bestimmten Trigger</span><span class="sxs-lookup"><span data-stu-id="856c3-113">Example 1: Get information about a specific trigger</span></span>
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

<span data-ttu-id="856c3-114">Ruft eine Liste aller Trigger ab, die in der Data Factory "WikiADF" erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="856c3-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="856c3-115">Beispiel 2: Abrufen von Informationen zu allen Triggern</span><span class="sxs-lookup"><span data-stu-id="856c3-115">Example 2: Get information about all triggers</span></span>
```
Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="856c3-116">Ruft einen einzelnen Trigger mit dem Namen "ScheduledTrigger" in der Data Factory "WikiADF" ab.</span><span class="sxs-lookup"><span data-stu-id="856c3-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="856c3-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="856c3-117">PARAMETERS</span></span>

### <span data-ttu-id="856c3-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="856c3-118">-DataFactory</span></span>
<span data-ttu-id="856c3-119">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="856c3-119">The data factory object.</span></span>

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

### <span data-ttu-id="856c3-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="856c3-120">-DataFactoryName</span></span>
<span data-ttu-id="856c3-121">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="856c3-121">The data factory name.</span></span>

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

### <span data-ttu-id="856c3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="856c3-122">-DefaultProfile</span></span>
<span data-ttu-id="856c3-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="856c3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="856c3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="856c3-124">-Name</span></span>
<span data-ttu-id="856c3-125">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="856c3-125">The trigger name.</span></span>

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

### <span data-ttu-id="856c3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="856c3-126">-ResourceGroupName</span></span>
<span data-ttu-id="856c3-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="856c3-127">The resource group name.</span></span>

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

### <span data-ttu-id="856c3-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="856c3-128">-ResourceId</span></span>
<span data-ttu-id="856c3-129">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="856c3-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="856c3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="856c3-130">CommonParameters</span></span>
<span data-ttu-id="856c3-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="856c3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="856c3-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="856c3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="856c3-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="856c3-133">INPUTS</span></span>

### <span data-ttu-id="856c3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="856c3-134">System.String</span></span>

### <span data-ttu-id="856c3-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="856c3-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="856c3-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="856c3-136">OUTPUTS</span></span>

### <span data-ttu-id="856c3-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="856c3-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="856c3-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="856c3-138">NOTES</span></span>

## <span data-ttu-id="856c3-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="856c3-139">RELATED LINKS</span></span>

[<span data-ttu-id="856c3-140">Satz-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="856c3-140">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="856c3-141">Anfang-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="856c3-141">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="856c3-142">Stopp-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="856c3-142">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="856c3-143">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="856c3-143">Remove-AzDataFactoryV2Trigger</span></span>]()
