---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: d200d342bfa16fb0b2864e0196dc9648b4aa7fcd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659408"
---
# <span data-ttu-id="f84d7-101">Get-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f84d7-101">Get-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="f84d7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f84d7-102">SYNOPSIS</span></span>
<span data-ttu-id="f84d7-103">Ruft die Details eines Ereignis Hubs NetwrokruleSet des Namespaces im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="f84d7-103">Gets the details of an Event Hubs NetwrokruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="f84d7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f84d7-104">SYNTAX</span></span>

### <span data-ttu-id="f84d7-105">NetworkRuleSetPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f84d7-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f84d7-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="f84d7-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [[-ResourceGroupName] <String>] [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f84d7-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f84d7-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f84d7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f84d7-108">DESCRIPTION</span></span>
<span data-ttu-id="f84d7-109">Ruft die Details eines Ereignis Hubs NetwrokruleSet des Namespaces im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="f84d7-109">Gets the details of an Event Hubs NetwrokruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="f84d7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f84d7-110">EXAMPLES</span></span>

### <span data-ttu-id="f84d7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f84d7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="f84d7-112">Name: standardmäßige Standard-/Subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/Providers/Microsoft.ServiceBus/Namespaces/ServiceBus-Namespace-1122/networkRuleSets/default: Allow ID: Typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, allow} VirtualNetworkRules: {/Subscriptions/SubscriptionId/ResourceGroups/v-ajnavtest/Providers/Microsoft.Network/virtualNetworks/sbehvnettest1/Subnets/default; falsch}</span><span class="sxs-lookup"><span data-stu-id="f84d7-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="f84d7-113">Abrufen der Details von Ereignis Hubs NetwrokruleSet des Namespaces mithilfe von ResourceGroup-und Namesape-Parametern</span><span class="sxs-lookup"><span data-stu-id="f84d7-113">Get the details of Event Hubs NetwrokruleSet of namespace using ResourceGroup and Namesape parameters.</span></span> 

### <span data-ttu-id="f84d7-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f84d7-114">Example 2</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="f84d7-115">Name: standardmäßige Standard-/Subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/Providers/Microsoft.ServiceBus/Namespaces/ServiceBus-Namespace-1122/networkRuleSets/default: Allow ID: Typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, allow} VirtualNetworkRules: {/Subscriptions/SubscriptionId/ResourceGroups/v-ajnavtest/Providers/Microsoft.Network/virtualNetworks/sbehvnettest1/Subnets/default; falsch}</span><span class="sxs-lookup"><span data-stu-id="f84d7-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="f84d7-116">Rufen Sie die Details der Ereignis Hubs NetwrokruleSet des Namespaces mit Namespace ab, der im aktuellen Abonnement enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="f84d7-116">Get the details of Event Hubs NetwrokruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="f84d7-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f84d7-117">Example 3</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389
```

<span data-ttu-id="f84d7-118">Name: standardmäßige Standard-/Subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/Providers/Microsoft.ServiceBus/Namespaces/ServiceBus-Namespace-2389/networkRuleSets/default: Allow ID: Typ: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, allow} VirtualNetworkRules: {/Subscriptions/SubscriptionId/ResourceGroups/v-ajnavtest/Providers/Microsoft.Network/virtualNetworks/sbehvnettest1/Subnets/default; falsch}</span><span class="sxs-lookup"><span data-stu-id="f84d7-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="f84d7-119">Abrufen der Details von Ereignis Hubs NetwrokruleSet des Namespaces mithilfe der Ressourcen-ID eines anderen Namespaces</span><span class="sxs-lookup"><span data-stu-id="f84d7-119">Get the details of Event Hubs NetwrokruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="f84d7-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="f84d7-120">PARAMETERS</span></span>

### <span data-ttu-id="f84d7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f84d7-121">-DefaultProfile</span></span>
<span data-ttu-id="f84d7-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f84d7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f84d7-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f84d7-123">-Namespace</span></span>
<span data-ttu-id="f84d7-124">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="f84d7-124">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet, NetworkRuleSetNamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f84d7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f84d7-125">-ResourceGroupName</span></span>
<span data-ttu-id="f84d7-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="f84d7-126">Resource Group Name</span></span>

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

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetNamespacePropertiesSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f84d7-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f84d7-127">-ResourceId</span></span>
<span data-ttu-id="f84d7-128">Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="f84d7-128">Namespace Resource Id</span></span>

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

### <span data-ttu-id="f84d7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f84d7-129">CommonParameters</span></span>
<span data-ttu-id="f84d7-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f84d7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f84d7-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f84d7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f84d7-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f84d7-132">INPUTS</span></span>

### <span data-ttu-id="f84d7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f84d7-133">System.String</span></span>

## <span data-ttu-id="f84d7-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f84d7-134">OUTPUTS</span></span>

### <span data-ttu-id="f84d7-135">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="f84d7-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="f84d7-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="f84d7-136">NOTES</span></span>

## <span data-ttu-id="f84d7-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f84d7-137">RELATED LINKS</span></span>