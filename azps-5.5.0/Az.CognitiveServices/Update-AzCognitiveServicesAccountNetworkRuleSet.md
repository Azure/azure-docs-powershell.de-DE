---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/update-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 0f094ba8bdfa8dbf40f2af8495ee2f8cfa6fca16
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171324"
---
# <span data-ttu-id="1014e-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1014e-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="1014e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1014e-102">SYNOPSIS</span></span>
<span data-ttu-id="1014e-103">Aktualisieren der Eigenschaft "NetworkRule" eines Cognitive Services-Kontos</span><span class="sxs-lookup"><span data-stu-id="1014e-103">Update the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="1014e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1014e-104">SYNTAX</span></span>

```
Update-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IpRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1014e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1014e-105">DESCRIPTION</span></span>
<span data-ttu-id="1014e-106">Das **Cmdlet "Update-AzCognitiveServicesAccountNetworkRuleSet"** aktualisiert die Eigenschaft "NetworkRule" eines Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="1014e-106">The **Update-AzCognitiveServicesAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="1014e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1014e-107">EXAMPLES</span></span>

### <span data-ttu-id="1014e-108">Beispiel 1: Aktualisieren aller Eigenschaften von NetworkRule, Eingaberegeln mit JSON</span><span class="sxs-lookup"><span data-stu-id="1014e-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -DefaultAction Allow -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2"})
```

<span data-ttu-id="1014e-109">Mit diesem Befehl werden alle Eigenschaften von NetworkRule und Eingaberegeln mit JSON aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1014e-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="1014e-110">Beispiel 2: Aktualisieren der Umgehungseigenschaft von NetworkRule</span><span class="sxs-lookup"><span data-stu-id="1014e-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="1014e-111">Mit diesem Befehl wird die Umgehungseigenschaft von NetworkRule aktualisiert (andere Eigenschaften werden nicht geändert).</span><span class="sxs-lookup"><span data-stu-id="1014e-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="1014e-112">Beispiel 3: Bereinigen von Regeln von "NetworkRule" eines Cognitive Services-Kontos</span><span class="sxs-lookup"><span data-stu-id="1014e-112">Example 3: Clean up rules of NetworkRule of a Cognitive Services account</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="1014e-113">Dieser Befehl bereinigt Regeln von NetworkRule eines Cognitive Services-Kontos (andere Eigenschaften ändern sich nicht).</span><span class="sxs-lookup"><span data-stu-id="1014e-113">This command clean up rules of NetworkRule of a Cognitive Services account (other properties not change).</span></span>

## <span data-ttu-id="1014e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1014e-114">PARAMETERS</span></span>

### <span data-ttu-id="1014e-115">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="1014e-115">-DefaultAction</span></span>
<span data-ttu-id="1014e-116">Cognitive Services Account NetworkRule DefaultAction.</span><span class="sxs-lookup"><span data-stu-id="1014e-116">Cognitive Services Account NetworkRule DefaultAction.</span></span> <span data-ttu-id="1014e-117">Standardwert. `Deny`</span><span class="sxs-lookup"><span data-stu-id="1014e-117">Default value `Deny`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1014e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1014e-118">-DefaultProfile</span></span>
<span data-ttu-id="1014e-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1014e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1014e-120">-IpRule</span><span class="sxs-lookup"><span data-stu-id="1014e-120">-IpRule</span></span>
<span data-ttu-id="1014e-121">Cognitive Services Account NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="1014e-121">Cognitive Services Account NetworkRule IpRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1014e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1014e-122">-Name</span></span>
<span data-ttu-id="1014e-123">Name des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="1014e-123">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="1014e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1014e-124">-ResourceGroupName</span></span>
<span data-ttu-id="1014e-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="1014e-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="1014e-126">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1014e-126">-VirtualNetworkRule</span></span>
<span data-ttu-id="1014e-127">Cognitive Services Account NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="1014e-127">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1014e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1014e-128">-Confirm</span></span>
<span data-ttu-id="1014e-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1014e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1014e-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1014e-130">-WhatIf</span></span>
<span data-ttu-id="1014e-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1014e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1014e-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1014e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1014e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1014e-133">CommonParameters</span></span>
<span data-ttu-id="1014e-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1014e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1014e-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1014e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1014e-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1014e-136">INPUTS</span></span>

### <span data-ttu-id="1014e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="1014e-137">System.String</span></span>

### <span data-ttu-id="1014e-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="1014e-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="1014e-139">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="1014e-139">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="1014e-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1014e-140">OUTPUTS</span></span>

### <span data-ttu-id="1014e-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1014e-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="1014e-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1014e-142">NOTES</span></span>

## <span data-ttu-id="1014e-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1014e-143">RELATED LINKS</span></span>
