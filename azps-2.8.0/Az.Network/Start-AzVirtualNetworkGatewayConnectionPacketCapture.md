---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 3a1d9c2f415d56263529fcd66aa1ee9535823bbf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823744"
---
# <span data-ttu-id="033b3-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="033b3-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="033b3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="033b3-102">SYNOPSIS</span></span>
<span data-ttu-id="033b3-103">Startet den Paket Erfassungsvorgang auf einer virtuellen Netzwerk Gateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="033b3-103">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="033b3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="033b3-104">SYNTAX</span></span>

### <span data-ttu-id="033b3-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="033b3-105">ByName (Default)</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="033b3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="033b3-106">ByInputObject</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="033b3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="033b3-107">ByResourceId</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="033b3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="033b3-108">DESCRIPTION</span></span>
<span data-ttu-id="033b3-109">Startet den Paket Erfassungsvorgang auf einer virtuellen Netzwerk Gateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="033b3-109">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="033b3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="033b3-110">EXAMPLES</span></span>

### <span data-ttu-id="033b3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="033b3-111">Example 1</span></span>
```powershell
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn"

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
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
### <span data-ttu-id="033b3-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="033b3-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
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

## <span data-ttu-id="033b3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="033b3-113">PARAMETERS</span></span>

### <span data-ttu-id="033b3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="033b3-114">-AsJob</span></span>
<span data-ttu-id="033b3-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="033b3-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="033b3-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="033b3-116">-Confirm</span></span>
<span data-ttu-id="033b3-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="033b3-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="033b3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="033b3-118">-DefaultProfile</span></span>
<span data-ttu-id="033b3-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="033b3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="033b3-120">-FilterData</span><span class="sxs-lookup"><span data-stu-id="033b3-120">-FilterData</span></span>
<span data-ttu-id="033b3-121">Filter Optionen für die Start-Paketerfassung bei einer virtuellen Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="033b3-121">Filter options for start packet capture on virtual network gateway connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="033b3-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="033b3-122">-InputObject</span></span>
<span data-ttu-id="033b3-123">Das virtuelle Netzwerkgateway-Verbindungsobjekt, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="033b3-123">The virtual network gateway connection object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGatewayConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="033b3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="033b3-124">-Name</span></span>
<span data-ttu-id="033b3-125">Der Verbindungsname des virtuellen Netzwerkgateways, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="033b3-125">The virtual network gateway connection name where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayConnectionName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="033b3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="033b3-126">-ResourceGroupName</span></span>
<span data-ttu-id="033b3-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="033b3-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="033b3-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="033b3-128">-ResourceId</span></span>
<span data-ttu-id="033b3-129">Die Azure-Ressourcen-ID des VirtualNetworkGatewayConnection, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="033b3-129">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="033b3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="033b3-130">-WhatIf</span></span>
<span data-ttu-id="033b3-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="033b3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="033b3-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="033b3-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="033b3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="033b3-133">CommonParameters</span></span>
<span data-ttu-id="033b3-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="033b3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="033b3-135">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="033b3-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="033b3-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="033b3-136">INPUTS</span></span>

### <span data-ttu-id="033b3-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="033b3-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="033b3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="033b3-138">System.String</span></span>

## <span data-ttu-id="033b3-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="033b3-139">OUTPUTS</span></span>

### <span data-ttu-id="033b3-140">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="033b3-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="033b3-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="033b3-141">NOTES</span></span>

## <span data-ttu-id="033b3-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="033b3-142">RELATED LINKS</span></span>
[<span data-ttu-id="033b3-143">Stopp-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="033b3-143">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>](./Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md)