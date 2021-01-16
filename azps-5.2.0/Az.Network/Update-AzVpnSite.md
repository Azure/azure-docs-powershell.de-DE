---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
ms.openlocfilehash: b7ed573ed8df8086cd5cef04204020498e1413c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295913"
---
# <span data-ttu-id="c19f2-101">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="c19f2-101">Update-AzVpnSite</span></span>

## <span data-ttu-id="c19f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c19f2-102">SYNOPSIS</span></span>
<span data-ttu-id="c19f2-103">Aktualisiert eine VPN-Website.</span><span class="sxs-lookup"><span data-stu-id="c19f2-103">Updates a VPN site.</span></span>

## <span data-ttu-id="c19f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c19f2-104">SYNTAX</span></span>

### <span data-ttu-id="c19f2-105">ByVpnSiteNameNoVirtualWanUpdate (Standard)</span><span class="sxs-lookup"><span data-stu-id="c19f2-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c19f2-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="c19f2-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c19f2-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="c19f2-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c19f2-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="c19f2-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c19f2-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="c19f2-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c19f2-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="c19f2-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c19f2-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="c19f2-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c19f2-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="c19f2-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c19f2-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="c19f2-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c19f2-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="c19f2-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c19f2-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="c19f2-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c19f2-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="c19f2-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -ResourceId <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c19f2-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c19f2-117">DESCRIPTION</span></span>
<span data-ttu-id="c19f2-118">Das **Cmdlet "Update-AzVpnSite"** aktualisiert eine VPN-Website.</span><span class="sxs-lookup"><span data-stu-id="c19f2-118">The **Update-AzVpnSite** cmdlet updates a VPN site.</span></span>

## <span data-ttu-id="c19f2-119">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c19f2-119">EXAMPLES</span></span>

### <span data-ttu-id="c19f2-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c19f2-120">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "2.3.5.5"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 2.3.4.5
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="c19f2-121">Im vorstehenden Beispiel wird in der Ressourcengruppe "testRG" in Azure eine Ressourcengruppe , virtuelles WAN in den USA, erstellt.</span><span class="sxs-lookup"><span data-stu-id="c19f2-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="c19f2-122">Anschließend erstellt sie eine VpnSite zur Darstellung eines Kundenzweigs und verknüpft sie mit dem virtuellen WAN.</span><span class="sxs-lookup"><span data-stu-id="c19f2-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="c19f2-123">Sobald die Website erstellt wurde, aktualisiert sie die "IpAddress" der Website mithilfe des Befehls Set-AzVpnSite".</span><span class="sxs-lookup"><span data-stu-id="c19f2-123">Once the site is created, it updates the IpAddress of the site using the Set-AzVpnSite command.</span></span>

## <span data-ttu-id="c19f2-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c19f2-124">PARAMETERS</span></span>

### <span data-ttu-id="c19f2-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="c19f2-125">-AddressSpace</span></span>
<span data-ttu-id="c19f2-126">Die Adresspräfixe des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="c19f2-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="c19f2-127">Verwenden Sie diese oder AddressSpaceObject, aber nicht beides.</span><span class="sxs-lookup"><span data-stu-id="c19f2-127">Use this or AddressSpaceObject but not both.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c19f2-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c19f2-128">-AsJob</span></span>
<span data-ttu-id="c19f2-129">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c19f2-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c19f2-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="c19f2-130">-BgpAsn</span></span>
<span data-ttu-id="c19f2-131">Der BGP ASN für diese VpnSite.</span><span class="sxs-lookup"><span data-stu-id="c19f2-131">The BGP ASN for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c19f2-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="c19f2-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="c19f2-133">Die BGP-Peeringadresse für diese VpnWebsite.</span><span class="sxs-lookup"><span data-stu-id="c19f2-133">The BGP Peering Address for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c19f2-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="c19f2-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="c19f2-135">Die Gewichtung für das BGP-Peering für diese VpnSite.</span><span class="sxs-lookup"><span data-stu-id="c19f2-135">The BGP Peering weight for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c19f2-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c19f2-136">-DefaultProfile</span></span>
<span data-ttu-id="c19f2-137">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c19f2-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c19f2-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="c19f2-138">-DeviceModel</span></span>
<span data-ttu-id="c19f2-139">Das Gerätemodell des Remote-VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="c19f2-139">The device model of the remote vpn device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c19f2-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="c19f2-140">-DeviceVendor</span></span>
<span data-ttu-id="c19f2-141">Der Geräteanbieter des Remote-VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="c19f2-141">The device vendor of the remote vpn device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c19f2-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c19f2-142">-InputObject</span></span>
<span data-ttu-id="c19f2-143">Das zu ändernde Vpn-Website-Objekt</span><span class="sxs-lookup"><span data-stu-id="c19f2-143">The vpn site object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnSiteObjectByVirtualWanName, ByVpnSiteObjectByVirtualWanResourceId, ByVpnSiteObjectByVirtualWanObject, ByVpnSiteObjectNoVirtualWanUpdate
Aliases: VpnSite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c19f2-144">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="c19f2-144">-IpAddress</span></span>
<span data-ttu-id="c19f2-145">Die IP-Adresse des lokalen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="c19f2-145">IP address of local network gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c19f2-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="c19f2-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="c19f2-147">Das Gerätemodell des Remote-VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="c19f2-147">The device model of the remote vpn device.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c19f2-148">-Name</span><span class="sxs-lookup"><span data-stu-id="c19f2-148">-Name</span></span>
<span data-ttu-id="c19f2-149">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="c19f2-149">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameNoVirtualWanUpdate, ByVpnSiteNameByVirtualWanName, ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteNameByVirtualWanObject
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c19f2-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="c19f2-150">-O365Policy</span></span>
<span data-ttu-id="c19f2-151">Die Office 365-Richtlinie für Die Unterbrechung des Datenverkehrs für diese VpnWebsite.</span><span class="sxs-lookup"><span data-stu-id="c19f2-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c19f2-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c19f2-152">-ResourceGroupName</span></span>
<span data-ttu-id="c19f2-153">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c19f2-153">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameNoVirtualWanUpdate, ByVpnSiteNameByVirtualWanName, ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteNameByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c19f2-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c19f2-154">-ResourceId</span></span>
<span data-ttu-id="c19f2-155">Die Azure-Ressourcen-ID für die VPN-Website.</span><span class="sxs-lookup"><span data-stu-id="c19f2-155">The Azure resource ID for the vpn site.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteResourceIdByVirtualWanName, ByVpnSiteResourceIdByVirtualWanResourceId, ByVpnSiteResourceIdByVirtualWanObject, ByVpnSiteResourceIdNoVirtualWanUpdate
Aliases: VpnSiteId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c19f2-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="c19f2-156">-Tag</span></span>
<span data-ttu-id="c19f2-157">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="c19f2-157">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c19f2-158">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="c19f2-158">-VirtualWan</span></span>
<span data-ttu-id="c19f2-159">Der VirtualWan, mit dem diese VpnSite verbunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="c19f2-159">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVpnSiteNameByVirtualWanObject, ByVpnSiteObjectByVirtualWanObject, ByVpnSiteResourceIdByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c19f2-160">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="c19f2-160">-VirtualWanId</span></span>
<span data-ttu-id="c19f2-161">Der ResourceId VirtualWan, mit dem diese VpnSite verbunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="c19f2-161">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteObjectByVirtualWanResourceId, ByVpnSiteResourceIdByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c19f2-162">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="c19f2-162">-VirtualWanName</span></span>
<span data-ttu-id="c19f2-163">Der Name des VirtualWan, mit dem diese VpnSite verbunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="c19f2-163">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanName, ByVpnSiteObjectByVirtualWanName, ByVpnSiteResourceIdByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c19f2-164">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c19f2-164">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="c19f2-165">Der Ressourcengruppenname von VirtualWan, mit dem diese VpnSite verbunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="c19f2-165">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanName, ByVpnSiteObjectByVirtualWanName, ByVpnSiteResourceIdByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c19f2-166">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="c19f2-166">-VpnSiteLink</span></span>
<span data-ttu-id="c19f2-167">Die Liste der VpnSiteLinks, über die diese VpnSite verfügt.</span><span class="sxs-lookup"><span data-stu-id="c19f2-167">The list of VpnSiteLinks that this VpnSite have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c19f2-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c19f2-168">-Confirm</span></span>
<span data-ttu-id="c19f2-169">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c19f2-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c19f2-170">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c19f2-170">-WhatIf</span></span>
<span data-ttu-id="c19f2-171">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c19f2-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c19f2-172">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c19f2-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c19f2-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c19f2-173">CommonParameters</span></span>
<span data-ttu-id="c19f2-174">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c19f2-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c19f2-175">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c19f2-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c19f2-176">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c19f2-176">INPUTS</span></span>

### <span data-ttu-id="c19f2-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="c19f2-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="c19f2-178">System.String</span><span class="sxs-lookup"><span data-stu-id="c19f2-178">System.String</span></span>

## <span data-ttu-id="c19f2-179">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c19f2-179">OUTPUTS</span></span>

### <span data-ttu-id="c19f2-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="c19f2-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="c19f2-181">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c19f2-181">NOTES</span></span>

## <span data-ttu-id="c19f2-182">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c19f2-182">RELATED LINKS</span></span>

[<span data-ttu-id="c19f2-183">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="c19f2-183">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="c19f2-184">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="c19f2-184">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="c19f2-185">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="c19f2-185">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)
