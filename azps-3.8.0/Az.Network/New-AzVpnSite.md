---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: a459ec99852d83dcba05a3a594ee2ae4378c318c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995719"
---
# <span data-ttu-id="92ffa-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="92ffa-101">New-AzVpnSite</span></span>

## <span data-ttu-id="92ffa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="92ffa-102">SYNOPSIS</span></span>
<span data-ttu-id="92ffa-103">Erstellt eine neue Azure VpnSite-Ressource.</span><span class="sxs-lookup"><span data-stu-id="92ffa-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="92ffa-104">Hierbei handelt es sich um eine RM-Darstellung von Kunden Zweigen, die für S2S-Konnektivität mit einem virtuellen Kortex-Hub in Azure hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="92ffa-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="92ffa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="92ffa-105">SYNTAX</span></span>

### <span data-ttu-id="92ffa-106">ByVirtualWanNameByVpnSiteIpAddress (Standard)</span><span class="sxs-lookup"><span data-stu-id="92ffa-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92ffa-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="92ffa-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92ffa-108">ByVirtualWanObjectByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="92ffa-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92ffa-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="92ffa-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92ffa-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="92ffa-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92ffa-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="92ffa-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92ffa-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92ffa-112">DESCRIPTION</span></span>
<span data-ttu-id="92ffa-113">Erstellt eine neue Azure VpnSite-Ressource.</span><span class="sxs-lookup"><span data-stu-id="92ffa-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="92ffa-114">Hierbei handelt es sich um eine RM-Darstellung von Kunden Zweigen, die für S2S-Konnektivität mit einem virtuellen Kortex-Hub in Azure hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="92ffa-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="92ffa-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="92ffa-115">EXAMPLES</span></span>

### <span data-ttu-id="92ffa-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="92ffa-116">Example 1</span></span>

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

<span data-ttu-id="92ffa-117">In der obigen Abbildung wird eine Ressourcengruppe, virtuelles WAN in Ost-USA, in der Ressourcengruppe "nonlinkSite" in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="92ffa-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="92ffa-118">Anschließend wird ein VpnSite erstellt, um einen Kunden Zweig darzustellen und mit dem virtuellen WAN zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="92ffa-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="92ffa-119">Eine IPSec-Verbindung kann dann mit dieser Verzweigung und einem VpnGateway mit dem Befehl New-AzVpnConnection eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="92ffa-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="92ffa-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="92ffa-120">Example 2</span></span>
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

<span data-ttu-id="92ffa-121">Das obige wird eine Ressourcengruppe, virtuelles WAN und einen VpnSite mit 1 VpnSiteLinks in Ost-USA in der Ressourcengruppe "Multilink" in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="92ffa-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

## <span data-ttu-id="92ffa-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="92ffa-122">PARAMETERS</span></span>

### <span data-ttu-id="92ffa-123">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="92ffa-123">-AddressSpace</span></span>
<span data-ttu-id="92ffa-124">Die Adresspräfixe des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="92ffa-124">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="92ffa-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92ffa-125">-AsJob</span></span>
<span data-ttu-id="92ffa-126">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="92ffa-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92ffa-127">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="92ffa-127">-BgpAsn</span></span>
<span data-ttu-id="92ffa-128">Der BGP ASN für diesen VpnSite.</span><span class="sxs-lookup"><span data-stu-id="92ffa-128">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="92ffa-129">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="92ffa-129">-BgpPeeringAddress</span></span>
<span data-ttu-id="92ffa-130">Die BGP-Peering-Adresse für diesen VpnSite.</span><span class="sxs-lookup"><span data-stu-id="92ffa-130">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="92ffa-131">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="92ffa-131">-BgpPeeringWeight</span></span>
<span data-ttu-id="92ffa-132">Das BGP-Peering Gewicht für dieses VpnSite.</span><span class="sxs-lookup"><span data-stu-id="92ffa-132">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="92ffa-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92ffa-133">-DefaultProfile</span></span>
<span data-ttu-id="92ffa-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="92ffa-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92ffa-135">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="92ffa-135">-DeviceModel</span></span>
<span data-ttu-id="92ffa-136">Das Gerätemodell des Remote-VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="92ffa-136">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="92ffa-137">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="92ffa-137">-DeviceVendor</span></span>
<span data-ttu-id="92ffa-138">Der Gerätehersteller des Remote-VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="92ffa-138">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="92ffa-139">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="92ffa-139">-IpAddress</span></span>
<span data-ttu-id="92ffa-140">Die IPAddress für diesen VpnSite.</span><span class="sxs-lookup"><span data-stu-id="92ffa-140">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="92ffa-141">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="92ffa-141">-LinkSpeedInMbps</span></span>
<span data-ttu-id="92ffa-142">Das Gerätemodell des Remote-VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="92ffa-142">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="92ffa-143">-Standort</span><span class="sxs-lookup"><span data-stu-id="92ffa-143">-Location</span></span>
<span data-ttu-id="92ffa-144">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="92ffa-144">The resource location.</span></span>

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

### <span data-ttu-id="92ffa-145">-Name</span><span class="sxs-lookup"><span data-stu-id="92ffa-145">-Name</span></span>
<span data-ttu-id="92ffa-146">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="92ffa-146">The resource name.</span></span>

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

### <span data-ttu-id="92ffa-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92ffa-147">-ResourceGroupName</span></span>
<span data-ttu-id="92ffa-148">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="92ffa-148">The resource name.</span></span>

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

### <span data-ttu-id="92ffa-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="92ffa-149">-Tag</span></span>
<span data-ttu-id="92ffa-150">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="92ffa-150">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="92ffa-151">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="92ffa-151">-VirtualWan</span></span>
<span data-ttu-id="92ffa-152">Das VirtualWan, mit dem dieser VpnSite verbunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="92ffa-152">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="92ffa-153">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="92ffa-153">-VirtualWanId</span></span>
<span data-ttu-id="92ffa-154">Das VirtualWan, mit dem dieser VpnSite verbunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="92ffa-154">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="92ffa-155">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="92ffa-155">-VirtualWanName</span></span>
<span data-ttu-id="92ffa-156">Der Name des VirtualWan, mit dem dieser VpnSite verbunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="92ffa-156">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="92ffa-157">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92ffa-157">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="92ffa-158">Der Ressourcengruppenname des VirtualWan, mit dem dieser VpnSite verbunden sein muss.</span><span class="sxs-lookup"><span data-stu-id="92ffa-158">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="92ffa-159">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="92ffa-159">-VpnSiteLink</span></span>
<span data-ttu-id="92ffa-160">Die Liste der VpnSiteLinks, die dieser VpnSite.</span><span class="sxs-lookup"><span data-stu-id="92ffa-160">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="92ffa-161">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="92ffa-161">-Confirm</span></span>
<span data-ttu-id="92ffa-162">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="92ffa-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92ffa-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92ffa-163">-WhatIf</span></span>
<span data-ttu-id="92ffa-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92ffa-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92ffa-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92ffa-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92ffa-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92ffa-166">CommonParameters</span></span>
<span data-ttu-id="92ffa-167">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92ffa-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92ffa-168">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92ffa-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92ffa-169">Eingaben</span><span class="sxs-lookup"><span data-stu-id="92ffa-169">INPUTS</span></span>

### <span data-ttu-id="92ffa-170">Keine</span><span class="sxs-lookup"><span data-stu-id="92ffa-170">None</span></span>

## <span data-ttu-id="92ffa-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="92ffa-171">OUTPUTS</span></span>

### <span data-ttu-id="92ffa-172">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="92ffa-172">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="92ffa-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="92ffa-173">NOTES</span></span>

## <span data-ttu-id="92ffa-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="92ffa-174">RELATED LINKS</span></span>

[<span data-ttu-id="92ffa-175">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="92ffa-175">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="92ffa-176">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="92ffa-176">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="92ffa-177">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="92ffa-177">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
