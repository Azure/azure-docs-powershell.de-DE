---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
ms.openlocfilehash: 509f10432139ca0f2d9aaca216f22d998b7963a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505038"
---
# <span data-ttu-id="2e2fe-101">Set-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="2e2fe-101">Set-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="2e2fe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2e2fe-102">SYNOPSIS</span></span>
<span data-ttu-id="2e2fe-103">Setzen Sie die Eigenschaften eines Ereignis Raster Themas.</span><span class="sxs-lookup"><span data-stu-id="2e2fe-103">Set the properties of an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e2fe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e2fe-104">SYNTAX</span></span>

### <span data-ttu-id="2e2fe-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2e2fe-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e2fe-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e2fe-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e2fe-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e2fe-107">TopicInputObjectParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e2fe-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e2fe-108">DESCRIPTION</span></span>
<span data-ttu-id="2e2fe-109">Setzen Sie die Eigenschaften eines Ereignis Raster Themas.</span><span class="sxs-lookup"><span data-stu-id="2e2fe-109">Set the properties of an Event Grid topic.</span></span> <span data-ttu-id="2e2fe-110">Dies kann verwendet werden, um die Tags eines Ereignis Raster Themas zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="2e2fe-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="2e2fe-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e2fe-111">EXAMPLES</span></span>

### <span data-ttu-id="2e2fe-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2e2fe-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="2e2fe-113">Legt die Eigenschaften des Ereignis Rasters Topic \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName fest \` , um die Tags durch die angegebenen Tags "Department" und "Environment" zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="2e2fe-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="2e2fe-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e2fe-114">PARAMETERS</span></span>

### <span data-ttu-id="2e2fe-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2e2fe-115">-InputObject</span></span>
<span data-ttu-id="2e2fe-116">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2e2fe-116">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="2e2fe-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2e2fe-117">-Name</span></span>
<span data-ttu-id="2e2fe-118">EventGrid-Themen Name</span><span class="sxs-lookup"><span data-stu-id="2e2fe-118">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="2e2fe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e2fe-119">-ResourceGroupName</span></span>
<span data-ttu-id="2e2fe-120">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2e2fe-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="2e2fe-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2e2fe-121">-ResourceId</span></span>
<span data-ttu-id="2e2fe-122">EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="2e2fe-122">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="2e2fe-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="2e2fe-123">-Tag</span></span>
<span data-ttu-id="2e2fe-124">Hashtables, die das Ressourcen-Tag darstellen.</span><span class="sxs-lookup"><span data-stu-id="2e2fe-124">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="2e2fe-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2e2fe-125">-Confirm</span></span>
<span data-ttu-id="2e2fe-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2e2fe-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e2fe-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e2fe-127">-WhatIf</span></span>
<span data-ttu-id="2e2fe-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2e2fe-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e2fe-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2e2fe-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e2fe-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e2fe-130">-DefaultProfile</span></span>
<span data-ttu-id="2e2fe-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2e2fe-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e2fe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e2fe-132">CommonParameters</span></span>
<span data-ttu-id="2e2fe-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e2fe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e2fe-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e2fe-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e2fe-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2e2fe-135">INPUTS</span></span>

### <span data-ttu-id="2e2fe-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2e2fe-136">System.String</span></span>
<span data-ttu-id="2e2fe-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2e2fe-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2e2fe-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2e2fe-138">OUTPUTS</span></span>

### <span data-ttu-id="2e2fe-139">Microsoft. Azure. Management. EventGrid. Models. Topic</span><span class="sxs-lookup"><span data-stu-id="2e2fe-139">Microsoft.Azure.Management.EventGrid.Models.Topic</span></span>

## <span data-ttu-id="2e2fe-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="2e2fe-140">NOTES</span></span>

## <span data-ttu-id="2e2fe-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2e2fe-141">RELATED LINKS</span></span>

