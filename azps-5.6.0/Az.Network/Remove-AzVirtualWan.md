---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: ae05b4afd18bb1cdb55c8c1b748068f1f6c5191f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922755"
---
# <span data-ttu-id="c595b-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c595b-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="c595b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c595b-102">SYNOPSIS</span></span>
<span data-ttu-id="c595b-103">Entfernt ein virtuelles Azure-WAN.</span><span class="sxs-lookup"><span data-stu-id="c595b-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="c595b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c595b-104">SYNTAX</span></span>

### <span data-ttu-id="c595b-105">ByVirtualWanName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c595b-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c595b-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="c595b-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c595b-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="c595b-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c595b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c595b-108">DESCRIPTION</span></span>
<span data-ttu-id="c595b-109">Entfernt ein virtuelles Azure-WAN.</span><span class="sxs-lookup"><span data-stu-id="c595b-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="c595b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c595b-110">EXAMPLES</span></span>

### <span data-ttu-id="c595b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c595b-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="c595b-112">In diesem Beispiel wird ein virtuelles WAN in einer Ressourcengruppe erstellt und dann sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c595b-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="c595b-113">Wenn Sie die Eingabeaufforderung beim Löschen des virtuellen WAN unterdrücken möchten, verwenden Sie das -Force-Flag.</span><span class="sxs-lookup"><span data-stu-id="c595b-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="c595b-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c595b-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="c595b-115">In diesem Beispiel wird ein virtuelles WAN in einer Ressourcengruppe erstellt und dann sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c595b-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="c595b-116">Dieser Löschvorgang erfolgt mithilfe des virtuellen wan-Objekts, das von New-AzVirtualWan zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c595b-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="c595b-117">Wenn Sie die Eingabeaufforderung beim Löschen des virtuellen WAN unterdrücken möchten, verwenden Sie das -Force-Flag.</span><span class="sxs-lookup"><span data-stu-id="c595b-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="c595b-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c595b-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="c595b-119">In diesem Beispiel wird ein virtuelles WAN in einer Ressourcengruppe erstellt und dann sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c595b-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="c595b-120">Dieser Löschvorgang erfolgt mithilfe der virtuellen Wan-Ressourcen-ID, die von New-AzVirtualWan zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c595b-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="c595b-121">Wenn Sie die Eingabeaufforderung beim Löschen des virtuellen WAN unterdrücken möchten, verwenden Sie das -Force-Flag.</span><span class="sxs-lookup"><span data-stu-id="c595b-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="c595b-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c595b-122">PARAMETERS</span></span>

### <span data-ttu-id="c595b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c595b-123">-DefaultProfile</span></span>
<span data-ttu-id="c595b-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c595b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c595b-125">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="c595b-125">-Force</span></span>
<span data-ttu-id="c595b-126">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="c595b-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c595b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c595b-127">-InputObject</span></span>
<span data-ttu-id="c595b-128">Das zu löschende virtuelle Wan-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c595b-128">The virtual wan object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c595b-129">-Name</span><span class="sxs-lookup"><span data-stu-id="c595b-129">-Name</span></span>
<span data-ttu-id="c595b-130">Der virtuelle Wanname.</span><span class="sxs-lookup"><span data-stu-id="c595b-130">The virtual wan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c595b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c595b-131">-PassThru</span></span>
<span data-ttu-id="c595b-132">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c595b-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c595b-133">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="c595b-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c595b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c595b-134">-ResourceGroupName</span></span>
<span data-ttu-id="c595b-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c595b-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c595b-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c595b-136">-ResourceId</span></span>
<span data-ttu-id="c595b-137">Die Azure-Ressourcen-ID für das virtuelle Wan, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="c595b-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c595b-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c595b-138">-Confirm</span></span>
<span data-ttu-id="c595b-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c595b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c595b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c595b-140">-WhatIf</span></span>
<span data-ttu-id="c595b-141">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c595b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c595b-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c595b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c595b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c595b-143">CommonParameters</span></span>
<span data-ttu-id="c595b-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c595b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c595b-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c595b-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c595b-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c595b-146">INPUTS</span></span>

### <span data-ttu-id="c595b-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c595b-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="c595b-148">System.String</span><span class="sxs-lookup"><span data-stu-id="c595b-148">System.String</span></span>

## <span data-ttu-id="c595b-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c595b-149">OUTPUTS</span></span>

### <span data-ttu-id="c595b-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c595b-150">System.Boolean</span></span>

## <span data-ttu-id="c595b-151">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c595b-151">NOTES</span></span>

## <span data-ttu-id="c595b-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c595b-152">RELATED LINKS</span></span>

[<span data-ttu-id="c595b-153">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c595b-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="c595b-154">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c595b-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="c595b-155">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c595b-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
