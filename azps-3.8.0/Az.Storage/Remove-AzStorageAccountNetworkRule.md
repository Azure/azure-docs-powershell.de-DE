---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 1eeaf3a7c9d0c4b5715bc5b75e42e53a8fa98c5e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004873"
---
# <span data-ttu-id="946bf-101">Remove-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="946bf-101">Remove-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="946bf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="946bf-102">SYNOPSIS</span></span>
<span data-ttu-id="946bf-103">Entfernen von IpRules oder VirtualNetworkRules aus der NetWorkRule-Eigenschaft eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="946bf-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="946bf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="946bf-104">SYNTAX</span></span>

### <span data-ttu-id="946bf-105">NetWorkRuleString (Standard)</span><span class="sxs-lookup"><span data-stu-id="946bf-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="946bf-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="946bf-106">IpRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="946bf-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="946bf-107">NetworkRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="946bf-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="946bf-108">IpRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="946bf-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="946bf-109">DESCRIPTION</span></span>
<span data-ttu-id="946bf-110">Das Cmdlet " **Remove-AzStorageAccountNetworkRule** " entfernt IpRules oder VirtualNetworkRules aus der NetWorkRule-Eigenschaft eines speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="946bf-110">The **Remove-AzStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="946bf-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="946bf-111">EXAMPLES</span></span>

### <span data-ttu-id="946bf-112">Beispiel 1: Entfernen mehrerer IpRules mit IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="946bf-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="946bf-113">Dieser Befehl entfernt mehrere IpRules mit IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="946bf-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="946bf-114">Beispiel 2: Entfernen eines VirtualNetworkRule mit VirtualNetworkRule-objekteingabe mit JSON</span><span class="sxs-lookup"><span data-stu-id="946bf-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="946bf-115">Mit diesem Befehl wird eine VirtualNetworkRule mit VirtualNetworkRule-objekteingabe mit JSON entfernt.</span><span class="sxs-lookup"><span data-stu-id="946bf-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="946bf-116">Beispiel 3: Entfernen des ersten IpRule mit Pipeline</span><span class="sxs-lookup"><span data-stu-id="946bf-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="946bf-117">Mit diesem Befehl wird First IpRule mit Pipeline entfernt.</span><span class="sxs-lookup"><span data-stu-id="946bf-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="946bf-118">Beispiel 4: Entfernen mehrerer VirtualNetworkRules mit VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="946bf-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="946bf-119">Dieser Befehl entfernt mehrere VirtualNetworkRules mit VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="946bf-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="946bf-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="946bf-120">PARAMETERS</span></span>

### <span data-ttu-id="946bf-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="946bf-121">-AsJob</span></span>
<span data-ttu-id="946bf-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="946bf-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="946bf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="946bf-123">-DefaultProfile</span></span>
<span data-ttu-id="946bf-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="946bf-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="946bf-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="946bf-125">-IPAddressOrRange</span></span>
<span data-ttu-id="946bf-126">Das IpAddressOrRange-Array entfernt IpRule mit demselben IpAddressOrRange aus der NetWorkRule-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="946bf-126">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="946bf-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="946bf-127">-IPRule</span></span>
<span data-ttu-id="946bf-128">Das Array von IpRule-Objekten, die aus der NetWorkRule-Eigenschaft entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="946bf-128">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="946bf-129">-Name</span><span class="sxs-lookup"><span data-stu-id="946bf-129">-Name</span></span>
<span data-ttu-id="946bf-130">Gibt den Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="946bf-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="946bf-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="946bf-131">-ResourceGroupName</span></span>
<span data-ttu-id="946bf-132">Gibt den Namen der Ressourcengruppe mit dem Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="946bf-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="946bf-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="946bf-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="946bf-134">Das VirtualNetworkResourceId-Array entfernt VirtualNetworkRule mit demselben VirtualNetworkResourceId aus der NetWorkRule-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="946bf-134">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="946bf-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="946bf-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="946bf-136">Das Array von VirtualNetworkRule-Objekten, die aus der NetWorkRule-Eigenschaft entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="946bf-136">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="946bf-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="946bf-137">-Confirm</span></span>
<span data-ttu-id="946bf-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="946bf-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="946bf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="946bf-139">-WhatIf</span></span>
<span data-ttu-id="946bf-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="946bf-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="946bf-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="946bf-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="946bf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="946bf-142">CommonParameters</span></span>
<span data-ttu-id="946bf-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="946bf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="946bf-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="946bf-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="946bf-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="946bf-145">INPUTS</span></span>

### <span data-ttu-id="946bf-146">System. String</span><span class="sxs-lookup"><span data-stu-id="946bf-146">System.String</span></span>

### <span data-ttu-id="946bf-147">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="946bf-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="946bf-148">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="946bf-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="946bf-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="946bf-149">OUTPUTS</span></span>

### <span data-ttu-id="946bf-150">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="946bf-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="946bf-151">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="946bf-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="946bf-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="946bf-152">NOTES</span></span>

## <span data-ttu-id="946bf-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="946bf-153">RELATED LINKS</span></span>
