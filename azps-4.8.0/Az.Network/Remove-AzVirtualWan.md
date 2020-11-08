---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: 802a87b4ba420fb84036756185c68a6250e70920
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174282"
---
# <span data-ttu-id="3dafe-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="3dafe-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="3dafe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3dafe-102">SYNOPSIS</span></span>
<span data-ttu-id="3dafe-103">Entfernt ein Azure-virtuelles WAN.</span><span class="sxs-lookup"><span data-stu-id="3dafe-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="3dafe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3dafe-104">SYNTAX</span></span>

### <span data-ttu-id="3dafe-105">ByVirtualWanName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3dafe-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dafe-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="3dafe-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dafe-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="3dafe-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dafe-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3dafe-108">DESCRIPTION</span></span>
<span data-ttu-id="3dafe-109">Entfernt ein Azure-virtuelles WAN.</span><span class="sxs-lookup"><span data-stu-id="3dafe-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="3dafe-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3dafe-110">EXAMPLES</span></span>

### <span data-ttu-id="3dafe-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3dafe-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="3dafe-112">In diesem Beispiel wird ein virtuelles WAN in einer Ressourcengruppe erstellt und anschließend sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3dafe-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="3dafe-113">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen des virtuellen WAN zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="3dafe-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="3dafe-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3dafe-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="3dafe-115">In diesem Beispiel wird ein virtuelles WAN in einer Ressourcengruppe erstellt und anschließend sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3dafe-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="3dafe-116">Dieser Löschvorgang erfolgt mithilfe des virtuellen WAN-Objekts, das von New-AzVirtualWan zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3dafe-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="3dafe-117">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen des virtuellen WAN zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="3dafe-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="3dafe-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="3dafe-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="3dafe-119">In diesem Beispiel wird ein virtuelles WAN in einer Ressourcengruppe erstellt und anschließend sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3dafe-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="3dafe-120">Dieser Löschvorgang erfolgt mithilfe der virtuellen WAN-Ressourcen-ID, die von New-AzVirtualWan zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3dafe-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="3dafe-121">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen des virtuellen WAN zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="3dafe-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="3dafe-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="3dafe-122">PARAMETERS</span></span>

### <span data-ttu-id="3dafe-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dafe-123">-DefaultProfile</span></span>
<span data-ttu-id="3dafe-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3dafe-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dafe-125">-Force</span><span class="sxs-lookup"><span data-stu-id="3dafe-125">-Force</span></span>
<span data-ttu-id="3dafe-126">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="3dafe-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3dafe-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3dafe-127">-InputObject</span></span>
<span data-ttu-id="3dafe-128">Das virtuelle WAN-Objekt, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="3dafe-128">The virtual wan object to be deleted.</span></span>

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

### <span data-ttu-id="3dafe-129">-Name</span><span class="sxs-lookup"><span data-stu-id="3dafe-129">-Name</span></span>
<span data-ttu-id="3dafe-130">Der virtuelle WAN-Name.</span><span class="sxs-lookup"><span data-stu-id="3dafe-130">The virtual wan name.</span></span>

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

### <span data-ttu-id="3dafe-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3dafe-131">-PassThru</span></span>
<span data-ttu-id="3dafe-132">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="3dafe-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3dafe-133">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="3dafe-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3dafe-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dafe-134">-ResourceGroupName</span></span>
<span data-ttu-id="3dafe-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3dafe-135">The resource group name.</span></span>

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

### <span data-ttu-id="3dafe-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3dafe-136">-ResourceId</span></span>
<span data-ttu-id="3dafe-137">Die Azure-Ressourcen-ID für das virtuelle WAN, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="3dafe-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

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

### <span data-ttu-id="3dafe-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3dafe-138">-Confirm</span></span>
<span data-ttu-id="3dafe-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3dafe-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dafe-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dafe-140">-WhatIf</span></span>
<span data-ttu-id="3dafe-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3dafe-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dafe-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3dafe-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dafe-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dafe-143">CommonParameters</span></span>
<span data-ttu-id="3dafe-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dafe-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dafe-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dafe-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dafe-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3dafe-146">INPUTS</span></span>

### <span data-ttu-id="3dafe-147">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="3dafe-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="3dafe-148">System. String</span><span class="sxs-lookup"><span data-stu-id="3dafe-148">System.String</span></span>

## <span data-ttu-id="3dafe-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3dafe-149">OUTPUTS</span></span>

### <span data-ttu-id="3dafe-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3dafe-150">System.Boolean</span></span>

## <span data-ttu-id="3dafe-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="3dafe-151">NOTES</span></span>

## <span data-ttu-id="3dafe-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3dafe-152">RELATED LINKS</span></span>

[<span data-ttu-id="3dafe-153">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="3dafe-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="3dafe-154">Neu – AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="3dafe-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="3dafe-155">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="3dafe-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
