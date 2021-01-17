---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 2faf890cda0c87d15704a14f9c4ae12c5b3d81c2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473166"
---
# <span data-ttu-id="f9249-101">Remove-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f9249-101">Remove-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="f9249-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9249-102">SYNOPSIS</span></span>
<span data-ttu-id="f9249-103">Entfernen von IpRules oder VirtualNetworkRules aus der Eigenschaft "NetWorkRule" eines Cognitive Services-Kontos</span><span class="sxs-lookup"><span data-stu-id="f9249-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="f9249-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9249-104">SYNTAX</span></span>

### <span data-ttu-id="f9249-105">NetWorkRuleString (Standard)</span><span class="sxs-lookup"><span data-stu-id="f9249-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9249-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="f9249-106">IpRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpRule <PSIpRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9249-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="f9249-107">NetworkRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9249-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="f9249-108">IpRuleString</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9249-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9249-109">DESCRIPTION</span></span>
<span data-ttu-id="f9249-110">Das **Cmdlet "Remove-AzCognitiveServicesAccountNetworkRule"** entfernt "IpRules" oder "VirtualNetworkRules" aus der Eigenschaft "NetWorkRule" eines Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="f9249-110">The **Remove-AzCognitiveServicesAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="f9249-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f9249-111">EXAMPLES</span></span>

### <span data-ttu-id="f9249-112">Beispiel 1: Entfernen mehrerer IpRules mit IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="f9249-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="f9249-113">Mit diesem Befehl werden mehrere IpRules mit "IPAddressOrRange" entfernt.</span><span class="sxs-lookup"><span data-stu-id="f9249-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="f9249-114">Beispiel 2: Entfernen einer VirtualNetworkRule mit VirtualNetworkRule-Objekteingabe mit JSON</span><span class="sxs-lookup"><span data-stu-id="f9249-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"})
```

<span data-ttu-id="f9249-115">Mit diesem Befehl wird eine VirtualNetworkRule mit einer VirtualNetworkRule-Objekteingabe mit JSON entfernt.</span><span class="sxs-lookup"><span data-stu-id="f9249-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="f9249-116">Beispiel 3: Entfernen der ersten IpRule mit Pipeline</span><span class="sxs-lookup"><span data-stu-id="f9249-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount").IpRules[0] | Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="f9249-117">Mit diesem Befehl wird die erste IpRule mit Pipeline entfernt.</span><span class="sxs-lookup"><span data-stu-id="f9249-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="f9249-118">Beispiel 4: Entfernen mehrerer VirtualNetworkRules mit VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="f9249-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="f9249-119">Mit diesem Befehl werden mehrere VirtualNetworkRules mit VirtualNetworkResourceID entfernt.</span><span class="sxs-lookup"><span data-stu-id="f9249-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span> 

## <span data-ttu-id="f9249-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9249-120">PARAMETERS</span></span>

### <span data-ttu-id="f9249-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9249-121">-DefaultProfile</span></span>
<span data-ttu-id="f9249-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f9249-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9249-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="f9249-123">-IpAddressOrRange</span></span>
<span data-ttu-id="f9249-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span><span class="sxs-lookup"><span data-stu-id="f9249-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IpRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9249-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="f9249-125">-IpRule</span></span>
<span data-ttu-id="f9249-126">Cognitive Services Account NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="f9249-126">Cognitive Services Account NetworkRule IpRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9249-127">-Name</span><span class="sxs-lookup"><span data-stu-id="f9249-127">-Name</span></span>
<span data-ttu-id="f9249-128">Name des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="f9249-128">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9249-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9249-129">-ResourceGroupName</span></span>
<span data-ttu-id="f9249-130">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="f9249-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="f9249-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="f9249-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="f9249-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f9249-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9249-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f9249-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="f9249-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="f9249-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9249-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9249-135">-Confirm</span></span>
<span data-ttu-id="f9249-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f9249-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9249-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f9249-137">-WhatIf</span></span>
<span data-ttu-id="f9249-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9249-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9249-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9249-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9249-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9249-140">CommonParameters</span></span>
<span data-ttu-id="f9249-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9249-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9249-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9249-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9249-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f9249-143">INPUTS</span></span>

### <span data-ttu-id="f9249-144">System.String</span><span class="sxs-lookup"><span data-stu-id="f9249-144">System.String</span></span>

### <span data-ttu-id="f9249-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="f9249-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="f9249-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="f9249-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="f9249-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f9249-147">OUTPUTS</span></span>

### <span data-ttu-id="f9249-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f9249-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="f9249-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="f9249-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="f9249-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f9249-150">NOTES</span></span>

## <span data-ttu-id="f9249-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f9249-151">RELATED LINKS</span></span>
