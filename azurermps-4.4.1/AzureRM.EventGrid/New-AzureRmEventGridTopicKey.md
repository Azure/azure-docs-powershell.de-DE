---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
ms.openlocfilehash: bb9cd92ff614a944c144f056d8d59aa1d4239b25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505050"
---
# <span data-ttu-id="6cd75-101">New-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="6cd75-101">New-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="6cd75-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6cd75-102">SYNOPSIS</span></span>
<span data-ttu-id="6cd75-103">Generiert die freigegebene Zugriffstaste für ein Azure-Ereignis Raster Thema neu.</span><span class="sxs-lookup"><span data-stu-id="6cd75-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cd75-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cd75-104">SYNTAX</span></span>

### <span data-ttu-id="6cd75-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6cd75-105">TopicNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cd75-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cd75-106">TopicInputObjectParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cd75-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cd75-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cd75-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6cd75-108">DESCRIPTION</span></span>
<span data-ttu-id="6cd75-109">Generiert die freigegebene Zugriffstaste für ein Azure-Ereignis Raster Thema neu.</span><span class="sxs-lookup"><span data-stu-id="6cd75-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="6cd75-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6cd75-110">EXAMPLES</span></span>

### <span data-ttu-id="6cd75-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6cd75-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="6cd75-112">Generieren Sie den Schlüssel entsprechend dem Schlüssel \' key1 ' \ des Ereignis Rasters Topic \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="6cd75-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="6cd75-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6cd75-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzureRmEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="6cd75-114">Generieren Sie den Schlüssel entsprechend dem Schlüssel \' key1 ' \ des Ereignis Rasters Topic \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="6cd75-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="6cd75-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cd75-115">PARAMETERS</span></span>

### <span data-ttu-id="6cd75-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6cd75-116">-InputObject</span></span>
<span data-ttu-id="6cd75-117">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6cd75-117">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="6cd75-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="6cd75-118">-KeyName</span></span>
<span data-ttu-id="6cd75-119">Der Name des Schlüssels, der neu generiert werden muss</span><span class="sxs-lookup"><span data-stu-id="6cd75-119">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cd75-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cd75-120">-ResourceGroupName</span></span>
<span data-ttu-id="6cd75-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6cd75-121">Resource group name.</span></span>

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

### <span data-ttu-id="6cd75-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6cd75-122">-ResourceId</span></span>
<span data-ttu-id="6cd75-123">Ressourcenbezeichner, der das Thema des Ereignis Rasters darstellt.</span><span class="sxs-lookup"><span data-stu-id="6cd75-123">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="6cd75-124">-Topicname</span><span class="sxs-lookup"><span data-stu-id="6cd75-124">-TopicName</span></span>
<span data-ttu-id="6cd75-125">Der Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="6cd75-125">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cd75-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6cd75-126">-Confirm</span></span>
<span data-ttu-id="6cd75-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6cd75-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cd75-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cd75-128">-WhatIf</span></span>
<span data-ttu-id="6cd75-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6cd75-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cd75-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6cd75-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cd75-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cd75-131">-DefaultProfile</span></span>
<span data-ttu-id="6cd75-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6cd75-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cd75-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cd75-133">CommonParameters</span></span>
<span data-ttu-id="6cd75-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cd75-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cd75-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cd75-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cd75-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6cd75-136">INPUTS</span></span>

### <span data-ttu-id="6cd75-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6cd75-137">System.String</span></span>

## <span data-ttu-id="6cd75-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6cd75-138">OUTPUTS</span></span>

### <span data-ttu-id="6cd75-139">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="6cd75-139">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="6cd75-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="6cd75-140">NOTES</span></span>

## <span data-ttu-id="6cd75-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6cd75-141">RELATED LINKS</span></span>

