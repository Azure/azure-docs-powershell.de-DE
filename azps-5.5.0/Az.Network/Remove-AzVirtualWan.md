---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: 802a87b4ba420fb84036756185c68a6250e70920
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146649"
---
# <span data-ttu-id="086a2-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="086a2-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="086a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="086a2-102">SYNOPSIS</span></span>
<span data-ttu-id="086a2-103">Entfernt ein virtuelles Azure-WAN.</span><span class="sxs-lookup"><span data-stu-id="086a2-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="086a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="086a2-104">SYNTAX</span></span>

### <span data-ttu-id="086a2-105">ByVirtualWanName (Standard)</span><span class="sxs-lookup"><span data-stu-id="086a2-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="086a2-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="086a2-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="086a2-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="086a2-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="086a2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="086a2-108">DESCRIPTION</span></span>
<span data-ttu-id="086a2-109">Entfernt ein virtuelles Azure-WAN.</span><span class="sxs-lookup"><span data-stu-id="086a2-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="086a2-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="086a2-110">EXAMPLES</span></span>

### <span data-ttu-id="086a2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="086a2-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="086a2-112">In diesem Beispiel wird ein virtuelles WAN in einer Ressourcengruppe erstellt und dann sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="086a2-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="086a2-113">Verwenden Sie das Kennzeichen "-Force", um die Eingabeaufforderung beim Löschen des virtuellen WAN zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="086a2-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="086a2-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="086a2-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="086a2-115">In diesem Beispiel wird ein virtuelles WAN in einer Ressourcengruppe erstellt und dann sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="086a2-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="086a2-116">Dieser Löschvorgang erfolgt mithilfe des virtuellen WAN-Objekts, das von "New-AzVirtualWan" zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="086a2-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="086a2-117">Verwenden Sie das Kennzeichen "-Force", um die Eingabeaufforderung beim Löschen des virtuellen WAN zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="086a2-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="086a2-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="086a2-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="086a2-119">In diesem Beispiel wird ein virtuelles WAN in einer Ressourcengruppe erstellt und dann sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="086a2-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="086a2-120">Dieser Löschvorgang erfolgt mithilfe der virtuellen WAN-Ressourcen-ID, die von New-AzVirtualWan zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="086a2-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="086a2-121">Verwenden Sie das Kennzeichen "-Force", um die Eingabeaufforderung beim Löschen des virtuellen WAN zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="086a2-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="086a2-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="086a2-122">PARAMETERS</span></span>

### <span data-ttu-id="086a2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="086a2-123">-DefaultProfile</span></span>
<span data-ttu-id="086a2-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="086a2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="086a2-125">-Force</span><span class="sxs-lookup"><span data-stu-id="086a2-125">-Force</span></span>
<span data-ttu-id="086a2-126">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="086a2-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="086a2-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="086a2-127">-InputObject</span></span>
<span data-ttu-id="086a2-128">Das virtuelle wan-Objekt, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="086a2-128">The virtual wan object to be deleted.</span></span>

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

### <span data-ttu-id="086a2-129">-Name</span><span class="sxs-lookup"><span data-stu-id="086a2-129">-Name</span></span>
<span data-ttu-id="086a2-130">Der virtuelle Wan-Name.</span><span class="sxs-lookup"><span data-stu-id="086a2-130">The virtual wan name.</span></span>

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

### <span data-ttu-id="086a2-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="086a2-131">-PassThru</span></span>
<span data-ttu-id="086a2-132">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="086a2-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="086a2-133">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="086a2-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="086a2-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="086a2-134">-ResourceGroupName</span></span>
<span data-ttu-id="086a2-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="086a2-135">The resource group name.</span></span>

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

### <span data-ttu-id="086a2-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="086a2-136">-ResourceId</span></span>
<span data-ttu-id="086a2-137">Die Azure-Ressourcen-ID für das zu löschende virtuelle Wan.</span><span class="sxs-lookup"><span data-stu-id="086a2-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

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

### <span data-ttu-id="086a2-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="086a2-138">-Confirm</span></span>
<span data-ttu-id="086a2-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="086a2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="086a2-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="086a2-140">-WhatIf</span></span>
<span data-ttu-id="086a2-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="086a2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="086a2-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="086a2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="086a2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="086a2-143">CommonParameters</span></span>
<span data-ttu-id="086a2-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="086a2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="086a2-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="086a2-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="086a2-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="086a2-146">INPUTS</span></span>

### <span data-ttu-id="086a2-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="086a2-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="086a2-148">System.String</span><span class="sxs-lookup"><span data-stu-id="086a2-148">System.String</span></span>

## <span data-ttu-id="086a2-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="086a2-149">OUTPUTS</span></span>

### <span data-ttu-id="086a2-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="086a2-150">System.Boolean</span></span>

## <span data-ttu-id="086a2-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="086a2-151">NOTES</span></span>

## <span data-ttu-id="086a2-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="086a2-152">RELATED LINKS</span></span>

[<span data-ttu-id="086a2-153">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="086a2-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="086a2-154">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="086a2-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="086a2-155">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="086a2-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
