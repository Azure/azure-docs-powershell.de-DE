---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualHub.md
ms.openlocfilehash: 65d319749424697c882012d23bf12f87f92adbc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503501"
---
# <span data-ttu-id="25e5a-101">Remove-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="25e5a-101">Remove-AzureRmVirtualHub</span></span>

## <span data-ttu-id="25e5a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25e5a-102">SYNOPSIS</span></span>
<span data-ttu-id="25e5a-103">Entfernt eine Azure VirtualHub-Ressource.</span><span class="sxs-lookup"><span data-stu-id="25e5a-103">Removes an Azure VirtualHub resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25e5a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25e5a-104">SYNTAX</span></span>

### <span data-ttu-id="25e5a-105">ByVirtualHubName (Standard)</span><span class="sxs-lookup"><span data-stu-id="25e5a-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25e5a-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="25e5a-106">ByVirtualHubResourceId</span></span>
```
Remove-AzureRmVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25e5a-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="25e5a-107">ByVirtualHubObject</span></span>
```
Remove-AzureRmVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25e5a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25e5a-108">DESCRIPTION</span></span>
<span data-ttu-id="25e5a-109">Entfernt eine Azure VirtualHub-Ressource.</span><span class="sxs-lookup"><span data-stu-id="25e5a-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="25e5a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25e5a-110">EXAMPLES</span></span>

### <span data-ttu-id="25e5a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="25e5a-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="25e5a-112">Das oben beschriebene erstellt eine Ressourcengruppe "testRG", ein virtuelles WAN und einen virtuellen Hub in West-USA in dieser Ressourcengruppe in Azure.</span><span class="sxs-lookup"><span data-stu-id="25e5a-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="25e5a-113">Der virtuelle Hub hat den Adressbereich "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="25e5a-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="25e5a-114">Anschließend wird der virtuelle Hub mithilfe des ResourceGroupName-und resourceName-Knotens gelöscht.</span><span class="sxs-lookup"><span data-stu-id="25e5a-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="25e5a-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="25e5a-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzureRmVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="25e5a-116">Das oben beschriebene erstellt eine Ressourcengruppe "testRG", ein virtuelles WAN und einen virtuellen Hub in West-USA in dieser Ressourcengruppe in Azure.</span><span class="sxs-lookup"><span data-stu-id="25e5a-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="25e5a-117">Der virtuelle Hub hat den Adressbereich "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="25e5a-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="25e5a-118">Anschließend wird der virtuelle Hub mit einem Eingabeobjekt gelöscht.</span><span class="sxs-lookup"><span data-stu-id="25e5a-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="25e5a-119">Das Eingabeobjekt ist vom Typ PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="25e5a-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="25e5a-120">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="25e5a-120">Example 3</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzureRmVirtualHub
```

<span data-ttu-id="25e5a-121">Das oben beschriebene erstellt eine Ressourcengruppe "testRG", ein virtuelles WAN und einen virtuellen Hub in West-USA in dieser Ressourcengruppe in Azure.</span><span class="sxs-lookup"><span data-stu-id="25e5a-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="25e5a-122">Der virtuelle Hub hat den Adressbereich "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="25e5a-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="25e5a-123">Anschließend wird der virtuelle Hub mithilfe der PowerShell-Rohrverlegung mithilfe der Ausgabe von Get-AzureRmVirtualHub gelöscht.</span><span class="sxs-lookup"><span data-stu-id="25e5a-123">It then deletes the virtual hub using powershell piping using output from Get-AzureRmVirtualHub.</span></span>

## <span data-ttu-id="25e5a-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="25e5a-124">PARAMETERS</span></span>

### <span data-ttu-id="25e5a-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25e5a-125">-AsJob</span></span>
<span data-ttu-id="25e5a-126">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="25e5a-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25e5a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25e5a-127">-DefaultProfile</span></span>
<span data-ttu-id="25e5a-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="25e5a-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25e5a-129">-Force</span><span class="sxs-lookup"><span data-stu-id="25e5a-129">-Force</span></span>
<span data-ttu-id="25e5a-130">Keine Bestätigung anfordern, wenn Sie eine Ressource overriten möchten</span><span class="sxs-lookup"><span data-stu-id="25e5a-130">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="25e5a-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="25e5a-131">-InputObject</span></span>
<span data-ttu-id="25e5a-132">Das virtuelle Hub-Objekt, das geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="25e5a-132">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="25e5a-133">-Name</span><span class="sxs-lookup"><span data-stu-id="25e5a-133">-Name</span></span>
<span data-ttu-id="25e5a-134">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="25e5a-134">The resource name.</span></span>

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

### <span data-ttu-id="25e5a-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25e5a-135">-PassThru</span></span>
<span data-ttu-id="25e5a-136">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="25e5a-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="25e5a-137">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="25e5a-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="25e5a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25e5a-138">-ResourceGroupName</span></span>
<span data-ttu-id="25e5a-139">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="25e5a-139">The resource group name.</span></span>

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

### <span data-ttu-id="25e5a-140">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="25e5a-140">-ResourceId</span></span>
<span data-ttu-id="25e5a-141">Die Ressourcen-ID des virtuellen Hubs, der geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="25e5a-141">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="25e5a-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="25e5a-142">-Confirm</span></span>
<span data-ttu-id="25e5a-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25e5a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25e5a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25e5a-144">-WhatIf</span></span>
<span data-ttu-id="25e5a-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25e5a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25e5a-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25e5a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25e5a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e5a-147">CommonParameters</span></span>
<span data-ttu-id="25e5a-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25e5a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e5a-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25e5a-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e5a-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25e5a-150">INPUTS</span></span>

### <span data-ttu-id="25e5a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="25e5a-151">System.String</span></span>

### <span data-ttu-id="25e5a-152">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="25e5a-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="25e5a-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25e5a-153">OUTPUTS</span></span>

### <span data-ttu-id="25e5a-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25e5a-154">System.Boolean</span></span>

## <span data-ttu-id="25e5a-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="25e5a-155">NOTES</span></span>

## <span data-ttu-id="25e5a-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25e5a-156">RELATED LINKS</span></span>
