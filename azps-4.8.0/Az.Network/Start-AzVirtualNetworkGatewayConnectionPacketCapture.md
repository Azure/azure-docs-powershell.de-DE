---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: d01fad830b9edcd8eced13a4f1e9317bb4930f9c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165107"
---
# <span data-ttu-id="d9e5f-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d9e5f-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="d9e5f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d9e5f-102">SYNOPSIS</span></span>
<span data-ttu-id="d9e5f-103">Startet den Paket Erfassungsvorgang auf einer virtuellen Netzwerk Gateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-103">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="d9e5f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9e5f-104">SYNTAX</span></span>

### <span data-ttu-id="d9e5f-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d9e5f-105">ByName (Default)</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9e5f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d9e5f-106">ByInputObject</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9e5f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d9e5f-107">ByResourceId</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9e5f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9e5f-108">DESCRIPTION</span></span>
<span data-ttu-id="d9e5f-109">Startet den Paket Erfassungsvorgang auf einer virtuellen Netzwerk Gateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-109">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="d9e5f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d9e5f-110">EXAMPLES</span></span>

### <span data-ttu-id="d9e5f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d9e5f-111">Example 1</span></span>
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
### <span data-ttu-id="d9e5f-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d9e5f-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
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
### <span data-ttu-id="d9e5f-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d9e5f-113">Example 3</span></span>
<span data-ttu-id="d9e5f-114">Beispiel für die Paketerfassung zum Erfassen aller inneren und äußeren Pakete</span><span class="sxs-lookup"><span data-stu-id="d9e5f-114">Packet Capture example for capture all inner and outer packets</span></span>
```powershell
$a = "{`"TracingFlags`": 11,`"MaxPacketBufferSize`": 120,`"MaxFileSize`": 500,`"Filters`" :[{`"CaptureSingleDirectionTrafficOnly`": false}]}"
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

## <span data-ttu-id="d9e5f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9e5f-115">PARAMETERS</span></span>

### <span data-ttu-id="d9e5f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9e5f-116">-AsJob</span></span>
<span data-ttu-id="d9e5f-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d9e5f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9e5f-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d9e5f-118">-Confirm</span></span>
<span data-ttu-id="d9e5f-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9e5f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9e5f-120">-DefaultProfile</span></span>
<span data-ttu-id="d9e5f-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9e5f-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="d9e5f-122">-FilterData</span></span>
<span data-ttu-id="d9e5f-123">Filter Optionen für die Start-Paketerfassung bei einer virtuellen Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-123">Filter options for start packet capture on virtual network gateway connection.</span></span>

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

### <span data-ttu-id="d9e5f-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d9e5f-124">-InputObject</span></span>
<span data-ttu-id="d9e5f-125">Das virtuelle Netzwerkgateway-Verbindungsobjekt, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-125">The virtual network gateway connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="d9e5f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="d9e5f-126">-Name</span></span>
<span data-ttu-id="d9e5f-127">Der Verbindungsname des virtuellen Netzwerkgateways, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-127">The virtual network gateway connection name where packet capture to be started.</span></span>

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

### <span data-ttu-id="d9e5f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9e5f-128">-ResourceGroupName</span></span>
<span data-ttu-id="d9e5f-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-129">The resource group name.</span></span>

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

### <span data-ttu-id="d9e5f-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d9e5f-130">-ResourceId</span></span>
<span data-ttu-id="d9e5f-131">Die Azure-Ressourcen-ID des VirtualNetworkGatewayConnection, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-131">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="d9e5f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9e5f-132">-WhatIf</span></span>
<span data-ttu-id="d9e5f-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9e5f-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9e5f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9e5f-135">CommonParameters</span></span>
<span data-ttu-id="d9e5f-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9e5f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9e5f-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9e5f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9e5f-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d9e5f-138">INPUTS</span></span>

### <span data-ttu-id="d9e5f-139">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d9e5f-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="d9e5f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d9e5f-140">System.String</span></span>

## <span data-ttu-id="d9e5f-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d9e5f-141">OUTPUTS</span></span>

### <span data-ttu-id="d9e5f-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="d9e5f-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="d9e5f-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="d9e5f-143">NOTES</span></span>

## <span data-ttu-id="d9e5f-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d9e5f-144">RELATED LINKS</span></span>
[<span data-ttu-id="d9e5f-145">Stopp-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d9e5f-145">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>](./Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md)