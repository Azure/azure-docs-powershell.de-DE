---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/set-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
ms.openlocfilehash: c6a975ee5071ff3f31ae3daa0e6e9bf6ed9a42ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482969"
---
# <span data-ttu-id="7eb4a-101">Set-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="7eb4a-101">Set-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="7eb4a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7eb4a-102">SYNOPSIS</span></span>
<span data-ttu-id="7eb4a-103">Legt die Eigenschaften eines Ereignis Raster Themas fest.</span><span class="sxs-lookup"><span data-stu-id="7eb4a-103">Sets the properties of an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eb4a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7eb4a-104">SYNTAX</span></span>

### <span data-ttu-id="7eb4a-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7eb4a-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7eb4a-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7eb4a-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7eb4a-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7eb4a-107">TopicInputObjectParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7eb4a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7eb4a-108">DESCRIPTION</span></span>
<span data-ttu-id="7eb4a-109">Legt die Eigenschaften eines Ereignis Raster Themas fest.</span><span class="sxs-lookup"><span data-stu-id="7eb4a-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="7eb4a-110">Dies kann verwendet werden, um die Tags eines Ereignis Raster Themas zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="7eb4a-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="7eb4a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7eb4a-111">EXAMPLES</span></span>

### <span data-ttu-id="7eb4a-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7eb4a-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="7eb4a-113">Legt die Eigenschaften des Ereignis Rasters Topic \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName fest \` , um die Tags durch die angegebenen Tags "Department" und "Environment" zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="7eb4a-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="7eb4a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7eb4a-114">PARAMETERS</span></span>

### <span data-ttu-id="7eb4a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eb4a-115">-DefaultProfile</span></span>
<span data-ttu-id="7eb4a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7eb4a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eb4a-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7eb4a-117">-InputObject</span></span>
<span data-ttu-id="7eb4a-118">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7eb4a-118">EventGrid Topic object.</span></span>

```yaml
Type: PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7eb4a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7eb4a-119">-Name</span></span>
<span data-ttu-id="7eb4a-120">EventGrid-Themen Name</span><span class="sxs-lookup"><span data-stu-id="7eb4a-120">EventGrid Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eb4a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eb4a-121">-ResourceGroupName</span></span>
<span data-ttu-id="7eb4a-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7eb4a-122">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eb4a-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7eb4a-123">-ResourceId</span></span>
<span data-ttu-id="7eb4a-124">EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="7eb4a-124">EventGrid Topic ResourceID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eb4a-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="7eb4a-125">-Tag</span></span>
<span data-ttu-id="7eb4a-126">Hashtables, die das Ressourcen-Tag darstellen.</span><span class="sxs-lookup"><span data-stu-id="7eb4a-126">Hashtables which represents resource Tag.</span></span>

```yaml
Type: Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eb4a-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7eb4a-127">-Confirm</span></span>
<span data-ttu-id="7eb4a-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7eb4a-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eb4a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eb4a-129">-WhatIf</span></span>
<span data-ttu-id="7eb4a-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7eb4a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eb4a-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7eb4a-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eb4a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb4a-132">CommonParameters</span></span>
<span data-ttu-id="7eb4a-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eb4a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb4a-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eb4a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb4a-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7eb4a-135">INPUTS</span></span>

### <span data-ttu-id="7eb4a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7eb4a-136">System.String</span></span>
<span data-ttu-id="7eb4a-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7eb4a-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7eb4a-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7eb4a-138">OUTPUTS</span></span>

### <span data-ttu-id="7eb4a-139">Microsoft. Azure. Management. EventGrid. Models. Topic</span><span class="sxs-lookup"><span data-stu-id="7eb4a-139">Microsoft.Azure.Management.EventGrid.Models.Topic</span></span>

## <span data-ttu-id="7eb4a-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="7eb4a-140">NOTES</span></span>

## <span data-ttu-id="7eb4a-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7eb4a-141">RELATED LINKS</span></span>

