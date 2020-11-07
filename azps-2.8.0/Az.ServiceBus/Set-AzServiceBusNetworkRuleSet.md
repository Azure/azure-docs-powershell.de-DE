---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 9465ad8d6f66b62da8b224ab635ca45fed1a8ca1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824751"
---
# <span data-ttu-id="93a62-101">Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="93a62-101">Set-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="93a62-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93a62-102">SYNOPSIS</span></span>
<span data-ttu-id="93a62-103">Aktualisieren Sie die NetworkruleSet des angegebenen Namespaces im aktuellen Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="93a62-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="93a62-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93a62-104">SYNTAX</span></span>

### <span data-ttu-id="93a62-105">NetworkRuleSetPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="93a62-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-IPRule] <PSNWRuleSetIpRulesAttributes[]> [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93a62-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="93a62-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93a62-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93a62-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93a62-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93a62-108">DESCRIPTION</span></span>
<span data-ttu-id="93a62-109">Aktualisieren Sie die NetwrokruleSet des angegebenen Namespaces im aktuellen Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="93a62-109">Update the NetwrokruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="93a62-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93a62-110">EXAMPLES</span></span>

### <span data-ttu-id="93a62-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="93a62-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\>  Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="93a62-112">Name: standardmäßige Standard: Allow ID:/Subscriptions/SubscriptionId/ResourceGroups/ResourceGroup/Providers/Microsoft.ServiceBus/Namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, allow, 3.3.3.3, allow} VirtualNetworkRules: {/Subscriptions/SubscriptionId/ResourceGroups/ResourceGroup/Providers/Microsoft.Network/virtualNetworks/sbehvnettest1/Subnets/default; true}</span><span class="sxs-lookup"><span data-stu-id="93a62-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="93a62-113">Aktualisieren der NetworkRuleSet mit-IPRule und-VirtualNetworkRule-Parametern</span><span class="sxs-lookup"><span data-stu-id="93a62-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="93a62-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="93a62-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="93a62-115">Name: standardmäßige Standard: Allow ID:/Subscriptions/SubscriptionId/ResourceGroups/ResourceGroup/Providers/Microsoft.ServiceBus/Namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, allow, 3.3.3.3, allow} VirtualNetworkRules: {/Subscriptions/SubscriptionId/ResourceGroups/ResourceGroup/Providers/Microsoft.Network/virtualNetworks/sbehvnettest1/Subnets/default; true}</span><span class="sxs-lookup"><span data-stu-id="93a62-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="93a62-116">Aktualisieren der NetworkRuleSet mit-Inputobject</span><span class="sxs-lookup"><span data-stu-id="93a62-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="93a62-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="93a62-117">Example 3</span></span>
```powershell
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```

<span data-ttu-id="93a62-118">Name: standardmäßige Standard: Allow ID:/Subscriptions/SubscriptionId/ResourceGroups/ResourceGroup/Providers/Microsoft.ServiceBus/Namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, allow, 3.3.3.3, allow} VirtualNetworkRules: {/Subscriptions/SubscriptionId/ResourceGroups/ResourceGroup/Providers/Microsoft.Network/virtualNetworks/sbehvnettest1/Subnets/default; true}</span><span class="sxs-lookup"><span data-stu-id="93a62-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="93a62-119">Aktualisieren Sie die NetworkRuleSet mithilfe der-Resourcen-und der anderen Namespace.</span><span class="sxs-lookup"><span data-stu-id="93a62-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="93a62-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="93a62-120">PARAMETERS</span></span>

### <span data-ttu-id="93a62-121">– Standardmäßig</span><span class="sxs-lookup"><span data-stu-id="93a62-121">-DefaultAction</span></span>
<span data-ttu-id="93a62-122">Standardaktion für NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="93a62-122">Default Action for NetworkRuleSet</span></span>

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

### <span data-ttu-id="93a62-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93a62-123">-DefaultProfile</span></span>
<span data-ttu-id="93a62-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="93a62-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93a62-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="93a62-125">-InputObject</span></span>
<span data-ttu-id="93a62-126">NetworkruleSet-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="93a62-126">NetworkruleSet Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes
Parameter Sets: NetwrokruleSetInputObjectSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93a62-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="93a62-127">-IPRule</span></span>
<span data-ttu-id="93a62-128">Liste der IPRuleSet</span><span class="sxs-lookup"><span data-stu-id="93a62-128">List of IPRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93a62-129">-Name</span><span class="sxs-lookup"><span data-stu-id="93a62-129">-Name</span></span>
<span data-ttu-id="93a62-130">Name des EventHub-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="93a62-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="93a62-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93a62-131">-ResourceGroupName</span></span>
<span data-ttu-id="93a62-132">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="93a62-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="93a62-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="93a62-133">-ResourceId</span></span>
<span data-ttu-id="93a62-134">Ressourcen-ID des Namespaces</span><span class="sxs-lookup"><span data-stu-id="93a62-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="93a62-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="93a62-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="93a62-136">Liste der VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="93a62-136">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: VirtualNteworkRule

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93a62-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="93a62-137">-Confirm</span></span>
<span data-ttu-id="93a62-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="93a62-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93a62-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93a62-139">-WhatIf</span></span>
<span data-ttu-id="93a62-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="93a62-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93a62-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="93a62-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93a62-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93a62-142">CommonParameters</span></span>
<span data-ttu-id="93a62-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93a62-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="93a62-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93a62-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93a62-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93a62-145">INPUTS</span></span>

### <span data-ttu-id="93a62-146">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="93a62-146">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="93a62-147">System. String</span><span class="sxs-lookup"><span data-stu-id="93a62-147">System.String</span></span>

## <span data-ttu-id="93a62-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93a62-148">OUTPUTS</span></span>

### <span data-ttu-id="93a62-149">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="93a62-149">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="93a62-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="93a62-150">NOTES</span></span>

## <span data-ttu-id="93a62-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93a62-151">RELATED LINKS</span></span>