---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: b8027083225b774d1795d8c96132a0e031f8a51e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946563"
---
# <span data-ttu-id="d04c2-101">Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d04c2-101">Set-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="d04c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d04c2-102">SYNOPSIS</span></span>
<span data-ttu-id="d04c2-103">Aktualisieren Sie das NetworkruleSet des angegebenen Namespaces im aktuellen Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d04c2-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="d04c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d04c2-104">SYNTAX</span></span>

### <span data-ttu-id="d04c2-105">NetworkRuleSetPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d04c2-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-TrustedServiceAccessEnabled] [-IPRule] <PSNWRuleSetIpRulesAttributes[]>
 [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d04c2-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d04c2-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d04c2-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d04c2-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d04c2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d04c2-108">DESCRIPTION</span></span>
<span data-ttu-id="d04c2-109">Aktualisieren Sie das NetworkruleSet des angegebenen Namespaces im aktuellen Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d04c2-109">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="d04c2-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d04c2-110">EXAMPLES</span></span>

### <span data-ttu-id="d04c2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d04c2-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace EventHub-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="d04c2-112">Name : default DefaultAction : Allow Id : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="d04c2-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="d04c2-113">Aktualisieren des NetworkRuleSets mithilfe der Parameter -IPRule und -VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d04c2-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="d04c2-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d04c2-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="d04c2-115">Name : default DefaultAction : Allow Id : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="d04c2-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="d04c2-116">Aktualisieren des NetworkRuleSets mit -InputObject</span><span class="sxs-lookup"><span data-stu-id="d04c2-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="d04c2-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d04c2-117">Example 3</span></span>
```powershell
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375
```
<span data-ttu-id="d04c2-118">Name : default DefaultAction : Allow Id : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="d04c2-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="d04c2-119">Aktualisieren Sie das NetworkRuleSet mit -ResourceId des anderen Namespaces.</span><span class="sxs-lookup"><span data-stu-id="d04c2-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="d04c2-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d04c2-120">PARAMETERS</span></span>

### <span data-ttu-id="d04c2-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="d04c2-121">-DefaultAction</span></span>
<span data-ttu-id="d04c2-122">Standardaktion für NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d04c2-122">Default Action for NetworkRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d04c2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d04c2-123">-DefaultProfile</span></span>
<span data-ttu-id="d04c2-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d04c2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d04c2-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d04c2-125">-InputObject</span></span>
<span data-ttu-id="d04c2-126">NetworkruleSet Configuration Object</span><span class="sxs-lookup"><span data-stu-id="d04c2-126">NetworkruleSet Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes
Parameter Sets: NetwrokruleSetInputObjectSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d04c2-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="d04c2-127">-IPRule</span></span>
<span data-ttu-id="d04c2-128">Liste von IPRuleSet</span><span class="sxs-lookup"><span data-stu-id="d04c2-128">List of IPRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d04c2-129">-Name</span><span class="sxs-lookup"><span data-stu-id="d04c2-129">-Name</span></span>
<span data-ttu-id="d04c2-130">Name des EventHub-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="d04c2-130">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d04c2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d04c2-131">-ResourceGroupName</span></span>
<span data-ttu-id="d04c2-132">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="d04c2-132">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d04c2-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d04c2-133">-ResourceId</span></span>
<span data-ttu-id="d04c2-134">Ressourcen-ID von Namespace</span><span class="sxs-lookup"><span data-stu-id="d04c2-134">Resource ID of Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d04c2-135">-TrustedServiceAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="d04c2-135">-TrustedServiceAccessEnabled</span></span>
<span data-ttu-id="d04c2-136">Gibt an, ob TrustedServiceAccessEnabled aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="d04c2-136">Indicates whether TrustedServiceAccessEnabled is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d04c2-137">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d04c2-137">-VirtualNetworkRule</span></span>
<span data-ttu-id="d04c2-138">Liste von VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="d04c2-138">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: VirtualNteworkRule

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d04c2-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d04c2-139">-Confirm</span></span>
<span data-ttu-id="d04c2-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d04c2-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d04c2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d04c2-141">-WhatIf</span></span>
<span data-ttu-id="d04c2-142">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d04c2-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d04c2-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d04c2-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d04c2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d04c2-144">CommonParameters</span></span>
<span data-ttu-id="d04c2-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d04c2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d04c2-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d04c2-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d04c2-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d04c2-147">INPUTS</span></span>

### <span data-ttu-id="d04c2-148">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="d04c2-148">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="d04c2-149">System.String</span><span class="sxs-lookup"><span data-stu-id="d04c2-149">System.String</span></span>

## <span data-ttu-id="d04c2-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d04c2-150">OUTPUTS</span></span>

### <span data-ttu-id="d04c2-151">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="d04c2-151">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="d04c2-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d04c2-152">NOTES</span></span>

## <span data-ttu-id="d04c2-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d04c2-153">RELATED LINKS</span></span>