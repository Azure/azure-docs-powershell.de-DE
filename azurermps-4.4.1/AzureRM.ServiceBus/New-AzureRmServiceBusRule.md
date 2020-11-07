---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
ms.openlocfilehash: 39cd0759f18c84f78a2e6a75f8e1c9b257fb9da9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664977"
---
# <span data-ttu-id="078a5-101">New-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="078a5-101">New-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="078a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="078a5-102">SYNOPSIS</span></span>
<span data-ttu-id="078a5-103">Erstellt eine neue Regel für ein bestimmtes Abonnement des Themas.</span><span class="sxs-lookup"><span data-stu-id="078a5-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="078a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="078a5-104">SYNTAX</span></span>

```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="078a5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="078a5-105">DESCRIPTION</span></span>
<span data-ttu-id="078a5-106">Das Cmdlet **New-AzureRmServiceBusRule** erstellt eine neue Regel für ein bestimmtes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="078a5-106">The **New-AzureRmServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="078a5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="078a5-107">EXAMPLES</span></span>

### <span data-ttu-id="078a5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="078a5-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="078a5-109">Das Cmdlet **New-AzureRmServiceBusRule** erstellt eine neue Regel für das angegebene Abonnement.</span><span class="sxs-lookup"><span data-stu-id="078a5-109">The **New-AzureRmServiceBusRule** cmdlet creates a new rule for the specified Subscription.</span></span>

## <span data-ttu-id="078a5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="078a5-110">PARAMETERS</span></span>

### <span data-ttu-id="078a5-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="078a5-111">-Confirm</span></span>
<span data-ttu-id="078a5-112">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="078a5-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="078a5-113">-Name</span><span class="sxs-lookup"><span data-stu-id="078a5-113">-Name</span></span>
<span data-ttu-id="078a5-114">Regelname</span><span class="sxs-lookup"><span data-stu-id="078a5-114">Rule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="078a5-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="078a5-115">-Namespace</span></span>
<span data-ttu-id="078a5-116">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="078a5-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="078a5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="078a5-117">-ResourceGroupName</span></span>
<span data-ttu-id="078a5-118">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="078a5-118">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="078a5-119">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="078a5-119">-SqlExpression</span></span>
<span data-ttu-id="078a5-120">SQL Fillter-Ausdruck</span><span class="sxs-lookup"><span data-stu-id="078a5-120">Sql Fillter Expression</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="078a5-121">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="078a5-121">-Subscription</span></span>
<span data-ttu-id="078a5-122">Name des Abonnements</span><span class="sxs-lookup"><span data-stu-id="078a5-122">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="078a5-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="078a5-123">-Topic</span></span>
<span data-ttu-id="078a5-124">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="078a5-124">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="078a5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="078a5-125">-WhatIf</span></span>
<span data-ttu-id="078a5-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="078a5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="078a5-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="078a5-127">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="078a5-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="078a5-128">INPUTS</span></span>

### <span data-ttu-id="078a5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="078a5-129">System.String</span></span>


## <span data-ttu-id="078a5-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="078a5-130">OUTPUTS</span></span>

### <span data-ttu-id="078a5-131">Microsoft. Azure. Commands. ServiceBus. Models. RulesAttributes</span><span class="sxs-lookup"><span data-stu-id="078a5-131">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>


## <span data-ttu-id="078a5-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="078a5-132">NOTES</span></span>

## <span data-ttu-id="078a5-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="078a5-133">RELATED LINKS</span></span>

