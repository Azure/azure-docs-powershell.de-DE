---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 72be362d513f447e32db0fe13b5e4b7b076ab947
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661014"
---
# <span data-ttu-id="66303-101">Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="66303-101">Set-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="66303-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66303-102">SYNOPSIS</span></span>
<span data-ttu-id="66303-103">Aktualisieren Sie die NetwrokruleSet des angegebenen Namespace im aktuellen Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="66303-103">Update the NetwrokruleSet of the given Namepsace in the current Azure subscription.</span></span>

## <span data-ttu-id="66303-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66303-104">SYNTAX</span></span>

### <span data-ttu-id="66303-105">NetworkRuleSetPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="66303-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-IPRule] <PSNWRuleSetIpRulesAttributes[]> [-VirtualNteworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66303-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="66303-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66303-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66303-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66303-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66303-108">DESCRIPTION</span></span>
<span data-ttu-id="66303-109">Aktualisieren Sie die NetwrokruleSet des angegebenen Namespace im aktuellen Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="66303-109">Update the NetwrokruleSet of the given Namepsace in the current Azure subscription.</span></span>

## <span data-ttu-id="66303-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66303-110">EXAMPLES</span></span>

### <span data-ttu-id="66303-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="66303-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace EventHub-Namespace1-1375 -IPRule $IpRules -VirtualNteworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="66303-112">Name: standardmäßige Standard: Allow ID:/Subscriptions/SubscriptionId/ResourceGroups/ResourceGroup/Providers/Microsoft.EventHub/Namespaces/EventHub-Namespace-1122/networkRuleSets/default Typ: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, allow, 3.3.3.3, allow} VirtualNetworkRules: {/Subscriptions/SubscriptionId/ResourceGroups/ResourceGroup/Providers/Microsoft.Network/virtualNetworks/sbehvnettest1/Subnets/default; true}</span><span class="sxs-lookup"><span data-stu-id="66303-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="66303-113">Aktualisieren der NetworkRuleSet mit-IPRule und-VirtualNteworkRule-Parametern</span><span class="sxs-lookup"><span data-stu-id="66303-113">Update the NetworkRuleSet using -IPRule and -VirtualNteworkRule parameters</span></span>

### <span data-ttu-id="66303-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="66303-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="66303-115">Name: standardmäßige Standard: Allow ID:/Subscriptions/SubscriptionId/ResourceGroups/ResourceGroup/Providers/Microsoft.EventHub/Namespaces/EventHub-Namespace-1122/networkRuleSets/default Typ: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, allow, 3.3.3.3, allow} VirtualNetworkRules: {/Subscriptions/SubscriptionId/ResourceGroups/ResourceGroup/Providers/Microsoft.Network/virtualNetworks/sbehvnettest1/Subnets/default; true}</span><span class="sxs-lookup"><span data-stu-id="66303-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="66303-116">Aktualisieren der NetworkRuleSet mit-Inputobject</span><span class="sxs-lookup"><span data-stu-id="66303-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="66303-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="66303-117">Example 3</span></span>
```powershell
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375
```
<span data-ttu-id="66303-118">Name: standardmäßige Standard: Allow ID:/Subscriptions/SubscriptionId/ResourceGroups/ResourceGroup/Providers/Microsoft.EventHub/Namespaces/EventHub-Namespace-1122/networkRuleSets/default Typ: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, allow, 3.3.3.3, allow} VirtualNetworkRules: {/Subscriptions/SubscriptionId/ResourceGroups/ResourceGroup/Providers/Microsoft.Network/virtualNetworks/sbehvnettest1/Subnets/default; true}</span><span class="sxs-lookup"><span data-stu-id="66303-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="66303-119">Aktualisieren Sie die NetworkRuleSet mithilfe der-Resourcen-und der anderen Namespace.</span><span class="sxs-lookup"><span data-stu-id="66303-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="66303-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="66303-120">PARAMETERS</span></span>

### <span data-ttu-id="66303-121">– Standardmäßig</span><span class="sxs-lookup"><span data-stu-id="66303-121">-DefaultAction</span></span>
<span data-ttu-id="66303-122">Standardaktion für NetwrokeuleSet</span><span class="sxs-lookup"><span data-stu-id="66303-122">Default Action for NetwrokeuleSet</span></span>

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

### <span data-ttu-id="66303-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66303-123">-DefaultProfile</span></span>
<span data-ttu-id="66303-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="66303-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66303-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="66303-125">-InputObject</span></span>
<span data-ttu-id="66303-126">NetworkruleSet-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="66303-126">NetworkruleSet Configuration Object</span></span>

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

### <span data-ttu-id="66303-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="66303-127">-IPRule</span></span>
<span data-ttu-id="66303-128">Liste der IPRuleSet</span><span class="sxs-lookup"><span data-stu-id="66303-128">List of IPRuleSet</span></span>

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

### <span data-ttu-id="66303-129">-Name</span><span class="sxs-lookup"><span data-stu-id="66303-129">-Name</span></span>
<span data-ttu-id="66303-130">Name des EventHub-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="66303-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="66303-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66303-131">-ResourceGroupName</span></span>
<span data-ttu-id="66303-132">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="66303-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="66303-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="66303-133">-ResourceId</span></span>
<span data-ttu-id="66303-134">Ressourcen-ID des Namespaces</span><span class="sxs-lookup"><span data-stu-id="66303-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="66303-135">-VirtualNteworkRule</span><span class="sxs-lookup"><span data-stu-id="66303-135">-VirtualNteworkRule</span></span>
<span data-ttu-id="66303-136">Liste der VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="66303-136">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66303-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="66303-137">-Confirm</span></span>
<span data-ttu-id="66303-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66303-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66303-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66303-139">-WhatIf</span></span>
<span data-ttu-id="66303-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66303-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66303-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66303-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66303-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66303-142">CommonParameters</span></span>
<span data-ttu-id="66303-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66303-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="66303-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66303-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66303-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66303-145">INPUTS</span></span>

### <span data-ttu-id="66303-146">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="66303-146">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="66303-147">System. String</span><span class="sxs-lookup"><span data-stu-id="66303-147">System.String</span></span>

## <span data-ttu-id="66303-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66303-148">OUTPUTS</span></span>

### <span data-ttu-id="66303-149">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="66303-149">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="66303-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="66303-150">NOTES</span></span>

## <span data-ttu-id="66303-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66303-151">RELATED LINKS</span></span>