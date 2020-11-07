---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bcd20fc9c6f0c08af2ae735558a6fccc6c9814d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665061"
---
# <span data-ttu-id="d7b54-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="d7b54-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="d7b54-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7b54-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b54-103">Erstellt eine neue Consumer-Gruppe für den angegebenen Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="d7b54-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7b54-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7b54-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [[-UserMetadata] <String>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="d7b54-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7b54-105">DESCRIPTION</span></span>
<span data-ttu-id="d7b54-106">Das New-AzureRmEventHubConsumerGroup-Cmdlet erstellt eine neue Consumer-Gruppe für den angegebenen Ereignis-Hub.</span><span class="sxs-lookup"><span data-stu-id="d7b54-106">The New-AzureRmEventHubConsumerGroup cmdlet creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="d7b54-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7b54-107">EXAMPLES</span></span>

### <span data-ttu-id="d7b54-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d7b54-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="d7b54-109">Erstellt die Consumer-Gruppe \` MyConsumerGroupName \` im Ereignis \` -Hub \` -MyEventHubName mit dem Namespace \` mynamespacename \` mit der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="d7b54-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d7b54-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7b54-110">PARAMETERS</span></span>

### <span data-ttu-id="d7b54-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7b54-111">-ResourceGroupName</span></span>
<span data-ttu-id="d7b54-112">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d7b54-112">Resource group name.</span></span>

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

### <span data-ttu-id="d7b54-113">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="d7b54-113">-UserMetadata</span></span>
<span data-ttu-id="d7b54-114">Benutzer Metadaten für die Consumer-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d7b54-114">User metadata for the consumer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7b54-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d7b54-115">-Confirm</span></span>
<span data-ttu-id="d7b54-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d7b54-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7b54-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7b54-117">-WhatIf</span></span>
<span data-ttu-id="d7b54-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d7b54-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7b54-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7b54-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7b54-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="d7b54-120">-EventHub</span></span>
<span data-ttu-id="d7b54-121">EventHub-Name.</span><span class="sxs-lookup"><span data-stu-id="d7b54-121">EventHub Name.</span></span>

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

### <span data-ttu-id="d7b54-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d7b54-122">-Name</span></span>
<span data-ttu-id="d7b54-123">Consumergroup-Name.</span><span class="sxs-lookup"><span data-stu-id="d7b54-123">ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="d7b54-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d7b54-124">-Namespace</span></span>
<span data-ttu-id="d7b54-125">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="d7b54-125">Namespace Name.</span></span>

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

## <span data-ttu-id="d7b54-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7b54-126">INPUTS</span></span>

### <span data-ttu-id="d7b54-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d7b54-127">System.String</span></span>

## <span data-ttu-id="d7b54-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7b54-128">OUTPUTS</span></span>

### <span data-ttu-id="d7b54-129">Microsoft. Azure. Commands. EventHub. Models. ConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="d7b54-129">Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes</span></span>

## <span data-ttu-id="d7b54-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7b54-130">NOTES</span></span>

## <span data-ttu-id="d7b54-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7b54-131">RELATED LINKS</span></span>

