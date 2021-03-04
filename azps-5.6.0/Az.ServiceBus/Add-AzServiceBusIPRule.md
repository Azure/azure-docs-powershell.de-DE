---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/add-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
ms.openlocfilehash: e0450df003b474cae57319d5450423af58f4d3eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926411"
---
# <span data-ttu-id="3f356-101">Add-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="3f356-101">Add-AzServiceBusIPRule</span></span>

## <span data-ttu-id="3f356-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f356-102">SYNOPSIS</span></span>
<span data-ttu-id="3f356-103">Hinzufügen einer einzelnen IP-Regel zum NetworkRuleSet des angegebenen Namespaces</span><span class="sxs-lookup"><span data-stu-id="3f356-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="3f356-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f356-104">SYNTAX</span></span>

### <span data-ttu-id="3f356-105">IPRulePropertiesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3f356-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f356-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f356-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f356-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f356-107">DESCRIPTION</span></span>
<span data-ttu-id="3f356-108">Hinzufügen einer einzelnen IP-Regel zum NetworkRuleSet des angegebenen Namespaces</span><span class="sxs-lookup"><span data-stu-id="3f356-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="3f356-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3f356-109">EXAMPLES</span></span>

### <span data-ttu-id="3f356-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3f356-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="3f356-111">Name : default DefaultAction : Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="3f356-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="3f356-112">fügen Sie das IPRule mit IpMask "11.22.33.44" und Aktion zulassen für den angegebenen Namespace hinzu.</span><span class="sxs-lookup"><span data-stu-id="3f356-112">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

### <span data-ttu-id="3f356-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3f356-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpRuleObject $ipruleObject
```
<span data-ttu-id="3f356-114">Name : default DefaultAction : Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="3f356-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="3f356-115">fügen Sie das IPRule mit IpMask "11.22.33.44" und Aktion zulassen für den angegebenen Namespace hinzu.</span><span class="sxs-lookup"><span data-stu-id="3f356-115">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

## <span data-ttu-id="3f356-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3f356-116">PARAMETERS</span></span>

### <span data-ttu-id="3f356-117">-Aktion</span><span class="sxs-lookup"><span data-stu-id="3f356-117">-Action</span></span>
<span data-ttu-id="3f356-118">Die AKTION "IP-Filter"</span><span class="sxs-lookup"><span data-stu-id="3f356-118">The IP Filter Action</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f356-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f356-119">-DefaultProfile</span></span>
<span data-ttu-id="3f356-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f356-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f356-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="3f356-121">-IpMask</span></span>
<span data-ttu-id="3f356-122">Subnetzressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="3f356-122">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f356-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="3f356-123">-IpRuleObject</span></span>
<span data-ttu-id="3f356-124">IpRule Configuration Object to be added</span><span class="sxs-lookup"><span data-stu-id="3f356-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f356-125">-Name</span><span class="sxs-lookup"><span data-stu-id="3f356-125">-Name</span></span>
<span data-ttu-id="3f356-126">Namespacename</span><span class="sxs-lookup"><span data-stu-id="3f356-126">Namespace Name</span></span>

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

### <span data-ttu-id="3f356-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f356-127">-ResourceGroupName</span></span>
<span data-ttu-id="3f356-128">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="3f356-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f356-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3f356-129">-Confirm</span></span>
<span data-ttu-id="3f356-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f356-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f356-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f356-131">-WhatIf</span></span>
<span data-ttu-id="3f356-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f356-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f356-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f356-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f356-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f356-134">CommonParameters</span></span>
<span data-ttu-id="3f356-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f356-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3f356-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f356-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f356-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3f356-137">INPUTS</span></span>

### <span data-ttu-id="3f356-138">System.String</span><span class="sxs-lookup"><span data-stu-id="3f356-138">System.String</span></span>

### <span data-ttu-id="3f356-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="3f356-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="3f356-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3f356-140">OUTPUTS</span></span>

### <span data-ttu-id="3f356-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="3f356-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="3f356-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3f356-142">NOTES</span></span>

## <span data-ttu-id="3f356-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3f356-143">RELATED LINKS</span></span>