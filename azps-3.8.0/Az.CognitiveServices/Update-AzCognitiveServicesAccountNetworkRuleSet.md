---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/update-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 5c01b692e47c3d246982be353093c436a91d6b64
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995001"
---
# <span data-ttu-id="d0d5c-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d0d5c-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="d0d5c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d0d5c-102">SYNOPSIS</span></span>
<span data-ttu-id="d0d5c-103">Aktualisieren der NetworkRule-Eigenschaft eines kognitiven Dienstkontos</span><span class="sxs-lookup"><span data-stu-id="d0d5c-103">Update the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="d0d5c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0d5c-104">SYNTAX</span></span>

```
Update-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IpRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0d5c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d0d5c-105">DESCRIPTION</span></span>
<span data-ttu-id="d0d5c-106">Das Cmdlet **Update-AzCognitiveServicesAccountNetworkRuleSet** aktualisiert die NetworkRule-Eigenschaft eines kognitiven Dienstkontos.</span><span class="sxs-lookup"><span data-stu-id="d0d5c-106">The **Update-AzCognitiveServicesAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="d0d5c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d0d5c-107">EXAMPLES</span></span>

### <span data-ttu-id="d0d5c-108">Beispiel 1: Aktualisieren aller Eigenschaften von NetworkRule, eingeben von Regeln mit JSON</span><span class="sxs-lookup"><span data-stu-id="d0d5c-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -DefaultAction Allow -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2"})
```

<span data-ttu-id="d0d5c-109">Mit diesem Befehl werden alle Eigenschaften von NetworkRule, Eingaberegeln mit JSON, aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d0d5c-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="d0d5c-110">Beispiel 2: Update-Bypass-Eigenschaft von NetworkRule</span><span class="sxs-lookup"><span data-stu-id="d0d5c-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="d0d5c-111">Diese Befehls Update-Bypass-Eigenschaft von NetworkRule (andere Eigenschaften werden nicht geändert).</span><span class="sxs-lookup"><span data-stu-id="d0d5c-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="d0d5c-112">Beispiel 3: Bereinigen von NetworkRule-Regeln eines kognitiven Dienstkontos</span><span class="sxs-lookup"><span data-stu-id="d0d5c-112">Example 3: Clean up rules of NetworkRule of a Cognitive Services account</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="d0d5c-113">Mit diesem Befehl werden Regeln für NetworkRule eines kognitiven Dienstkontos bereinigt (andere Eigenschaften werden nicht geändert).</span><span class="sxs-lookup"><span data-stu-id="d0d5c-113">This command clean up rules of NetworkRule of a Cognitive Services account (other properties not change).</span></span>

## <span data-ttu-id="d0d5c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0d5c-114">PARAMETERS</span></span>

### <span data-ttu-id="d0d5c-115">– Standardmäßig</span><span class="sxs-lookup"><span data-stu-id="d0d5c-115">-DefaultAction</span></span>
<span data-ttu-id="d0d5c-116">NetworkRule-Standardwert für Cognitive Services-Konto</span><span class="sxs-lookup"><span data-stu-id="d0d5c-116">Cognitive Services Account NetworkRule DefaultAction.</span></span>

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

### <span data-ttu-id="d0d5c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0d5c-117">-DefaultProfile</span></span>
<span data-ttu-id="d0d5c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d0d5c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0d5c-119">-IpRule</span><span class="sxs-lookup"><span data-stu-id="d0d5c-119">-IpRule</span></span>
<span data-ttu-id="d0d5c-120">Cognitive Services-Konto NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="d0d5c-120">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="d0d5c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d0d5c-121">-Name</span></span>
<span data-ttu-id="d0d5c-122">Name des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="d0d5c-122">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="d0d5c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0d5c-123">-ResourceGroupName</span></span>
<span data-ttu-id="d0d5c-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d0d5c-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="d0d5c-125">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d0d5c-125">-VirtualNetworkRule</span></span>
<span data-ttu-id="d0d5c-126">Cognitive Services-Konto NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="d0d5c-126">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="d0d5c-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d0d5c-127">-Confirm</span></span>
<span data-ttu-id="d0d5c-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d0d5c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0d5c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0d5c-129">-WhatIf</span></span>
<span data-ttu-id="d0d5c-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d0d5c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0d5c-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d0d5c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0d5c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0d5c-132">CommonParameters</span></span>
<span data-ttu-id="d0d5c-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0d5c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0d5c-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0d5c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0d5c-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d0d5c-135">INPUTS</span></span>

### <span data-ttu-id="d0d5c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d0d5c-136">System.String</span></span>

### <span data-ttu-id="d0d5c-137">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="d0d5c-137">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="d0d5c-138">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="d0d5c-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="d0d5c-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d0d5c-139">OUTPUTS</span></span>

### <span data-ttu-id="d0d5c-140">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d0d5c-140">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="d0d5c-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="d0d5c-141">NOTES</span></span>

## <span data-ttu-id="d0d5c-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d0d5c-142">RELATED LINKS</span></span>
