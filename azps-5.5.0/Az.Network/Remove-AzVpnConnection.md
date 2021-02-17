---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
ms.openlocfilehash: 825090358ea94223d483fe418d06896f1f741045
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158924"
---
# <span data-ttu-id="c72e7-101">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="c72e7-101">Remove-AzVpnConnection</span></span>

## <span data-ttu-id="c72e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c72e7-102">SYNOPSIS</span></span>
<span data-ttu-id="c72e7-103">Entfernt ein VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="c72e7-103">Removes a VpnConnection.</span></span>

## <span data-ttu-id="c72e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c72e7-104">SYNTAX</span></span>

### <span data-ttu-id="c72e7-105">ByVpnConnectionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c72e7-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c72e7-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="c72e7-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzVpnConnection -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c72e7-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="c72e7-107">ByVpnConnectionObject</span></span>
```
Remove-AzVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c72e7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c72e7-108">DESCRIPTION</span></span>
<span data-ttu-id="c72e7-109">Entfernt ein VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="c72e7-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="c72e7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c72e7-110">EXAMPLES</span></span>

### <span data-ttu-id="c72e7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c72e7-111">Example 1</span></span>
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

<span data-ttu-id="c72e7-112">Im vorstehenden Beispiel wird eine Ressourcengruppe, ein virtuelles WAN, ein virtuelles Netzwerk, ein virtueller Hub und eine VpnSite in Der USA in der Ressourcengruppe "testRG" in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="c72e7-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="c72e7-113">Anschließend wird im virtuellen Hub ein VPN-Gateway mit 2 Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="c72e7-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="c72e7-114">Sobald das Gateway erstellt wurde, wird es mithilfe des Befehls "New-AzVpnConnection Mit der VpnSite verbunden.</span><span class="sxs-lookup"><span data-stu-id="c72e7-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="c72e7-115">Anschließend wird die Verbindung unter dem Verbindungsnamen entfernt.</span><span class="sxs-lookup"><span data-stu-id="c72e7-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="c72e7-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c72e7-116">Example 2</span></span>

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

<span data-ttu-id="c72e7-117">Wie in Beispiel 1, aber jetzt wird die Verbindung mit dem piped-Objekt aus "Get-AzVpnConnection" entfernt.</span><span class="sxs-lookup"><span data-stu-id="c72e7-117">Same as example 1, but it now removes the connection using the piped object from Get-AzVpnConnection.</span></span>

## <span data-ttu-id="c72e7-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c72e7-118">PARAMETERS</span></span>

### <span data-ttu-id="c72e7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c72e7-119">-DefaultProfile</span></span>
<span data-ttu-id="c72e7-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c72e7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c72e7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c72e7-121">-Force</span></span>
<span data-ttu-id="c72e7-122">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="c72e7-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c72e7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c72e7-123">-InputObject</span></span>
<span data-ttu-id="c72e7-124">Das zu aktualisierende VpnConnection-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c72e7-124">The VpnConnection object to update.</span></span>

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

### <span data-ttu-id="c72e7-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c72e7-125">-Name</span></span>
<span data-ttu-id="c72e7-126">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="c72e7-126">The resource name.</span></span>

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

### <span data-ttu-id="c72e7-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="c72e7-127">-ParentResourceName</span></span>
<span data-ttu-id="c72e7-128">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="c72e7-128">The parent resource name.</span></span>

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

### <span data-ttu-id="c72e7-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c72e7-129">-PassThru</span></span>
<span data-ttu-id="c72e7-130">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c72e7-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c72e7-131">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="c72e7-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c72e7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c72e7-132">-ResourceGroupName</span></span>
<span data-ttu-id="c72e7-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c72e7-133">The resource group name.</span></span>

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

### <span data-ttu-id="c72e7-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c72e7-134">-ResourceId</span></span>
<span data-ttu-id="c72e7-135">Die Ressourcen-ID des zu löschende VpnConnection-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c72e7-135">The resource id of the VpnConnection object to delete.</span></span>

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

### <span data-ttu-id="c72e7-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c72e7-136">-Confirm</span></span>
<span data-ttu-id="c72e7-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c72e7-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c72e7-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c72e7-138">-WhatIf</span></span>
<span data-ttu-id="c72e7-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c72e7-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c72e7-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c72e7-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c72e7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c72e7-141">CommonParameters</span></span>
<span data-ttu-id="c72e7-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c72e7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c72e7-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c72e7-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c72e7-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c72e7-144">INPUTS</span></span>

### <span data-ttu-id="c72e7-145">System.String</span><span class="sxs-lookup"><span data-stu-id="c72e7-145">System.String</span></span>

### <span data-ttu-id="c72e7-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="c72e7-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="c72e7-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c72e7-147">OUTPUTS</span></span>

### <span data-ttu-id="c72e7-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c72e7-148">System.Boolean</span></span>

## <span data-ttu-id="c72e7-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c72e7-149">NOTES</span></span>

## <span data-ttu-id="c72e7-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c72e7-150">RELATED LINKS</span></span>

[<span data-ttu-id="c72e7-151">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="c72e7-151">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="c72e7-152">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="c72e7-152">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="c72e7-153">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="c72e7-153">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
