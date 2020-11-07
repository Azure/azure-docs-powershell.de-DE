---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: d1ec777d6574aa34a6b19fa7cdc94d9c349dbc48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660299"
---
# <span data-ttu-id="8cbf5-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8cbf5-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="8cbf5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8cbf5-102">SYNOPSIS</span></span>
<span data-ttu-id="8cbf5-103">Entfernt ein Azure-virtuelles WAN.</span><span class="sxs-lookup"><span data-stu-id="8cbf5-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="8cbf5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cbf5-104">SYNTAX</span></span>

### <span data-ttu-id="8cbf5-105">ByVirtualWanName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8cbf5-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cbf5-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="8cbf5-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cbf5-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="8cbf5-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cbf5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cbf5-108">DESCRIPTION</span></span>
<span data-ttu-id="8cbf5-109">Entfernt ein Azure-virtuelles WAN.</span><span class="sxs-lookup"><span data-stu-id="8cbf5-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="8cbf5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8cbf5-110">EXAMPLES</span></span>

### <span data-ttu-id="8cbf5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8cbf5-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="8cbf5-112">In diesem Beispiel wird ein virtuelles WAN in einer Ressourcengruppe erstellt und anschließend sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8cbf5-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="8cbf5-113">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen des virtuellen WAN zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="8cbf5-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="8cbf5-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8cbf5-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="8cbf5-115">In diesem Beispiel wird ein virtuelles WAN in einer Ressourcengruppe erstellt und anschließend sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8cbf5-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="8cbf5-116">Dieser Löschvorgang erfolgt mithilfe des virtuellen WAN-Objekts, das von New-AzVirtualWan zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8cbf5-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="8cbf5-117">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen des virtuellen WAN zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="8cbf5-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="8cbf5-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="8cbf5-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="8cbf5-119">In diesem Beispiel wird ein virtuelles WAN in einer Ressourcengruppe erstellt und anschließend sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8cbf5-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="8cbf5-120">Dieser Löschvorgang erfolgt mithilfe der virtuellen WAN-Ressourcen-ID, die von New-AzVirtualWan zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8cbf5-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="8cbf5-121">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen des virtuellen WAN zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="8cbf5-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="8cbf5-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cbf5-122">PARAMETERS</span></span>

### <span data-ttu-id="8cbf5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cbf5-123">-DefaultProfile</span></span>
<span data-ttu-id="8cbf5-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8cbf5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cbf5-125">-Force</span><span class="sxs-lookup"><span data-stu-id="8cbf5-125">-Force</span></span>
<span data-ttu-id="8cbf5-126">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="8cbf5-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8cbf5-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8cbf5-127">-InputObject</span></span>
<span data-ttu-id="8cbf5-128">Das virtuelle WAN-Objekt, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="8cbf5-128">The virtual wan object to be deleted.</span></span>

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

### <span data-ttu-id="8cbf5-129">-Name</span><span class="sxs-lookup"><span data-stu-id="8cbf5-129">-Name</span></span>
<span data-ttu-id="8cbf5-130">Der virtuelle WAN-Name.</span><span class="sxs-lookup"><span data-stu-id="8cbf5-130">The virtual wan name.</span></span>

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

### <span data-ttu-id="8cbf5-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8cbf5-131">-PassThru</span></span>
<span data-ttu-id="8cbf5-132">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="8cbf5-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8cbf5-133">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="8cbf5-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8cbf5-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cbf5-134">-ResourceGroupName</span></span>
<span data-ttu-id="8cbf5-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8cbf5-135">The resource group name.</span></span>

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

### <span data-ttu-id="8cbf5-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8cbf5-136">-ResourceId</span></span>
<span data-ttu-id="8cbf5-137">Die Azure-Ressourcen-ID für das virtuelle WAN, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="8cbf5-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

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

### <span data-ttu-id="8cbf5-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8cbf5-138">-Confirm</span></span>
<span data-ttu-id="8cbf5-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8cbf5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cbf5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cbf5-140">-WhatIf</span></span>
<span data-ttu-id="8cbf5-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8cbf5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cbf5-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cbf5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cbf5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cbf5-143">CommonParameters</span></span>
<span data-ttu-id="8cbf5-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cbf5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cbf5-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cbf5-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cbf5-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8cbf5-146">INPUTS</span></span>

### <span data-ttu-id="8cbf5-147">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8cbf5-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="8cbf5-148">System. String</span><span class="sxs-lookup"><span data-stu-id="8cbf5-148">System.String</span></span>

## <span data-ttu-id="8cbf5-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8cbf5-149">OUTPUTS</span></span>

### <span data-ttu-id="8cbf5-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8cbf5-150">System.Boolean</span></span>

## <span data-ttu-id="8cbf5-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="8cbf5-151">NOTES</span></span>

## <span data-ttu-id="8cbf5-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8cbf5-152">RELATED LINKS</span></span>

[<span data-ttu-id="8cbf5-153">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8cbf5-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="8cbf5-154">Neu – AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8cbf5-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="8cbf5-155">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8cbf5-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
