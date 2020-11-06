---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnConnection.md
ms.openlocfilehash: da023b7c0b060e9e263b6b0677065746568524b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482213"
---
# <span data-ttu-id="178e5-101">Remove-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="178e5-101">Remove-AzureRmVpnConnection</span></span>

## <span data-ttu-id="178e5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="178e5-102">SYNOPSIS</span></span>
<span data-ttu-id="178e5-103">Entfernt eine VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="178e5-103">Removes a VpnConnection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="178e5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="178e5-104">SYNTAX</span></span>

### <span data-ttu-id="178e5-105">ByVpnConnectionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="178e5-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="178e5-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="178e5-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzureRmVpnConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="178e5-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="178e5-107">ByVpnConnectionObject</span></span>
```
Remove-AzureRmVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="178e5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="178e5-108">DESCRIPTION</span></span>
<span data-ttu-id="178e5-109">Entfernt eine VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="178e5-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="178e5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="178e5-110">EXAMPLES</span></span>

### <span data-ttu-id="178e5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="178e5-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Remove-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"
```

<span data-ttu-id="178e5-112">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuellen Hub und einen VpnSite in West US in "testRG"-Ressourcengruppe in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="178e5-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="178e5-113">Anschließend wird ein VPN-Gateway im virtuellen Hub mit 2 Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="178e5-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="178e5-114">Nachdem das Gateway erstellt wurde, wird es mit dem VpnSite mit dem Befehl New-AzureRmVpnConnection verbunden.</span><span class="sxs-lookup"><span data-stu-id="178e5-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="178e5-115">Anschließend wird die Verbindung mit dem Verbindungsnamen entfernt.</span><span class="sxs-lookup"><span data-stu-id="178e5-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="178e5-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="178e5-116">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" | Remove-AzureRmVpnConnection
```

<span data-ttu-id="178e5-117">Identisch mit Beispiel 1, aber jetzt wird die Verbindung mit dem piped-Objekt aus Get-AzureRmVpnConnection entfernt.</span><span class="sxs-lookup"><span data-stu-id="178e5-117">Same as example 1, but it now removes the connection using the piped object from Get-AzureRmVpnConnection.</span></span>

## <span data-ttu-id="178e5-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="178e5-118">PARAMETERS</span></span>

### <span data-ttu-id="178e5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="178e5-119">-DefaultProfile</span></span>
<span data-ttu-id="178e5-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="178e5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178e5-121">-Force</span><span class="sxs-lookup"><span data-stu-id="178e5-121">-Force</span></span>
<span data-ttu-id="178e5-122">Keine Bestätigung anfordern, wenn Sie eine Ressource overriten möchten</span><span class="sxs-lookup"><span data-stu-id="178e5-122">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="178e5-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="178e5-123">-InputObject</span></span>
<span data-ttu-id="178e5-124">Das zu Aktualisier VpnConenction-Objekt.</span><span class="sxs-lookup"><span data-stu-id="178e5-124">The VpnConenction object to update.</span></span>

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

### <span data-ttu-id="178e5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="178e5-125">-Name</span></span>
<span data-ttu-id="178e5-126">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="178e5-126">The resource name.</span></span>

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

### <span data-ttu-id="178e5-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="178e5-127">-ParentResourceName</span></span>
<span data-ttu-id="178e5-128">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="178e5-128">The parent resource name.</span></span>

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

### <span data-ttu-id="178e5-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="178e5-129">-PassThru</span></span>
<span data-ttu-id="178e5-130">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="178e5-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="178e5-131">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="178e5-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="178e5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="178e5-132">-ResourceGroupName</span></span>
<span data-ttu-id="178e5-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="178e5-133">The resource group name.</span></span>

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

### <span data-ttu-id="178e5-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="178e5-134">-ResourceId</span></span>
<span data-ttu-id="178e5-135">Die Ressourcen-ID des zu löschenden VpnConenction-Objekts.</span><span class="sxs-lookup"><span data-stu-id="178e5-135">The resource id of the VpnConenction object to delete.</span></span>

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

### <span data-ttu-id="178e5-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="178e5-136">-Confirm</span></span>
<span data-ttu-id="178e5-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="178e5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="178e5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="178e5-138">-WhatIf</span></span>
<span data-ttu-id="178e5-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="178e5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="178e5-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="178e5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="178e5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="178e5-141">CommonParameters</span></span>
<span data-ttu-id="178e5-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="178e5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="178e5-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="178e5-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="178e5-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="178e5-144">INPUTS</span></span>

### <span data-ttu-id="178e5-145">System. String</span><span class="sxs-lookup"><span data-stu-id="178e5-145">System.String</span></span>

### <span data-ttu-id="178e5-146">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="178e5-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="178e5-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="178e5-147">OUTPUTS</span></span>

### <span data-ttu-id="178e5-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="178e5-148">System.Boolean</span></span>

## <span data-ttu-id="178e5-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="178e5-149">NOTES</span></span>

## <span data-ttu-id="178e5-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="178e5-150">RELATED LINKS</span></span>
