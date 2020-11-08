---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: ac203d499674e97080edd645f9643b12291873d1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175003"
---
# <span data-ttu-id="89726-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="89726-101">New-AzVpnSite</span></span>

## <span data-ttu-id="89726-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="89726-102">SYNOPSIS</span></span>
<span data-ttu-id="89726-103">Erstellt eine neue Azure VpnSite-Ressource.</span><span class="sxs-lookup"><span data-stu-id="89726-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="89726-104">Hierbei handelt es sich um eine RM-Darstellung von Kunden Zweigen, die für S2S-Konnektivität mit einem virtuellen Kortex-Hub in Azure hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="89726-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="89726-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="89726-105">SYNTAX</span></span>

### <span data-ttu-id="89726-106">ByVirtualWanNameByVpnSiteIpAddress (Standard)</span><span class="sxs-lookup"><span data-stu-id="89726-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89726-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="89726-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89726-108">ByVirtualWanObjectByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="89726-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89726-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="89726-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89726-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="89726-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89726-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="89726-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89726-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89726-112">DESCRIPTION</span></span>
<span data-ttu-id="89726-113">Erstellt eine neue Azure VpnSite-Ressource.</span><span class="sxs-lookup"><span data-stu-id="89726-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="89726-114">Hierbei handelt es sich um eine RM-Darstellung von Kunden Zweigen, die für S2S-Konnektivität mit einem virtuellen Kortex-Hub in Azure hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="89726-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="89726-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89726-115">EXAMPLES</span></span>

### <span data-ttu-id="89726-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="89726-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "East US" -Name "nonlinkSite"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "nonlinkSite" -Name myVirtualWAN -Location "East US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzVpnSite -ResourceGroupName "nonlinkSite" -Name "testVpnSite" -Location "East US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

ResourceGroupName : nonlinkSite
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/nonlinkSite/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/nonlinkSite/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="89726-117">In der obigen Abbildung wird eine Ressourcengruppe, virtuelles WAN in Ost-USA, in der Ressourcengruppe "nonlinkSite" in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="89726-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="89726-118">Anschließend wird ein VpnSite erstellt, um einen Kunden Zweig darzustellen und mit dem virtuellen WAN zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="89726-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="89726-119">Eine IPSec-Verbindung kann dann mit dieser Verzweigung und einem VpnGateway mit dem Befehl New-AzVpnConnection eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="89726-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="89726-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="89726-120">Example 2</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "East US" -Name "multilink"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName multilink -Name myVirtualWAN -Location "East US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSiteLink2 = New-AzVpnSiteLink -Name "testVpnSiteLink2" -IpAddress "15.25.35.55" -LinkProviderName "SomeTelecomProvider2" -LinkSpeedInMbps "100"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "multilink" -Name "testVpnSite" -Location "East US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink1, $vpnSiteLink2)
```

<span data-ttu-id="89726-121">Das obige wird eine Ressourcengruppe, virtuelles WAN und einen VpnSite mit 1 VpnSiteLinks in Ost-USA in der Ressourcengruppe "Multilink" in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="89726-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

### <span data-ttu-id="89726-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="89726-122">Example 3</span></span>

<span data-ttu-id="89726-123">Erstellt eine neue Azure VpnSite-Ressource.</span><span class="sxs-lookup"><span data-stu-id="89726-123">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="89726-124">automatisch</span><span class="sxs-lookup"><span data-stu-id="89726-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnSite -AddressSpace <String[]> -DeviceModel 'SomeDevice' -DeviceVendor 'SomeDeviceVendor' -IpAddress '1.2.3.4' -LinkSpeedInMbps '10' -Location 'East US' -Name 'testVpnSite' -ResourceGroupName 'multilink' -VirtualWanName <String> -VirtualWanResourceGroupName <String>
```

## <span data-ttu-id="89726-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="89726-125">PARAMETERS</span></span>

### <span data-ttu-id="89726-126">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="89726-126">-AddressSpace</span></span>
<span data-ttu-id="89726-127">Die Adresspräfixe des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="89726-127">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="89726-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89726-128">-AsJob</span></span>
<span data-ttu-id="89726-129">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="89726-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89726-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="89726-130">-BgpAsn</span></span>
<span data-ttu-id="89726-131">Der BGP ASN für diesen VpnSite.</span><span class="sxs-lookup"><span data-stu-id="89726-131">The BGP ASN for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89726-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="89726-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="89726-133">Die BGP-Peering-Adresse für diesen VpnSite.</span><span class="sxs-lookup"><span data-stu-id="89726-133">The BGP Peering Address for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89726-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="89726-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="89726-135">Das BGP-Peering Gewicht für dieses VpnSite.</span><span class="sxs-lookup"><span data-stu-id="89726-135">The BGP Peering weight for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89726-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89726-136">-DefaultProfile</span></span>
<span data-ttu-id="89726-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="89726-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89726-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="89726-138">-DeviceModel</span></span>
<span data-ttu-id="89726-139">Das Gerätemodell des Remote-VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="89726-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="89726-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="89726-140">-DeviceVendor</span></span>
<span data-ttu-id="89726-141">Der Gerätehersteller des Remote-VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="89726-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="89726-142">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="89726-142">-IpAddress</span></span>
<span data-ttu-id="89726-143">Die IPAddress für diesen VpnSite.</span><span class="sxs-lookup"><span data-stu-id="89726-143">The IPAddress for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89726-144">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="89726-144">-LinkSpeedInMbps</span></span>
<span data-ttu-id="89726-145">Das Gerätemodell des Remote-VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="89726-145">The device model of the remote vpn device.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89726-146">-Standort</span><span class="sxs-lookup"><span data-stu-id="89726-146">-Location</span></span>
<span data-ttu-id="89726-147">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="89726-147">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89726-148">-Name</span><span class="sxs-lookup"><span data-stu-id="89726-148">-Name</span></span>
<span data-ttu-id="89726-149">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="89726-149">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89726-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="89726-150">-O365Policy</span></span>
<span data-ttu-id="89726-151">Die Office 365 Traffic-Breakout-Richtlinie für diesen VpnSite.</span><span class="sxs-lookup"><span data-stu-id="89726-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="89726-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89726-152">-ResourceGroupName</span></span>
<span data-ttu-id="89726-153">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="89726-153">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89726-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="89726-154">-Tag</span></span>
<span data-ttu-id="89726-155">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="89726-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="89726-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="89726-156">-VirtualWan</span></span>
<span data-ttu-id="89726-157">Das VirtualWan, mit dem dieser VpnSite verbunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="89726-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89726-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="89726-158">-VirtualWanId</span></span>
<span data-ttu-id="89726-159">Das VirtualWan, mit dem dieser VpnSite verbunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="89726-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceIdByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89726-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="89726-160">-VirtualWanName</span></span>
<span data-ttu-id="89726-161">Der Name des VirtualWan, mit dem dieser VpnSite verbunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="89726-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanNameByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89726-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89726-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="89726-163">Der Ressourcengruppenname des VirtualWan, mit dem dieser VpnSite verbunden sein muss.</span><span class="sxs-lookup"><span data-stu-id="89726-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanNameByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89726-164">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="89726-164">-VpnSiteLink</span></span>
<span data-ttu-id="89726-165">Die Liste der VpnSiteLinks, die dieser VpnSite.</span><span class="sxs-lookup"><span data-stu-id="89726-165">The list of VpnSiteLinks that this VpnSite have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink[]
Parameter Sets: ByVirtualWanNameByVpnSiteLinkObject, ByVirtualWanObjectByVpnSiteLinkObject, ByVirtualWanResourceIdByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89726-166">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="89726-166">-Confirm</span></span>
<span data-ttu-id="89726-167">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="89726-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89726-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89726-168">-WhatIf</span></span>
<span data-ttu-id="89726-169">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="89726-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89726-170">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="89726-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89726-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89726-171">CommonParameters</span></span>
<span data-ttu-id="89726-172">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89726-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89726-173">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89726-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89726-174">Eingaben</span><span class="sxs-lookup"><span data-stu-id="89726-174">INPUTS</span></span>

### <span data-ttu-id="89726-175">Keine</span><span class="sxs-lookup"><span data-stu-id="89726-175">None</span></span>

## <span data-ttu-id="89726-176">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="89726-176">OUTPUTS</span></span>

### <span data-ttu-id="89726-177">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="89726-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="89726-178">Notizen</span><span class="sxs-lookup"><span data-stu-id="89726-178">NOTES</span></span>

## <span data-ttu-id="89726-179">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="89726-179">RELATED LINKS</span></span>

[<span data-ttu-id="89726-180">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="89726-180">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="89726-181">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="89726-181">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="89726-182">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="89726-182">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
