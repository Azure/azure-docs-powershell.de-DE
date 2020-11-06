---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: c8684e9af0bca55dca52f336a458f4c428ca67a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500049"
---
# <span data-ttu-id="4213b-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="4213b-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="4213b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4213b-102">SYNOPSIS</span></span>
<span data-ttu-id="4213b-103">Löscht die angegebene Event Hubs-Verbrauchergruppe.</span><span class="sxs-lookup"><span data-stu-id="4213b-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4213b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4213b-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="4213b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4213b-105">DESCRIPTION</span></span>
<span data-ttu-id="4213b-106">Das Remove-AzureRmEventHubConsumerGroup-Cmdlet entfernt die angegebene Consumer-Gruppe aus dem angegebenen Ereignis-Hub und löscht sie.</span><span class="sxs-lookup"><span data-stu-id="4213b-106">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="4213b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4213b-107">EXAMPLES</span></span>

### <span data-ttu-id="4213b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4213b-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="4213b-109">Löscht die Consumer \` -Gruppen \` -MyConsumerGroupName aus dem \` Event \` -Hub-MyEventHubName, der auf den \` mynamespacename-Namespace beschränkt ist \` .</span><span class="sxs-lookup"><span data-stu-id="4213b-109">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

## <span data-ttu-id="4213b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4213b-110">PARAMETERS</span></span>

### <span data-ttu-id="4213b-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4213b-111">-ResourceGroupName</span></span>
<span data-ttu-id="4213b-112">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4213b-112">Resource group name.</span></span>

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

### <span data-ttu-id="4213b-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4213b-113">-Confirm</span></span>
<span data-ttu-id="4213b-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4213b-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4213b-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4213b-115">-WhatIf</span></span>
<span data-ttu-id="4213b-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4213b-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4213b-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4213b-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4213b-118">-EventHub</span><span class="sxs-lookup"><span data-stu-id="4213b-118">-EventHub</span></span>
<span data-ttu-id="4213b-119">EventHub-Name.</span><span class="sxs-lookup"><span data-stu-id="4213b-119">EventHub Name.</span></span>

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

### <span data-ttu-id="4213b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4213b-120">-Name</span></span>
<span data-ttu-id="4213b-121">Consumergroup-Name.</span><span class="sxs-lookup"><span data-stu-id="4213b-121">ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4213b-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4213b-122">-Namespace</span></span>
<span data-ttu-id="4213b-123">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="4213b-123">Namespace Name.</span></span>

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

## <span data-ttu-id="4213b-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4213b-124">INPUTS</span></span>

### <span data-ttu-id="4213b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4213b-125">System.String</span></span>

## <span data-ttu-id="4213b-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4213b-126">OUTPUTS</span></span>

### <span data-ttu-id="4213b-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="4213b-127">System.Object</span></span>

## <span data-ttu-id="4213b-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="4213b-128">NOTES</span></span>

## <span data-ttu-id="4213b-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4213b-129">RELATED LINKS</span></span>

