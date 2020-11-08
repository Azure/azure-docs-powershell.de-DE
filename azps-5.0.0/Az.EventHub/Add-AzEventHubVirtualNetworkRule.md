---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 627519cd4325e7fb9677c358146f2f8a9081151a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177657"
---
# <span data-ttu-id="0e210-101">Add-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0e210-101">Add-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="0e210-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e210-102">SYNOPSIS</span></span>
<span data-ttu-id="0e210-103">Hinzufügen eines einzelnen VirtualNetworkRule zu NetworkRuleSet für den angegebenen Namespace</span><span class="sxs-lookup"><span data-stu-id="0e210-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="0e210-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e210-104">SYNTAX</span></span>

### <span data-ttu-id="0e210-105">VirtualNetworkRulePropertiesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0e210-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e210-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e210-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e210-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e210-107">DESCRIPTION</span></span>
<span data-ttu-id="0e210-108">Hinzufügen eines einzelnen VirtualNetworkRule zu NetworkRuleSet für den angegebenen Namespace</span><span class="sxs-lookup"><span data-stu-id="0e210-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="0e210-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e210-109">EXAMPLES</span></span>

### <span data-ttu-id="0e210-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0e210-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```

<span data-ttu-id="0e210-111">Name: standardmäßige Standard-/Subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/Providers/Microsoft.Eventhub/Namespaces/Eventhub-Namespace-1122/networkRuleSets/default: Allow ID: Type: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/Subscriptions/SubscriptionId/ResourceGroups/v-ajnavtest/Providers/Microsoft.Network/virtualNetworks/sbehvnettest1/Subnets/default; false}</span><span class="sxs-lookup"><span data-stu-id="0e210-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="0e210-112">Addiert das angegebene Subnetz und IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) zu NetworkRuleSet für den angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="0e210-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="0e210-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0e210-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="0e210-114">Name: standardmäßige Standard-/Subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/Providers/Microsoft.Eventhub/Namespaces/Eventhub-Namespace-1122/networkRuleSets/default: Allow ID: Type: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/Subscriptions/SubscriptionId/ResourceGroups/v-ajnavtest/Providers/Microsoft.Network/virtualNetworks/sbehvnettest1/Subnets/default; false}</span><span class="sxs-lookup"><span data-stu-id="0e210-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="0e210-115">Addiert die $virtualruleset 1 zu NetworkRuleSet für den angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="0e210-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="0e210-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e210-116">PARAMETERS</span></span>

### <span data-ttu-id="0e210-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e210-117">-DefaultProfile</span></span>
<span data-ttu-id="0e210-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0e210-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e210-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e210-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="0e210-120">Arm-ID des Subnets</span><span class="sxs-lookup"><span data-stu-id="0e210-120">ARM ID of Subnet</span></span>

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

### <span data-ttu-id="0e210-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0e210-121">-Name</span></span>
<span data-ttu-id="0e210-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="0e210-122">Namespace Name</span></span>

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

### <span data-ttu-id="0e210-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e210-123">-ResourceGroupName</span></span>
<span data-ttu-id="0e210-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="0e210-124">Resource Group Name</span></span>

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

### <span data-ttu-id="0e210-125">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="0e210-125">-SubnetId</span></span>
<span data-ttu-id="0e210-126">Subnet-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="0e210-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="0e210-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="0e210-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="0e210-128">VirtualNetworkRule-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="0e210-128">VirtualNetworkRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e210-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0e210-129">-Confirm</span></span>
<span data-ttu-id="0e210-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0e210-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e210-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e210-131">-WhatIf</span></span>
<span data-ttu-id="0e210-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0e210-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e210-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e210-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e210-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e210-134">CommonParameters</span></span>
<span data-ttu-id="0e210-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e210-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0e210-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e210-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e210-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e210-137">INPUTS</span></span>

### <span data-ttu-id="0e210-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0e210-138">System.String</span></span>

### <span data-ttu-id="0e210-139">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="0e210-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="0e210-140">Microsoft. Azure. Commands. EventHub. Models. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="0e210-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="0e210-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e210-141">OUTPUTS</span></span>

### <span data-ttu-id="0e210-142">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="0e210-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="0e210-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e210-143">NOTES</span></span>

## <span data-ttu-id="0e210-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e210-144">RELATED LINKS</span></span>
