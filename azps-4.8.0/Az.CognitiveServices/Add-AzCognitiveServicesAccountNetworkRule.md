---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/add-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 039a3e4bf676f29d55f48e7e0883f5818e7367b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010250"
---
# <span data-ttu-id="f5628-101">Add-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f5628-101">Add-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="f5628-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5628-102">SYNOPSIS</span></span>
<span data-ttu-id="f5628-103">Hinzufügen von IpRules oder VirtualNetworkRules zur NetworkRule-Eigenschaft eines kognitiven Dienstkontos</span><span class="sxs-lookup"><span data-stu-id="f5628-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="f5628-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5628-104">SYNTAX</span></span>

### <span data-ttu-id="f5628-105">NetWorkRuleString (Standard)</span><span class="sxs-lookup"><span data-stu-id="f5628-105">NetWorkRuleString (Default)</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5628-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="f5628-106">IpRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IpRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5628-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="f5628-107">NetworkRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5628-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="f5628-108">IpRuleString</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5628-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5628-109">DESCRIPTION</span></span>
<span data-ttu-id="f5628-110">Das **Add-AzCognitiveServicesAccountNetworkRule-** Cmdlet fügt IpRules oder VirtualNetworkRules der NetworkRule-Eigenschaft eines kognitiven Dienstkontos hinzu.</span><span class="sxs-lookup"><span data-stu-id="f5628-110">The **Add-AzCognitiveServicesAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="f5628-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5628-111">EXAMPLES</span></span>

### <span data-ttu-id="f5628-112">Beispiel 1: Hinzufügen mehrerer IpRules mit IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="f5628-112">Example 1: Add several IpRules with IpAddressOrRange</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "200.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="f5628-113">Mit diesem Befehl werden mehrere IpRules mit IpAddressOrRange hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f5628-113">This command add several IpRules with IpAddressOrRange.</span></span>

### <span data-ttu-id="f5628-114">Beispiel 2: Hinzufügen eines VirtualNetworkRule mit VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="f5628-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="f5628-115">Mit diesem Befehl wird ein VirtualNetworkRule mit VirtualNetworkResourceID hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f5628-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="f5628-116">Beispiel 3: Hinzufügen von VirtualNetworkRules mit VirtualNetworkRule-Objekten aus einem anderen Konto</span><span class="sxs-lookup"><span data-stu-id="f5628-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount1"
PS C:\> Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="f5628-117">Mit diesem Befehl fügen Sie VirtualNetworkRules mit VirtualNetworkRule-Objekten aus einem anderen Konto hinzu.</span><span class="sxs-lookup"><span data-stu-id="f5628-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="f5628-118">Beispiel 4: Hinzufügen mehrerer IpRule mit IpRule-Objekten, Eingabe mit JSON</span><span class="sxs-lookup"><span data-stu-id="f5628-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
```

<span data-ttu-id="f5628-119">Dieser Befehl fügt mehrere IpRule mit IpRule-Objekten hinzu, die mit JSON eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f5628-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="f5628-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5628-120">PARAMETERS</span></span>

### <span data-ttu-id="f5628-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5628-121">-DefaultProfile</span></span>
<span data-ttu-id="f5628-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f5628-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5628-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="f5628-123">-IpAddressOrRange</span></span>
<span data-ttu-id="f5628-124">Cognitive Services-Konto NetworkRule IpRules IpAddressOrRange in einer Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f5628-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="f5628-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="f5628-125">-IpRule</span></span>
<span data-ttu-id="f5628-126">Cognitive Services-Konto NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="f5628-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="f5628-127">-Name</span><span class="sxs-lookup"><span data-stu-id="f5628-127">-Name</span></span>
<span data-ttu-id="f5628-128">Name des Cognitive Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="f5628-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="f5628-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5628-129">-ResourceGroupName</span></span>
<span data-ttu-id="f5628-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f5628-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="f5628-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="f5628-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="f5628-132">Cognitive Services-Konto NetworkRule VirtualNetworkRules VirtualNetworkResourceId in einer Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f5628-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="f5628-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f5628-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="f5628-134">Cognitive Services-Konto NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="f5628-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="f5628-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f5628-135">-Confirm</span></span>
<span data-ttu-id="f5628-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f5628-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5628-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5628-137">-WhatIf</span></span>
<span data-ttu-id="f5628-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f5628-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5628-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5628-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5628-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5628-140">CommonParameters</span></span>
<span data-ttu-id="f5628-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5628-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5628-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5628-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5628-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5628-143">INPUTS</span></span>

### <span data-ttu-id="f5628-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f5628-144">System.String</span></span>

### <span data-ttu-id="f5628-145">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="f5628-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="f5628-146">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="f5628-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="f5628-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5628-147">OUTPUTS</span></span>

### <span data-ttu-id="f5628-148">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f5628-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="f5628-149">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="f5628-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="f5628-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5628-150">NOTES</span></span>

## <span data-ttu-id="f5628-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5628-151">RELATED LINKS</span></span>
