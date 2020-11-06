---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/new-azurermeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 3600d7523e95b937f20d9d0b97d677c5cf02ca0f
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "93506018"
---
# <span data-ttu-id="d3e84-101">New-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="d3e84-101">New-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="d3e84-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d3e84-102">SYNOPSIS</span></span>
<span data-ttu-id="d3e84-103">Generiert die freigegebene Zugriffstaste für ein Azure-Ereignis Raster Thema neu.</span><span class="sxs-lookup"><span data-stu-id="d3e84-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3e84-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3e84-104">SYNTAX</span></span>

### <span data-ttu-id="d3e84-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d3e84-105">TopicNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e84-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3e84-106">TopicInputObjectParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e84-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3e84-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3e84-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3e84-108">DESCRIPTION</span></span>
<span data-ttu-id="d3e84-109">Generiert die freigegebene Zugriffstaste für ein Azure-Ereignis Raster Thema neu.</span><span class="sxs-lookup"><span data-stu-id="d3e84-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="d3e84-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d3e84-110">EXAMPLES</span></span>

### <span data-ttu-id="d3e84-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d3e84-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="d3e84-112">Generieren Sie den Schlüssel entsprechend dem Schlüssel \' key1 ' \ des Ereignis Rasters Topic \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="d3e84-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d3e84-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d3e84-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzureRmEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="d3e84-114">Generieren Sie den Schlüssel entsprechend dem Schlüssel \' key1 ' \ des Ereignis Rasters Topic \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="d3e84-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d3e84-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3e84-115">PARAMETERS</span></span>

### <span data-ttu-id="d3e84-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3e84-116">-DefaultProfile</span></span>
<span data-ttu-id="d3e84-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d3e84-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3e84-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d3e84-118">-InputObject</span></span>
<span data-ttu-id="d3e84-119">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d3e84-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="d3e84-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d3e84-120">-KeyName</span></span>
<span data-ttu-id="d3e84-121">Der Name des Schlüssels, der neu generiert werden muss</span><span class="sxs-lookup"><span data-stu-id="d3e84-121">The name of the key that needs to be regenerated</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e84-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3e84-122">-ResourceGroupName</span></span>
<span data-ttu-id="d3e84-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d3e84-123">Resource group name.</span></span>

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

### <span data-ttu-id="d3e84-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d3e84-124">-ResourceId</span></span>
<span data-ttu-id="d3e84-125">Ressourcenbezeichner, der das Thema des Ereignis Rasters darstellt.</span><span class="sxs-lookup"><span data-stu-id="d3e84-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="d3e84-126">-Topicname</span><span class="sxs-lookup"><span data-stu-id="d3e84-126">-TopicName</span></span>
<span data-ttu-id="d3e84-127">Der Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="d3e84-127">The name of the topic.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e84-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d3e84-128">-Confirm</span></span>
<span data-ttu-id="d3e84-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d3e84-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3e84-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3e84-130">-WhatIf</span></span>
<span data-ttu-id="d3e84-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3e84-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3e84-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3e84-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3e84-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3e84-133">CommonParameters</span></span>
<span data-ttu-id="d3e84-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3e84-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3e84-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3e84-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3e84-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d3e84-136">INPUTS</span></span>

### <span data-ttu-id="d3e84-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d3e84-137">System.String</span></span>

## <span data-ttu-id="d3e84-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d3e84-138">OUTPUTS</span></span>

### <span data-ttu-id="d3e84-139">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="d3e84-139">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="d3e84-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="d3e84-140">NOTES</span></span>

## <span data-ttu-id="d3e84-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d3e84-141">RELATED LINKS</span></span>

