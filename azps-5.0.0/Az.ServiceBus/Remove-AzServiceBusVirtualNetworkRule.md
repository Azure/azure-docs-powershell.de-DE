---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
ms.openlocfilehash: d72c7e1ebfdd7543740ea8fafeb62861f4394093
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302427"
---
# <span data-ttu-id="298a5-101">Remove-AzServiceBusVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="298a5-101">Remove-AzServiceBusVirtualNetworkRule</span></span>

## <span data-ttu-id="298a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="298a5-102">SYNOPSIS</span></span>
<span data-ttu-id="298a5-103">Entfernt den einzelnen angegebenen VirtualNetworkRule für die NetworkRuleSet des Namespaces.</span><span class="sxs-lookup"><span data-stu-id="298a5-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="298a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="298a5-104">SYNTAX</span></span>

### <span data-ttu-id="298a5-105">VirtualNetworkRulePropertiesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="298a5-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="298a5-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="298a5-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="298a5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="298a5-107">DESCRIPTION</span></span>
<span data-ttu-id="298a5-108">Entfernt den einzelnen angegebenen VirtualNetworkRule für die NetworkRuleSet des Namespaces.</span><span class="sxs-lookup"><span data-stu-id="298a5-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="298a5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="298a5-109">EXAMPLES</span></span>

### <span data-ttu-id="298a5-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="298a5-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="298a5-111">Entfernt den einzelnen angegebenen VirtualNetworkRule für die NetworkRuleSet des Namespaces.</span><span class="sxs-lookup"><span data-stu-id="298a5-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="298a5-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="298a5-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="298a5-113">Entfernen des $virtualruleset 1 von NetworkRuleSet für den angegebenen Namespace</span><span class="sxs-lookup"><span data-stu-id="298a5-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="298a5-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="298a5-114">PARAMETERS</span></span>

### <span data-ttu-id="298a5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="298a5-115">-AsJob</span></span>
<span data-ttu-id="298a5-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="298a5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="298a5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="298a5-117">-DefaultProfile</span></span>
<span data-ttu-id="298a5-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="298a5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="298a5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="298a5-119">-Name</span></span>
<span data-ttu-id="298a5-120">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="298a5-120">Namespace Name</span></span>

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

### <span data-ttu-id="298a5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="298a5-121">-PassThru</span></span>
<span data-ttu-id="298a5-122">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="298a5-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="298a5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="298a5-123">-ResourceGroupName</span></span>
<span data-ttu-id="298a5-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="298a5-124">Resource Group Name</span></span>

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

### <span data-ttu-id="298a5-125">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="298a5-125">-SubnetId</span></span>
<span data-ttu-id="298a5-126">Subnet-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="298a5-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="298a5-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="298a5-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="298a5-128">IPRule-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="298a5-128">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="298a5-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="298a5-129">-Confirm</span></span>
<span data-ttu-id="298a5-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="298a5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="298a5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="298a5-131">-WhatIf</span></span>
<span data-ttu-id="298a5-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="298a5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="298a5-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="298a5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="298a5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="298a5-134">CommonParameters</span></span>
<span data-ttu-id="298a5-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="298a5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="298a5-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="298a5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="298a5-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="298a5-137">INPUTS</span></span>

### <span data-ttu-id="298a5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="298a5-138">System.String</span></span>

### <span data-ttu-id="298a5-139">Microsoft. Azure. Commands. ServiceBus. Models. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="298a5-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="298a5-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="298a5-140">OUTPUTS</span></span>

### <span data-ttu-id="298a5-141">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="298a5-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="298a5-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="298a5-142">NOTES</span></span>

## <span data-ttu-id="298a5-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="298a5-143">RELATED LINKS</span></span>
