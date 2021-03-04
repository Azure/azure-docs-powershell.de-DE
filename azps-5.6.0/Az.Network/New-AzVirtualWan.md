---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 3bb2a2d7c8e53cc7ba336234e3c5b24ad58e2faa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941064"
---
# <span data-ttu-id="2d3cc-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="2d3cc-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="2d3cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d3cc-102">SYNOPSIS</span></span>
<span data-ttu-id="2d3cc-103">Erstellt ein virtuelles Azure WAN.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="2d3cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d3cc-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-VirtualWANType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d3cc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d3cc-105">DESCRIPTION</span></span>
<span data-ttu-id="2d3cc-106">Erstellt eine neue Azure VirtualWAN-Ressource.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="2d3cc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2d3cc-107">EXAMPLES</span></span>

### <span data-ttu-id="2d3cc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2d3cc-108">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="2d3cc-109">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe "testRG" in der Region "West US" und ein virtuelles Azure WAN mit In-Branch-Datenverkehr erstellt, der in dieser Ressourcengruppe in Azure zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="2d3cc-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2d3cc-110">PARAMETERS</span></span>

### <span data-ttu-id="2d3cc-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="2d3cc-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="2d3cc-112">Branch to branch traffic for VirtualWan zulassen.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="2d3cc-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="2d3cc-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="2d3cc-114">Zulassen, dass vnet-Datenverkehr für VirtualWan verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="2d3cc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d3cc-115">-AsJob</span></span>
<span data-ttu-id="2d3cc-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2d3cc-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d3cc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d3cc-117">-DefaultProfile</span></span>
<span data-ttu-id="2d3cc-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d3cc-119">-Location</span><span class="sxs-lookup"><span data-stu-id="2d3cc-119">-Location</span></span>
<span data-ttu-id="2d3cc-120">Der Speicherort der VirtualWAN-Ressource.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-120">The location of the VirtualWAN resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3cc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2d3cc-121">-Name</span></span>
<span data-ttu-id="2d3cc-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3cc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d3cc-123">-ResourceGroupName</span></span>
<span data-ttu-id="2d3cc-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3cc-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="2d3cc-125">-Tag</span></span>
<span data-ttu-id="2d3cc-126">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="2d3cc-127">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="2d3cc-127">-VirtualWANType</span></span>
<span data-ttu-id="2d3cc-128">Der Typ des virtuellen Wan.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-128">The type of the Virtual Wan.</span></span>

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

### <span data-ttu-id="2d3cc-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2d3cc-129">-Confirm</span></span>
<span data-ttu-id="2d3cc-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d3cc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d3cc-131">-WhatIf</span></span>
<span data-ttu-id="2d3cc-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d3cc-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d3cc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d3cc-134">CommonParameters</span></span>
<span data-ttu-id="2d3cc-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d3cc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d3cc-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d3cc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d3cc-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2d3cc-137">INPUTS</span></span>

### <span data-ttu-id="2d3cc-138">Keine</span><span class="sxs-lookup"><span data-stu-id="2d3cc-138">None</span></span>

## <span data-ttu-id="2d3cc-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2d3cc-139">OUTPUTS</span></span>

### <span data-ttu-id="2d3cc-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="2d3cc-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="2d3cc-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2d3cc-141">NOTES</span></span>

## <span data-ttu-id="2d3cc-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2d3cc-142">RELATED LINKS</span></span>

[<span data-ttu-id="2d3cc-143">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="2d3cc-143">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="2d3cc-144">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="2d3cc-144">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="2d3cc-145">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="2d3cc-145">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
