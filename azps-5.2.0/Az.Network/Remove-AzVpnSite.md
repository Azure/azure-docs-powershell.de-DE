---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
ms.openlocfilehash: 9b9ab59496ff52be2dc8ca538ea044ec34c34970
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301707"
---
# <span data-ttu-id="c6c3a-101">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="c6c3a-101">Remove-AzVpnSite</span></span>

## <span data-ttu-id="c6c3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6c3a-102">SYNOPSIS</span></span>
<span data-ttu-id="c6c3a-103">Entfernt eine Azure VpnSite-Ressource.</span><span class="sxs-lookup"><span data-stu-id="c6c3a-103">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="c6c3a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6c3a-104">SYNTAX</span></span>

### <span data-ttu-id="c6c3a-105">ByVpnSiteName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c6c3a-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6c3a-106">ByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="c6c3a-106">ByVpnSiteObject</span></span>
```
Remove-AzVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6c3a-107">ByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="c6c3a-107">ByVpnSiteResourceId</span></span>
```
Remove-AzVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6c3a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6c3a-108">DESCRIPTION</span></span>
<span data-ttu-id="c6c3a-109">Entfernt eine Azure VpnSite-Ressource.</span><span class="sxs-lookup"><span data-stu-id="c6c3a-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="c6c3a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c6c3a-110">EXAMPLES</span></span>

### <span data-ttu-id="c6c3a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c6c3a-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="c6c3a-112">Im vorstehenden Beispiel wird in der Ressourcengruppe "testRG" in Azure eine Ressourcengruppe erstellt, virtuelles WAN in west US.</span><span class="sxs-lookup"><span data-stu-id="c6c3a-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="c6c3a-113">Anschließend erstellt sie eine VpnSite zur Darstellung einer Kundenverzweigung und verknüpft sie mit dem virtuellen WAN.</span><span class="sxs-lookup"><span data-stu-id="c6c3a-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="c6c3a-114">Sobald die Website erstellt wurde, wird sie sofort mithilfe des Befehls Remove-AzVpnSite entfernt.</span><span class="sxs-lookup"><span data-stu-id="c6c3a-114">Once the site is created, it is immediately removed using the Remove-AzVpnSite command.</span></span>

### <span data-ttu-id="c6c3a-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c6c3a-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzVpnSite
```

<span data-ttu-id="c6c3a-116">Wie in Beispiel 1, aber hier erfolgt das Entfernen mithilfe der ausgabe von "Get-AzVpnSite".</span><span class="sxs-lookup"><span data-stu-id="c6c3a-116">Same as example 1 but here the removal happens using the piped output from Get-AzVpnSite.</span></span>

## <span data-ttu-id="c6c3a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6c3a-117">PARAMETERS</span></span>

### <span data-ttu-id="c6c3a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6c3a-118">-DefaultProfile</span></span>
<span data-ttu-id="c6c3a-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6c3a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6c3a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c6c3a-120">-Force</span></span>
<span data-ttu-id="c6c3a-121">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="c6c3a-121">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6c3a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6c3a-122">-InputObject</span></span>
<span data-ttu-id="c6c3a-123">Das zu löschende vpnSite-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c6c3a-123">The vpnSite object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnSiteObject
Aliases: VpnSite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6c3a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c6c3a-124">-Name</span></span>
<span data-ttu-id="c6c3a-125">Der Name der vpnSite.</span><span class="sxs-lookup"><span data-stu-id="c6c3a-125">The vpnSite name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteName
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6c3a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6c3a-126">-PassThru</span></span>
<span data-ttu-id="c6c3a-127">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c6c3a-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="c6c3a-128">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="c6c3a-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6c3a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6c3a-129">-ResourceGroupName</span></span>
<span data-ttu-id="c6c3a-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c6c3a-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6c3a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6c3a-131">-ResourceId</span></span>
<span data-ttu-id="c6c3a-132">Die Azure-Ressourcen-ID für die zu löschende vpn-Website.</span><span class="sxs-lookup"><span data-stu-id="c6c3a-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteResourceId
Aliases: VpnSiteId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6c3a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6c3a-133">-Confirm</span></span>
<span data-ttu-id="c6c3a-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c6c3a-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6c3a-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c6c3a-135">-WhatIf</span></span>
<span data-ttu-id="c6c3a-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c6c3a-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6c3a-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6c3a-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6c3a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6c3a-138">CommonParameters</span></span>
<span data-ttu-id="c6c3a-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6c3a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6c3a-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6c3a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6c3a-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c6c3a-141">INPUTS</span></span>

### <span data-ttu-id="c6c3a-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="c6c3a-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="c6c3a-143">System.String</span><span class="sxs-lookup"><span data-stu-id="c6c3a-143">System.String</span></span>

## <span data-ttu-id="c6c3a-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c6c3a-144">OUTPUTS</span></span>

### <span data-ttu-id="c6c3a-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c6c3a-145">System.Boolean</span></span>

## <span data-ttu-id="c6c3a-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c6c3a-146">NOTES</span></span>

## <span data-ttu-id="c6c3a-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c6c3a-147">RELATED LINKS</span></span>

[<span data-ttu-id="c6c3a-148">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="c6c3a-148">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="c6c3a-149">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="c6c3a-149">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="c6c3a-150">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="c6c3a-150">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
