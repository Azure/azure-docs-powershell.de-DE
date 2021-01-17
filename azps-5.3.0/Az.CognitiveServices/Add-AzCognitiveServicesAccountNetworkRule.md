---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/add-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 039a3e4bf676f29d55f48e7e0883f5818e7367b7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470983"
---
# <span data-ttu-id="6ab20-101">Add-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6ab20-101">Add-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="6ab20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ab20-102">SYNOPSIS</span></span>
<span data-ttu-id="6ab20-103">Hinzufügen von IpRules oder VirtualNetworkRules zur Eigenschaft "NetworkRule" eines Cognitive Services-Kontos</span><span class="sxs-lookup"><span data-stu-id="6ab20-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="6ab20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ab20-104">SYNTAX</span></span>

### <span data-ttu-id="6ab20-105">NetWorkRuleString (Standard)</span><span class="sxs-lookup"><span data-stu-id="6ab20-105">NetWorkRuleString (Default)</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ab20-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="6ab20-106">IpRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IpRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ab20-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="6ab20-107">NetworkRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ab20-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="6ab20-108">IpRuleString</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ab20-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ab20-109">DESCRIPTION</span></span>
<span data-ttu-id="6ab20-110">Das **Cmdlet "Add-AzCognitiveServicesAccountNetworkRule"** fügt "IpRules" oder "VirtualNetworkRules" zur Eigenschaft "NetworkRule" eines Cognitive Services-Kontos hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ab20-110">The **Add-AzCognitiveServicesAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="6ab20-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6ab20-111">EXAMPLES</span></span>

### <span data-ttu-id="6ab20-112">Beispiel 1: Hinzufügen mehrerer IpRules mit "IpAddressOrRange"</span><span class="sxs-lookup"><span data-stu-id="6ab20-112">Example 1: Add several IpRules with IpAddressOrRange</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "200.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="6ab20-113">Mit diesem Befehl werden mehrere IpRules mit "IpAddressOrRange" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6ab20-113">This command add several IpRules with IpAddressOrRange.</span></span>

### <span data-ttu-id="6ab20-114">Beispiel 2: Hinzufügen einer VirtualNetworkRule mit VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="6ab20-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="6ab20-115">Mit diesem Befehl wird eine VirtualNetworkRule mit VirtualNetworkResourceID hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6ab20-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="6ab20-116">Beispiel 3: Hinzufügen von VirtualNetworkRules mit VirtualNetworkRule-Objekten aus einem anderen Konto</span><span class="sxs-lookup"><span data-stu-id="6ab20-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount1"
PS C:\> Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="6ab20-117">Mit diesem Befehl können Sie VirtualNetworkRules mit VirtualNetworkRule-Objekten aus einem anderen Konto hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6ab20-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="6ab20-118">Beispiel 4: Hinzufügen mehrerer IpRule mit IpRule-Objekten, Eingabe mit JSON</span><span class="sxs-lookup"><span data-stu-id="6ab20-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
```

<span data-ttu-id="6ab20-119">Mit diesem Befehl werden mehrere IpRule-Objekte mit JSON-Eingaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6ab20-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="6ab20-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ab20-120">PARAMETERS</span></span>

### <span data-ttu-id="6ab20-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab20-121">-DefaultProfile</span></span>
<span data-ttu-id="6ab20-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ab20-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ab20-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="6ab20-123">-IpAddressOrRange</span></span>
<span data-ttu-id="6ab20-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span><span class="sxs-lookup"><span data-stu-id="6ab20-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="6ab20-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="6ab20-125">-IpRule</span></span>
<span data-ttu-id="6ab20-126">Cognitive Services Account NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="6ab20-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="6ab20-127">-Name</span><span class="sxs-lookup"><span data-stu-id="6ab20-127">-Name</span></span>
<span data-ttu-id="6ab20-128">Name des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="6ab20-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="6ab20-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ab20-129">-ResourceGroupName</span></span>
<span data-ttu-id="6ab20-130">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="6ab20-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="6ab20-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="6ab20-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="6ab20-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6ab20-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="6ab20-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6ab20-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="6ab20-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="6ab20-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="6ab20-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ab20-135">-Confirm</span></span>
<span data-ttu-id="6ab20-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6ab20-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ab20-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6ab20-137">-WhatIf</span></span>
<span data-ttu-id="6ab20-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ab20-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ab20-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ab20-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ab20-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab20-140">CommonParameters</span></span>
<span data-ttu-id="6ab20-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ab20-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab20-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ab20-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab20-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6ab20-143">INPUTS</span></span>

### <span data-ttu-id="6ab20-144">System.String</span><span class="sxs-lookup"><span data-stu-id="6ab20-144">System.String</span></span>

### <span data-ttu-id="6ab20-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="6ab20-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="6ab20-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="6ab20-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="6ab20-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6ab20-147">OUTPUTS</span></span>

### <span data-ttu-id="6ab20-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6ab20-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="6ab20-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="6ab20-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="6ab20-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6ab20-150">NOTES</span></span>

## <span data-ttu-id="6ab20-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6ab20-151">RELATED LINKS</span></span>
