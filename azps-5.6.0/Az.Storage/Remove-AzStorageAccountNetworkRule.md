---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 295f79f48ffa966024561486745cdcf52ec8e38f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929280"
---
# <span data-ttu-id="0232c-101">Remove-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0232c-101">Remove-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="0232c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0232c-102">SYNOPSIS</span></span>
<span data-ttu-id="0232c-103">Entfernen von IpRules oder VirtualNetworkRules aus der NetWorkRule-Eigenschaft eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="0232c-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="0232c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0232c-104">SYNTAX</span></span>

### <span data-ttu-id="0232c-105">NetWorkRuleString (Standard)</span><span class="sxs-lookup"><span data-stu-id="0232c-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0232c-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="0232c-106">IpRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0232c-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="0232c-107">NetworkRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0232c-108">ResourceAccessRuleObject</span><span class="sxs-lookup"><span data-stu-id="0232c-108">ResourceAccessRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -ResourceAccessRule <PSResourceAccessRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0232c-109">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="0232c-109">IpRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0232c-110">ResourceAccessRuleString</span><span class="sxs-lookup"><span data-stu-id="0232c-110">ResourceAccessRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -TenantId <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0232c-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0232c-111">DESCRIPTION</span></span>
<span data-ttu-id="0232c-112">Das **Cmdlet Remove-AzStorageAccountNetworkRule** entfernt IpRules oder VirtualNetworkRules aus der NetWorkRule-Eigenschaft eines Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="0232c-112">The **Remove-AzStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="0232c-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0232c-113">EXAMPLES</span></span>

### <span data-ttu-id="0232c-114">Beispiel 1: Entfernen mehrerer IpRules mit IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="0232c-114">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="0232c-115">Mit diesem Befehl werden mehrere IpRules mit IPAddressOrRange entfernt.</span><span class="sxs-lookup"><span data-stu-id="0232c-115">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="0232c-116">Beispiel 2: Entfernen einer VirtualNetworkRule mit VirtualNetworkRule-Objekteingabe mit JSON</span><span class="sxs-lookup"><span data-stu-id="0232c-116">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="0232c-117">Mit diesem Befehl wird eine VirtualNetworkRule mit VirtualNetworkRule-Objekteingabe mit JSON entfernt.</span><span class="sxs-lookup"><span data-stu-id="0232c-117">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="0232c-118">Beispiel 3: Entfernen der ersten IpRule mit Pipeline</span><span class="sxs-lookup"><span data-stu-id="0232c-118">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="0232c-119">Mit diesem Befehl wird zuerst IpRule mit Pipeline entfernt.</span><span class="sxs-lookup"><span data-stu-id="0232c-119">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="0232c-120">Beispiel 4: Entfernen mehrerer VirtualNetworkRules mit VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="0232c-120">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="0232c-121">Mit diesem Befehl werden mehrere VirtualNetworkRules mit VirtualNetworkResourceID entfernt.</span><span class="sxs-lookup"><span data-stu-id="0232c-121">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="0232c-122">Beispiel 5: Entfernen einer Ressourcenzugriffsregel mit TenantId und ResourceId.</span><span class="sxs-lookup"><span data-stu-id="0232c-122">Example 5: Remove a resource access rule with TenantId and ResourceId.</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount"  -TenantId $tenantId -ResourceId $ResourceId
```

<span data-ttu-id="0232c-123">Mit diesem Befehl wird eine Ressourcenzugriffsregel mit TenantId und ResourceId entfernt.</span><span class="sxs-lookup"><span data-stu-id="0232c-123">This command removes a resource access rule with TenantId and ResourceId.</span></span>

### <span data-ttu-id="0232c-124">Beispiel 6: Entfernen der ersten drei Ressourcenzugriffsregeln aus einem Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="0232c-124">Example 6: Remove the first 3 resource access rules from a storage account</span></span>
```
PS C:\> (Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount").ResourceAccessRules | Select-Object -First 3 | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="0232c-125">Mit diesem Befehl werden die ersten drei Ressourcenzugriffsregeln aus einem Speicherkonto entfernt.</span><span class="sxs-lookup"><span data-stu-id="0232c-125">This command removes the first 3 resource access rules from a storage account.</span></span>

## <span data-ttu-id="0232c-126">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0232c-126">PARAMETERS</span></span>

### <span data-ttu-id="0232c-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0232c-127">-AsJob</span></span>
<span data-ttu-id="0232c-128">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0232c-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0232c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0232c-129">-DefaultProfile</span></span>
<span data-ttu-id="0232c-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0232c-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0232c-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="0232c-131">-IPAddressOrRange</span></span>
<span data-ttu-id="0232c-132">Das Array von IpAddressOrRange entfernt IpRule mit demselben IpAddressOrRange aus der NetWorkRule-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0232c-132">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="0232c-133">-IPRule</span><span class="sxs-lookup"><span data-stu-id="0232c-133">-IPRule</span></span>
<span data-ttu-id="0232c-134">Das Array von IpRule-Objekten, die aus der NetWorkRule-Eigenschaft entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="0232c-134">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="0232c-135">-Name</span><span class="sxs-lookup"><span data-stu-id="0232c-135">-Name</span></span>
<span data-ttu-id="0232c-136">Gibt den Namen des Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="0232c-136">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="0232c-137">-ResourceAccessRule</span><span class="sxs-lookup"><span data-stu-id="0232c-137">-ResourceAccessRule</span></span>
<span data-ttu-id="0232c-138">Storage Account NetworkRule ResourceAccessRules.</span><span class="sxs-lookup"><span data-stu-id="0232c-138">Storage Account NetworkRule ResourceAccessRules.</span></span>

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

### <span data-ttu-id="0232c-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0232c-139">-ResourceGroupName</span></span>
<span data-ttu-id="0232c-140">Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="0232c-140">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="0232c-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0232c-141">-ResourceId</span></span>
<span data-ttu-id="0232c-142">Storage Account ResourceAccessRule ResourceId in string.</span><span class="sxs-lookup"><span data-stu-id="0232c-142">Storage Account ResourceAccessRule ResourceId  in string.</span></span>

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

### <span data-ttu-id="0232c-143">-TenantId</span><span class="sxs-lookup"><span data-stu-id="0232c-143">-TenantId</span></span>
<span data-ttu-id="0232c-144">Storage Account ResourceAccessRule TenantId in string.</span><span class="sxs-lookup"><span data-stu-id="0232c-144">Storage Account ResourceAccessRule TenantId  in string.</span></span>

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

### <span data-ttu-id="0232c-145">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="0232c-145">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="0232c-146">Das Array von VirtualNetworkResourceId entfernt VirtualNetworkRule mit derselben VirtualNetworkResourceId aus der NetWorkRule-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0232c-146">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="0232c-147">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0232c-147">-VirtualNetworkRule</span></span>
<span data-ttu-id="0232c-148">Das Array von VirtualNetworkRule-Objekten, die aus der NetWorkRule-Eigenschaft entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="0232c-148">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="0232c-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0232c-149">-Confirm</span></span>
<span data-ttu-id="0232c-150">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0232c-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0232c-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0232c-151">-WhatIf</span></span>
<span data-ttu-id="0232c-152">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0232c-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0232c-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0232c-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0232c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0232c-154">CommonParameters</span></span>
<span data-ttu-id="0232c-155">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0232c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0232c-156">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0232c-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0232c-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0232c-157">INPUTS</span></span>

### <span data-ttu-id="0232c-158">System.String</span><span class="sxs-lookup"><span data-stu-id="0232c-158">System.String</span></span>

### <span data-ttu-id="0232c-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="0232c-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="0232c-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="0232c-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="0232c-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0232c-161">OUTPUTS</span></span>

### <span data-ttu-id="0232c-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0232c-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="0232c-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="0232c-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="0232c-164">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0232c-164">NOTES</span></span>

## <span data-ttu-id="0232c-165">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0232c-165">RELATED LINKS</span></span>
