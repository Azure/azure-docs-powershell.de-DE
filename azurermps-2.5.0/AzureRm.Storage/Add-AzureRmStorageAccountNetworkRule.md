---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/add-azurermstorageaccountnetworkrule
schema: 2.0.0
ms.openlocfilehash: 0b1d497bbd7e976d942bdc3f99c6bea2d4c2c1cb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849011"
---
# <span data-ttu-id="70ee1-101">Add-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="70ee1-101">Add-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="70ee1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="70ee1-102">SYNOPSIS</span></span>
 <span data-ttu-id="70ee1-103">Hinzufügen von IpRules oder VirtualNetworkRules zur NetworkRule-Eigenschaft eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="70ee1-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70ee1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="70ee1-104">SYNTAX</span></span>

### <span data-ttu-id="70ee1-105">NetWorkRuleString (Standard)</span><span class="sxs-lookup"><span data-stu-id="70ee1-105">NetWorkRuleString (Default)</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70ee1-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="70ee1-106">IpRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70ee1-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="70ee1-107">NetworkRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70ee1-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="70ee1-108">IpRuleString</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70ee1-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70ee1-109">DESCRIPTION</span></span>
<span data-ttu-id="70ee1-110">Das **Add-AzureRmStorageAccountNetworkRule-** Cmdlet fügt IpRules oder VirtualNetworkRules der NetworkRule-Eigenschaft eines speicherkontos hinzu.</span><span class="sxs-lookup"><span data-stu-id="70ee1-110">The **Add-AzureRmStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="70ee1-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70ee1-111">EXAMPLES</span></span>

### <span data-ttu-id="70ee1-112">Beispiel 1: Hinzufügen mehrerer IpRules mit IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="70ee1-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="70ee1-113">Mit diesem Befehl werden mehrere IpRules mit IPAddressOrRange hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="70ee1-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="70ee1-114">Beispiel 2: Hinzufügen eines VirtualNetworkRule mit VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="70ee1-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzureRmVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzureRmVirtualNetworkSubnetConfig
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="70ee1-115">Mit diesem Befehl wird ein VirtualNetworkRule mit VirtualNetworkResourceID hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="70ee1-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="70ee1-116">Beispiel 3: Hinzufügen von VirtualNetworkRules mit VirtualNetworkRule-Objekten aus einem anderen Konto</span><span class="sxs-lookup"><span data-stu-id="70ee1-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzureRMStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="70ee1-117">Mit diesem Befehl fügen Sie VirtualNetworkRules mit VirtualNetworkRule-Objekten aus einem anderen Konto hinzu.</span><span class="sxs-lookup"><span data-stu-id="70ee1-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="70ee1-118">Beispiel 4: Hinzufügen mehrerer IpRule mit IpRule-Objekten, Eingabe mit JSON</span><span class="sxs-lookup"><span data-stu-id="70ee1-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="70ee1-119">Dieser Befehl fügt mehrere IpRule mit IpRule-Objekten hinzu, die mit JSON eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="70ee1-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="70ee1-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="70ee1-120">PARAMETERS</span></span>

### <span data-ttu-id="70ee1-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70ee1-121">-AsJob</span></span>
<span data-ttu-id="70ee1-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="70ee1-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70ee1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70ee1-123">-DefaultProfile</span></span>
<span data-ttu-id="70ee1-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="70ee1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70ee1-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="70ee1-125">-IPAddressOrRange</span></span>
<span data-ttu-id="70ee1-126">Das Array von IpAddressOrRange, fügen Sie IpRules mit der Eingabe IpAddressOrRange und der Standardaktion NetworkRule-Eigenschaft zulassen hinzu.</span><span class="sxs-lookup"><span data-stu-id="70ee1-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="70ee1-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="70ee1-127">-IPRule</span></span>
<span data-ttu-id="70ee1-128">Das Array der IpRule-Objekte, die der NetworkRule-Eigenschaft hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="70ee1-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="70ee1-129">-Name</span><span class="sxs-lookup"><span data-stu-id="70ee1-129">-Name</span></span>
<span data-ttu-id="70ee1-130">Gibt den Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="70ee1-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="70ee1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70ee1-131">-ResourceGroupName</span></span>
<span data-ttu-id="70ee1-132">Gibt den Namen der Ressourcengruppe mit dem Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="70ee1-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="70ee1-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="70ee1-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="70ee1-134">Das VirtualNetworkResourceId-Array fügt VirtualNetworkRule mit der Eingabe VirtualNetworkResourceId und der Standardaktion für die NetworkRule-Eigenschaft hinzu.</span><span class="sxs-lookup"><span data-stu-id="70ee1-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="70ee1-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="70ee1-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="70ee1-136">Das Array der VirtualNetworkRule-Objekte, die der NetworkRule-Eigenschaft hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="70ee1-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="70ee1-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="70ee1-137">-Confirm</span></span>
<span data-ttu-id="70ee1-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="70ee1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70ee1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70ee1-139">-WhatIf</span></span>
<span data-ttu-id="70ee1-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="70ee1-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70ee1-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="70ee1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70ee1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70ee1-142">CommonParameters</span></span>
<span data-ttu-id="70ee1-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70ee1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70ee1-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70ee1-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70ee1-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="70ee1-145">INPUTS</span></span>

### <span data-ttu-id="70ee1-146">System. String</span><span class="sxs-lookup"><span data-stu-id="70ee1-146">System.String</span></span>

### <span data-ttu-id="70ee1-147">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="70ee1-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="70ee1-148">Parameter: IPRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="70ee1-148">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="70ee1-149">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="70ee1-149">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="70ee1-150">Parameter: VirtualNetworkRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="70ee1-150">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="70ee1-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="70ee1-151">OUTPUTS</span></span>

### <span data-ttu-id="70ee1-152">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="70ee1-152">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="70ee1-153">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="70ee1-153">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="70ee1-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="70ee1-154">NOTES</span></span>

## <span data-ttu-id="70ee1-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="70ee1-155">RELATED LINKS</span></span>
