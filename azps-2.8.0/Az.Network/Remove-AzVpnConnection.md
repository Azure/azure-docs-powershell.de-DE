---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
ms.openlocfilehash: 46b3c223cebd59d155747b70196288f344a54c6b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822791"
---
# <span data-ttu-id="fae70-101">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fae70-101">Remove-AzVpnConnection</span></span>

## <span data-ttu-id="fae70-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fae70-102">SYNOPSIS</span></span>
<span data-ttu-id="fae70-103">Entfernt eine VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="fae70-103">Removes a VpnConnection.</span></span>

## <span data-ttu-id="fae70-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fae70-104">SYNTAX</span></span>

### <span data-ttu-id="fae70-105">ByVpnConnectionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fae70-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fae70-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="fae70-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzVpnConnection -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fae70-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="fae70-107">ByVpnConnectionObject</span></span>
```
Remove-AzVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fae70-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fae70-108">DESCRIPTION</span></span>
<span data-ttu-id="fae70-109">Entfernt eine VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="fae70-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="fae70-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fae70-110">EXAMPLES</span></span>

### <span data-ttu-id="fae70-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fae70-111">Example 1</span></span>
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

<span data-ttu-id="fae70-112">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuellen Hub und einen VpnSite in West US in "testRG"-Ressourcengruppe in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="fae70-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="fae70-113">Anschließend wird ein VPN-Gateway im virtuellen Hub mit 2 Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="fae70-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="fae70-114">Nachdem das Gateway erstellt wurde, wird es mit dem VpnSite mit dem Befehl New-AzVpnConnection verbunden.</span><span class="sxs-lookup"><span data-stu-id="fae70-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="fae70-115">Anschließend wird die Verbindung mit dem Verbindungsnamen entfernt.</span><span class="sxs-lookup"><span data-stu-id="fae70-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="fae70-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fae70-116">Example 2</span></span>

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

<span data-ttu-id="fae70-117">Identisch mit Beispiel 1, aber jetzt wird die Verbindung mit dem piped-Objekt aus Get-AzVpnConnection entfernt.</span><span class="sxs-lookup"><span data-stu-id="fae70-117">Same as example 1, but it now removes the connection using the piped object from Get-AzVpnConnection.</span></span>

## <span data-ttu-id="fae70-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="fae70-118">PARAMETERS</span></span>

### <span data-ttu-id="fae70-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae70-119">-DefaultProfile</span></span>
<span data-ttu-id="fae70-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fae70-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fae70-121">-Force</span><span class="sxs-lookup"><span data-stu-id="fae70-121">-Force</span></span>
<span data-ttu-id="fae70-122">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="fae70-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fae70-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fae70-123">-InputObject</span></span>
<span data-ttu-id="fae70-124">Das zu Aktualisier VpnConnection-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fae70-124">The VpnConnection object to update.</span></span>

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

### <span data-ttu-id="fae70-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fae70-125">-Name</span></span>
<span data-ttu-id="fae70-126">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="fae70-126">The resource name.</span></span>

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

### <span data-ttu-id="fae70-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="fae70-127">-ParentResourceName</span></span>
<span data-ttu-id="fae70-128">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="fae70-128">The parent resource name.</span></span>

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

### <span data-ttu-id="fae70-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fae70-129">-PassThru</span></span>
<span data-ttu-id="fae70-130">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="fae70-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fae70-131">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="fae70-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fae70-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fae70-132">-ResourceGroupName</span></span>
<span data-ttu-id="fae70-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fae70-133">The resource group name.</span></span>

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

### <span data-ttu-id="fae70-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fae70-134">-ResourceId</span></span>
<span data-ttu-id="fae70-135">Die Ressourcen-ID des zu löschenden VpnConnection-Objekts.</span><span class="sxs-lookup"><span data-stu-id="fae70-135">The resource id of the VpnConnection object to delete.</span></span>

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

### <span data-ttu-id="fae70-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fae70-136">-Confirm</span></span>
<span data-ttu-id="fae70-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fae70-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fae70-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fae70-138">-WhatIf</span></span>
<span data-ttu-id="fae70-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fae70-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fae70-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fae70-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fae70-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae70-141">CommonParameters</span></span>
<span data-ttu-id="fae70-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fae70-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae70-143">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fae70-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae70-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fae70-144">INPUTS</span></span>

### <span data-ttu-id="fae70-145">System. String</span><span class="sxs-lookup"><span data-stu-id="fae70-145">System.String</span></span>

### <span data-ttu-id="fae70-146">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fae70-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="fae70-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fae70-147">OUTPUTS</span></span>

### <span data-ttu-id="fae70-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fae70-148">System.Boolean</span></span>

## <span data-ttu-id="fae70-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="fae70-149">NOTES</span></span>

## <span data-ttu-id="fae70-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fae70-150">RELATED LINKS</span></span>

[<span data-ttu-id="fae70-151">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fae70-151">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="fae70-152">Neu – AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fae70-152">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="fae70-153">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fae70-153">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
