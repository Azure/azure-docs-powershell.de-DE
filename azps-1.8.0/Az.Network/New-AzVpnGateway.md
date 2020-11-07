---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: 08915aaf72fbab91d8173480f4e608ebdbaa28ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660446"
---
# <span data-ttu-id="370c8-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="370c8-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="370c8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="370c8-102">SYNOPSIS</span></span>
<span data-ttu-id="370c8-103">Erstellt ein skalierbares VPN-Gateway.</span><span class="sxs-lookup"><span data-stu-id="370c8-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="370c8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="370c8-104">SYNTAX</span></span>

### <span data-ttu-id="370c8-105">ByVirtualHubName (Standard)</span><span class="sxs-lookup"><span data-stu-id="370c8-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="370c8-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="370c8-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="370c8-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="370c8-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="370c8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="370c8-108">DESCRIPTION</span></span>

<span data-ttu-id="370c8-109">New-AzVpnGateway erstellt ein skalierbares VPN-Gateway.</span><span class="sxs-lookup"><span data-stu-id="370c8-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span> <span data-ttu-id="370c8-110">Hierbei handelt es sich um Software definierte Konnektivität für Standort-zu-Standort-Verbindungen innerhalb des VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="370c8-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span> 

<span data-ttu-id="370c8-111">Dieses Gateway ändert die Größe und skaliert basierend auf der in diesem oder dem Set-AzVpnGateway-Cmdlet angegebenen Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="370c8-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span> 

<span data-ttu-id="370c8-112">Eine Verbindung wird von einer Verzweigung/Website eingerichtet, die als "VPNSite" für das skalierbare Gateway bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="370c8-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="370c8-113">Jede Verbindung besteht aus zwei Active-Active Tunnels.</span><span class="sxs-lookup"><span data-stu-id="370c8-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="370c8-114">Die VpnGateway befindet sich am gleichen Speicherort wie die referenzierte VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="370c8-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="370c8-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="370c8-115">EXAMPLES</span></span>

### <span data-ttu-id="370c8-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="370c8-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="370c8-117">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuelles Drehkreuz in West US in der Ressourcengruppe "testRG" in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="370c8-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="370c8-118">Anschließend wird ein VPN-Gateway im virtuellen Hub mit 2 Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="370c8-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="370c8-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="370c8-119">PARAMETERS</span></span>

### <span data-ttu-id="370c8-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="370c8-120">-AsJob</span></span>
<span data-ttu-id="370c8-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="370c8-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="370c8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="370c8-122">-DefaultProfile</span></span>
<span data-ttu-id="370c8-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="370c8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="370c8-124">-Name</span><span class="sxs-lookup"><span data-stu-id="370c8-124">-Name</span></span>
<span data-ttu-id="370c8-125">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="370c8-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="370c8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="370c8-126">-ResourceGroupName</span></span>
<span data-ttu-id="370c8-127">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="370c8-127">The resource name.</span></span>

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

### <span data-ttu-id="370c8-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="370c8-128">-Tag</span></span>
<span data-ttu-id="370c8-129">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="370c8-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="370c8-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="370c8-130">-VirtualHub</span></span>
<span data-ttu-id="370c8-131">Das VirtualHub, dem dieses VpnGateway zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="370c8-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="370c8-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="370c8-132">-VirtualHubId</span></span>
<span data-ttu-id="370c8-133">Die ID des VirtualHub, dem dieses VpnGateway zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="370c8-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="370c8-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="370c8-134">-VirtualHubName</span></span>
<span data-ttu-id="370c8-135">Die ID des VirtualHub, dem dieses VpnGateway zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="370c8-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="370c8-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="370c8-136">-VpnConnection</span></span>
<span data-ttu-id="370c8-137">Die Liste der VpnConnections, die dieser VpnGateway haben muss.</span><span class="sxs-lookup"><span data-stu-id="370c8-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="370c8-138">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="370c8-138">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="370c8-139">Die Skalierungseinheit für diesen VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="370c8-139">The scale unit for this VpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="370c8-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="370c8-140">-Confirm</span></span>
<span data-ttu-id="370c8-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="370c8-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="370c8-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="370c8-142">-WhatIf</span></span>
<span data-ttu-id="370c8-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="370c8-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="370c8-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="370c8-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="370c8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="370c8-145">CommonParameters</span></span>
<span data-ttu-id="370c8-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="370c8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="370c8-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="370c8-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="370c8-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="370c8-148">INPUTS</span></span>

### <span data-ttu-id="370c8-149">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="370c8-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="370c8-150">System. String</span><span class="sxs-lookup"><span data-stu-id="370c8-150">System.String</span></span>

## <span data-ttu-id="370c8-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="370c8-151">OUTPUTS</span></span>

### <span data-ttu-id="370c8-152">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="370c8-152">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="370c8-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="370c8-153">NOTES</span></span>

## <span data-ttu-id="370c8-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="370c8-154">RELATED LINKS</span></span>

[<span data-ttu-id="370c8-155">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="370c8-155">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="370c8-156">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="370c8-156">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="370c8-157">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="370c8-157">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
