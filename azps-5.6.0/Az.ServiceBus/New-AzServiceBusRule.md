---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: 12064269e3a8c2e424bbd0e15888968c679784e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923443"
---
# <span data-ttu-id="73104-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="73104-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="73104-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73104-102">SYNOPSIS</span></span>
<span data-ttu-id="73104-103">Erstellt eine neue Regel für ein bestimmtes Abonnement von Thema.</span><span class="sxs-lookup"><span data-stu-id="73104-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="73104-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73104-104">SYNTAX</span></span>

### <span data-ttu-id="73104-105">RulePropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="73104-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73104-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="73104-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73104-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73104-107">DESCRIPTION</span></span>
<span data-ttu-id="73104-108">Das **Cmdlet New-AzServiceBusRule** Erstellt eine neue Regel für ein bestimmtes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="73104-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="73104-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="73104-109">EXAMPLES</span></span>

### <span data-ttu-id="73104-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="73104-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="73104-111">Das New-AzServiceBusRule-Cmdlet erstellt eine neue Regel für das angegebene Abonnement.</span><span class="sxs-lookup"><span data-stu-id="73104-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="73104-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="73104-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="73104-113">Das New-AzServiceBusRule-Cmdlet erstellt eine neue Regel für das angegebene Abonnement mit ActionFilter.</span><span class="sxs-lookup"><span data-stu-id="73104-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="73104-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="73104-114">PARAMETERS</span></span>

### <span data-ttu-id="73104-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="73104-115">-ActionSqlExpression</span></span>
<span data-ttu-id="73104-116">Aktion SqlFilter-Ausdruck</span><span class="sxs-lookup"><span data-stu-id="73104-116">Action SqlFilter Expression</span></span>

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

### <span data-ttu-id="73104-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73104-117">-DefaultProfile</span></span>
<span data-ttu-id="73104-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="73104-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73104-119">-Name</span><span class="sxs-lookup"><span data-stu-id="73104-119">-Name</span></span>
<span data-ttu-id="73104-120">Regelname</span><span class="sxs-lookup"><span data-stu-id="73104-120">Rule Name</span></span>

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

### <span data-ttu-id="73104-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="73104-121">-Namespace</span></span>
<span data-ttu-id="73104-122">Namespacename</span><span class="sxs-lookup"><span data-stu-id="73104-122">Namespace Name</span></span>

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

### <span data-ttu-id="73104-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="73104-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="73104-124">Aktion erfordert Die Vorverarbeitung</span><span class="sxs-lookup"><span data-stu-id="73104-124">Action Requires Preprocessing</span></span>

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

### <span data-ttu-id="73104-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73104-125">-ResourceGroupName</span></span>
<span data-ttu-id="73104-126">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="73104-126">The name of the resource group</span></span>

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

### <span data-ttu-id="73104-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="73104-127">-SqlExpression</span></span>
<span data-ttu-id="73104-128">Sql Filter-Ausdruck</span><span class="sxs-lookup"><span data-stu-id="73104-128">Sql Filter Expression</span></span>

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

### <span data-ttu-id="73104-129">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="73104-129">-Subscription</span></span>
<span data-ttu-id="73104-130">Abonnementname</span><span class="sxs-lookup"><span data-stu-id="73104-130">Subscription Name</span></span>

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

### <span data-ttu-id="73104-131">-Topic</span><span class="sxs-lookup"><span data-stu-id="73104-131">-Topic</span></span>
<span data-ttu-id="73104-132">Topic Name</span><span class="sxs-lookup"><span data-stu-id="73104-132">Topic Name</span></span>

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

### <span data-ttu-id="73104-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="73104-133">-Confirm</span></span>
<span data-ttu-id="73104-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="73104-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73104-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73104-135">-WhatIf</span></span>
<span data-ttu-id="73104-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73104-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73104-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73104-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73104-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73104-138">CommonParameters</span></span>
<span data-ttu-id="73104-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73104-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73104-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73104-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73104-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="73104-141">INPUTS</span></span>

### <span data-ttu-id="73104-142">System.String</span><span class="sxs-lookup"><span data-stu-id="73104-142">System.String</span></span>

## <span data-ttu-id="73104-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="73104-143">OUTPUTS</span></span>

### <span data-ttu-id="73104-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="73104-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="73104-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="73104-145">NOTES</span></span>

## <span data-ttu-id="73104-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="73104-146">RELATED LINKS</span></span>
