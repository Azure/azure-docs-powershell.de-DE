---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 3d5db6b7aa1b7c2ffdd63292696230e2d12bd4c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479870"
---
# <span data-ttu-id="b1130-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b1130-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="b1130-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1130-102">SYNOPSIS</span></span>
<span data-ttu-id="b1130-103">Ruft Informationen zu Triggern in einer Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="b1130-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1130-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1130-104">SYNTAX</span></span>

### <span data-ttu-id="b1130-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b1130-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1130-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b1130-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1130-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1130-107">DESCRIPTION</span></span>
<span data-ttu-id="b1130-108">Das Cmdlet " **Get-AzureRmDataFactoryV2Trigger** " Ruft Informationen zu Triggern in einer Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="b1130-108">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="b1130-109">Wenn Sie den Namen eines Triggers angeben, ruft das Cmdlet Informationen zu diesem Trigger ab.</span><span class="sxs-lookup"><span data-stu-id="b1130-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="b1130-110">Wenn Sie keinen Namen angeben, ruft das Cmdlet Informationen zu allen Triggern in der Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="b1130-110">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="b1130-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1130-111">EXAMPLES</span></span>

### <span data-ttu-id="b1130-112">Beispiel 1: Abrufen von Informationen zu einem bestimmten Trigger</span><span class="sxs-lookup"><span data-stu-id="b1130-112">Example 1: Get information about a specific trigger</span></span>
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

<span data-ttu-id="b1130-113">Ruft eine Liste aller Trigger ab, die in der Data Factory "WikiADF" erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b1130-113">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="b1130-114">Beispiel 2: Abrufen von Informationen zu allen Triggern</span><span class="sxs-lookup"><span data-stu-id="b1130-114">Example 2: Get information about all triggers</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="b1130-115">Ruft einen einzelnen Trigger mit dem Namen "ScheduledTrigger" in der Data Factory "WikiADF" ab.</span><span class="sxs-lookup"><span data-stu-id="b1130-115">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="b1130-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1130-116">PARAMETERS</span></span>

### <span data-ttu-id="b1130-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b1130-117">-DataFactory</span></span>
<span data-ttu-id="b1130-118">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b1130-118">The data factory object.</span></span>

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

### <span data-ttu-id="b1130-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="b1130-119">-DataFactoryName</span></span>
<span data-ttu-id="b1130-120">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="b1130-120">The data factory name.</span></span>

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

### <span data-ttu-id="b1130-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b1130-121">-Name</span></span>
<span data-ttu-id="b1130-122">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="b1130-122">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1130-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1130-123">-ResourceGroupName</span></span>
<span data-ttu-id="b1130-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b1130-124">The resource group name.</span></span>

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

### <span data-ttu-id="b1130-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1130-125">-DefaultProfile</span></span>
<span data-ttu-id="b1130-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1130-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1130-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1130-127">CommonParameters</span></span>
<span data-ttu-id="b1130-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1130-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1130-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1130-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1130-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1130-130">INPUTS</span></span>

### <span data-ttu-id="b1130-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b1130-131">System.String</span></span>
<span data-ttu-id="b1130-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b1130-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="b1130-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1130-133">OUTPUTS</span></span>

### <span data-ttu-id="b1130-134">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b1130-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="b1130-135">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="b1130-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="b1130-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1130-136">NOTES</span></span>

## <span data-ttu-id="b1130-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1130-137">RELATED LINKS</span></span>

[<span data-ttu-id="b1130-138">Satz-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b1130-138">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="b1130-139">Anfang-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b1130-139">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="b1130-140">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b1130-140">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="b1130-141">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b1130-141">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
