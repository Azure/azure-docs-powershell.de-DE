---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: 720b81b858799e2930ed3d2cdd45e25220697e6a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303520"
---
# <span data-ttu-id="45e49-101">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="45e49-101">Start-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="45e49-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="45e49-102">SYNOPSIS</span></span>
<span data-ttu-id="45e49-103">Startet den Paket Erfassungsvorgang für eine VPN-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="45e49-103">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="45e49-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="45e49-104">SYNTAX</span></span>

### <span data-ttu-id="45e49-105">ByVpnConnectionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="45e49-105">ByVpnConnectionName (Default)</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-FilterData <String>] -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45e49-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="45e49-106">ByVpnConnectionObject</span></span>
```
Start-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> [-FilterData <String>]
 -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45e49-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="45e49-107">ByVpnConnectionResourceId</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceId <String> [-FilterData <String>] -LinkConnectionName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45e49-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45e49-108">DESCRIPTION</span></span>
<span data-ttu-id="45e49-109">Startet den Paket Erfassungsvorgang für eine VPN-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="45e49-109">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="45e49-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45e49-110">EXAMPLES</span></span>

### <span data-ttu-id="45e49-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="45e49-111">Example 1</span></span>
```powershell
Start-AzVpnConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -ParentResourceName "VpnGw1" -LinkConnectionName "PktCaptureTestSite2Site1CnLink1"
Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
LinkConnectionName: PktCaptureTestSite2Site1CnLink1
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```

### <span data-ttu-id="45e49-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="45e49-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVpnConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -ParentResourceName "VpnGw1" -LinkConnectionName "PktCaptureTestSite2Site1CnLink1,PktCaptureTestSite2Site1CnLink1" -FilterData $a 
Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
LinkConnectionName: PktCaptureTestSite2Site1CnLink1,PktCaptureTestSite2Site1CnLink1
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```

## <span data-ttu-id="45e49-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="45e49-113">PARAMETERS</span></span>

### <span data-ttu-id="45e49-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45e49-114">-AsJob</span></span>
<span data-ttu-id="45e49-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="45e49-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45e49-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45e49-116">-DefaultProfile</span></span>
<span data-ttu-id="45e49-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="45e49-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45e49-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="45e49-118">-FilterData</span></span>
<span data-ttu-id="45e49-119">Filter Optionen für Start-Paketerfassung bei VPN-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="45e49-119">Filter options for start packet capture on Vpn connection.</span></span>

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

### <span data-ttu-id="45e49-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="45e49-120">-InputObject</span></span>
<span data-ttu-id="45e49-121">Das VPN-Verbindungsobjekt, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="45e49-121">The Vpn connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="45e49-122">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="45e49-122">-LinkConnectionName</span></span>
<span data-ttu-id="45e49-123">Die Namen der SiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="45e49-123">The names of the SiteLinkConnection.</span></span>

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

### <span data-ttu-id="45e49-124">-Name</span><span class="sxs-lookup"><span data-stu-id="45e49-124">-Name</span></span>
<span data-ttu-id="45e49-125">Der VPN-Verbindungsname, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="45e49-125">The Vpn connection name where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45e49-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="45e49-126">-ParentResourceName</span></span>
<span data-ttu-id="45e49-127">Der Name des übergeordneten Vpngateway.</span><span class="sxs-lookup"><span data-stu-id="45e49-127">The name of the Parent Vpngateway.</span></span>

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

### <span data-ttu-id="45e49-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45e49-128">-ResourceGroupName</span></span>
<span data-ttu-id="45e49-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="45e49-129">The resource group name.</span></span>

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

### <span data-ttu-id="45e49-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="45e49-130">-ResourceId</span></span>
<span data-ttu-id="45e49-131">Die Azure-Ressourcen-ID des VpnConnection, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="45e49-131">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45e49-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="45e49-132">-Confirm</span></span>
<span data-ttu-id="45e49-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="45e49-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45e49-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45e49-134">-WhatIf</span></span>
<span data-ttu-id="45e49-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="45e49-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45e49-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="45e49-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45e49-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45e49-137">CommonParameters</span></span>
<span data-ttu-id="45e49-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45e49-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45e49-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45e49-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45e49-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="45e49-140">INPUTS</span></span>

### <span data-ttu-id="45e49-141">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="45e49-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="45e49-142">System. String</span><span class="sxs-lookup"><span data-stu-id="45e49-142">System.String</span></span>

## <span data-ttu-id="45e49-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="45e49-143">OUTPUTS</span></span>

### <span data-ttu-id="45e49-144">Microsoft. Azure. Commands. Network. Models. PSVpnConnectionPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="45e49-144">Microsoft.Azure.Commands.Network.Models.PSVpnConnectionPacketCaptureResult</span></span>

## <span data-ttu-id="45e49-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="45e49-145">NOTES</span></span>

## <span data-ttu-id="45e49-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="45e49-146">RELATED LINKS</span></span>

[<span data-ttu-id="45e49-147">Stopp-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="45e49-147">Stop-AzVpnConnectionPacketCapture</span></span>](./Stop-AzVpnConnectionPacketCapture.md)