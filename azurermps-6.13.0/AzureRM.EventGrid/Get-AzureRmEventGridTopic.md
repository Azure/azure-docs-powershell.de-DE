---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
ms.openlocfilehash: 2d18e923e14caf4c0048575465e9f52fb14596f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477845"
---
# <span data-ttu-id="4f886-101">Get-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="4f886-101">Get-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="4f886-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4f886-102">SYNOPSIS</span></span>
<span data-ttu-id="4f886-103">Ruft die Details eines Ereignis Raster Themas ab oder ruft eine Liste aller Themen des Ereignis Rasters im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="4f886-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f886-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f886-104">SYNTAX</span></span>

### <span data-ttu-id="4f886-105">ResourceGroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4f886-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f886-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f886-106">TopicNameParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f886-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f886-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f886-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f886-108">DESCRIPTION</span></span>
<span data-ttu-id="4f886-109">Das Get-AzureRmEventGridTopic-Cmdlet ruft entweder die Details eines angegebenen Ereignis Raster Themas oder eine Liste aller Themen des Ereignis Rasters im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="4f886-109">The Get-AzureRmEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="4f886-110">Wenn der Name des Themas angegeben ist, werden die Details für ein einzelnes Ereignis Raster Thema zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4f886-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="4f886-111">Wenn der Name des Themas nicht angegeben wird, wird eine Liste der Themen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4f886-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="4f886-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f886-112">EXAMPLES</span></span>

### <span data-ttu-id="4f886-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4f886-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="4f886-114">Ruft die Details des Ereignis Rasters Topic \` THEMA1 hat \` in Resource Group \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="4f886-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="4f886-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4f886-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="4f886-116">Ruft die Details des Ereignis Rasters Topic \` THEMA1 hat \` in Resource Group \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="4f886-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="4f886-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4f886-117">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="4f886-118">Listen Sie alle Themen des Ereignis Rasters in der Ressourcengruppe \` MyResourceGroupName auf \` .</span><span class="sxs-lookup"><span data-stu-id="4f886-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="4f886-119">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="4f886-119">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridTopic
```

<span data-ttu-id="4f886-120">Listen Sie alle Themen des Ereignis Rasters im Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="4f886-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="4f886-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f886-121">PARAMETERS</span></span>

### <span data-ttu-id="4f886-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f886-122">-DefaultProfile</span></span>
<span data-ttu-id="4f886-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4f886-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f886-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4f886-124">-Name</span></span>
<span data-ttu-id="4f886-125">EventGrid-Themen Name</span><span class="sxs-lookup"><span data-stu-id="4f886-125">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="4f886-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f886-126">-ResourceGroupName</span></span>
<span data-ttu-id="4f886-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4f886-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="4f886-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4f886-128">-ResourceId</span></span>
<span data-ttu-id="4f886-129">Ressourcenbezeichner, der das Thema des Ereignis Rasters darstellt.</span><span class="sxs-lookup"><span data-stu-id="4f886-129">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="4f886-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f886-130">CommonParameters</span></span>
<span data-ttu-id="4f886-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f886-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f886-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f886-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f886-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4f886-133">INPUTS</span></span>

### <span data-ttu-id="4f886-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4f886-134">System.String</span></span>

## <span data-ttu-id="4f886-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4f886-135">OUTPUTS</span></span>

### <span data-ttu-id="4f886-136">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="4f886-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="4f886-137">Microsoft. Azure. Commands. EventGrid. Models. PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="4f886-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="4f886-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="4f886-138">NOTES</span></span>

## <span data-ttu-id="4f886-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4f886-139">RELATED LINKS</span></span>
