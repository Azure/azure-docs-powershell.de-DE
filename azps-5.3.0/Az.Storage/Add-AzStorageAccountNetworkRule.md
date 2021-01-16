---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: e1517801c964c4794c21ada6b7d64152c6e58178
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376367"
---
# <span data-ttu-id="d5a0f-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d5a0f-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="d5a0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5a0f-102">SYNOPSIS</span></span>
 <span data-ttu-id="d5a0f-103">Hinzufügen von IpRules oder VirtualNetworkRules zur Eigenschaft "NetworkRule" eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="d5a0f-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="d5a0f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5a0f-104">SYNTAX</span></span>

### <span data-ttu-id="d5a0f-105">NetWorkRuleString (Standard)</span><span class="sxs-lookup"><span data-stu-id="d5a0f-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5a0f-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="d5a0f-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5a0f-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="d5a0f-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5a0f-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="d5a0f-108">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5a0f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5a0f-109">DESCRIPTION</span></span>
<span data-ttu-id="d5a0f-110">Das **Cmdlet "Add-AzStorageAccountNetworkRule"** fügt "IpRules" oder "VirtualNetworkRules" zur Eigenschaft "NetworkRule" eines Speicherkontos hinzu.</span><span class="sxs-lookup"><span data-stu-id="d5a0f-110">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="d5a0f-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d5a0f-111">EXAMPLES</span></span>

### <span data-ttu-id="d5a0f-112">Beispiel 1: Hinzufügen mehrerer IpRules mit "IPAddressOrRange"</span><span class="sxs-lookup"><span data-stu-id="d5a0f-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="d5a0f-113">Mit diesem Befehl werden mehrere IpRules mit "IPAddressOrRange" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d5a0f-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="d5a0f-114">Beispiel 2: Hinzufügen einer VirtualNetworkRule mit VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="d5a0f-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="d5a0f-115">Mit diesem Befehl wird eine VirtualNetworkRule mit VirtualNetworkResourceID hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d5a0f-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="d5a0f-116">Beispiel 3: Hinzufügen von VirtualNetworkRules mit VirtualNetworkRule-Objekten aus einem anderen Konto</span><span class="sxs-lookup"><span data-stu-id="d5a0f-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="d5a0f-117">Mit diesem Befehl können Sie VirtualNetworkRules mit VirtualNetworkRule-Objekten aus einem anderen Konto hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d5a0f-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="d5a0f-118">Beispiel 4: Hinzufügen mehrerer IpRule mit IpRule-Objekten, Eingabe mit JSON</span><span class="sxs-lookup"><span data-stu-id="d5a0f-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="d5a0f-119">Mit diesem Befehl werden mehrere IpRule-Objekte mit JSON-Eingaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d5a0f-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="d5a0f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5a0f-120">PARAMETERS</span></span>

### <span data-ttu-id="d5a0f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5a0f-121">-AsJob</span></span>
<span data-ttu-id="d5a0f-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d5a0f-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5a0f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a0f-123">-DefaultProfile</span></span>
<span data-ttu-id="d5a0f-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5a0f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5a0f-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="d5a0f-125">-IPAddressOrRange</span></span>
<span data-ttu-id="d5a0f-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span><span class="sxs-lookup"><span data-stu-id="d5a0f-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="d5a0f-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="d5a0f-127">-IPRule</span></span>
<span data-ttu-id="d5a0f-128">Das Array von IpRule-Objekten, die der Eigenschaft "NetworkRule" hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d5a0f-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a0f-129">-Name</span><span class="sxs-lookup"><span data-stu-id="d5a0f-129">-Name</span></span>
<span data-ttu-id="d5a0f-130">Gibt den Namen des Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="d5a0f-130">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a0f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5a0f-131">-ResourceGroupName</span></span>
<span data-ttu-id="d5a0f-132">Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="d5a0f-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="d5a0f-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="d5a0f-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="d5a0f-134">Das Array von "VirtualNetworkResourceId" fügt "VirtualNetworkRule" mit der Eingabe "VirtualNetworkResourceId" und der Standardeigenschaft "Action Allow" für die Eigenschaft "NetworkRule" hinzu.</span><span class="sxs-lookup"><span data-stu-id="d5a0f-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="d5a0f-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d5a0f-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="d5a0f-136">Das Array der VirtualNetworkRule-Objekte, die der Eigenschaft "NetworkRule" hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d5a0f-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a0f-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5a0f-137">-Confirm</span></span>
<span data-ttu-id="d5a0f-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5a0f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5a0f-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d5a0f-139">-WhatIf</span></span>
<span data-ttu-id="d5a0f-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5a0f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5a0f-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5a0f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5a0f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a0f-142">CommonParameters</span></span>
<span data-ttu-id="d5a0f-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5a0f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a0f-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5a0f-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a0f-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d5a0f-145">INPUTS</span></span>

### <span data-ttu-id="d5a0f-146">System.String</span><span class="sxs-lookup"><span data-stu-id="d5a0f-146">System.String</span></span>

### <span data-ttu-id="d5a0f-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="d5a0f-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="d5a0f-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="d5a0f-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="d5a0f-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d5a0f-149">OUTPUTS</span></span>

### <span data-ttu-id="d5a0f-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d5a0f-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="d5a0f-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="d5a0f-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="d5a0f-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d5a0f-152">NOTES</span></span>

## <span data-ttu-id="d5a0f-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d5a0f-153">RELATED LINKS</span></span>
