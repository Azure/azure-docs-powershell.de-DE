---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
ms.openlocfilehash: b7ed573ed8df8086cd5cef04204020498e1413c6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173170"
---
# <span data-ttu-id="49202-101">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="49202-101">Update-AzVpnSite</span></span>

## <span data-ttu-id="49202-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="49202-102">SYNOPSIS</span></span>
<span data-ttu-id="49202-103">Aktualisiert eine VPN-Website.</span><span class="sxs-lookup"><span data-stu-id="49202-103">Updates a VPN site.</span></span>

## <span data-ttu-id="49202-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="49202-104">SYNTAX</span></span>

### <span data-ttu-id="49202-105">ByVpnSiteNameNoVirtualWanUpdate (Standard)</span><span class="sxs-lookup"><span data-stu-id="49202-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49202-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="49202-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49202-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="49202-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49202-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="49202-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49202-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="49202-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49202-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="49202-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49202-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="49202-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49202-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="49202-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49202-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="49202-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49202-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="49202-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49202-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="49202-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49202-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="49202-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -ResourceId <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49202-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49202-117">DESCRIPTION</span></span>
<span data-ttu-id="49202-118">Das Cmdlet **Update-AzVpnSite** aktualisiert eine VPN-Website.</span><span class="sxs-lookup"><span data-stu-id="49202-118">The **Update-AzVpnSite** cmdlet updates a VPN site.</span></span>

## <span data-ttu-id="49202-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49202-119">EXAMPLES</span></span>

### <span data-ttu-id="49202-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="49202-120">Example 1</span></span>

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

<span data-ttu-id="49202-121">Das obige wird eine Ressourcengruppe erstellen, virtuelles WAN in West US in "testRG" Ressourcengruppe in Azure.</span><span class="sxs-lookup"><span data-stu-id="49202-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="49202-122">Anschließend wird ein VpnSite erstellt, um einen Kunden Zweig darzustellen und mit dem virtuellen WAN zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="49202-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="49202-123">Nachdem die Website erstellt wurde, aktualisiert Sie die IPAddress der Website mit dem Befehl Set-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="49202-123">Once the site is created, it updates the IpAddress of the site using the Set-AzVpnSite command.</span></span>

## <span data-ttu-id="49202-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="49202-124">PARAMETERS</span></span>

### <span data-ttu-id="49202-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="49202-125">-AddressSpace</span></span>
<span data-ttu-id="49202-126">Die Adresspräfixe des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="49202-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="49202-127">Verwenden Sie diese oder AddressSpaceObject, aber nicht beide.</span><span class="sxs-lookup"><span data-stu-id="49202-127">Use this or AddressSpaceObject but not both.</span></span>

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

### <span data-ttu-id="49202-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49202-128">-AsJob</span></span>
<span data-ttu-id="49202-129">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="49202-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49202-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="49202-130">-BgpAsn</span></span>
<span data-ttu-id="49202-131">Der BGP ASN für diesen VpnSite.</span><span class="sxs-lookup"><span data-stu-id="49202-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="49202-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="49202-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="49202-133">Die BGP-Peering-Adresse für diesen VpnSite.</span><span class="sxs-lookup"><span data-stu-id="49202-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="49202-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="49202-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="49202-135">Das BGP-Peering Gewicht für dieses VpnSite.</span><span class="sxs-lookup"><span data-stu-id="49202-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="49202-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49202-136">-DefaultProfile</span></span>
<span data-ttu-id="49202-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="49202-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49202-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="49202-138">-DeviceModel</span></span>
<span data-ttu-id="49202-139">Das Gerätemodell des Remote-VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="49202-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="49202-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="49202-140">-DeviceVendor</span></span>
<span data-ttu-id="49202-141">Der Gerätehersteller des Remote-VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="49202-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="49202-142">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="49202-142">-InputObject</span></span>
<span data-ttu-id="49202-143">Das zu ändernde VPN-Websiteobjekt</span><span class="sxs-lookup"><span data-stu-id="49202-143">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="49202-144">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="49202-144">-IpAddress</span></span>
<span data-ttu-id="49202-145">IP-Adresse des lokalen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="49202-145">IP address of local network gateway.</span></span>

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

### <span data-ttu-id="49202-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="49202-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="49202-147">Das Gerätemodell des Remote-VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="49202-147">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="49202-148">-Name</span><span class="sxs-lookup"><span data-stu-id="49202-148">-Name</span></span>
<span data-ttu-id="49202-149">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="49202-149">The resource name.</span></span>

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

### <span data-ttu-id="49202-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="49202-150">-O365Policy</span></span>
<span data-ttu-id="49202-151">Die Office 365 Traffic-Breakout-Richtlinie für diesen VpnSite.</span><span class="sxs-lookup"><span data-stu-id="49202-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="49202-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49202-152">-ResourceGroupName</span></span>
<span data-ttu-id="49202-153">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="49202-153">The resource group name.</span></span>

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

### <span data-ttu-id="49202-154">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="49202-154">-ResourceId</span></span>
<span data-ttu-id="49202-155">Die Azure-Ressourcen-ID für die VPN-Website.</span><span class="sxs-lookup"><span data-stu-id="49202-155">The Azure resource ID for the vpn site.</span></span>

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

### <span data-ttu-id="49202-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="49202-156">-Tag</span></span>
<span data-ttu-id="49202-157">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="49202-157">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="49202-158">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="49202-158">-VirtualWan</span></span>
<span data-ttu-id="49202-159">Das VirtualWan, mit dem dieser VpnSite verbunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="49202-159">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="49202-160">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="49202-160">-VirtualWanId</span></span>
<span data-ttu-id="49202-161">Das VirtualWan, mit dem dieser VpnSite verbunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="49202-161">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="49202-162">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="49202-162">-VirtualWanName</span></span>
<span data-ttu-id="49202-163">Der Name des VirtualWan, mit dem dieser VpnSite verbunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="49202-163">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="49202-164">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49202-164">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="49202-165">Der Ressourcengruppenname des VirtualWan, mit dem dieser VpnSite verbunden sein muss.</span><span class="sxs-lookup"><span data-stu-id="49202-165">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="49202-166">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="49202-166">-VpnSiteLink</span></span>
<span data-ttu-id="49202-167">Die Liste der VpnSiteLinks, die dieser VpnSite.</span><span class="sxs-lookup"><span data-stu-id="49202-167">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="49202-168">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="49202-168">-Confirm</span></span>
<span data-ttu-id="49202-169">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="49202-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49202-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49202-170">-WhatIf</span></span>
<span data-ttu-id="49202-171">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49202-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49202-172">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="49202-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49202-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49202-173">CommonParameters</span></span>
<span data-ttu-id="49202-174">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49202-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49202-175">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49202-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49202-176">Eingaben</span><span class="sxs-lookup"><span data-stu-id="49202-176">INPUTS</span></span>

### <span data-ttu-id="49202-177">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="49202-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="49202-178">System. String</span><span class="sxs-lookup"><span data-stu-id="49202-178">System.String</span></span>

## <span data-ttu-id="49202-179">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49202-179">OUTPUTS</span></span>

### <span data-ttu-id="49202-180">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="49202-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="49202-181">Notizen</span><span class="sxs-lookup"><span data-stu-id="49202-181">NOTES</span></span>

## <span data-ttu-id="49202-182">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="49202-182">RELATED LINKS</span></span>

[<span data-ttu-id="49202-183">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="49202-183">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="49202-184">Neu – AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="49202-184">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="49202-185">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="49202-185">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)
