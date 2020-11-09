---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: e1517801c964c4794c21ada6b7d64152c6e58178
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302961"
---
# <span data-ttu-id="1d8fa-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1d8fa-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="1d8fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1d8fa-102">SYNOPSIS</span></span>
 <span data-ttu-id="1d8fa-103">Hinzufügen von IpRules oder VirtualNetworkRules zur NetworkRule-Eigenschaft eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="1d8fa-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="1d8fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d8fa-104">SYNTAX</span></span>

### <span data-ttu-id="1d8fa-105">NetWorkRuleString (Standard)</span><span class="sxs-lookup"><span data-stu-id="1d8fa-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1d8fa-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="1d8fa-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d8fa-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="1d8fa-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d8fa-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="1d8fa-108">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d8fa-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d8fa-109">DESCRIPTION</span></span>
<span data-ttu-id="1d8fa-110">Das **Add-AzStorageAccountNetworkRule-** Cmdlet fügt IpRules oder VirtualNetworkRules der NetworkRule-Eigenschaft eines speicherkontos hinzu.</span><span class="sxs-lookup"><span data-stu-id="1d8fa-110">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="1d8fa-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1d8fa-111">EXAMPLES</span></span>

### <span data-ttu-id="1d8fa-112">Beispiel 1: Hinzufügen mehrerer IpRules mit IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="1d8fa-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="1d8fa-113">Mit diesem Befehl werden mehrere IpRules mit IPAddressOrRange hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1d8fa-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="1d8fa-114">Beispiel 2: Hinzufügen eines VirtualNetworkRule mit VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="1d8fa-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="1d8fa-115">Mit diesem Befehl wird ein VirtualNetworkRule mit VirtualNetworkResourceID hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1d8fa-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="1d8fa-116">Beispiel 3: Hinzufügen von VirtualNetworkRules mit VirtualNetworkRule-Objekten aus einem anderen Konto</span><span class="sxs-lookup"><span data-stu-id="1d8fa-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="1d8fa-117">Mit diesem Befehl fügen Sie VirtualNetworkRules mit VirtualNetworkRule-Objekten aus einem anderen Konto hinzu.</span><span class="sxs-lookup"><span data-stu-id="1d8fa-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="1d8fa-118">Beispiel 4: Hinzufügen mehrerer IpRule mit IpRule-Objekten, Eingabe mit JSON</span><span class="sxs-lookup"><span data-stu-id="1d8fa-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="1d8fa-119">Dieser Befehl fügt mehrere IpRule mit IpRule-Objekten hinzu, die mit JSON eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1d8fa-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="1d8fa-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d8fa-120">PARAMETERS</span></span>

### <span data-ttu-id="1d8fa-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d8fa-121">-AsJob</span></span>
<span data-ttu-id="1d8fa-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1d8fa-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d8fa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d8fa-123">-DefaultProfile</span></span>
<span data-ttu-id="1d8fa-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1d8fa-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d8fa-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="1d8fa-125">-IPAddressOrRange</span></span>
<span data-ttu-id="1d8fa-126">Das Array von IpAddressOrRange, fügen Sie IpRules mit der Eingabe IpAddressOrRange und der Standardaktion NetworkRule-Eigenschaft zulassen hinzu.</span><span class="sxs-lookup"><span data-stu-id="1d8fa-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="1d8fa-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="1d8fa-127">-IPRule</span></span>
<span data-ttu-id="1d8fa-128">Das Array der IpRule-Objekte, die der NetworkRule-Eigenschaft hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1d8fa-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="1d8fa-129">-Name</span><span class="sxs-lookup"><span data-stu-id="1d8fa-129">-Name</span></span>
<span data-ttu-id="1d8fa-130">Gibt den Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="1d8fa-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="1d8fa-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d8fa-131">-ResourceGroupName</span></span>
<span data-ttu-id="1d8fa-132">Gibt den Namen der Ressourcengruppe mit dem Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="1d8fa-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="1d8fa-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="1d8fa-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="1d8fa-134">Das VirtualNetworkResourceId-Array fügt VirtualNetworkRule mit der Eingabe VirtualNetworkResourceId und der Standardaktion für die NetworkRule-Eigenschaft hinzu.</span><span class="sxs-lookup"><span data-stu-id="1d8fa-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="1d8fa-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1d8fa-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="1d8fa-136">Das Array der VirtualNetworkRule-Objekte, die der NetworkRule-Eigenschaft hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1d8fa-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="1d8fa-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1d8fa-137">-Confirm</span></span>
<span data-ttu-id="1d8fa-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1d8fa-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d8fa-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d8fa-139">-WhatIf</span></span>
<span data-ttu-id="1d8fa-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d8fa-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d8fa-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d8fa-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d8fa-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d8fa-142">CommonParameters</span></span>
<span data-ttu-id="1d8fa-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d8fa-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d8fa-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d8fa-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d8fa-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1d8fa-145">INPUTS</span></span>

### <span data-ttu-id="1d8fa-146">System. String</span><span class="sxs-lookup"><span data-stu-id="1d8fa-146">System.String</span></span>

### <span data-ttu-id="1d8fa-147">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="1d8fa-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="1d8fa-148">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="1d8fa-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="1d8fa-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1d8fa-149">OUTPUTS</span></span>

### <span data-ttu-id="1d8fa-150">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1d8fa-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="1d8fa-151">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="1d8fa-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="1d8fa-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="1d8fa-152">NOTES</span></span>

## <span data-ttu-id="1d8fa-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1d8fa-153">RELATED LINKS</span></span>
