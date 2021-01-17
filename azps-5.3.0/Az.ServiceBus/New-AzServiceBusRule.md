---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: d667049fb512545aebfd9681b3ad3d9f44651951
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471891"
---
# <span data-ttu-id="9d1fb-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="9d1fb-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="9d1fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d1fb-102">SYNOPSIS</span></span>
<span data-ttu-id="9d1fb-103">Erstellt eine neue Regel für ein bestimmtes Abonnement von Thema.</span><span class="sxs-lookup"><span data-stu-id="9d1fb-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="9d1fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d1fb-104">SYNTAX</span></span>

### <span data-ttu-id="9d1fb-105">RulePropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9d1fb-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d1fb-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="9d1fb-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d1fb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d1fb-107">DESCRIPTION</span></span>
<span data-ttu-id="9d1fb-108">Das **Cmdlet "New-AzServiceBusRule"** erstellt eine neue Regel für ein angegebenes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9d1fb-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="9d1fb-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9d1fb-109">EXAMPLES</span></span>

### <span data-ttu-id="9d1fb-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9d1fb-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="9d1fb-111">Das New-AzServiceBusRule erstellt eine neue Regel für das angegebene Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9d1fb-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="9d1fb-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9d1fb-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="9d1fb-113">Das New-AzServiceBusRule erstellt eine neue Regel für das angegebene Abonnement mit ActionFilter.</span><span class="sxs-lookup"><span data-stu-id="9d1fb-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="9d1fb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d1fb-114">PARAMETERS</span></span>

### <span data-ttu-id="9d1fb-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="9d1fb-115">-ActionSqlExpression</span></span>
<span data-ttu-id="9d1fb-116">Aktion "SqlFilter-Ausdruck"</span><span class="sxs-lookup"><span data-stu-id="9d1fb-116">Action SqlFilter Expression</span></span>

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

### <span data-ttu-id="9d1fb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d1fb-117">-DefaultProfile</span></span>
<span data-ttu-id="9d1fb-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d1fb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d1fb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9d1fb-119">-Name</span></span>
<span data-ttu-id="9d1fb-120">Regelname</span><span class="sxs-lookup"><span data-stu-id="9d1fb-120">Rule Name</span></span>

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

### <span data-ttu-id="9d1fb-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9d1fb-121">-Namespace</span></span>
<span data-ttu-id="9d1fb-122">Namespacename</span><span class="sxs-lookup"><span data-stu-id="9d1fb-122">Namespace Name</span></span>

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

### <span data-ttu-id="9d1fb-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="9d1fb-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="9d1fb-124">Aktion erfordert Vorverarbeitung</span><span class="sxs-lookup"><span data-stu-id="9d1fb-124">Action Requires Preprocessing</span></span>

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

### <span data-ttu-id="9d1fb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d1fb-125">-ResourceGroupName</span></span>
<span data-ttu-id="9d1fb-126">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="9d1fb-126">The name of the resource group</span></span>

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

### <span data-ttu-id="9d1fb-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="9d1fb-127">-SqlExpression</span></span>
<span data-ttu-id="9d1fb-128">Sql Filter Expression</span><span class="sxs-lookup"><span data-stu-id="9d1fb-128">Sql Filter Expression</span></span>

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

### <span data-ttu-id="9d1fb-129">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="9d1fb-129">-Subscription</span></span>
<span data-ttu-id="9d1fb-130">Abonnementname</span><span class="sxs-lookup"><span data-stu-id="9d1fb-130">Subscription Name</span></span>

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

### <span data-ttu-id="9d1fb-131">-Topic</span><span class="sxs-lookup"><span data-stu-id="9d1fb-131">-Topic</span></span>
<span data-ttu-id="9d1fb-132">Themaname</span><span class="sxs-lookup"><span data-stu-id="9d1fb-132">Topic Name</span></span>

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

### <span data-ttu-id="9d1fb-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d1fb-133">-Confirm</span></span>
<span data-ttu-id="9d1fb-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9d1fb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d1fb-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9d1fb-135">-WhatIf</span></span>
<span data-ttu-id="9d1fb-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9d1fb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d1fb-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9d1fb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d1fb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d1fb-138">CommonParameters</span></span>
<span data-ttu-id="9d1fb-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d1fb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d1fb-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d1fb-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d1fb-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9d1fb-141">INPUTS</span></span>

### <span data-ttu-id="9d1fb-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9d1fb-142">System.String</span></span>

## <span data-ttu-id="9d1fb-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9d1fb-143">OUTPUTS</span></span>

### <span data-ttu-id="9d1fb-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="9d1fb-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="9d1fb-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9d1fb-145">NOTES</span></span>

## <span data-ttu-id="9d1fb-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9d1fb-146">RELATED LINKS</span></span>
