---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
ms.openlocfilehash: c620c2f927fa5de60a637f45e8f0ff64f2a25b27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660318"
---
# <span data-ttu-id="c565e-101">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c565e-101">Remove-AzVirtualHub</span></span>

## <span data-ttu-id="c565e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c565e-102">SYNOPSIS</span></span>
<span data-ttu-id="c565e-103">Entfernt eine Azure VirtualHub-Ressource.</span><span class="sxs-lookup"><span data-stu-id="c565e-103">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="c565e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c565e-104">SYNTAX</span></span>

### <span data-ttu-id="c565e-105">ByVirtualHubName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c565e-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c565e-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="c565e-106">ByVirtualHubResourceId</span></span>
```
Remove-AzVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c565e-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="c565e-107">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c565e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c565e-108">DESCRIPTION</span></span>
<span data-ttu-id="c565e-109">Entfernt eine Azure VirtualHub-Ressource.</span><span class="sxs-lookup"><span data-stu-id="c565e-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="c565e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c565e-110">EXAMPLES</span></span>

### <span data-ttu-id="c565e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c565e-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="c565e-112">Das oben beschriebene erstellt eine Ressourcengruppe "testRG", ein virtuelles WAN und einen virtuellen Hub in West-USA in dieser Ressourcengruppe in Azure.</span><span class="sxs-lookup"><span data-stu-id="c565e-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="c565e-113">Der virtuelle Hub hat den Adressbereich "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="c565e-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="c565e-114">Anschließend wird der virtuelle Hub mithilfe des ResourceGroupName-und resourceName-Knotens gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c565e-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="c565e-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c565e-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="c565e-116">Das oben beschriebene erstellt eine Ressourcengruppe "testRG", ein virtuelles WAN und einen virtuellen Hub in West-USA in dieser Ressourcengruppe in Azure.</span><span class="sxs-lookup"><span data-stu-id="c565e-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="c565e-117">Der virtuelle Hub hat den Adressbereich "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="c565e-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="c565e-118">Anschließend wird der virtuelle Hub mit einem Eingabeobjekt gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c565e-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="c565e-119">Das Eingabeobjekt ist vom Typ PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="c565e-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="c565e-120">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c565e-120">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzVirtualHub
```

<span data-ttu-id="c565e-121">Das oben beschriebene erstellt eine Ressourcengruppe "testRG", ein virtuelles WAN und einen virtuellen Hub in West-USA in dieser Ressourcengruppe in Azure.</span><span class="sxs-lookup"><span data-stu-id="c565e-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="c565e-122">Der virtuelle Hub hat den Adressbereich "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="c565e-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="c565e-123">Anschließend wird der virtuelle Hub mithilfe der PowerShell-Rohrverlegung mithilfe der Ausgabe von Get-AzVirtualHub gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c565e-123">It then deletes the virtual hub using powershell piping using output from Get-AzVirtualHub.</span></span>

## <span data-ttu-id="c565e-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="c565e-124">PARAMETERS</span></span>

### <span data-ttu-id="c565e-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c565e-125">-AsJob</span></span>
<span data-ttu-id="c565e-126">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c565e-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c565e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c565e-127">-DefaultProfile</span></span>
<span data-ttu-id="c565e-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c565e-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c565e-129">-Force</span><span class="sxs-lookup"><span data-stu-id="c565e-129">-Force</span></span>
<span data-ttu-id="c565e-130">Keine Bestätigung anfordern, wenn Sie eine Ressource overriten möchten</span><span class="sxs-lookup"><span data-stu-id="c565e-130">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="c565e-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c565e-131">-InputObject</span></span>
<span data-ttu-id="c565e-132">Das virtuelle Hub-Objekt, das geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c565e-132">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c565e-133">-Name</span><span class="sxs-lookup"><span data-stu-id="c565e-133">-Name</span></span>
<span data-ttu-id="c565e-134">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="c565e-134">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c565e-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c565e-135">-PassThru</span></span>
<span data-ttu-id="c565e-136">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c565e-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c565e-137">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="c565e-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c565e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c565e-138">-ResourceGroupName</span></span>
<span data-ttu-id="c565e-139">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c565e-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c565e-140">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c565e-140">-ResourceId</span></span>
<span data-ttu-id="c565e-141">Die Ressourcen-ID des virtuellen Hubs, der geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c565e-141">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c565e-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c565e-142">-Confirm</span></span>
<span data-ttu-id="c565e-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c565e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c565e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c565e-144">-WhatIf</span></span>
<span data-ttu-id="c565e-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c565e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c565e-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c565e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c565e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c565e-147">CommonParameters</span></span>
<span data-ttu-id="c565e-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c565e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c565e-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c565e-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c565e-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c565e-150">INPUTS</span></span>

### <span data-ttu-id="c565e-151">System. String</span><span class="sxs-lookup"><span data-stu-id="c565e-151">System.String</span></span>

### <span data-ttu-id="c565e-152">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c565e-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="c565e-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c565e-153">OUTPUTS</span></span>

### <span data-ttu-id="c565e-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c565e-154">System.Boolean</span></span>

## <span data-ttu-id="c565e-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="c565e-155">NOTES</span></span>

## <span data-ttu-id="c565e-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c565e-156">RELATED LINKS</span></span>

[<span data-ttu-id="c565e-157">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c565e-157">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="c565e-158">Neu – AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c565e-158">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="c565e-159">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c565e-159">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
