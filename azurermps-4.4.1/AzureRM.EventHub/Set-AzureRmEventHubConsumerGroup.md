---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: c871036c6f3113bd40e17fb5bbc201fa6297573c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501865"
---
# <span data-ttu-id="e2bee-101">Set-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="e2bee-101">Set-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="e2bee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e2bee-102">SYNOPSIS</span></span>
<span data-ttu-id="e2bee-103">Aktualisiert die angegebene Event Hubs-Verbrauchergruppe.</span><span class="sxs-lookup"><span data-stu-id="e2bee-103">Updates the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2bee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2bee-104">SYNTAX</span></span>

```
Set-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [[-UserMetadata] <String>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e2bee-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2bee-105">DESCRIPTION</span></span>
<span data-ttu-id="e2bee-106">Das Set-AzureRmEventHubConsumerGroup-Cmdlet aktualisiert die angegebene Event Hubs-Verbrauchergruppe.</span><span class="sxs-lookup"><span data-stu-id="e2bee-106">The Set-AzureRmEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="e2bee-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e2bee-107">EXAMPLES</span></span>

### <span data-ttu-id="e2bee-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e2bee-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="e2bee-109">Legt die Benutzer Metadaten der Verbrauchergruppe \` MyConsumerGroupName \` auf "testen" fest.</span><span class="sxs-lookup"><span data-stu-id="e2bee-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="e2bee-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2bee-110">PARAMETERS</span></span>

### <span data-ttu-id="e2bee-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2bee-111">-ResourceGroupName</span></span>
<span data-ttu-id="e2bee-112">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e2bee-112">Resource group name.</span></span>

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

### <span data-ttu-id="e2bee-113">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="e2bee-113">-UserMetadata</span></span>
<span data-ttu-id="e2bee-114">Benutzer Metadaten für die Consumer-Gruppe (optional).</span><span class="sxs-lookup"><span data-stu-id="e2bee-114">User metadata for the consumer group (optional).</span></span>

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

### <span data-ttu-id="e2bee-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e2bee-115">-Confirm</span></span>
<span data-ttu-id="e2bee-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e2bee-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2bee-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2bee-117">-WhatIf</span></span>
<span data-ttu-id="e2bee-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e2bee-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2bee-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e2bee-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2bee-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="e2bee-120">-EventHub</span></span>
<span data-ttu-id="e2bee-121">EventHub-Name.</span><span class="sxs-lookup"><span data-stu-id="e2bee-121">EventHub Name.</span></span>

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

### <span data-ttu-id="e2bee-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e2bee-122">-Name</span></span>
<span data-ttu-id="e2bee-123">Consumergroup-Name.</span><span class="sxs-lookup"><span data-stu-id="e2bee-123">ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="e2bee-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e2bee-124">-Namespace</span></span>
<span data-ttu-id="e2bee-125">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="e2bee-125">Namespace Name.</span></span>

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

## <span data-ttu-id="e2bee-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e2bee-126">INPUTS</span></span>

### <span data-ttu-id="e2bee-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e2bee-127">System.String</span></span>

## <span data-ttu-id="e2bee-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e2bee-128">OUTPUTS</span></span>

### <span data-ttu-id="e2bee-129">Microsoft. Azure. Commands. EventHub. Models. ConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="e2bee-129">Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes</span></span>

## <span data-ttu-id="e2bee-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="e2bee-130">NOTES</span></span>

## <span data-ttu-id="e2bee-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e2bee-131">RELATED LINKS</span></span>

