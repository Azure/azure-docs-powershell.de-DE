---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: ac203d499674e97080edd645f9643b12291873d1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298896"
---
# <span data-ttu-id="47773-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="47773-101">New-AzVpnSite</span></span>

## <span data-ttu-id="47773-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47773-102">SYNOPSIS</span></span>
<span data-ttu-id="47773-103">Erstellt eine neue Azure VpnSite-Ressource.</span><span class="sxs-lookup"><span data-stu-id="47773-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="47773-104">Dies ist eine RM-Darstellung von Kundenverzweigungen, die für die Azure für S2S-Konnektivität mit einem virtuellenTex-Hub hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="47773-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="47773-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47773-105">SYNTAX</span></span>

### <span data-ttu-id="47773-106">ByVirtualWanNameByVpnSiteIpAddress (Standard)</span><span class="sxs-lookup"><span data-stu-id="47773-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47773-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="47773-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47773-108">ByVirtualWanObjectByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="47773-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47773-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="47773-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47773-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="47773-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47773-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="47773-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47773-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47773-112">DESCRIPTION</span></span>
<span data-ttu-id="47773-113">Erstellt eine neue Azure VpnSite-Ressource.</span><span class="sxs-lookup"><span data-stu-id="47773-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="47773-114">Dies ist eine RM-Darstellung von Kundenverzweigungen, die in Azure für S2S-Konnektivität mit einem virtuellenTex-Hub hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="47773-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="47773-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="47773-115">EXAMPLES</span></span>

### <span data-ttu-id="47773-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="47773-116">Example 1</span></span>

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

<span data-ttu-id="47773-117">Im vorstehenden Beispiel wird eine Ressourcengruppe, virtuelles WAN im Osten der USA, in der Ressourcengruppe "nonlinkSite" in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="47773-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="47773-118">Anschließend erstellt sie eine VpnSite zur Darstellung eines Kundenzweigs und verknüpft sie mit dem virtuellen WAN.</span><span class="sxs-lookup"><span data-stu-id="47773-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="47773-119">Anschließend kann mithilfe des Befehls "Verzweigung" und einem VpnGateway eine New-AzVpnConnection eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="47773-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="47773-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="47773-120">Example 2</span></span>
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

<span data-ttu-id="47773-121">Im vorstehenden Beispiel werden eine Ressourcengruppe, ein virtuelles WAN und eine VpnSite mit 1 VpnSiteLinks im Osten der USA in der Ressourcengruppe "multilink" in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="47773-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

### <span data-ttu-id="47773-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="47773-122">Example 3</span></span>

<span data-ttu-id="47773-123">Erstellt eine neue Azure VpnSite-Ressource.</span><span class="sxs-lookup"><span data-stu-id="47773-123">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="47773-124">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="47773-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnSite -AddressSpace <String[]> -DeviceModel 'SomeDevice' -DeviceVendor 'SomeDeviceVendor' -IpAddress '1.2.3.4' -LinkSpeedInMbps '10' -Location 'East US' -Name 'testVpnSite' -ResourceGroupName 'multilink' -VirtualWanName <String> -VirtualWanResourceGroupName <String>
```

## <span data-ttu-id="47773-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47773-125">PARAMETERS</span></span>

### <span data-ttu-id="47773-126">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="47773-126">-AddressSpace</span></span>
<span data-ttu-id="47773-127">Die Adresspräfixe des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="47773-127">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="47773-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47773-128">-AsJob</span></span>
<span data-ttu-id="47773-129">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="47773-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47773-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="47773-130">-BgpAsn</span></span>
<span data-ttu-id="47773-131">Der BGP ASN für diese VpnSite.</span><span class="sxs-lookup"><span data-stu-id="47773-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="47773-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="47773-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="47773-133">Die BGP-Peeringadresse für diese VpnWebsite.</span><span class="sxs-lookup"><span data-stu-id="47773-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="47773-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="47773-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="47773-135">Die Gewichtung für das BGP-Peering für diese VpnSite.</span><span class="sxs-lookup"><span data-stu-id="47773-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="47773-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47773-136">-DefaultProfile</span></span>
<span data-ttu-id="47773-137">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47773-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47773-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="47773-138">-DeviceModel</span></span>
<span data-ttu-id="47773-139">Das Gerätemodell des Remote-VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="47773-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="47773-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="47773-140">-DeviceVendor</span></span>
<span data-ttu-id="47773-141">Der Geräteanbieter des Remote-VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="47773-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="47773-142">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="47773-142">-IpAddress</span></span>
<span data-ttu-id="47773-143">Die IPAddress für diese VpnSite.</span><span class="sxs-lookup"><span data-stu-id="47773-143">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="47773-144">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="47773-144">-LinkSpeedInMbps</span></span>
<span data-ttu-id="47773-145">Das Gerätemodell des Remote-VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="47773-145">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="47773-146">-Location</span><span class="sxs-lookup"><span data-stu-id="47773-146">-Location</span></span>
<span data-ttu-id="47773-147">Der Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="47773-147">The resource location.</span></span>

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

### <span data-ttu-id="47773-148">-Name</span><span class="sxs-lookup"><span data-stu-id="47773-148">-Name</span></span>
<span data-ttu-id="47773-149">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="47773-149">The resource name.</span></span>

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

### <span data-ttu-id="47773-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="47773-150">-O365Policy</span></span>
<span data-ttu-id="47773-151">Die Office 365-Richtlinie für Die Unterbrechung des Datenverkehrs für diese VpnWebsite.</span><span class="sxs-lookup"><span data-stu-id="47773-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="47773-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47773-152">-ResourceGroupName</span></span>
<span data-ttu-id="47773-153">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="47773-153">The resource name.</span></span>

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

### <span data-ttu-id="47773-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="47773-154">-Tag</span></span>
<span data-ttu-id="47773-155">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="47773-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="47773-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="47773-156">-VirtualWan</span></span>
<span data-ttu-id="47773-157">Der VirtualWan, mit dem diese VpnSite verbunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="47773-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="47773-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="47773-158">-VirtualWanId</span></span>
<span data-ttu-id="47773-159">Der ResourceId VirtualWan, mit dem diese VpnSite verbunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="47773-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="47773-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="47773-160">-VirtualWanName</span></span>
<span data-ttu-id="47773-161">Der Name des VirtualWan, mit dem diese VpnSite verbunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="47773-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="47773-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47773-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="47773-163">Der Ressourcengruppenname von VirtualWan, mit dem diese VpnSite verbunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="47773-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="47773-164">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="47773-164">-VpnSiteLink</span></span>
<span data-ttu-id="47773-165">Die Liste der VpnSiteLinks, über die diese VpnSite verfügt.</span><span class="sxs-lookup"><span data-stu-id="47773-165">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="47773-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47773-166">-Confirm</span></span>
<span data-ttu-id="47773-167">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="47773-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47773-168">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="47773-168">-WhatIf</span></span>
<span data-ttu-id="47773-169">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47773-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47773-170">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47773-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47773-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47773-171">CommonParameters</span></span>
<span data-ttu-id="47773-172">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47773-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47773-173">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47773-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47773-174">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="47773-174">INPUTS</span></span>

### <span data-ttu-id="47773-175">Keine</span><span class="sxs-lookup"><span data-stu-id="47773-175">None</span></span>

## <span data-ttu-id="47773-176">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="47773-176">OUTPUTS</span></span>

### <span data-ttu-id="47773-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="47773-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="47773-178">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="47773-178">NOTES</span></span>

## <span data-ttu-id="47773-179">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="47773-179">RELATED LINKS</span></span>

[<span data-ttu-id="47773-180">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="47773-180">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="47773-181">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="47773-181">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="47773-182">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="47773-182">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
