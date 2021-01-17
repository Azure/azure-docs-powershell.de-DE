---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 68aa2d4d0d5ba29cdb2c8ddf86d49c6be1280c88
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306507"
---
# <span data-ttu-id="1afc2-101">Remove-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1afc2-101">Remove-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="1afc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1afc2-102">SYNOPSIS</span></span>
<span data-ttu-id="1afc2-103">Entfernt die einzelne angegebene VirtualNetworkRule für das NetworkRuleSet des Namespace.</span><span class="sxs-lookup"><span data-stu-id="1afc2-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="1afc2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1afc2-104">SYNTAX</span></span>

### <span data-ttu-id="1afc2-105">VirtualNetworkRulePropertiesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1afc2-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1afc2-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1afc2-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1afc2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1afc2-107">DESCRIPTION</span></span>
<span data-ttu-id="1afc2-108">Entfernt die einzelne angegebene VirtualNetworkRule für das NetworkRuleSet des Namespace.</span><span class="sxs-lookup"><span data-stu-id="1afc2-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="1afc2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1afc2-109">EXAMPLES</span></span>

### <span data-ttu-id="1afc2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1afc2-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="1afc2-111">Entfernt die einzelne angegebene VirtualNetworkRule für das NetworkRuleSet des Namespace.</span><span class="sxs-lookup"><span data-stu-id="1afc2-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="1afc2-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1afc2-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="1afc2-113">Entfernen der $virtualruleset 1 von NetworkRuleSet für den angegebenen Namespace</span><span class="sxs-lookup"><span data-stu-id="1afc2-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="1afc2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1afc2-114">PARAMETERS</span></span>

### <span data-ttu-id="1afc2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1afc2-115">-AsJob</span></span>
<span data-ttu-id="1afc2-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1afc2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1afc2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1afc2-117">-DefaultProfile</span></span>
<span data-ttu-id="1afc2-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1afc2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1afc2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1afc2-119">-Name</span></span>
<span data-ttu-id="1afc2-120">Namespacename</span><span class="sxs-lookup"><span data-stu-id="1afc2-120">Namespace Name</span></span>

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

### <span data-ttu-id="1afc2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1afc2-121">-PassThru</span></span>
<span data-ttu-id="1afc2-122">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1afc2-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1afc2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1afc2-123">-ResourceGroupName</span></span>
<span data-ttu-id="1afc2-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="1afc2-124">Resource Group Name</span></span>

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

### <span data-ttu-id="1afc2-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="1afc2-125">-SubnetId</span></span>
<span data-ttu-id="1afc2-126">Subnetzressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="1afc2-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="1afc2-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="1afc2-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="1afc2-128">IPRule Configuration Object</span><span class="sxs-lookup"><span data-stu-id="1afc2-128">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="1afc2-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1afc2-129">-Confirm</span></span>
<span data-ttu-id="1afc2-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1afc2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1afc2-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1afc2-131">-WhatIf</span></span>
<span data-ttu-id="1afc2-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1afc2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1afc2-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1afc2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1afc2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1afc2-134">CommonParameters</span></span>
<span data-ttu-id="1afc2-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1afc2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1afc2-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1afc2-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1afc2-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1afc2-137">INPUTS</span></span>

### <span data-ttu-id="1afc2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1afc2-138">System.String</span></span>

### <span data-ttu-id="1afc2-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="1afc2-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="1afc2-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1afc2-140">OUTPUTS</span></span>

### <span data-ttu-id="1afc2-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="1afc2-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="1afc2-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1afc2-142">NOTES</span></span>

## <span data-ttu-id="1afc2-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1afc2-143">RELATED LINKS</span></span>