---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 68aa2d4d0d5ba29cdb2c8ddf86d49c6be1280c88
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469836"
---
# <span data-ttu-id="8e3fa-101">Remove-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8e3fa-101">Remove-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="8e3fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e3fa-102">SYNOPSIS</span></span>
<span data-ttu-id="8e3fa-103">Entfernt die einzelne angegebene VirtualNetworkRule für das NetworkRuleSet des Namespace.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="8e3fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e3fa-104">SYNTAX</span></span>

### <span data-ttu-id="8e3fa-105">VirtualNetworkRulePropertiesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e3fa-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e3fa-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e3fa-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e3fa-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e3fa-107">DESCRIPTION</span></span>
<span data-ttu-id="8e3fa-108">Entfernt die einzelne angegebene VirtualNetworkRule für das NetworkRuleSet des Namespace.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="8e3fa-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8e3fa-109">EXAMPLES</span></span>

### <span data-ttu-id="8e3fa-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8e3fa-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="8e3fa-111">Entfernt die einzelne angegebene VirtualNetworkRule für das NetworkRuleSet des Namespace.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="8e3fa-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8e3fa-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="8e3fa-113">Entfernen der $virtualruleset 1 von NetworkRuleSet für den angegebenen Namespace</span><span class="sxs-lookup"><span data-stu-id="8e3fa-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="8e3fa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e3fa-114">PARAMETERS</span></span>

### <span data-ttu-id="8e3fa-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e3fa-115">-AsJob</span></span>
<span data-ttu-id="8e3fa-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8e3fa-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e3fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e3fa-117">-DefaultProfile</span></span>
<span data-ttu-id="8e3fa-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e3fa-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8e3fa-119">-Name</span></span>
<span data-ttu-id="8e3fa-120">Namespacename</span><span class="sxs-lookup"><span data-stu-id="8e3fa-120">Namespace Name</span></span>

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

### <span data-ttu-id="8e3fa-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e3fa-121">-PassThru</span></span>
<span data-ttu-id="8e3fa-122">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8e3fa-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8e3fa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e3fa-123">-ResourceGroupName</span></span>
<span data-ttu-id="8e3fa-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="8e3fa-124">Resource Group Name</span></span>

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

### <span data-ttu-id="8e3fa-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8e3fa-125">-SubnetId</span></span>
<span data-ttu-id="8e3fa-126">Subnetzressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="8e3fa-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="8e3fa-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="8e3fa-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="8e3fa-128">IPRule Configuration Object</span><span class="sxs-lookup"><span data-stu-id="8e3fa-128">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="8e3fa-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e3fa-129">-Confirm</span></span>
<span data-ttu-id="8e3fa-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e3fa-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8e3fa-131">-WhatIf</span></span>
<span data-ttu-id="8e3fa-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e3fa-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e3fa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e3fa-134">CommonParameters</span></span>
<span data-ttu-id="8e3fa-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e3fa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8e3fa-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e3fa-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e3fa-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8e3fa-137">INPUTS</span></span>

### <span data-ttu-id="8e3fa-138">System.String</span><span class="sxs-lookup"><span data-stu-id="8e3fa-138">System.String</span></span>

### <span data-ttu-id="8e3fa-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="8e3fa-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="8e3fa-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8e3fa-140">OUTPUTS</span></span>

### <span data-ttu-id="8e3fa-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="8e3fa-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="8e3fa-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8e3fa-142">NOTES</span></span>

## <span data-ttu-id="8e3fa-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8e3fa-143">RELATED LINKS</span></span>