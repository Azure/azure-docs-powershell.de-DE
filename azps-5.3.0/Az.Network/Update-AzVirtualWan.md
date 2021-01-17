---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: e93bcc320f14a8311a29c6be9824da16506ea499
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472108"
---
# <span data-ttu-id="9047f-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="9047f-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="9047f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9047f-102">SYNOPSIS</span></span>
<span data-ttu-id="9047f-103">Aktualisiert ein virtuelles Azure-WAN.</span><span class="sxs-lookup"><span data-stu-id="9047f-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="9047f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9047f-104">SYNTAX</span></span>

### <span data-ttu-id="9047f-105">ByVirtualWanName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9047f-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9047f-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="9047f-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9047f-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="9047f-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9047f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9047f-108">DESCRIPTION</span></span>
<span data-ttu-id="9047f-109">Aktualisiert ein virtuelles Azure-WAN.</span><span class="sxs-lookup"><span data-stu-id="9047f-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="9047f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9047f-110">EXAMPLES</span></span>

### <span data-ttu-id="9047f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9047f-111">Example 1</span></span>

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

<span data-ttu-id="9047f-112">Im vorstehenden Beispiel wird eine Ressourcengruppe "testRG" in der Region "West US" und ein virtuelles Azure-WAN in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="9047f-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="9047f-113">VirtualWan wird mit neuen Eigenschaften aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9047f-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="9047f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9047f-114">PARAMETERS</span></span>

### <span data-ttu-id="9047f-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="9047f-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="9047f-116">Verzweigungs-zu-Verzweigungsverkehr für VirtualWan zulassen.</span><span class="sxs-lookup"><span data-stu-id="9047f-116">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="9047f-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="9047f-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="9047f-118">Lassen Sie vnet den vnet-Datenverkehr für VirtualWan zu.</span><span class="sxs-lookup"><span data-stu-id="9047f-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="9047f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9047f-119">-AsJob</span></span>
<span data-ttu-id="9047f-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9047f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9047f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9047f-121">-DefaultProfile</span></span>
<span data-ttu-id="9047f-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9047f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9047f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9047f-123">-Force</span></span>
<span data-ttu-id="9047f-124">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="9047f-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9047f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9047f-125">-InputObject</span></span>
<span data-ttu-id="9047f-126">Das virtuelle wan-Objekt, das geändert werden soll</span><span class="sxs-lookup"><span data-stu-id="9047f-126">The virtual wan object to be modified</span></span>

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

### <span data-ttu-id="9047f-127">-Name</span><span class="sxs-lookup"><span data-stu-id="9047f-127">-Name</span></span>
<span data-ttu-id="9047f-128">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="9047f-128">The resource name.</span></span>

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

### <span data-ttu-id="9047f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9047f-129">-ResourceGroupName</span></span>
<span data-ttu-id="9047f-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9047f-130">The resource group name.</span></span>

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

### <span data-ttu-id="9047f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9047f-131">-ResourceId</span></span>
<span data-ttu-id="9047f-132">Die Azure-Ressourcen-ID für das virtuelle Wan.</span><span class="sxs-lookup"><span data-stu-id="9047f-132">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="9047f-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="9047f-133">-Tag</span></span>
<span data-ttu-id="9047f-134">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="9047f-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="9047f-135">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="9047f-135">-VirtualWANType</span></span>
<span data-ttu-id="9047f-136">Der Typ des virtuellen Wan.</span><span class="sxs-lookup"><span data-stu-id="9047f-136">The type of the Virtual Wan.</span></span>

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

### <span data-ttu-id="9047f-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9047f-137">-Confirm</span></span>
<span data-ttu-id="9047f-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9047f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9047f-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9047f-139">-WhatIf</span></span>
<span data-ttu-id="9047f-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9047f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9047f-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9047f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9047f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9047f-142">CommonParameters</span></span>
<span data-ttu-id="9047f-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9047f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9047f-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9047f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9047f-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9047f-145">INPUTS</span></span>

### <span data-ttu-id="9047f-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="9047f-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="9047f-147">System.String</span><span class="sxs-lookup"><span data-stu-id="9047f-147">System.String</span></span>

## <span data-ttu-id="9047f-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9047f-148">OUTPUTS</span></span>

### <span data-ttu-id="9047f-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="9047f-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="9047f-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9047f-150">NOTES</span></span>

## <span data-ttu-id="9047f-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9047f-151">RELATED LINKS</span></span>

[<span data-ttu-id="9047f-152">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="9047f-152">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="9047f-153">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="9047f-153">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="9047f-154">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="9047f-154">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)
