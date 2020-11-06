---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/set-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
ms.openlocfilehash: 384c05e6424ab7b8d4fbb01a0c4822b73702c419
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497469"
---
# <span data-ttu-id="3b688-101">Set-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="3b688-101">Set-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="3b688-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3b688-102">SYNOPSIS</span></span>
<span data-ttu-id="3b688-103">Legt die Eigenschaften eines Ereignis Raster Themas fest.</span><span class="sxs-lookup"><span data-stu-id="3b688-103">Sets the properties of an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b688-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b688-104">SYNTAX</span></span>

### <span data-ttu-id="3b688-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3b688-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b688-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b688-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b688-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b688-107">TopicInputObjectParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b688-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b688-108">DESCRIPTION</span></span>
<span data-ttu-id="3b688-109">Legt die Eigenschaften eines Ereignis Raster Themas fest.</span><span class="sxs-lookup"><span data-stu-id="3b688-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="3b688-110">Dies kann verwendet werden, um die Tags eines Ereignis Raster Themas zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="3b688-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="3b688-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b688-111">EXAMPLES</span></span>

### <span data-ttu-id="3b688-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3b688-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="3b688-113">Legt die Eigenschaften des Ereignis Rasters Topic \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName fest \` , um die Tags durch die angegebenen Tags "Department" und "Environment" zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="3b688-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="3b688-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b688-114">PARAMETERS</span></span>

### <span data-ttu-id="3b688-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b688-115">-DefaultProfile</span></span>
<span data-ttu-id="3b688-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3b688-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b688-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3b688-117">-InputObject</span></span>
<span data-ttu-id="3b688-118">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3b688-118">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b688-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3b688-119">-Name</span></span>
<span data-ttu-id="3b688-120">EventGrid-Themen Name</span><span class="sxs-lookup"><span data-stu-id="3b688-120">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b688-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b688-121">-ResourceGroupName</span></span>
<span data-ttu-id="3b688-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3b688-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b688-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3b688-123">-ResourceId</span></span>
<span data-ttu-id="3b688-124">EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="3b688-124">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b688-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="3b688-125">-Tag</span></span>
<span data-ttu-id="3b688-126">Hashtables, die das Ressourcen-Tag darstellen.</span><span class="sxs-lookup"><span data-stu-id="3b688-126">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b688-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3b688-127">-Confirm</span></span>
<span data-ttu-id="3b688-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b688-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b688-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b688-129">-WhatIf</span></span>
<span data-ttu-id="3b688-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b688-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b688-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b688-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b688-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b688-132">CommonParameters</span></span>
<span data-ttu-id="3b688-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b688-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b688-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b688-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b688-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3b688-135">INPUTS</span></span>

### <span data-ttu-id="3b688-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3b688-136">System.String</span></span>

### <span data-ttu-id="3b688-137">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="3b688-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="3b688-138">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3b688-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="3b688-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3b688-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3b688-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3b688-140">OUTPUTS</span></span>

### <span data-ttu-id="3b688-141">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="3b688-141">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="3b688-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="3b688-142">NOTES</span></span>

## <span data-ttu-id="3b688-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3b688-143">RELATED LINKS</span></span>
