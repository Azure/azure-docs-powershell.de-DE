---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnGateway.md
ms.openlocfilehash: 00730f6e252373eebbbbc476fdd889b2eeb39e12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663118"
---
# <span data-ttu-id="a6df1-101">Update-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a6df1-101">Update-AzureRmVpnGateway</span></span>

## <span data-ttu-id="a6df1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a6df1-102">SYNOPSIS</span></span>
<span data-ttu-id="a6df1-103">Update-AzureRmVpnGateway aktualisiert ein skalierbares VPN-Gateway in den entsprechenden Zielzustand.</span><span class="sxs-lookup"><span data-stu-id="a6df1-103">Update-AzureRmVpnGateway updates a scalable VPN Gateway to the appropriate goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6df1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6df1-104">SYNTAX</span></span>

### <span data-ttu-id="a6df1-105">ByVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a6df1-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6df1-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="a6df1-106">ByVpnGatewayObject</span></span>
```
Update-AzureRmVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6df1-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="a6df1-107">ByVpnGatewayResourceId</span></span>
```
Update-AzureRmVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6df1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6df1-108">DESCRIPTION</span></span>
<span data-ttu-id="a6df1-109">Update-AzureRmVpnGateway aktualisiert ein skalierbares VPN-Gateway in den entsprechenden Zielzustand.</span><span class="sxs-lookup"><span data-stu-id="a6df1-109">Update-AzureRmVpnGateway updates a scalable VPN Gateway to the appropriate goal state.</span></span> <span data-ttu-id="a6df1-110">Eine AzureRmVpnGateway ist eine Software definierte Konnektivität für Website-zu-Standort-Verbindungen innerhalb des VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="a6df1-110">An AzureRmVpnGateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="a6df1-111">Dieses Gateway ändert die Größe und skaliert basierend auf der vom Benutzer angegebenen Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="a6df1-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="a6df1-112">Eine Verbindung kann über eine Verzweigung/Website, die als VPNSite bezeichnet wird, zum skalierbaren Gateway eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="a6df1-112">A connection can be set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="a6df1-113">Jede Verbindung besteht aus zwei Active-Active Tunneln</span><span class="sxs-lookup"><span data-stu-id="a6df1-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="a6df1-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a6df1-114">EXAMPLES</span></span>

### <span data-ttu-id="a6df1-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a6df1-115">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Set-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="a6df1-116">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuelles Drehkreuz in West US in der Ressourcengruppe "testRG" in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="a6df1-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="a6df1-117">Anschließend wird ein VPN-Gateway im virtuellen Hub mit 2 Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="a6df1-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="a6df1-118">Nachdem das Gateway erstellt wurde, wird Set-AzureRmVpnGateway verwendet, um das Gateway auf 3 Skaleneinheiten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a6df1-118">After the gateway has been created, it uses Set-AzureRmVpnGateway to upgrade the gateway to 3 scale units.</span></span>

## <span data-ttu-id="a6df1-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6df1-119">PARAMETERS</span></span>

### <span data-ttu-id="a6df1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6df1-120">-AsJob</span></span>
<span data-ttu-id="a6df1-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a6df1-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a6df1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6df1-122">-DefaultProfile</span></span>
<span data-ttu-id="a6df1-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a6df1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6df1-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a6df1-124">-InputObject</span></span>
<span data-ttu-id="a6df1-125">Das zu ändernde VPN-Gateway-Objekt</span><span class="sxs-lookup"><span data-stu-id="a6df1-125">The vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6df1-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a6df1-126">-Name</span></span>
<span data-ttu-id="a6df1-127">Der virtuelle WAN-Name.</span><span class="sxs-lookup"><span data-stu-id="a6df1-127">The virtual wan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6df1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6df1-128">-ResourceGroupName</span></span>
<span data-ttu-id="a6df1-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a6df1-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6df1-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a6df1-130">-ResourceId</span></span>
<span data-ttu-id="a6df1-131">Die Azure-Ressourcen-ID des zu ändernden VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a6df1-131">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6df1-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="a6df1-132">-Tag</span></span>
<span data-ttu-id="a6df1-133">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="a6df1-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a6df1-134">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="a6df1-134">-VpnConnection</span></span>
<span data-ttu-id="a6df1-135">Die Liste der VpnConnections, die dieser VpnGateway haben muss.</span><span class="sxs-lookup"><span data-stu-id="a6df1-135">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="a6df1-136">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="a6df1-136">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="a6df1-137">Die Skalierungseinheit für diesen VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a6df1-137">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="a6df1-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a6df1-138">-Confirm</span></span>
<span data-ttu-id="a6df1-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a6df1-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6df1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6df1-140">-WhatIf</span></span>
<span data-ttu-id="a6df1-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6df1-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6df1-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6df1-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6df1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6df1-143">CommonParameters</span></span>
<span data-ttu-id="a6df1-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6df1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6df1-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6df1-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6df1-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a6df1-146">INPUTS</span></span>

### <span data-ttu-id="a6df1-147">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a6df1-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="a6df1-148">System. String</span><span class="sxs-lookup"><span data-stu-id="a6df1-148">System.String</span></span>

## <span data-ttu-id="a6df1-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a6df1-149">OUTPUTS</span></span>

### <span data-ttu-id="a6df1-150">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a6df1-150">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="a6df1-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="a6df1-151">NOTES</span></span>

## <span data-ttu-id="a6df1-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a6df1-152">RELATED LINKS</span></span>
