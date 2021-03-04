---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/update-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 4c5cd8caef4499d8d603b1947c1fa1dd8a9d5cf6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931408"
---
# <span data-ttu-id="0f9d0-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0f9d0-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="0f9d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f9d0-102">SYNOPSIS</span></span>
<span data-ttu-id="0f9d0-103">Aktualisieren der NetworkRule-Eigenschaft eines Cognitive Services-Kontos</span><span class="sxs-lookup"><span data-stu-id="0f9d0-103">Update the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="0f9d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f9d0-104">SYNTAX</span></span>

```
Update-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IpRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f9d0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f9d0-105">DESCRIPTION</span></span>
<span data-ttu-id="0f9d0-106">Das **Cmdlet Update-AzCognitiveServicesAccountNetworkRuleSet** aktualisiert die NetworkRule-Eigenschaft eines Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="0f9d0-106">The **Update-AzCognitiveServicesAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="0f9d0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0f9d0-107">EXAMPLES</span></span>

### <span data-ttu-id="0f9d0-108">Beispiel 1: Aktualisieren aller Eigenschaften von NetworkRule, Eingaberegeln mit JSON</span><span class="sxs-lookup"><span data-stu-id="0f9d0-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -DefaultAction Allow -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2"})
```

<span data-ttu-id="0f9d0-109">Dieser Befehl aktualisiert alle Eigenschaften von NetworkRule, Eingaberegeln mit JSON.</span><span class="sxs-lookup"><span data-stu-id="0f9d0-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="0f9d0-110">Beispiel 2: Update Bypass-Eigenschaft von NetworkRule</span><span class="sxs-lookup"><span data-stu-id="0f9d0-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="0f9d0-111">Dieses Befehlsupdate Umgehen der Eigenschaft von NetworkRule (andere Eigenschaften werden nicht geändert).</span><span class="sxs-lookup"><span data-stu-id="0f9d0-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="0f9d0-112">Beispiel 3: Bereinigen von Regeln für NetworkRule eines Cognitive Services-Kontos</span><span class="sxs-lookup"><span data-stu-id="0f9d0-112">Example 3: Clean up rules of NetworkRule of a Cognitive Services account</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="0f9d0-113">Mit diesem Befehl werden Regeln von NetworkRule eines Cognitive Services-Kontos bereinigt (andere Eigenschaften werden nicht geändert).</span><span class="sxs-lookup"><span data-stu-id="0f9d0-113">This command clean up rules of NetworkRule of a Cognitive Services account (other properties not change).</span></span>

## <span data-ttu-id="0f9d0-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0f9d0-114">PARAMETERS</span></span>

### <span data-ttu-id="0f9d0-115">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="0f9d0-115">-DefaultAction</span></span>
<span data-ttu-id="0f9d0-116">Cognitive Services Account NetworkRule DefaultAction.</span><span class="sxs-lookup"><span data-stu-id="0f9d0-116">Cognitive Services Account NetworkRule DefaultAction.</span></span> <span data-ttu-id="0f9d0-117">Standardwert `Deny` .</span><span class="sxs-lookup"><span data-stu-id="0f9d0-117">Default value `Deny`.</span></span>

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

### <span data-ttu-id="0f9d0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f9d0-118">-DefaultProfile</span></span>
<span data-ttu-id="0f9d0-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0f9d0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f9d0-120">-IpRule</span><span class="sxs-lookup"><span data-stu-id="0f9d0-120">-IpRule</span></span>
<span data-ttu-id="0f9d0-121">Cognitive Services Account NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="0f9d0-121">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="0f9d0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0f9d0-122">-Name</span></span>
<span data-ttu-id="0f9d0-123">Name des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="0f9d0-123">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="0f9d0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f9d0-124">-ResourceGroupName</span></span>
<span data-ttu-id="0f9d0-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="0f9d0-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="0f9d0-126">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0f9d0-126">-VirtualNetworkRule</span></span>
<span data-ttu-id="0f9d0-127">Cognitive Services Account NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="0f9d0-127">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="0f9d0-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0f9d0-128">-Confirm</span></span>
<span data-ttu-id="0f9d0-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0f9d0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f9d0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f9d0-130">-WhatIf</span></span>
<span data-ttu-id="0f9d0-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0f9d0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f9d0-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0f9d0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f9d0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f9d0-133">CommonParameters</span></span>
<span data-ttu-id="0f9d0-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f9d0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f9d0-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f9d0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f9d0-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0f9d0-136">INPUTS</span></span>

### <span data-ttu-id="0f9d0-137">System.String</span><span class="sxs-lookup"><span data-stu-id="0f9d0-137">System.String</span></span>

### <span data-ttu-id="0f9d0-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="0f9d0-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="0f9d0-139">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="0f9d0-139">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="0f9d0-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0f9d0-140">OUTPUTS</span></span>

### <span data-ttu-id="0f9d0-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0f9d0-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="0f9d0-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0f9d0-142">NOTES</span></span>

## <span data-ttu-id="0f9d0-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0f9d0-143">RELATED LINKS</span></span>
