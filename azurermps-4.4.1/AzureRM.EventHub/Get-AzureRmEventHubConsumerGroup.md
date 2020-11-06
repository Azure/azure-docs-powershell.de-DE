---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a2608ee3d3f874183a35fe6b81f7cd169123416
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505029"
---
# <span data-ttu-id="cc74a-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="cc74a-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="cc74a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc74a-102">SYNOPSIS</span></span>
<span data-ttu-id="cc74a-103">Ruft die Details einer angegebenen Event Hubs-Verbrauchergruppe ab oder ruft eine Liste von Verbrauchergruppen in einem Ereignis-Hub ab.</span><span class="sxs-lookup"><span data-stu-id="cc74a-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc74a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc74a-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 [-Name <String>]
```

## <span data-ttu-id="cc74a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc74a-105">DESCRIPTION</span></span>
<span data-ttu-id="cc74a-106">Das Get-AzureRmEventHubConsumerGroup-Cmdlet ruft entweder die Details einer angegebenen Event Hubs-Verbrauchergruppe oder eine Liste von Verbrauchergruppen in einem bestimmten Ereignis-Hub ab.</span><span class="sxs-lookup"><span data-stu-id="cc74a-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="cc74a-107">Wenn der Name einer Consumer-Gruppe bereitgestellt wird, werden die Details einer einzelnen Consumer-Gruppe zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cc74a-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="cc74a-108">Wenn der Name einer Consumer-Gruppe nicht angegeben wird, wird eine Liste der Verbrauchergruppen im angegebenen Ereignis-Hub zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cc74a-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="cc74a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc74a-109">EXAMPLES</span></span>

### <span data-ttu-id="cc74a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cc74a-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="cc74a-111">Ruft die Gruppe der \` Consumer \` -MyConsumerGroupName im MyEventHubName des Ereignis Hubs ab \` \` , die im Namespace \` mynamespacename \` mit Ressourcengruppe MyResourceGroupName vorhanden ist \` \` .</span><span class="sxs-lookup"><span data-stu-id="cc74a-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="cc74a-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cc74a-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="cc74a-113">Ruft eine Liste der Verbrauchergruppen im MyEventHubName des Ereignis Hubs ab \` \` , die im Namespace \` mynamespacename \` mit Ressourcengruppe MyResourceGroupName vorhanden ist \` \` .</span><span class="sxs-lookup"><span data-stu-id="cc74a-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="cc74a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc74a-114">PARAMETERS</span></span>

### <span data-ttu-id="cc74a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc74a-115">-ResourceGroupName</span></span>
<span data-ttu-id="cc74a-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cc74a-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc74a-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="cc74a-117">-EventHub</span></span>
<span data-ttu-id="cc74a-118">EventHub-Name.</span><span class="sxs-lookup"><span data-stu-id="cc74a-118">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc74a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cc74a-119">-Name</span></span>
<span data-ttu-id="cc74a-120">Consumergroup-Name.</span><span class="sxs-lookup"><span data-stu-id="cc74a-120">ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc74a-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cc74a-121">-Namespace</span></span>
<span data-ttu-id="cc74a-122">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="cc74a-122">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="cc74a-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc74a-123">INPUTS</span></span>

### <span data-ttu-id="cc74a-124">System. String</span><span class="sxs-lookup"><span data-stu-id="cc74a-124">System.String</span></span>

## <span data-ttu-id="cc74a-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc74a-125">OUTPUTS</span></span>

### <span data-ttu-id="cc74a-126">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventHub. Models. ConsumerGroupAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="cc74a-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="cc74a-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc74a-127">NOTES</span></span>

## <span data-ttu-id="cc74a-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc74a-128">RELATED LINKS</span></span>

