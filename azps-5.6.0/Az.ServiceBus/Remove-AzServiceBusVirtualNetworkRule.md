---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
ms.openlocfilehash: eb04f3db26b7601b715369d695b21a234f2feb25
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945694"
---
# <span data-ttu-id="39289-101">Remove-AzServiceBusVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="39289-101">Remove-AzServiceBusVirtualNetworkRule</span></span>

## <span data-ttu-id="39289-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39289-102">SYNOPSIS</span></span>
<span data-ttu-id="39289-103">Entfernt die einzelne angegebene VirtualNetworkRule für das NetworkRuleSet des Namespaces.</span><span class="sxs-lookup"><span data-stu-id="39289-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="39289-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39289-104">SYNTAX</span></span>

### <span data-ttu-id="39289-105">VirtualNetworkRulePropertiesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="39289-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39289-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39289-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39289-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39289-107">DESCRIPTION</span></span>
<span data-ttu-id="39289-108">Entfernt die einzelne angegebene VirtualNetworkRule für das NetworkRuleSet des Namespaces.</span><span class="sxs-lookup"><span data-stu-id="39289-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="39289-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="39289-109">EXAMPLES</span></span>

### <span data-ttu-id="39289-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="39289-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="39289-111">Entfernt die einzelne angegebene VirtualNetworkRule für das NetworkRuleSet des Namespaces.</span><span class="sxs-lookup"><span data-stu-id="39289-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="39289-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="39289-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="39289-113">Entfernen des $virtualruleset 1 von NetworkRuleSet für den angegebenen Namespace</span><span class="sxs-lookup"><span data-stu-id="39289-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="39289-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="39289-114">PARAMETERS</span></span>

### <span data-ttu-id="39289-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39289-115">-AsJob</span></span>
<span data-ttu-id="39289-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="39289-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39289-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39289-117">-DefaultProfile</span></span>
<span data-ttu-id="39289-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39289-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39289-119">-Name</span><span class="sxs-lookup"><span data-stu-id="39289-119">-Name</span></span>
<span data-ttu-id="39289-120">Namespacename</span><span class="sxs-lookup"><span data-stu-id="39289-120">Namespace Name</span></span>

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

### <span data-ttu-id="39289-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39289-121">-PassThru</span></span>
<span data-ttu-id="39289-122">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="39289-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="39289-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39289-123">-ResourceGroupName</span></span>
<span data-ttu-id="39289-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="39289-124">Resource Group Name</span></span>

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

### <span data-ttu-id="39289-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="39289-125">-SubnetId</span></span>
<span data-ttu-id="39289-126">Subnetzressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="39289-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="39289-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="39289-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="39289-128">IPRule Configuration Object</span><span class="sxs-lookup"><span data-stu-id="39289-128">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="39289-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="39289-129">-Confirm</span></span>
<span data-ttu-id="39289-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39289-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39289-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39289-131">-WhatIf</span></span>
<span data-ttu-id="39289-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39289-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39289-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39289-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39289-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39289-134">CommonParameters</span></span>
<span data-ttu-id="39289-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39289-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="39289-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39289-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39289-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="39289-137">INPUTS</span></span>

### <span data-ttu-id="39289-138">System.String</span><span class="sxs-lookup"><span data-stu-id="39289-138">System.String</span></span>

### <span data-ttu-id="39289-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="39289-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="39289-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="39289-140">OUTPUTS</span></span>

### <span data-ttu-id="39289-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="39289-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="39289-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="39289-142">NOTES</span></span>

## <span data-ttu-id="39289-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="39289-143">RELATED LINKS</span></span>
