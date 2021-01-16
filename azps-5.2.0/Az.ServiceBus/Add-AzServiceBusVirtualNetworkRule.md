---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/add-azservicebusvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusVirtualNetworkRule.md
ms.openlocfilehash: 3ff1f64bf65a4474dc9f47aa6bd419c442b49698
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296375"
---
# <span data-ttu-id="4ebfa-101">Add-AzServiceBusVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4ebfa-101">Add-AzServiceBusVirtualNetworkRule</span></span>

## <span data-ttu-id="4ebfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ebfa-102">SYNOPSIS</span></span>
<span data-ttu-id="4ebfa-103">Hinzufügen einer einzelnen VirtualNetworkRule zu NetworkRuleSet für den angegebenen Namespace</span><span class="sxs-lookup"><span data-stu-id="4ebfa-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="4ebfa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ebfa-104">SYNTAX</span></span>

### <span data-ttu-id="4ebfa-105">VirtualNetworkRulePropertiesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4ebfa-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ebfa-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ebfa-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ebfa-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ebfa-107">DESCRIPTION</span></span>
<span data-ttu-id="4ebfa-108">Hinzufügen einer einzelnen VirtualNetworkRule zu NetworkRuleSet für den angegebenen Namespace</span><span class="sxs-lookup"><span data-stu-id="4ebfa-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="4ebfa-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4ebfa-109">EXAMPLES</span></span>

### <span data-ttu-id="4ebfa-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ebfa-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```
<span data-ttu-id="4ebfa-111">Name: defaultAction : Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="4ebfa-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="4ebfa-112">Fügt das angegebene Subnetz und ignoreMissingVnetServiceEndpoint (VirtualNetworkRule) zu NetworkRuleSet für den angegebenen Namespace hinzu.</span><span class="sxs-lookup"><span data-stu-id="4ebfa-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="4ebfa-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4ebfa-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```
<span data-ttu-id="4ebfa-114">Name: defaultAction : Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="4ebfa-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="4ebfa-115">Fügt "$virtualruleset 1" zu "NetworkRuleSet" für den angegebenen Namespace hinzu.</span><span class="sxs-lookup"><span data-stu-id="4ebfa-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="4ebfa-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ebfa-116">PARAMETERS</span></span>

### <span data-ttu-id="4ebfa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ebfa-117">-DefaultProfile</span></span>
<span data-ttu-id="4ebfa-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ebfa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ebfa-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4ebfa-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="4ebfa-120">ARM-ID des Subnetzes</span><span class="sxs-lookup"><span data-stu-id="4ebfa-120">ARM ID of Subnet</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ebfa-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4ebfa-121">-Name</span></span>
<span data-ttu-id="4ebfa-122">Namespacename</span><span class="sxs-lookup"><span data-stu-id="4ebfa-122">Namespace Name</span></span>

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

### <span data-ttu-id="4ebfa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ebfa-123">-ResourceGroupName</span></span>
<span data-ttu-id="4ebfa-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="4ebfa-124">Resource Group Name</span></span>

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

### <span data-ttu-id="4ebfa-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4ebfa-125">-SubnetId</span></span>
<span data-ttu-id="4ebfa-126">Subnetzressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4ebfa-126">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ebfa-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="4ebfa-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="4ebfa-128">VirtualNetworkRule Configuration Object</span><span class="sxs-lookup"><span data-stu-id="4ebfa-128">VirtualNetworkRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ebfa-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ebfa-129">-Confirm</span></span>
<span data-ttu-id="4ebfa-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4ebfa-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ebfa-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4ebfa-131">-WhatIf</span></span>
<span data-ttu-id="4ebfa-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4ebfa-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ebfa-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ebfa-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ebfa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ebfa-134">CommonParameters</span></span>
<span data-ttu-id="4ebfa-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ebfa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4ebfa-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ebfa-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ebfa-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4ebfa-137">INPUTS</span></span>

### <span data-ttu-id="4ebfa-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4ebfa-138">System.String</span></span>

### <span data-ttu-id="4ebfa-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4ebfa-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4ebfa-140">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="4ebfa-140">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="4ebfa-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4ebfa-141">OUTPUTS</span></span>

### <span data-ttu-id="4ebfa-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="4ebfa-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="4ebfa-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4ebfa-143">NOTES</span></span>

## <span data-ttu-id="4ebfa-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4ebfa-144">RELATED LINKS</span></span>