---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 6c803f399bf88c6e4887441ec9f9bd50c058361b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007819"
---
# <span data-ttu-id="3439c-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="3439c-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="3439c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3439c-102">SYNOPSIS</span></span>
<span data-ttu-id="3439c-103">Entfernt die NetworkRuleSet für den angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="3439c-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="3439c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3439c-104">SYNTAX</span></span>

### <span data-ttu-id="3439c-105">NetworkRuleSetPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3439c-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3439c-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3439c-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3439c-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3439c-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3439c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3439c-108">DESCRIPTION</span></span>
<span data-ttu-id="3439c-109">Entfernt die NetworkRuleSet für den angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="3439c-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="3439c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3439c-110">EXAMPLES</span></span>

### <span data-ttu-id="3439c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3439c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="3439c-112">Name: standardmäßige Standardeinstellung: Allow ID:/Subscriptions/SubscriptionId/resourceGroups/ResourceGroup/Providers/Microsoft.ServiceBus/Namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="3439c-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="3439c-113">Löscht die NetworkRuleSet für den angegebenen Namespace "ServiceBus-Namespace1-1375"</span><span class="sxs-lookup"><span data-stu-id="3439c-113">Deletes the NetworkRuleSet for the Given "ServiceBus-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="3439c-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3439c-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="3439c-115">Name: standardmäßige Standardeinstellung: Allow ID:/Subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/Providers/Microsoft.EventHub/Namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="3439c-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="3439c-116">Löscht die NetworkRuleSet mit Inputobject</span><span class="sxs-lookup"><span data-stu-id="3439c-116">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="3439c-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="3439c-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="3439c-118">Name: standardmäßige Standardeinstellung: Allow ID:/Subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/Providers/Microsoft.EventHub/Namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="3439c-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="3439c-119">Löscht die NetworkRuleSet mit der "Resourcen-Nr" des Namespaces.</span><span class="sxs-lookup"><span data-stu-id="3439c-119">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="3439c-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="3439c-120">PARAMETERS</span></span>

### <span data-ttu-id="3439c-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3439c-121">-AsJob</span></span>
<span data-ttu-id="3439c-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3439c-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3439c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3439c-123">-DefaultProfile</span></span>
<span data-ttu-id="3439c-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3439c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3439c-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3439c-125">-InputObject</span></span>
<span data-ttu-id="3439c-126">Namespace-Objekt</span><span class="sxs-lookup"><span data-stu-id="3439c-126">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3439c-127">-Name</span><span class="sxs-lookup"><span data-stu-id="3439c-127">-Name</span></span>
<span data-ttu-id="3439c-128">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="3439c-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3439c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3439c-129">-PassThru</span></span>
<span data-ttu-id="3439c-130">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="3439c-130">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3439c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3439c-131">-ResourceGroupName</span></span>
<span data-ttu-id="3439c-132">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="3439c-132">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3439c-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3439c-133">-ResourceId</span></span>
<span data-ttu-id="3439c-134">Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="3439c-134">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3439c-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3439c-135">-Confirm</span></span>
<span data-ttu-id="3439c-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3439c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3439c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3439c-137">-WhatIf</span></span>
<span data-ttu-id="3439c-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3439c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3439c-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3439c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3439c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3439c-140">CommonParameters</span></span>
<span data-ttu-id="3439c-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3439c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3439c-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3439c-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3439c-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3439c-143">INPUTS</span></span>

### <span data-ttu-id="3439c-144">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="3439c-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="3439c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="3439c-145">System.String</span></span>

## <span data-ttu-id="3439c-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3439c-146">OUTPUTS</span></span>

### <span data-ttu-id="3439c-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3439c-147">System.Boolean</span></span>

## <span data-ttu-id="3439c-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="3439c-148">NOTES</span></span>

## <span data-ttu-id="3439c-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3439c-149">RELATED LINKS</span></span>
