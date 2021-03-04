---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: eb6611bef2499c9aaf164ddbe2e7a31c63051751
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918352"
---
# <span data-ttu-id="0c17c-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0c17c-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="0c17c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c17c-102">SYNOPSIS</span></span>
<span data-ttu-id="0c17c-103">Aktualisiert ein virtuelles Azure WAN.</span><span class="sxs-lookup"><span data-stu-id="0c17c-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="0c17c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c17c-104">SYNTAX</span></span>

### <span data-ttu-id="0c17c-105">ByVirtualWanName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0c17c-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c17c-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="0c17c-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c17c-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="0c17c-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c17c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c17c-108">DESCRIPTION</span></span>
<span data-ttu-id="0c17c-109">Aktualisiert ein virtuelles Azure WAN.</span><span class="sxs-lookup"><span data-stu-id="0c17c-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="0c17c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0c17c-110">EXAMPLES</span></span>

### <span data-ttu-id="0c17c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0c17c-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="0c17c-112">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe "testRG" in der Region "West US" und ein virtuelles Azure-WAN in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="0c17c-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="0c17c-113">VirtualWan wird mit neuen Eigenschaften aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0c17c-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="0c17c-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0c17c-114">PARAMETERS</span></span>

### <span data-ttu-id="0c17c-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="0c17c-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="0c17c-116">Branch to branch traffic for VirtualWan zulassen.</span><span class="sxs-lookup"><span data-stu-id="0c17c-116">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c17c-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="0c17c-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="0c17c-118">Zulassen, dass vnet-Datenverkehr für VirtualWan verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0c17c-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c17c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c17c-119">-AsJob</span></span>
<span data-ttu-id="0c17c-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0c17c-120">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c17c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c17c-121">-DefaultProfile</span></span>
<span data-ttu-id="0c17c-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0c17c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c17c-123">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="0c17c-123">-Force</span></span>
<span data-ttu-id="0c17c-124">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="0c17c-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c17c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c17c-125">-InputObject</span></span>
<span data-ttu-id="0c17c-126">Das zu ändernde virtuelle Wan-Objekt</span><span class="sxs-lookup"><span data-stu-id="0c17c-126">The virtual wan object to be modified</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c17c-127">-Name</span><span class="sxs-lookup"><span data-stu-id="0c17c-127">-Name</span></span>
<span data-ttu-id="0c17c-128">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="0c17c-128">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c17c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c17c-129">-ResourceGroupName</span></span>
<span data-ttu-id="0c17c-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0c17c-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c17c-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c17c-131">-ResourceId</span></span>
<span data-ttu-id="0c17c-132">Die Azure-Ressourcen-ID für das virtuelle Wan.</span><span class="sxs-lookup"><span data-stu-id="0c17c-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c17c-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="0c17c-133">-Tag</span></span>
<span data-ttu-id="0c17c-134">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="0c17c-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c17c-135">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="0c17c-135">-VirtualWANType</span></span>
<span data-ttu-id="0c17c-136">Der Typ des virtuellen Wan.</span><span class="sxs-lookup"><span data-stu-id="0c17c-136">The type of the Virtual Wan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c17c-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0c17c-137">-Confirm</span></span>
<span data-ttu-id="0c17c-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0c17c-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c17c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c17c-139">-WhatIf</span></span>
<span data-ttu-id="0c17c-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0c17c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c17c-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0c17c-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c17c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c17c-142">CommonParameters</span></span>
<span data-ttu-id="0c17c-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c17c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c17c-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c17c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c17c-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0c17c-145">INPUTS</span></span>

### <span data-ttu-id="0c17c-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0c17c-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="0c17c-147">System.String</span><span class="sxs-lookup"><span data-stu-id="0c17c-147">System.String</span></span>

## <span data-ttu-id="0c17c-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0c17c-148">OUTPUTS</span></span>

### <span data-ttu-id="0c17c-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0c17c-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="0c17c-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0c17c-150">NOTES</span></span>

## <span data-ttu-id="0c17c-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0c17c-151">RELATED LINKS</span></span>

[<span data-ttu-id="0c17c-152">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0c17c-152">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="0c17c-153">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0c17c-153">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="0c17c-154">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0c17c-154">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)
