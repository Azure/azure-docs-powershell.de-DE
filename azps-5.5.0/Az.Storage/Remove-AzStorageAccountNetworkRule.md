---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 1eeaf3a7c9d0c4b5715bc5b75e42e53a8fa98c5e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157988"
---
# <span data-ttu-id="29c2a-101">Remove-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="29c2a-101">Remove-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="29c2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29c2a-102">SYNOPSIS</span></span>
<span data-ttu-id="29c2a-103">Entfernen von IpRules oder VirtualNetworkRules aus der Eigenschaft "NetWorkRule" eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="29c2a-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="29c2a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29c2a-104">SYNTAX</span></span>

### <span data-ttu-id="29c2a-105">NetWorkRuleString (Standard)</span><span class="sxs-lookup"><span data-stu-id="29c2a-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29c2a-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="29c2a-106">IpRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29c2a-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="29c2a-107">NetworkRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29c2a-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="29c2a-108">IpRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29c2a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29c2a-109">DESCRIPTION</span></span>
<span data-ttu-id="29c2a-110">Das **Cmdlet "Remove-AzStorageAccountNetworkRule"** entfernt "IpRules" oder "VirtualNetworkRules" aus der Eigenschaft "NetWorkRule" eines Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="29c2a-110">The **Remove-AzStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="29c2a-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="29c2a-111">EXAMPLES</span></span>

### <span data-ttu-id="29c2a-112">Beispiel 1: Entfernen mehrerer IpRules mit IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="29c2a-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="29c2a-113">Mit diesem Befehl werden mehrere IpRules mit "IPAddressOrRange" entfernt.</span><span class="sxs-lookup"><span data-stu-id="29c2a-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="29c2a-114">Beispiel 2: Entfernen einer VirtualNetworkRule mit VirtualNetworkRule-Objekteingabe mit JSON</span><span class="sxs-lookup"><span data-stu-id="29c2a-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="29c2a-115">Mit diesem Befehl wird eine VirtualNetworkRule mit einer VirtualNetworkRule-Objekteingabe mit JSON entfernt.</span><span class="sxs-lookup"><span data-stu-id="29c2a-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="29c2a-116">Beispiel 3: Entfernen der ersten IpRule mit Pipeline</span><span class="sxs-lookup"><span data-stu-id="29c2a-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="29c2a-117">Mit diesem Befehl wird die erste IpRule mit Pipeline entfernt.</span><span class="sxs-lookup"><span data-stu-id="29c2a-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="29c2a-118">Beispiel 4: Entfernen mehrerer VirtualNetworkRules mit VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="29c2a-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="29c2a-119">Mit diesem Befehl werden mehrere VirtualNetworkRules mit VirtualNetworkResourceID entfernt.</span><span class="sxs-lookup"><span data-stu-id="29c2a-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="29c2a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29c2a-120">PARAMETERS</span></span>

### <span data-ttu-id="29c2a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29c2a-121">-AsJob</span></span>
<span data-ttu-id="29c2a-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="29c2a-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29c2a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29c2a-123">-DefaultProfile</span></span>
<span data-ttu-id="29c2a-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29c2a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29c2a-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="29c2a-125">-IPAddressOrRange</span></span>
<span data-ttu-id="29c2a-126">Das Array von "IpAddressOrRange" entfernt "IpRule" mit derselben "IpAddressOrRange" aus der NetWorkRule-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="29c2a-126">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="29c2a-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="29c2a-127">-IPRule</span></span>
<span data-ttu-id="29c2a-128">Das Array von IpRule-Objekten, die aus der Eigenschaft "NetWorkRule" entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="29c2a-128">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="29c2a-129">-Name</span><span class="sxs-lookup"><span data-stu-id="29c2a-129">-Name</span></span>
<span data-ttu-id="29c2a-130">Gibt den Namen des Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="29c2a-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="29c2a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29c2a-131">-ResourceGroupName</span></span>
<span data-ttu-id="29c2a-132">Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="29c2a-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="29c2a-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="29c2a-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="29c2a-134">Das Array von VirtualNetworkResourceId entfernt "VirtualNetworkRule" mit derselben VirtualNetworkResourceId aus der NetWorkRule-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="29c2a-134">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="29c2a-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="29c2a-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="29c2a-136">Das Array von VirtualNetworkRule-Objekten, die aus der "NetWorkRule"-Eigenschaft entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="29c2a-136">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="29c2a-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29c2a-137">-Confirm</span></span>
<span data-ttu-id="29c2a-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29c2a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29c2a-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="29c2a-139">-WhatIf</span></span>
<span data-ttu-id="29c2a-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29c2a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29c2a-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29c2a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29c2a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29c2a-142">CommonParameters</span></span>
<span data-ttu-id="29c2a-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29c2a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29c2a-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29c2a-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29c2a-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="29c2a-145">INPUTS</span></span>

### <span data-ttu-id="29c2a-146">System.String</span><span class="sxs-lookup"><span data-stu-id="29c2a-146">System.String</span></span>

### <span data-ttu-id="29c2a-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="29c2a-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="29c2a-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="29c2a-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="29c2a-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="29c2a-149">OUTPUTS</span></span>

### <span data-ttu-id="29c2a-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="29c2a-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="29c2a-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="29c2a-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="29c2a-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="29c2a-152">NOTES</span></span>

## <span data-ttu-id="29c2a-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="29c2a-153">RELATED LINKS</span></span>
