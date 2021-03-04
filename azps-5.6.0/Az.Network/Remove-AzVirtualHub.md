---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
ms.openlocfilehash: 7a5724346f1b94af0dbc07df16f9cdab5f798523
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945880"
---
# <span data-ttu-id="4f8da-101">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4f8da-101">Remove-AzVirtualHub</span></span>

## <span data-ttu-id="4f8da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f8da-102">SYNOPSIS</span></span>
<span data-ttu-id="4f8da-103">Entfernt eine Azure VirtualHub-Ressource.</span><span class="sxs-lookup"><span data-stu-id="4f8da-103">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="4f8da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f8da-104">SYNTAX</span></span>

### <span data-ttu-id="4f8da-105">ByVirtualHubName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4f8da-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f8da-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="4f8da-106">ByVirtualHubResourceId</span></span>
```
Remove-AzVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f8da-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="4f8da-107">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f8da-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f8da-108">DESCRIPTION</span></span>
<span data-ttu-id="4f8da-109">Entfernt eine Azure VirtualHub-Ressource.</span><span class="sxs-lookup"><span data-stu-id="4f8da-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="4f8da-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4f8da-110">EXAMPLES</span></span>

### <span data-ttu-id="4f8da-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4f8da-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="4f8da-112">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe "testRG", ein virtuelles WAN und ein virtueller Hub in West USA in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="4f8da-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="4f8da-113">Der virtuelle Hub hat den Adressbereich "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="4f8da-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="4f8da-114">Anschließend löscht er den virtuellen Hub mit seinem ResourceGroupName und ResourceName.</span><span class="sxs-lookup"><span data-stu-id="4f8da-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="4f8da-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4f8da-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="4f8da-116">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe "testRG", ein virtuelles WAN und ein virtueller Hub in West USA in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="4f8da-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="4f8da-117">Der virtuelle Hub hat den Adressbereich "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="4f8da-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="4f8da-118">Anschließend wird der virtuelle Hub mithilfe eines Eingabeobjekts gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4f8da-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="4f8da-119">Das Eingabeobjekt hat den Typ PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="4f8da-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="4f8da-120">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4f8da-120">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzVirtualHub
```

<span data-ttu-id="4f8da-121">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe "testRG", ein virtuelles WAN und ein virtueller Hub in West USA in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="4f8da-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="4f8da-122">Der virtuelle Hub hat den Adressbereich "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="4f8da-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="4f8da-123">Anschließend wird der virtuelle Hub mithilfe von Powershellpipeing mithilfe der Ausgabe von Get-AzVirtualHub gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4f8da-123">It then deletes the virtual hub using powershell piping using output from Get-AzVirtualHub.</span></span>

## <span data-ttu-id="4f8da-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4f8da-124">PARAMETERS</span></span>

### <span data-ttu-id="4f8da-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f8da-125">-AsJob</span></span>
<span data-ttu-id="4f8da-126">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4f8da-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f8da-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f8da-127">-DefaultProfile</span></span>
<span data-ttu-id="4f8da-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f8da-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f8da-129">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="4f8da-129">-Force</span></span>
<span data-ttu-id="4f8da-130">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="4f8da-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4f8da-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f8da-131">-InputObject</span></span>
<span data-ttu-id="4f8da-132">Das zu ändernde Virtual Hub-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4f8da-132">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="4f8da-133">-Name</span><span class="sxs-lookup"><span data-stu-id="4f8da-133">-Name</span></span>
<span data-ttu-id="4f8da-134">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="4f8da-134">The resource name.</span></span>

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

### <span data-ttu-id="4f8da-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f8da-135">-PassThru</span></span>
<span data-ttu-id="4f8da-136">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="4f8da-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4f8da-137">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="4f8da-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4f8da-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f8da-138">-ResourceGroupName</span></span>
<span data-ttu-id="4f8da-139">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4f8da-139">The resource group name.</span></span>

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

### <span data-ttu-id="4f8da-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f8da-140">-ResourceId</span></span>
<span data-ttu-id="4f8da-141">Die Ressourcen-ID des virtuellen Hubs, der geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f8da-141">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="4f8da-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4f8da-142">-Confirm</span></span>
<span data-ttu-id="4f8da-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f8da-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f8da-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f8da-144">-WhatIf</span></span>
<span data-ttu-id="4f8da-145">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f8da-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f8da-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f8da-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f8da-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f8da-147">CommonParameters</span></span>
<span data-ttu-id="4f8da-148">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f8da-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f8da-149">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f8da-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f8da-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4f8da-150">INPUTS</span></span>

### <span data-ttu-id="4f8da-151">System.String</span><span class="sxs-lookup"><span data-stu-id="4f8da-151">System.String</span></span>

### <span data-ttu-id="4f8da-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4f8da-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="4f8da-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4f8da-153">OUTPUTS</span></span>

### <span data-ttu-id="4f8da-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4f8da-154">System.Boolean</span></span>

## <span data-ttu-id="4f8da-155">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4f8da-155">NOTES</span></span>

## <span data-ttu-id="4f8da-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4f8da-156">RELATED LINKS</span></span>

[<span data-ttu-id="4f8da-157">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4f8da-157">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="4f8da-158">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4f8da-158">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="4f8da-159">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4f8da-159">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
