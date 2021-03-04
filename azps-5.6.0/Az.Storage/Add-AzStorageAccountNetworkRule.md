---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 0104c64bf65acc945609f4e2e0ae78ff288b142d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930704"
---
# <span data-ttu-id="3e5f0-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3e5f0-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="3e5f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e5f0-102">SYNOPSIS</span></span>
 <span data-ttu-id="3e5f0-103">Hinzufügen von IpRules oder VirtualNetworkRules zur NetworkRule-Eigenschaft eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="3e5f0-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="3e5f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e5f0-104">SYNTAX</span></span>

### <span data-ttu-id="3e5f0-105">NetWorkRuleString (Standard)</span><span class="sxs-lookup"><span data-stu-id="3e5f0-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e5f0-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="3e5f0-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e5f0-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="3e5f0-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e5f0-108">ResourceAccessRuleObject</span><span class="sxs-lookup"><span data-stu-id="3e5f0-108">ResourceAccessRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -ResourceAccessRule <PSResourceAccessRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e5f0-109">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="3e5f0-109">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e5f0-110">ResourceAccessRuleString</span><span class="sxs-lookup"><span data-stu-id="3e5f0-110">ResourceAccessRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -TenantId <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e5f0-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e5f0-111">DESCRIPTION</span></span>
<span data-ttu-id="3e5f0-112">Das **Add-AzStorageAccountNetworkRule-Cmdlet** fügt der NetworkRule-Eigenschaft eines Speicherkontos IpRules oder VirtualNetworkRules hinzu.</span><span class="sxs-lookup"><span data-stu-id="3e5f0-112">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="3e5f0-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3e5f0-113">EXAMPLES</span></span>

### <span data-ttu-id="3e5f0-114">Beispiel 1: Hinzufügen mehrerer IpRules mit IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3e5f0-114">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="3e5f0-115">Mit diesem Befehl werden mehrere IpRules mit IPAddressOrRange hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3e5f0-115">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="3e5f0-116">Beispiel 2: Hinzufügen einer VirtualNetworkRule mit VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="3e5f0-116">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="3e5f0-117">Mit diesem Befehl wird eine VirtualNetworkRule mit VirtualNetworkResourceID hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3e5f0-117">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="3e5f0-118">Beispiel 3: Hinzufügen von VirtualNetworkRules mit VirtualNetworkRule-Objekten aus einem anderen Konto</span><span class="sxs-lookup"><span data-stu-id="3e5f0-118">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="3e5f0-119">Mit diesem Befehl können Sie VirtualNetworkRules mit VirtualNetworkRule-Objekten aus einem anderen Konto hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3e5f0-119">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="3e5f0-120">Beispiel 4: Hinzufügen mehrerer IpRule mit IpRule-Objekten, Eingabe mit JSON</span><span class="sxs-lookup"><span data-stu-id="3e5f0-120">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="3e5f0-121">Mit diesem Befehl werden mehrere IpRule mit IpRule-Objekten hinzugefügt, die mit JSON eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3e5f0-121">This command add several IpRule with IpRule objects, input with JSON.</span></span>

### <span data-ttu-id="3e5f0-122">Beispiel 5: Hinzufügen einer Ressourcenzugriffsregel</span><span class="sxs-lookup"><span data-stu-id="3e5f0-122">Example 5: Add a resource access rule</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -TenantId $tenantId -ResourceId $ResourceId
```

<span data-ttu-id="3e5f0-123">Mit diesem Befehl wird eine Ressourcenzugriffsregel mit TenantId und ResourceId addiert.</span><span class="sxs-lookup"><span data-stu-id="3e5f0-123">This command adds a resource access rule with TenantId and ResourceId.</span></span>

### <span data-ttu-id="3e5f0-124">Beispiel 6: Hinzufügen aller Ressourcenzugriffsregeln eines Speicherkontos zu einem anderen Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="3e5f0-124">Example 6: Add all resource access rules of one storage account to another storage account</span></span>
```
PS C:\> (Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1").ResourceAccessRules | Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2"
```

<span data-ttu-id="3e5f0-125">Dieser Befehl ruft alle Ressourcenzugriffsregeln aus einem Speicherkonto ab und fügt sie einem anderen Speicherkonto hinzu.</span><span class="sxs-lookup"><span data-stu-id="3e5f0-125">This command gets all resource access rules from one storage account, and adds them to another storage account.</span></span>

## <span data-ttu-id="3e5f0-126">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3e5f0-126">PARAMETERS</span></span>

### <span data-ttu-id="3e5f0-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e5f0-127">-AsJob</span></span>
<span data-ttu-id="3e5f0-128">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3e5f0-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e5f0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e5f0-129">-DefaultProfile</span></span>
<span data-ttu-id="3e5f0-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e5f0-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e5f0-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3e5f0-131">-IPAddressOrRange</span></span>
<span data-ttu-id="3e5f0-132">Fügen Sie im Array von IpAddressOrRange IpRules mit der Eingabe "IpAddressOrRange" und der Standardmäßigen Aktionseigenschaft "An NetworkRule zulassen" hinzu.</span><span class="sxs-lookup"><span data-stu-id="3e5f0-132">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="3e5f0-133">-IPRule</span><span class="sxs-lookup"><span data-stu-id="3e5f0-133">-IPRule</span></span>
<span data-ttu-id="3e5f0-134">Das Array der IpRule-Objekte, die der NetworkRule-Eigenschaft hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="3e5f0-134">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="3e5f0-135">-Name</span><span class="sxs-lookup"><span data-stu-id="3e5f0-135">-Name</span></span>
<span data-ttu-id="3e5f0-136">Gibt den Namen des Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="3e5f0-136">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="3e5f0-137">-ResourceAccessRule</span><span class="sxs-lookup"><span data-stu-id="3e5f0-137">-ResourceAccessRule</span></span>
<span data-ttu-id="3e5f0-138">Storage Account NetworkRule ResourceAccessRules.</span><span class="sxs-lookup"><span data-stu-id="3e5f0-138">Storage Account NetworkRule ResourceAccessRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSResourceAccessRule[]
Parameter Sets: ResourceAccessRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e5f0-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e5f0-139">-ResourceGroupName</span></span>
<span data-ttu-id="3e5f0-140">Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="3e5f0-140">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="3e5f0-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e5f0-141">-ResourceId</span></span>
<span data-ttu-id="3e5f0-142">Storage Account ResourceAccessRule ResourceId in string.</span><span class="sxs-lookup"><span data-stu-id="3e5f0-142">Storage Account ResourceAccessRule ResourceId  in string.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceAccessRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e5f0-143">-TenantId</span><span class="sxs-lookup"><span data-stu-id="3e5f0-143">-TenantId</span></span>
<span data-ttu-id="3e5f0-144">Storage Account ResourceAccessRule TenantId in string.</span><span class="sxs-lookup"><span data-stu-id="3e5f0-144">Storage Account ResourceAccessRule TenantId  in string.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceAccessRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e5f0-145">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="3e5f0-145">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="3e5f0-146">Das Array von VirtualNetworkResourceId fügt VirtualNetworkRule mit der Eingabe VirtualNetworkResourceId und der standardmäßigen Aktionseigenschaft "NetworkRule zulassen" hinzu.</span><span class="sxs-lookup"><span data-stu-id="3e5f0-146">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="3e5f0-147">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3e5f0-147">-VirtualNetworkRule</span></span>
<span data-ttu-id="3e5f0-148">Das Array von VirtualNetworkRule-Objekten, die der NetworkRule-Eigenschaft hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="3e5f0-148">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="3e5f0-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3e5f0-149">-Confirm</span></span>
<span data-ttu-id="3e5f0-150">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3e5f0-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e5f0-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e5f0-151">-WhatIf</span></span>
<span data-ttu-id="3e5f0-152">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3e5f0-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e5f0-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e5f0-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e5f0-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e5f0-154">CommonParameters</span></span>
<span data-ttu-id="3e5f0-155">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e5f0-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e5f0-156">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e5f0-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e5f0-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3e5f0-157">INPUTS</span></span>

### <span data-ttu-id="3e5f0-158">System.String</span><span class="sxs-lookup"><span data-stu-id="3e5f0-158">System.String</span></span>

### <span data-ttu-id="3e5f0-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="3e5f0-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="3e5f0-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="3e5f0-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="3e5f0-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3e5f0-161">OUTPUTS</span></span>

### <span data-ttu-id="3e5f0-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3e5f0-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="3e5f0-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="3e5f0-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="3e5f0-164">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3e5f0-164">NOTES</span></span>

## <span data-ttu-id="3e5f0-165">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3e5f0-165">RELATED LINKS</span></span>
