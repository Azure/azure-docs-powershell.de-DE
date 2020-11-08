---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnConfiguration.md
ms.openlocfilehash: 6e67f192cab1d1183d8c8cfd1a38f6c398311bf9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005070"
---
# <span data-ttu-id="67e7f-101">Get-AzVirtualWanVpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="67e7f-101">Get-AzVirtualWanVpnConfiguration</span></span>

## <span data-ttu-id="67e7f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67e7f-102">SYNOPSIS</span></span>
<span data-ttu-id="67e7f-103">Ruft die VPN-Konfiguration für eine Teilmenge von VpnSites ab, die über VpnConnections mit diesem WAN verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="67e7f-103">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="67e7f-104">Lädt die generierte VPN-Konfiguration in einen vom Kunden angegebenen Speicher-BLOB hoch.</span><span class="sxs-lookup"><span data-stu-id="67e7f-104">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="67e7f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="67e7f-105">SYNTAX</span></span>

### <span data-ttu-id="67e7f-106">ByVirtualWanNameByVpnSiteObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="67e7f-106">ByVirtualWanNameByVpnSiteObject (Default)</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67e7f-107">ByVirtualWanNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="67e7f-107">ByVirtualWanNameByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSiteId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67e7f-108">ByVirtualWanObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="67e7f-108">ByVirtualWanObjectByVpnSiteObject</span></span>
```
Get-AzVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67e7f-109">ByVirtualWanObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="67e7f-109">ByVirtualWanObjectByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67e7f-110">ByVirtualWanResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="67e7f-110">ByVirtualWanResourceIdByVpnSiteObject</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67e7f-111">ByVirtualWanResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="67e7f-111">ByVirtualWanResourceIdByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67e7f-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67e7f-112">DESCRIPTION</span></span>
<span data-ttu-id="67e7f-113">Ruft die VPN-Konfiguration für eine Teilmenge von VpnSites ab, die über VpnConnections mit diesem WAN verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="67e7f-113">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="67e7f-114">Lädt die generierte VPN-Konfiguration in einen vom Kunden angegebenen Speicher-BLOB hoch.</span><span class="sxs-lookup"><span data-stu-id="67e7f-114">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="67e7f-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67e7f-115">EXAMPLES</span></span>

### <span data-ttu-id="67e7f-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="67e7f-116">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite

PS C:\> $vpnSitesForConfig = New-Object Microsoft.Azure.Commands.Network.Models.PSVpnSite[] 1
PS C:\> $vpnSitesForConfig[0] = $vpnSite
PS C:\> Get-AzVirtualWanVpnConfiguration -VirtualWan $virtualWan -StorageSasUrl "SignedSasUrl" -VpnSite $vpnSitesForConfig

SasUrl
------
SignedSasUrl
```

<span data-ttu-id="67e7f-117">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuellen Hub und einen VpnSite in West US in "testRG"-Ressourcengruppe in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="67e7f-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="67e7f-118">Anschließend wird ein VPN-Gateway im virtuellen Hub mit 2 Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="67e7f-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="67e7f-119">Nachdem das Gateway erstellt wurde, wird es mit dem VpnSite mit dem Befehl New-AzVpnConnection verbunden.</span><span class="sxs-lookup"><span data-stu-id="67e7f-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="67e7f-120">Die Konfiguration wird dann mit diesem Unifiedgroup heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="67e7f-120">The configuration is then downloaded using this commandlet.</span></span>

<span data-ttu-id="67e7f-121">Wenn der Unifiedgroup erfolgreich ist, wird die Download Konfiguration in das vom SignedSasUrl angegebene BLOB geschrieben.</span><span class="sxs-lookup"><span data-stu-id="67e7f-121">If the commandlet is successful, then the download configuration will be written to the blob indicated by the SignedSasUrl.</span></span>

## <span data-ttu-id="67e7f-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="67e7f-122">PARAMETERS</span></span>

### <span data-ttu-id="67e7f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67e7f-123">-DefaultProfile</span></span>
<span data-ttu-id="67e7f-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="67e7f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67e7f-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="67e7f-125">-InputObject</span></span>
<span data-ttu-id="67e7f-126">Das zu ändernde VPN-Websiteobjekt</span><span class="sxs-lookup"><span data-stu-id="67e7f-126">The vpn site object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnSiteObject, ByVirtualWanObjectByVpnSiteResourceId
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67e7f-127">-Name</span><span class="sxs-lookup"><span data-stu-id="67e7f-127">-Name</span></span>
<span data-ttu-id="67e7f-128">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="67e7f-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanNameByVpnSiteResourceId
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67e7f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67e7f-129">-ResourceGroupName</span></span>
<span data-ttu-id="67e7f-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="67e7f-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67e7f-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="67e7f-131">-ResourceId</span></span>
<span data-ttu-id="67e7f-132">Die Azure-Ressourcen-ID für das virtuelle WAN.</span><span class="sxs-lookup"><span data-stu-id="67e7f-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceIdByVpnSiteObject, ByVirtualWanResourceIdByVpnSiteResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67e7f-133">-StorageSasUrl</span><span class="sxs-lookup"><span data-stu-id="67e7f-133">-StorageSasUrl</span></span>
<span data-ttu-id="67e7f-134">Die SAS-URL für den Speicherort, an dem die Konfiguration generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="67e7f-134">The SAS Url for the storage location where the configuration is to be generated.</span></span>

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

### <span data-ttu-id="67e7f-135">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="67e7f-135">-VpnSite</span></span>
<span data-ttu-id="67e7f-136">Die Liste der VpnSite-Ressourcen-IDs, für die eine Konfiguration generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="67e7f-136">The list of VpnSite resource ids to generate configuration for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite[]
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanObjectByVpnSiteObject, ByVirtualWanResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67e7f-137">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="67e7f-137">-VpnSiteId</span></span>
<span data-ttu-id="67e7f-138">Die Liste der VpnSite-Ressourcen-IDs, für die eine Konfiguration generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="67e7f-138">The list of VpnSite resource ids to generate configuration for.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVirtualWanNameByVpnSiteResourceId, ByVirtualWanObjectByVpnSiteResourceId, ByVirtualWanResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67e7f-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="67e7f-139">-Confirm</span></span>
<span data-ttu-id="67e7f-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="67e7f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67e7f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67e7f-141">-WhatIf</span></span>
<span data-ttu-id="67e7f-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67e7f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67e7f-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="67e7f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67e7f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67e7f-144">CommonParameters</span></span>
<span data-ttu-id="67e7f-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67e7f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67e7f-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67e7f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67e7f-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67e7f-147">INPUTS</span></span>

### <span data-ttu-id="67e7f-148">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="67e7f-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="67e7f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="67e7f-149">System.String</span></span>

## <span data-ttu-id="67e7f-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67e7f-150">OUTPUTS</span></span>

### <span data-ttu-id="67e7f-151">Microsoft. Azure. Commands. Network. Models. PSVirtualWanVpnSitesConfiguration</span><span class="sxs-lookup"><span data-stu-id="67e7f-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span></span>

## <span data-ttu-id="67e7f-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="67e7f-152">NOTES</span></span>

## <span data-ttu-id="67e7f-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67e7f-153">RELATED LINKS</span></span>
