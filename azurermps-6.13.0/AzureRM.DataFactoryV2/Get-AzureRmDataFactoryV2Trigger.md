---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 7c14b5c53cdffa51671a64ad40fe18a400ae6803
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502157"
---
# <span data-ttu-id="df18b-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="df18b-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="df18b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="df18b-102">SYNOPSIS</span></span>
<span data-ttu-id="df18b-103">Ruft Informationen zu Triggern in einer Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="df18b-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df18b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="df18b-104">SYNTAX</span></span>

### <span data-ttu-id="df18b-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="df18b-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df18b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="df18b-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df18b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="df18b-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df18b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df18b-108">DESCRIPTION</span></span>
<span data-ttu-id="df18b-109">Das Cmdlet " **Get-AzureRmDataFactoryV2Trigger** " Ruft Informationen zu Triggern in einer Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="df18b-109">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="df18b-110">Wenn Sie den Namen eines Triggers angeben, ruft das Cmdlet Informationen zu diesem Trigger ab.</span><span class="sxs-lookup"><span data-stu-id="df18b-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="df18b-111">Wenn Sie keinen Namen angeben, ruft das Cmdlet Informationen zu allen Triggern in der Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="df18b-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="df18b-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df18b-112">EXAMPLES</span></span>

### <span data-ttu-id="df18b-113">Beispiel 1: Abrufen von Informationen zu einem bestimmten Trigger</span><span class="sxs-lookup"><span data-stu-id="df18b-113">Example 1: Get information about a specific trigger</span></span>
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

<span data-ttu-id="df18b-114">Ruft eine Liste aller Trigger ab, die in der Data Factory "WikiADF" erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="df18b-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="df18b-115">Beispiel 2: Abrufen von Informationen zu allen Triggern</span><span class="sxs-lookup"><span data-stu-id="df18b-115">Example 2: Get information about all triggers</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="df18b-116">Ruft einen einzelnen Trigger mit dem Namen "ScheduledTrigger" in der Data Factory "WikiADF" ab.</span><span class="sxs-lookup"><span data-stu-id="df18b-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="df18b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="df18b-117">PARAMETERS</span></span>

### <span data-ttu-id="df18b-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="df18b-118">-DataFactory</span></span>
<span data-ttu-id="df18b-119">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="df18b-119">The data factory object.</span></span>

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

### <span data-ttu-id="df18b-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="df18b-120">-DataFactoryName</span></span>
<span data-ttu-id="df18b-121">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="df18b-121">The data factory name.</span></span>

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

### <span data-ttu-id="df18b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df18b-122">-DefaultProfile</span></span>
<span data-ttu-id="df18b-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="df18b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df18b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="df18b-124">-Name</span></span>
<span data-ttu-id="df18b-125">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="df18b-125">The trigger name.</span></span>

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

### <span data-ttu-id="df18b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df18b-126">-ResourceGroupName</span></span>
<span data-ttu-id="df18b-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="df18b-127">The resource group name.</span></span>

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

### <span data-ttu-id="df18b-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="df18b-128">-ResourceId</span></span>
<span data-ttu-id="df18b-129">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="df18b-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="df18b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df18b-130">CommonParameters</span></span>
<span data-ttu-id="df18b-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df18b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df18b-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df18b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df18b-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="df18b-133">INPUTS</span></span>

### <span data-ttu-id="df18b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="df18b-134">System.String</span></span>

### <span data-ttu-id="df18b-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="df18b-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="df18b-136">Parameter: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="df18b-136">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="df18b-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="df18b-137">OUTPUTS</span></span>

### <span data-ttu-id="df18b-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="df18b-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="df18b-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="df18b-139">NOTES</span></span>

## <span data-ttu-id="df18b-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="df18b-140">RELATED LINKS</span></span>

[<span data-ttu-id="df18b-141">Satz-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="df18b-141">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="df18b-142">Anfang-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="df18b-142">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="df18b-143">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="df18b-143">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="df18b-144">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="df18b-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
