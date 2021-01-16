---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnConfiguration.md
ms.openlocfilehash: 6e67f192cab1d1183d8c8cfd1a38f6c398311bf9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379755"
---
# <span data-ttu-id="3ea58-101">Get-AzVirtualWanVpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ea58-101">Get-AzVirtualWanVpnConfiguration</span></span>

## <span data-ttu-id="3ea58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ea58-102">SYNOPSIS</span></span>
<span data-ttu-id="3ea58-103">Ruft die Vpn-Konfiguration für eine Teilmenge von VpnSites ab, die über VpnConnections mit diesem WAN verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="3ea58-103">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="3ea58-104">Lädt die generierte Vpn-Konfiguration in ein Speicher-BLOB hoch, das vom Kunden angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="3ea58-104">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="3ea58-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ea58-105">SYNTAX</span></span>

### <span data-ttu-id="3ea58-106">ByVirtualWanNameByVpnSiteObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="3ea58-106">ByVirtualWanNameByVpnSiteObject (Default)</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ea58-107">ByVirtualWanNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="3ea58-107">ByVirtualWanNameByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSiteId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ea58-108">ByVirtualWanObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="3ea58-108">ByVirtualWanObjectByVpnSiteObject</span></span>
```
Get-AzVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ea58-109">ByVirtualWanObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="3ea58-109">ByVirtualWanObjectByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ea58-110">ByVirtualWanResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="3ea58-110">ByVirtualWanResourceIdByVpnSiteObject</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ea58-111">ByVirtualWanResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="3ea58-111">ByVirtualWanResourceIdByVpnSiteResourceId</span></span>
```
Get-AzVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ea58-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ea58-112">DESCRIPTION</span></span>
<span data-ttu-id="3ea58-113">Ruft die Vpn-Konfiguration für eine Teilmenge von VpnSites ab, die über VpnConnections mit diesem WAN verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="3ea58-113">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="3ea58-114">Lädt die generierte Vpn-Konfiguration in ein Speicher-BLOB hoch, das vom Kunden angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="3ea58-114">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="3ea58-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3ea58-115">EXAMPLES</span></span>

### <span data-ttu-id="3ea58-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3ea58-116">Example 1</span></span>
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

<span data-ttu-id="3ea58-117">Im vorstehenden Beispiel wird eine Ressourcengruppe, ein virtuelles WAN, ein virtuelles Netzwerk, ein virtueller Hub und eine VpnSite in Der USA in der Ressourcengruppe "testRG" in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="3ea58-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="3ea58-118">Anschließend wird im virtuellen Hub ein VPN-Gateway mit 2 Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="3ea58-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="3ea58-119">Sobald das Gateway erstellt wurde, wird es mithilfe des Befehls "New-AzVpnConnection Mit der VpnSite verbunden.</span><span class="sxs-lookup"><span data-stu-id="3ea58-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="3ea58-120">Die Konfiguration wird dann mit diesem Befehlslet heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="3ea58-120">The configuration is then downloaded using this commandlet.</span></span>

<span data-ttu-id="3ea58-121">Wenn das Befehlslet erfolgreich ist, wird die Downloadkonfiguration in das blob geschrieben, das von "SignedSasUrl" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3ea58-121">If the commandlet is successful, then the download configuration will be written to the blob indicated by the SignedSasUrl.</span></span>

## <span data-ttu-id="3ea58-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ea58-122">PARAMETERS</span></span>

### <span data-ttu-id="3ea58-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ea58-123">-DefaultProfile</span></span>
<span data-ttu-id="3ea58-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ea58-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ea58-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ea58-125">-InputObject</span></span>
<span data-ttu-id="3ea58-126">Das zu ändernde Vpn-Website-Objekt</span><span class="sxs-lookup"><span data-stu-id="3ea58-126">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="3ea58-127">-Name</span><span class="sxs-lookup"><span data-stu-id="3ea58-127">-Name</span></span>
<span data-ttu-id="3ea58-128">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="3ea58-128">The resource name.</span></span>

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

### <span data-ttu-id="3ea58-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ea58-129">-ResourceGroupName</span></span>
<span data-ttu-id="3ea58-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3ea58-130">The resource group name.</span></span>

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

### <span data-ttu-id="3ea58-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ea58-131">-ResourceId</span></span>
<span data-ttu-id="3ea58-132">Die Azure-Ressourcen-ID für das virtuelle Wan.</span><span class="sxs-lookup"><span data-stu-id="3ea58-132">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="3ea58-133">-StorageSasUrl</span><span class="sxs-lookup"><span data-stu-id="3ea58-133">-StorageSasUrl</span></span>
<span data-ttu-id="3ea58-134">Die SAS-URL für den Speicherort, an dem die Konfiguration generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ea58-134">The SAS Url for the storage location where the configuration is to be generated.</span></span>

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

### <span data-ttu-id="3ea58-135">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="3ea58-135">-VpnSite</span></span>
<span data-ttu-id="3ea58-136">Die Liste der VpnSite-Ressourcen-IDs, für die die Konfiguration generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ea58-136">The list of VpnSite resource ids to generate configuration for.</span></span>

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

### <span data-ttu-id="3ea58-137">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="3ea58-137">-VpnSiteId</span></span>
<span data-ttu-id="3ea58-138">Die Liste der VpnSite-Ressourcen-IDs, für die die Konfiguration generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ea58-138">The list of VpnSite resource ids to generate configuration for.</span></span>

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

### <span data-ttu-id="3ea58-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ea58-139">-Confirm</span></span>
<span data-ttu-id="3ea58-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3ea58-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ea58-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3ea58-141">-WhatIf</span></span>
<span data-ttu-id="3ea58-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3ea58-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ea58-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3ea58-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ea58-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ea58-144">CommonParameters</span></span>
<span data-ttu-id="3ea58-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ea58-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ea58-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ea58-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ea58-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3ea58-147">INPUTS</span></span>

### <span data-ttu-id="3ea58-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="3ea58-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="3ea58-149">System.String</span><span class="sxs-lookup"><span data-stu-id="3ea58-149">System.String</span></span>

## <span data-ttu-id="3ea58-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3ea58-150">OUTPUTS</span></span>

### <span data-ttu-id="3ea58-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ea58-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span></span>

## <span data-ttu-id="3ea58-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3ea58-152">NOTES</span></span>

## <span data-ttu-id="3ea58-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3ea58-153">RELATED LINKS</span></span>
