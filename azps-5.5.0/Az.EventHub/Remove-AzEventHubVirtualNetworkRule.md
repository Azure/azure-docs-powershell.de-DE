---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 68aa2d4d0d5ba29cdb2c8ddf86d49c6be1280c88
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167596"
---
# <span data-ttu-id="2d68f-101">Remove-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2d68f-101">Remove-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="2d68f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d68f-102">SYNOPSIS</span></span>
<span data-ttu-id="2d68f-103">Entfernt die einzelne angegebene VirtualNetworkRule für das NetworkRuleSet des Namespace.</span><span class="sxs-lookup"><span data-stu-id="2d68f-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="2d68f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d68f-104">SYNTAX</span></span>

### <span data-ttu-id="2d68f-105">VirtualNetworkRulePropertiesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d68f-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d68f-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d68f-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d68f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d68f-107">DESCRIPTION</span></span>
<span data-ttu-id="2d68f-108">Entfernt die einzelne angegebene VirtualNetworkRule für das NetworkRuleSet des Namespace.</span><span class="sxs-lookup"><span data-stu-id="2d68f-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="2d68f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2d68f-109">EXAMPLES</span></span>

### <span data-ttu-id="2d68f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2d68f-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="2d68f-111">Entfernt die einzelne angegebene VirtualNetworkRule für das NetworkRuleSet des Namespace.</span><span class="sxs-lookup"><span data-stu-id="2d68f-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="2d68f-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2d68f-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="2d68f-113">Entfernen der $virtualruleset 1 von NetworkRuleSet für den angegebenen Namespace</span><span class="sxs-lookup"><span data-stu-id="2d68f-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="2d68f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d68f-114">PARAMETERS</span></span>

### <span data-ttu-id="2d68f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d68f-115">-AsJob</span></span>
<span data-ttu-id="2d68f-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2d68f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d68f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d68f-117">-DefaultProfile</span></span>
<span data-ttu-id="2d68f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d68f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d68f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2d68f-119">-Name</span></span>
<span data-ttu-id="2d68f-120">Namespacename</span><span class="sxs-lookup"><span data-stu-id="2d68f-120">Namespace Name</span></span>

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

### <span data-ttu-id="2d68f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d68f-121">-PassThru</span></span>
<span data-ttu-id="2d68f-122">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2d68f-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2d68f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d68f-123">-ResourceGroupName</span></span>
<span data-ttu-id="2d68f-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="2d68f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="2d68f-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="2d68f-125">-SubnetId</span></span>
<span data-ttu-id="2d68f-126">Subnetzressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="2d68f-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="2d68f-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="2d68f-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="2d68f-128">IPRule Configuration Object</span><span class="sxs-lookup"><span data-stu-id="2d68f-128">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="2d68f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d68f-129">-Confirm</span></span>
<span data-ttu-id="2d68f-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d68f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d68f-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2d68f-131">-WhatIf</span></span>
<span data-ttu-id="2d68f-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d68f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d68f-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d68f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d68f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d68f-134">CommonParameters</span></span>
<span data-ttu-id="2d68f-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d68f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2d68f-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d68f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d68f-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2d68f-137">INPUTS</span></span>

### <span data-ttu-id="2d68f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2d68f-138">System.String</span></span>

### <span data-ttu-id="2d68f-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="2d68f-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="2d68f-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2d68f-140">OUTPUTS</span></span>

### <span data-ttu-id="2d68f-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="2d68f-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="2d68f-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2d68f-142">NOTES</span></span>

## <span data-ttu-id="2d68f-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2d68f-143">RELATED LINKS</span></span>