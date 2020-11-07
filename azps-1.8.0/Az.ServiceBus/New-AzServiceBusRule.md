---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: 869bfdaa7ff772980b7acf1caee6c7d6a8784d37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659386"
---
# <span data-ttu-id="2068b-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="2068b-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="2068b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2068b-102">SYNOPSIS</span></span>
<span data-ttu-id="2068b-103">Erstellt eine neue Regel für ein bestimmtes Abonnement des Themas.</span><span class="sxs-lookup"><span data-stu-id="2068b-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="2068b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2068b-104">SYNTAX</span></span>

### <span data-ttu-id="2068b-105">RulePropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2068b-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2068b-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="2068b-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2068b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2068b-107">DESCRIPTION</span></span>
<span data-ttu-id="2068b-108">Das Cmdlet **New-AzServiceBusRule** erstellt eine neue Regel für ein bestimmtes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2068b-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="2068b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2068b-109">EXAMPLES</span></span>

### <span data-ttu-id="2068b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2068b-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="2068b-111">Das New-AzServiceBusRule-Cmdlet erstellt eine neue Regel für das angegebene Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2068b-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="2068b-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2068b-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="2068b-113">Das New-AzServiceBusRule-Cmdlet erstellt eine neue Regel für das angegebene Abonnement mit Action Filter.</span><span class="sxs-lookup"><span data-stu-id="2068b-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="2068b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2068b-114">PARAMETERS</span></span>

### <span data-ttu-id="2068b-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="2068b-115">-ActionSqlExpression</span></span>
<span data-ttu-id="2068b-116">Action-SqlFillter-Ausdruck</span><span class="sxs-lookup"><span data-stu-id="2068b-116">Action SqlFillter Expression</span></span>

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

### <span data-ttu-id="2068b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2068b-117">-DefaultProfile</span></span>
<span data-ttu-id="2068b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2068b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2068b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2068b-119">-Name</span></span>
<span data-ttu-id="2068b-120">Regelname</span><span class="sxs-lookup"><span data-stu-id="2068b-120">Rule Name</span></span>

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

### <span data-ttu-id="2068b-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2068b-121">-Namespace</span></span>
<span data-ttu-id="2068b-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="2068b-122">Namespace Name</span></span>

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

### <span data-ttu-id="2068b-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="2068b-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="2068b-124">Aktion erfordert Vorverarbeitung</span><span class="sxs-lookup"><span data-stu-id="2068b-124">Action Requires Preprocessing</span></span>

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

### <span data-ttu-id="2068b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2068b-125">-ResourceGroupName</span></span>
<span data-ttu-id="2068b-126">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2068b-126">The name of the resource group</span></span>

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

### <span data-ttu-id="2068b-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="2068b-127">-SqlExpression</span></span>
<span data-ttu-id="2068b-128">SQL Fillter-Ausdruck</span><span class="sxs-lookup"><span data-stu-id="2068b-128">Sql Fillter Expression</span></span>

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

### <span data-ttu-id="2068b-129">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="2068b-129">-Subscription</span></span>
<span data-ttu-id="2068b-130">Name des Abonnements</span><span class="sxs-lookup"><span data-stu-id="2068b-130">Subscription Name</span></span>

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

### <span data-ttu-id="2068b-131">-Topic</span><span class="sxs-lookup"><span data-stu-id="2068b-131">-Topic</span></span>
<span data-ttu-id="2068b-132">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="2068b-132">Topic Name</span></span>

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

### <span data-ttu-id="2068b-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2068b-133">-Confirm</span></span>
<span data-ttu-id="2068b-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2068b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2068b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2068b-135">-WhatIf</span></span>
<span data-ttu-id="2068b-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2068b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2068b-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2068b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2068b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2068b-138">CommonParameters</span></span>
<span data-ttu-id="2068b-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2068b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2068b-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2068b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2068b-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2068b-141">INPUTS</span></span>

### <span data-ttu-id="2068b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2068b-142">System.String</span></span>

## <span data-ttu-id="2068b-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2068b-143">OUTPUTS</span></span>

### <span data-ttu-id="2068b-144">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="2068b-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="2068b-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="2068b-145">NOTES</span></span>

## <span data-ttu-id="2068b-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2068b-146">RELATED LINKS</span></span>
