---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
ms.openlocfilehash: 5b728195c34db0261bd27525f0916c634cf3d9e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944915"
---
# <span data-ttu-id="55d0e-101">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="55d0e-101">Remove-AzVpnConnection</span></span>

## <span data-ttu-id="55d0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55d0e-102">SYNOPSIS</span></span>
<span data-ttu-id="55d0e-103">Entfernt eine VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="55d0e-103">Removes a VpnConnection.</span></span>

## <span data-ttu-id="55d0e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55d0e-104">SYNTAX</span></span>

### <span data-ttu-id="55d0e-105">ByVpnConnectionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="55d0e-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55d0e-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="55d0e-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzVpnConnection -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55d0e-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="55d0e-107">ByVpnConnectionObject</span></span>
```
Remove-AzVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55d0e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55d0e-108">DESCRIPTION</span></span>
<span data-ttu-id="55d0e-109">Entfernt eine VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="55d0e-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="55d0e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="55d0e-110">EXAMPLES</span></span>

### <span data-ttu-id="55d0e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="55d0e-111">Example 1</span></span>
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
PS C:\> Remove-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"
```

<span data-ttu-id="55d0e-112">Mit dem vorstehenden Beispiel werden eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub und eine VpnWebsite in West USA in der Ressourcengruppe "testRG" in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="55d0e-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="55d0e-113">Anschließend wird im virtuellen Hub ein VPN-Gateway mit zwei Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="55d0e-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="55d0e-114">Nachdem das Gateway erstellt wurde, wird es mithilfe des Befehls New-AzVpnConnection mit der VpnSite verbunden.</span><span class="sxs-lookup"><span data-stu-id="55d0e-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="55d0e-115">Anschließend wird die Verbindung mithilfe des Verbindungsnamens entfernt.</span><span class="sxs-lookup"><span data-stu-id="55d0e-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="55d0e-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="55d0e-116">Example 2</span></span>

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
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" | Remove-AzVpnConnection
```

<span data-ttu-id="55d0e-117">Wie Beispiel 1 wird die Verbindung mit dem piped-Objekt nun aus Get-AzVpnConnection entfernt.</span><span class="sxs-lookup"><span data-stu-id="55d0e-117">Same as example 1, but it now removes the connection using the piped object from Get-AzVpnConnection.</span></span>

## <span data-ttu-id="55d0e-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="55d0e-118">PARAMETERS</span></span>

### <span data-ttu-id="55d0e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55d0e-119">-DefaultProfile</span></span>
<span data-ttu-id="55d0e-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55d0e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55d0e-121">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="55d0e-121">-Force</span></span>
<span data-ttu-id="55d0e-122">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="55d0e-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="55d0e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55d0e-123">-InputObject</span></span>
<span data-ttu-id="55d0e-124">Das zu aktualisierende VpnConnection-Objekt.</span><span class="sxs-lookup"><span data-stu-id="55d0e-124">The VpnConnection object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55d0e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="55d0e-125">-Name</span></span>
<span data-ttu-id="55d0e-126">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="55d0e-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55d0e-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="55d0e-127">-ParentResourceName</span></span>
<span data-ttu-id="55d0e-128">Der übergeordnete Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="55d0e-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55d0e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55d0e-129">-PassThru</span></span>
<span data-ttu-id="55d0e-130">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="55d0e-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="55d0e-131">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="55d0e-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="55d0e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55d0e-132">-ResourceGroupName</span></span>
<span data-ttu-id="55d0e-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="55d0e-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55d0e-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55d0e-134">-ResourceId</span></span>
<span data-ttu-id="55d0e-135">Die Ressourcen-ID des zu löschende VpnConnection-Objekts.</span><span class="sxs-lookup"><span data-stu-id="55d0e-135">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55d0e-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="55d0e-136">-Confirm</span></span>
<span data-ttu-id="55d0e-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55d0e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55d0e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55d0e-138">-WhatIf</span></span>
<span data-ttu-id="55d0e-139">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55d0e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55d0e-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55d0e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55d0e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55d0e-141">CommonParameters</span></span>
<span data-ttu-id="55d0e-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55d0e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55d0e-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55d0e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55d0e-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="55d0e-144">INPUTS</span></span>

### <span data-ttu-id="55d0e-145">System.String</span><span class="sxs-lookup"><span data-stu-id="55d0e-145">System.String</span></span>

### <span data-ttu-id="55d0e-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="55d0e-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="55d0e-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="55d0e-147">OUTPUTS</span></span>

### <span data-ttu-id="55d0e-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="55d0e-148">System.Boolean</span></span>

## <span data-ttu-id="55d0e-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="55d0e-149">NOTES</span></span>

## <span data-ttu-id="55d0e-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="55d0e-150">RELATED LINKS</span></span>

[<span data-ttu-id="55d0e-151">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="55d0e-151">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="55d0e-152">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="55d0e-152">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="55d0e-153">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="55d0e-153">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
