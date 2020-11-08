---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: d667049fb512545aebfd9681b3ad3d9f44651951
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166092"
---
# <span data-ttu-id="151e4-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="151e4-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="151e4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="151e4-102">SYNOPSIS</span></span>
<span data-ttu-id="151e4-103">Erstellt eine neue Regel für ein bestimmtes Abonnement des Themas.</span><span class="sxs-lookup"><span data-stu-id="151e4-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="151e4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="151e4-104">SYNTAX</span></span>

### <span data-ttu-id="151e4-105">RulePropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="151e4-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="151e4-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="151e4-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="151e4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="151e4-107">DESCRIPTION</span></span>
<span data-ttu-id="151e4-108">Das Cmdlet **New-AzServiceBusRule** erstellt eine neue Regel für ein bestimmtes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="151e4-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="151e4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="151e4-109">EXAMPLES</span></span>

### <span data-ttu-id="151e4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="151e4-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="151e4-111">Das New-AzServiceBusRule-Cmdlet erstellt eine neue Regel für das angegebene Abonnement.</span><span class="sxs-lookup"><span data-stu-id="151e4-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="151e4-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="151e4-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="151e4-113">Das New-AzServiceBusRule-Cmdlet erstellt eine neue Regel für das angegebene Abonnement mit Action Filter.</span><span class="sxs-lookup"><span data-stu-id="151e4-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="151e4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="151e4-114">PARAMETERS</span></span>

### <span data-ttu-id="151e4-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="151e4-115">-ActionSqlExpression</span></span>
<span data-ttu-id="151e4-116">Aktion-sqlfilter-Ausdruck</span><span class="sxs-lookup"><span data-stu-id="151e4-116">Action SqlFilter Expression</span></span>

```yaml
Type: System.String
Parameter Sets: RuleActionPropertiesSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="151e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="151e4-117">-DefaultProfile</span></span>
<span data-ttu-id="151e4-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="151e4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="151e4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="151e4-119">-Name</span></span>
<span data-ttu-id="151e4-120">Regelname</span><span class="sxs-lookup"><span data-stu-id="151e4-120">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="151e4-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="151e4-121">-Namespace</span></span>
<span data-ttu-id="151e4-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="151e4-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="151e4-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="151e4-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="151e4-124">Aktion erfordert Vorverarbeitung</span><span class="sxs-lookup"><span data-stu-id="151e4-124">Action Requires Preprocessing</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RuleActionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="151e4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="151e4-125">-ResourceGroupName</span></span>
<span data-ttu-id="151e4-126">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="151e4-126">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="151e4-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="151e4-127">-SqlExpression</span></span>
<span data-ttu-id="151e4-128">SQL-Filter Ausdruck</span><span class="sxs-lookup"><span data-stu-id="151e4-128">Sql Filter Expression</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="151e4-129">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="151e4-129">-Subscription</span></span>
<span data-ttu-id="151e4-130">Name des Abonnements</span><span class="sxs-lookup"><span data-stu-id="151e4-130">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="151e4-131">-Topic</span><span class="sxs-lookup"><span data-stu-id="151e4-131">-Topic</span></span>
<span data-ttu-id="151e4-132">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="151e4-132">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="151e4-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="151e4-133">-Confirm</span></span>
<span data-ttu-id="151e4-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="151e4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="151e4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="151e4-135">-WhatIf</span></span>
<span data-ttu-id="151e4-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="151e4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="151e4-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="151e4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="151e4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="151e4-138">CommonParameters</span></span>
<span data-ttu-id="151e4-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="151e4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="151e4-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="151e4-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="151e4-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="151e4-141">INPUTS</span></span>

### <span data-ttu-id="151e4-142">System. String</span><span class="sxs-lookup"><span data-stu-id="151e4-142">System.String</span></span>

## <span data-ttu-id="151e4-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="151e4-143">OUTPUTS</span></span>

### <span data-ttu-id="151e4-144">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="151e4-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="151e4-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="151e4-145">NOTES</span></span>

## <span data-ttu-id="151e4-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="151e4-146">RELATED LINKS</span></span>
