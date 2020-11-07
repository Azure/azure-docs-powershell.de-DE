---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageAccountNetworkRule.md
ms.openlocfilehash: 9f8d098cb27532980b01cf46da6c83d4da30ed48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663296"
---
# <span data-ttu-id="11e3a-101">Add-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="11e3a-101">Add-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="11e3a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="11e3a-102">SYNOPSIS</span></span>
 <span data-ttu-id="11e3a-103">Hinzufügen von IpRules oder VirtualNetworkRules zur NetworkRule-Eigenschaft eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="11e3a-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11e3a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="11e3a-104">SYNTAX</span></span>

### <span data-ttu-id="11e3a-105">NetWorkRuleString (Standard)</span><span class="sxs-lookup"><span data-stu-id="11e3a-105">NetWorkRuleString (Default)</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11e3a-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="11e3a-106">IpRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11e3a-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="11e3a-107">NetworkRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11e3a-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="11e3a-108">IpRuleString</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11e3a-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11e3a-109">DESCRIPTION</span></span>
<span data-ttu-id="11e3a-110">Das **Add-AzureRmStorageAccountNetworkRule-** Cmdlet fügt IpRules oder VirtualNetworkRules der NetworkRule-Eigenschaft eines speicherkontos hinzu.</span><span class="sxs-lookup"><span data-stu-id="11e3a-110">The **Add-AzureRmStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage Account</span></span>

## <span data-ttu-id="11e3a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11e3a-111">EXAMPLES</span></span>

### <span data-ttu-id="11e3a-112">Beispiel 1: Hinzufügen mehrerer IpRules mit IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="11e3a-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="11e3a-113">Mit diesem Befehl werden mehrere IpRules mit IPAddressOrRange hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="11e3a-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="11e3a-114">Beispiel 2: Hinzufügen eines VirtualNetworkRule mit VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="11e3a-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzureRmVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzureRmVirtualNetworkSubnetConfig
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="11e3a-115">Mit diesem Befehl wird ein VirtualNetworkRule mit VirtualNetworkResourceID hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="11e3a-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="11e3a-116">Beispiel 3: Hinzufügen von VirtualNetworkRules mit VirtualNetworkRule-Objekten aus einem anderen Konto</span><span class="sxs-lookup"><span data-stu-id="11e3a-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzureRMStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount1"
PS C:\> Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="11e3a-117">Mit diesem Befehl fügen Sie VirtualNetworkRules mit VirtualNetworkRule-Objekten aus einem anderen Konto hinzu.</span><span class="sxs-lookup"><span data-stu-id="11e3a-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="11e3a-118">Beispiel 4: Hinzufügen mehrerer IpRule mit IpRule-Objekten, Eingabe mit JSON</span><span class="sxs-lookup"><span data-stu-id="11e3a-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="11e3a-119">Dieser Befehl fügt mehrere IpRule mit IpRule-Objekten hinzu, die mit JSON eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="11e3a-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="11e3a-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="11e3a-120">PARAMETERS</span></span>

### <span data-ttu-id="11e3a-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="11e3a-121">-IPAddressOrRange</span></span>
<span data-ttu-id="11e3a-122">Das Array von IpAddressOrRange, fügen Sie IpRules mit der Eingabe IpAddressOrRange und der Standardaktion NetworkRule-Eigenschaft zulassen hinzu.</span><span class="sxs-lookup"><span data-stu-id="11e3a-122">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="11e3a-123">-IPRule</span><span class="sxs-lookup"><span data-stu-id="11e3a-123">-IPRule</span></span>
<span data-ttu-id="11e3a-124">Das Array der IpRule-Objekte, die der NetworkRule-Eigenschaft hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="11e3a-124">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="11e3a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="11e3a-125">-Name</span></span>
<span data-ttu-id="11e3a-126">Gibt den Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="11e3a-126">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="11e3a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11e3a-127">-ResourceGroupName</span></span>
<span data-ttu-id="11e3a-128">Gibt den Namen der Ressourcengruppe mit dem Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="11e3a-128">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="11e3a-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="11e3a-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="11e3a-130">Das VirtualNetworkResourceId-Array fügt VirtualNetworkRule mit der Eingabe VirtualNetworkResourceId und der Standardaktion für die NetworkRule-Eigenschaft hinzu.</span><span class="sxs-lookup"><span data-stu-id="11e3a-130">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="11e3a-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="11e3a-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="11e3a-132">Das Array der VirtualNetworkRule-Objekte, die der NetworkRule-Eigenschaft hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="11e3a-132">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="11e3a-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="11e3a-133">-Confirm</span></span>
<span data-ttu-id="11e3a-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="11e3a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11e3a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11e3a-135">-WhatIf</span></span>
<span data-ttu-id="11e3a-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="11e3a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11e3a-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="11e3a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11e3a-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e3a-138">-DefaultProfile</span></span>
<span data-ttu-id="11e3a-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="11e3a-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11e3a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e3a-140">CommonParameters</span></span>
<span data-ttu-id="11e3a-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11e3a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e3a-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11e3a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e3a-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="11e3a-143">INPUTS</span></span>

### <span data-ttu-id="11e3a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="11e3a-144">System.String</span></span>
<span data-ttu-id="11e3a-145">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule [] Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="11e3a-145">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="11e3a-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="11e3a-146">OUTPUTS</span></span>

### <span data-ttu-id="11e3a-147">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="11e3a-147">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>
<span data-ttu-id="11e3a-148">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="11e3a-148">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="11e3a-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="11e3a-149">NOTES</span></span>

## <span data-ttu-id="11e3a-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="11e3a-150">RELATED LINKS</span></span>

