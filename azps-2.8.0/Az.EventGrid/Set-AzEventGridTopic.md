---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: f27533a36314ae2b31cd0055e8cc17027c95016a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651209"
---
# <span data-ttu-id="a0b21-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="a0b21-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="a0b21-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a0b21-102">SYNOPSIS</span></span>
<span data-ttu-id="a0b21-103">Legt die Eigenschaften eines Ereignis Raster Themas fest.</span><span class="sxs-lookup"><span data-stu-id="a0b21-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="a0b21-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0b21-104">SYNTAX</span></span>

### <span data-ttu-id="a0b21-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0b21-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0b21-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0b21-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0b21-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0b21-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0b21-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0b21-108">DESCRIPTION</span></span>
<span data-ttu-id="a0b21-109">Legt die Eigenschaften eines Ereignis Raster Themas fest.</span><span class="sxs-lookup"><span data-stu-id="a0b21-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="a0b21-110">Dies kann verwendet werden, um die Tags eines Ereignis Raster Themas zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="a0b21-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="a0b21-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0b21-111">EXAMPLES</span></span>

### <span data-ttu-id="a0b21-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a0b21-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="a0b21-113">Legt die Eigenschaften des Ereignis Rasters Topic \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName fest \` , um die Tags durch die angegebenen Tags "Department" und "Environment" zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="a0b21-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="a0b21-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0b21-114">PARAMETERS</span></span>

### <span data-ttu-id="a0b21-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0b21-115">-DefaultProfile</span></span>
<span data-ttu-id="a0b21-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a0b21-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0b21-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a0b21-117">-InputObject</span></span>
<span data-ttu-id="a0b21-118">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a0b21-118">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="a0b21-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a0b21-119">-Name</span></span>
<span data-ttu-id="a0b21-120">EventGrid-Themen Name</span><span class="sxs-lookup"><span data-stu-id="a0b21-120">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="a0b21-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0b21-121">-ResourceGroupName</span></span>
<span data-ttu-id="a0b21-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a0b21-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="a0b21-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a0b21-123">-ResourceId</span></span>
<span data-ttu-id="a0b21-124">EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="a0b21-124">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="a0b21-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0b21-125">-Tag</span></span>
<span data-ttu-id="a0b21-126">Hashtables, die das Ressourcen-Tag darstellen.</span><span class="sxs-lookup"><span data-stu-id="a0b21-126">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="a0b21-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a0b21-127">-Confirm</span></span>
<span data-ttu-id="a0b21-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0b21-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0b21-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0b21-129">-WhatIf</span></span>
<span data-ttu-id="a0b21-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0b21-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0b21-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0b21-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0b21-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0b21-132">CommonParameters</span></span>
<span data-ttu-id="a0b21-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0b21-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0b21-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0b21-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0b21-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a0b21-135">INPUTS</span></span>

### <span data-ttu-id="a0b21-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a0b21-136">System.String</span></span>

### <span data-ttu-id="a0b21-137">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="a0b21-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="a0b21-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a0b21-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a0b21-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a0b21-139">OUTPUTS</span></span>

### <span data-ttu-id="a0b21-140">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="a0b21-140">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="a0b21-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="a0b21-141">NOTES</span></span>

## <span data-ttu-id="a0b21-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a0b21-142">RELATED LINKS</span></span>
