---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: 720b81b858799e2930ed3d2cdd45e25220697e6a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169602"
---
# <span data-ttu-id="f1bc4-101">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f1bc4-101">Start-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="f1bc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1bc4-102">SYNOPSIS</span></span>
<span data-ttu-id="f1bc4-103">Startet den Paketerfassungsvorgang für eine Vpn-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="f1bc4-103">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="f1bc4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1bc4-104">SYNTAX</span></span>

### <span data-ttu-id="f1bc4-105">ByVpnConnectionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1bc4-105">ByVpnConnectionName (Default)</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-FilterData <String>] -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1bc4-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="f1bc4-106">ByVpnConnectionObject</span></span>
```
Start-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> [-FilterData <String>]
 -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1bc4-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="f1bc4-107">ByVpnConnectionResourceId</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceId <String> [-FilterData <String>] -LinkConnectionName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1bc4-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1bc4-108">DESCRIPTION</span></span>
<span data-ttu-id="f1bc4-109">Startet den Paketerfassungsvorgang für eine Vpn-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="f1bc4-109">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="f1bc4-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f1bc4-110">EXAMPLES</span></span>

### <span data-ttu-id="f1bc4-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f1bc4-111">Example 1</span></span>
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

### <span data-ttu-id="f1bc4-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f1bc4-112">Example 2</span></span>
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

## <span data-ttu-id="f1bc4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1bc4-113">PARAMETERS</span></span>

### <span data-ttu-id="f1bc4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1bc4-114">-AsJob</span></span>
<span data-ttu-id="f1bc4-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f1bc4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1bc4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1bc4-116">-DefaultProfile</span></span>
<span data-ttu-id="f1bc4-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1bc4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1bc4-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="f1bc4-118">-FilterData</span></span>
<span data-ttu-id="f1bc4-119">Filteroptionen für das Starten der Paketerfassung bei einer Vpn-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="f1bc4-119">Filter options for start packet capture on Vpn connection.</span></span>

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

### <span data-ttu-id="f1bc4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1bc4-120">-InputObject</span></span>
<span data-ttu-id="f1bc4-121">Das Vpn-Verbindungsobjekt, in dem die Paketaufzeichnung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1bc4-121">The Vpn connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="f1bc4-122">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="f1bc4-122">-LinkConnectionName</span></span>
<span data-ttu-id="f1bc4-123">Die Namen von SiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="f1bc4-123">The names of the SiteLinkConnection.</span></span>

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

### <span data-ttu-id="f1bc4-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f1bc4-124">-Name</span></span>
<span data-ttu-id="f1bc4-125">Der Name der Vpn-Verbindung, in dem die Paketaufzeichnung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1bc4-125">The Vpn connection name where packet capture to be started.</span></span>

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

### <span data-ttu-id="f1bc4-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="f1bc4-126">-ParentResourceName</span></span>
<span data-ttu-id="f1bc4-127">Der Name des übergeordneten Vpngateways.</span><span class="sxs-lookup"><span data-stu-id="f1bc4-127">The name of the Parent Vpngateway.</span></span>

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

### <span data-ttu-id="f1bc4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1bc4-128">-ResourceGroupName</span></span>
<span data-ttu-id="f1bc4-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f1bc4-129">The resource group name.</span></span>

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

### <span data-ttu-id="f1bc4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1bc4-130">-ResourceId</span></span>
<span data-ttu-id="f1bc4-131">Die Azure-Ressourcen-ID des VpnConnection-Kontos, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1bc4-131">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="f1bc4-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1bc4-132">-Confirm</span></span>
<span data-ttu-id="f1bc4-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1bc4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1bc4-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f1bc4-134">-WhatIf</span></span>
<span data-ttu-id="f1bc4-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1bc4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1bc4-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1bc4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1bc4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1bc4-137">CommonParameters</span></span>
<span data-ttu-id="f1bc4-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1bc4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1bc4-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1bc4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1bc4-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f1bc4-140">INPUTS</span></span>

### <span data-ttu-id="f1bc4-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="f1bc4-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="f1bc4-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f1bc4-142">System.String</span></span>

## <span data-ttu-id="f1bc4-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f1bc4-143">OUTPUTS</span></span>

### <span data-ttu-id="f1bc4-144">Microsoft.Azure.Commands.Network.Models.PSVpnConnectionPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="f1bc4-144">Microsoft.Azure.Commands.Network.Models.PSVpnConnectionPacketCaptureResult</span></span>

## <span data-ttu-id="f1bc4-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f1bc4-145">NOTES</span></span>

## <span data-ttu-id="f1bc4-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f1bc4-146">RELATED LINKS</span></span>

[<span data-ttu-id="f1bc4-147">Stop-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f1bc4-147">Stop-AzVpnConnectionPacketCapture</span></span>](./Stop-AzVpnConnectionPacketCapture.md)