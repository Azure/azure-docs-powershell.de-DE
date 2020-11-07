---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: 23004583a08dbcf5ef8785b62d0457b6b6ee0897
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661084"
---
# <span data-ttu-id="027b5-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="027b5-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="027b5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="027b5-102">SYNOPSIS</span></span>
<span data-ttu-id="027b5-103">Ruft die Details eines Ereignis Raster Themas ab oder ruft eine Liste aller Themen des Ereignis Rasters im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="027b5-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="027b5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="027b5-104">SYNTAX</span></span>

### <span data-ttu-id="027b5-105">ResourceGroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="027b5-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="027b5-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="027b5-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="027b5-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="027b5-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="027b5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="027b5-108">DESCRIPTION</span></span>
<span data-ttu-id="027b5-109">Das Get-AzEventGridTopic-Cmdlet ruft entweder die Details eines angegebenen Ereignis Raster Themas oder eine Liste aller Themen des Ereignis Rasters im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="027b5-109">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="027b5-110">Wenn der Name des Themas angegeben ist, werden die Details für ein einzelnes Ereignis Raster Thema zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="027b5-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="027b5-111">Wenn der Name des Themas nicht angegeben wird, wird eine Liste der Themen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="027b5-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="027b5-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="027b5-112">EXAMPLES</span></span>

### <span data-ttu-id="027b5-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="027b5-113">Example 1</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="027b5-114">Ruft die Details des Ereignis Rasters Topic \` THEMA1 hat \` in Resource Group \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="027b5-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="027b5-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="027b5-115">Example 2</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="027b5-116">Ruft die Details des Ereignis Rasters Topic \` THEMA1 hat \` in Resource Group \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="027b5-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="027b5-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="027b5-117">Example 3</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="027b5-118">Listen Sie alle Themen des Ereignis Rasters in der Ressourcengruppe \` MyResourceGroupName auf \` .</span><span class="sxs-lookup"><span data-stu-id="027b5-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="027b5-119">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="027b5-119">Example 4</span></span>
```
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="027b5-120">Listen Sie alle Themen des Ereignis Rasters im Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="027b5-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="027b5-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="027b5-121">PARAMETERS</span></span>

### <span data-ttu-id="027b5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="027b5-122">-DefaultProfile</span></span>
<span data-ttu-id="027b5-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="027b5-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="027b5-124">-Name</span><span class="sxs-lookup"><span data-stu-id="027b5-124">-Name</span></span>
<span data-ttu-id="027b5-125">EventGrid-Themen Name</span><span class="sxs-lookup"><span data-stu-id="027b5-125">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="027b5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="027b5-126">-ResourceGroupName</span></span>
<span data-ttu-id="027b5-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="027b5-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="027b5-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="027b5-128">-ResourceId</span></span>
<span data-ttu-id="027b5-129">Ressourcenbezeichner, der das Thema des Ereignis Rasters darstellt.</span><span class="sxs-lookup"><span data-stu-id="027b5-129">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="027b5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="027b5-130">CommonParameters</span></span>
<span data-ttu-id="027b5-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="027b5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="027b5-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="027b5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="027b5-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="027b5-133">INPUTS</span></span>

### <span data-ttu-id="027b5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="027b5-134">System.String</span></span>

## <span data-ttu-id="027b5-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="027b5-135">OUTPUTS</span></span>

### <span data-ttu-id="027b5-136">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="027b5-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="027b5-137">Microsoft. Azure. Commands. EventGrid. Models. PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="027b5-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="027b5-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="027b5-138">NOTES</span></span>

## <span data-ttu-id="027b5-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="027b5-139">RELATED LINKS</span></span>
