---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: edccb9bf46a75c8a9f6fe0c577a87e13d11a2ba9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995635"
---
# <span data-ttu-id="45229-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="45229-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="45229-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="45229-102">SYNOPSIS</span></span>
<span data-ttu-id="45229-103">Legt die Eigenschaften eines Ereignis Raster Themas fest.</span><span class="sxs-lookup"><span data-stu-id="45229-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="45229-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="45229-104">SYNTAX</span></span>

### <span data-ttu-id="45229-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="45229-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45229-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="45229-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45229-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="45229-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45229-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45229-108">DESCRIPTION</span></span>
<span data-ttu-id="45229-109">Legt die Eigenschaften eines Ereignis Raster Themas fest.</span><span class="sxs-lookup"><span data-stu-id="45229-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="45229-110">Dies kann verwendet werden, um die Tags eines Ereignis Raster Themas zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="45229-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="45229-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45229-111">EXAMPLES</span></span>

### <span data-ttu-id="45229-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="45229-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="45229-113">Legt die Eigenschaften des Ereignis Rasters Topic \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName fest \` , um die Tags durch die angegebenen Tags "Department" und "Environment" zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="45229-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="45229-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="45229-114">PARAMETERS</span></span>

### <span data-ttu-id="45229-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45229-115">-DefaultProfile</span></span>
<span data-ttu-id="45229-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="45229-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45229-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="45229-117">-InputObject</span></span>
<span data-ttu-id="45229-118">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="45229-118">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="45229-119">-Name</span><span class="sxs-lookup"><span data-stu-id="45229-119">-Name</span></span>
<span data-ttu-id="45229-120">EventGrid-Themen Name</span><span class="sxs-lookup"><span data-stu-id="45229-120">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="45229-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45229-121">-ResourceGroupName</span></span>
<span data-ttu-id="45229-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="45229-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="45229-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="45229-123">-ResourceId</span></span>
<span data-ttu-id="45229-124">EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="45229-124">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="45229-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="45229-125">-Tag</span></span>
<span data-ttu-id="45229-126">Hashtables, die das Ressourcen-Tag darstellen.</span><span class="sxs-lookup"><span data-stu-id="45229-126">Hashtables which represents resource Tag.</span></span>

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

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45229-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="45229-127">-Confirm</span></span>
<span data-ttu-id="45229-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="45229-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45229-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45229-129">-WhatIf</span></span>
<span data-ttu-id="45229-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="45229-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45229-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="45229-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45229-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45229-132">CommonParameters</span></span>
<span data-ttu-id="45229-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45229-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45229-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45229-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45229-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="45229-135">INPUTS</span></span>

### <span data-ttu-id="45229-136">System. String</span><span class="sxs-lookup"><span data-stu-id="45229-136">System.String</span></span>

### <span data-ttu-id="45229-137">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="45229-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="45229-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="45229-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="45229-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="45229-139">OUTPUTS</span></span>

### <span data-ttu-id="45229-140">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="45229-140">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="45229-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="45229-141">NOTES</span></span>

## <span data-ttu-id="45229-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="45229-142">RELATED LINKS</span></span>
