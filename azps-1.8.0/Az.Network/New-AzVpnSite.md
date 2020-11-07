---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: 980b84fd1b23cb7e4b034dee485b785b96893f11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660443"
---
# <span data-ttu-id="62bdd-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="62bdd-101">New-AzVpnSite</span></span>

## <span data-ttu-id="62bdd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="62bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="62bdd-103">Erstellt eine neue Azure VpnSite-Ressource.</span><span class="sxs-lookup"><span data-stu-id="62bdd-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="62bdd-104">Hierbei handelt es sich um eine RM-Darstellung von Kunden Zweigen, die für S2S-Konnektivität mit einem virtuellen Kortex-Hub in Azure hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="62bdd-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="62bdd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="62bdd-105">SYNTAX</span></span>

### <span data-ttu-id="62bdd-106">ByVirtualWanName (Standard)</span><span class="sxs-lookup"><span data-stu-id="62bdd-106">ByVirtualWanName (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62bdd-107">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="62bdd-107">ByVirtualWanObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="62bdd-108">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="62bdd-108">ByVirtualWanResourceId</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62bdd-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62bdd-109">DESCRIPTION</span></span>
<span data-ttu-id="62bdd-110">Erstellt eine neue Azure VpnSite-Ressource.</span><span class="sxs-lookup"><span data-stu-id="62bdd-110">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="62bdd-111">Hierbei handelt es sich um eine RM-Darstellung von Kunden Zweigen, die für S2S-Konnektivität mit einem virtuellen Kortex-Hub in Azure hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="62bdd-111">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="62bdd-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="62bdd-112">EXAMPLES</span></span>

### <span data-ttu-id="62bdd-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="62bdd-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="62bdd-114">Das obige wird eine Ressourcengruppe erstellen, virtuelles WAN in West US in "testRG" Ressourcengruppe in Azure.</span><span class="sxs-lookup"><span data-stu-id="62bdd-114">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="62bdd-115">Anschließend wird ein VpnSite erstellt, um einen Kunden Zweig darzustellen und mit dem virtuellen WAN zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="62bdd-115">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="62bdd-116">Eine IPSec-Verbindung kann dann mit dieser Verzweigung und einem VpnGateway mit dem Befehl New-AzVpnConnection eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="62bdd-116">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

## <span data-ttu-id="62bdd-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="62bdd-117">PARAMETERS</span></span>

### <span data-ttu-id="62bdd-118">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="62bdd-118">-AddressSpace</span></span>
<span data-ttu-id="62bdd-119">Die Adresspräfixe des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="62bdd-119">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="62bdd-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62bdd-120">-AsJob</span></span>
<span data-ttu-id="62bdd-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="62bdd-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62bdd-122">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="62bdd-122">-BgpAsn</span></span>
<span data-ttu-id="62bdd-123">Der BGP ASN für diesen VpnSite.</span><span class="sxs-lookup"><span data-stu-id="62bdd-123">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="62bdd-124">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="62bdd-124">-BgpPeeringAddress</span></span>
<span data-ttu-id="62bdd-125">Die BGP-Peering-Adresse für diesen VpnSite.</span><span class="sxs-lookup"><span data-stu-id="62bdd-125">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="62bdd-126">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="62bdd-126">-BgpPeeringWeight</span></span>
<span data-ttu-id="62bdd-127">Das BGP-Peering Gewicht für dieses VpnSite.</span><span class="sxs-lookup"><span data-stu-id="62bdd-127">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="62bdd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62bdd-128">-DefaultProfile</span></span>
<span data-ttu-id="62bdd-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="62bdd-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62bdd-130">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="62bdd-130">-DeviceModel</span></span>
<span data-ttu-id="62bdd-131">Das Gerätemodell des Remote-VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="62bdd-131">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="62bdd-132">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="62bdd-132">-DeviceVendor</span></span>
<span data-ttu-id="62bdd-133">Der Gerätehersteller des Remote-VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="62bdd-133">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="62bdd-134">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="62bdd-134">-IpAddress</span></span>
<span data-ttu-id="62bdd-135">Die IPAddress für diesen VpnSite.</span><span class="sxs-lookup"><span data-stu-id="62bdd-135">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="62bdd-136">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="62bdd-136">-LinkSpeedInMbps</span></span>
<span data-ttu-id="62bdd-137">Das Gerätemodell des Remote-VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="62bdd-137">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="62bdd-138">-Standort</span><span class="sxs-lookup"><span data-stu-id="62bdd-138">-Location</span></span>
<span data-ttu-id="62bdd-139">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="62bdd-139">The resource location.</span></span>

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

### <span data-ttu-id="62bdd-140">-Name</span><span class="sxs-lookup"><span data-stu-id="62bdd-140">-Name</span></span>
<span data-ttu-id="62bdd-141">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="62bdd-141">The resource name.</span></span>

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

### <span data-ttu-id="62bdd-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62bdd-142">-ResourceGroupName</span></span>
<span data-ttu-id="62bdd-143">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="62bdd-143">The resource name.</span></span>

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

### <span data-ttu-id="62bdd-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="62bdd-144">-Tag</span></span>
<span data-ttu-id="62bdd-145">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="62bdd-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="62bdd-146">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="62bdd-146">-VirtualWan</span></span>
<span data-ttu-id="62bdd-147">Das VirtualWan, mit dem dieser VpnSite verbunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="62bdd-147">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bdd-148">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="62bdd-148">-VirtualWanId</span></span>
<span data-ttu-id="62bdd-149">Das VirtualWan, mit dem dieser VpnSite verbunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="62bdd-149">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bdd-150">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="62bdd-150">-VirtualWanName</span></span>
<span data-ttu-id="62bdd-151">Der Name des VirtualWan, mit dem dieser VpnSite verbunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="62bdd-151">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="62bdd-152">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62bdd-152">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="62bdd-153">Der Ressourcengruppenname des VirtualWan, mit dem dieser VpnSite verbunden sein muss.</span><span class="sxs-lookup"><span data-stu-id="62bdd-153">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="62bdd-154">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="62bdd-154">-Confirm</span></span>
<span data-ttu-id="62bdd-155">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="62bdd-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62bdd-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62bdd-156">-WhatIf</span></span>
<span data-ttu-id="62bdd-157">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="62bdd-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62bdd-158">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="62bdd-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62bdd-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62bdd-159">CommonParameters</span></span>
<span data-ttu-id="62bdd-160">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62bdd-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62bdd-161">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62bdd-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62bdd-162">Eingaben</span><span class="sxs-lookup"><span data-stu-id="62bdd-162">INPUTS</span></span>

### <span data-ttu-id="62bdd-163">Keine</span><span class="sxs-lookup"><span data-stu-id="62bdd-163">None</span></span>

## <span data-ttu-id="62bdd-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="62bdd-164">OUTPUTS</span></span>

### <span data-ttu-id="62bdd-165">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="62bdd-165">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="62bdd-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="62bdd-166">NOTES</span></span>

## <span data-ttu-id="62bdd-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="62bdd-167">RELATED LINKS</span></span>

[<span data-ttu-id="62bdd-168">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="62bdd-168">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="62bdd-169">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="62bdd-169">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="62bdd-170">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="62bdd-170">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
