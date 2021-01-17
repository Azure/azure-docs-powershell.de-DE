---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: b86b9629062515afb1ee70e7c7372cbc7687bfa5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471853"
---
# <span data-ttu-id="5e5d3-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="5e5d3-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="5e5d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e5d3-102">SYNOPSIS</span></span>
<span data-ttu-id="5e5d3-103">Aktualisiert die angegebene Regelbeschreibung für das angegebene Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e5d3-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="5e5d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e5d3-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e5d3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e5d3-105">DESCRIPTION</span></span>
<span data-ttu-id="5e5d3-106">Das **Cmdlet "Set-AzServiceBusRule"** aktualisiert die Beschreibung für die angegebene Regel des angegebenen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="5e5d3-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="5e5d3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5e5d3-107">EXAMPLES</span></span>

### <span data-ttu-id="5e5d3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5e5d3-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="5e5d3-109">Aktualisiert den Sql-Ausdruck **"mysqlexpression='condition"** der Regel `SBRule` des Abonnements in `SBSubscription` "Topic". `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="5e5d3-109">Updates the sql expression **mysqlexpression='condition'** of the rule `SBRule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="5e5d3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e5d3-110">PARAMETERS</span></span>

### <span data-ttu-id="5e5d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e5d3-111">-DefaultProfile</span></span>
<span data-ttu-id="5e5d3-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e5d3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e5d3-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e5d3-113">-InputObject</span></span>
<span data-ttu-id="5e5d3-114">Definition von ServiceBus-Regeln.</span><span class="sxs-lookup"><span data-stu-id="5e5d3-114">ServiceBus Rules definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e5d3-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5e5d3-115">-Name</span></span>
<span data-ttu-id="5e5d3-116">Regelname.</span><span class="sxs-lookup"><span data-stu-id="5e5d3-116">Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e5d3-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5e5d3-117">-Namespace</span></span>
<span data-ttu-id="5e5d3-118">Namespacename.</span><span class="sxs-lookup"><span data-stu-id="5e5d3-118">Namespace Name.</span></span>

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

### <span data-ttu-id="5e5d3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e5d3-119">-ResourceGroupName</span></span>
<span data-ttu-id="5e5d3-120">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5e5d3-120">The name of the resource group</span></span>

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

### <span data-ttu-id="5e5d3-121">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="5e5d3-121">-Subscription</span></span>
<span data-ttu-id="5e5d3-122">Abonnementname.</span><span class="sxs-lookup"><span data-stu-id="5e5d3-122">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e5d3-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="5e5d3-123">-Topic</span></span>
<span data-ttu-id="5e5d3-124">Themaname.</span><span class="sxs-lookup"><span data-stu-id="5e5d3-124">Topic Name.</span></span>

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

### <span data-ttu-id="5e5d3-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e5d3-125">-Confirm</span></span>
<span data-ttu-id="5e5d3-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e5d3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e5d3-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5e5d3-127">-WhatIf</span></span>
<span data-ttu-id="5e5d3-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e5d3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e5d3-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e5d3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e5d3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e5d3-130">CommonParameters</span></span>
<span data-ttu-id="5e5d3-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e5d3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e5d3-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e5d3-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e5d3-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5e5d3-133">INPUTS</span></span>

### <span data-ttu-id="5e5d3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="5e5d3-134">System.String</span></span>

### <span data-ttu-id="5e5d3-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="5e5d3-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="5e5d3-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5e5d3-136">OUTPUTS</span></span>

### <span data-ttu-id="5e5d3-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="5e5d3-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="5e5d3-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5e5d3-138">NOTES</span></span>

## <span data-ttu-id="5e5d3-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5e5d3-139">RELATED LINKS</span></span>
