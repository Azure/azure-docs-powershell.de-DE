---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
ms.openlocfilehash: b0010134ac6b819afc3e8621b11d5530a08008a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303526"
---
# <span data-ttu-id="a77a3-101">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a77a3-101">Start-AzVirtualnetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="a77a3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a77a3-102">SYNOPSIS</span></span>
<span data-ttu-id="a77a3-103">Startet den Paket Erfassungsvorgang auf einem virtuellen Netzwerk Gateway.</span><span class="sxs-lookup"><span data-stu-id="a77a3-103">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="a77a3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a77a3-104">SYNTAX</span></span>

### <span data-ttu-id="a77a3-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a77a3-105">ByName (Default)</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a77a3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a77a3-106">ByInputObject</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a77a3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a77a3-107">ByResourceId</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a77a3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a77a3-108">DESCRIPTION</span></span>
<span data-ttu-id="a77a3-109">Startet den Paket Erfassungsvorgang auf einem virtuellen Netzwerk Gateway.</span><span class="sxs-lookup"><span data-stu-id="a77a3-109">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="a77a3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a77a3-110">EXAMPLES</span></span>

### <span data-ttu-id="a77a3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a77a3-111">Example 1</span></span>
```powershell
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG"

Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```
### <span data-ttu-id="a77a3-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a77a3-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```
### <span data-ttu-id="a77a3-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a77a3-113">Example 3</span></span>
<span data-ttu-id="a77a3-114">Beispiel für die Paketerfassung zum Erfassen aller inneren und äußeren Pakete</span><span class="sxs-lookup"><span data-stu-id="a77a3-114">Packet Capture example for capture all inner and outer packets</span></span>
```powershell
$a = "{`"TracingFlags`": 11,`"MaxPacketBufferSize`": 120,`"MaxFileSize`": 500,`"Filters`" :[{`"CaptureSingleDirectionTrafficOnly`": false}]}"
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```

## <span data-ttu-id="a77a3-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a77a3-115">PARAMETERS</span></span>

### <span data-ttu-id="a77a3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a77a3-116">-AsJob</span></span>
<span data-ttu-id="a77a3-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a77a3-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a77a3-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a77a3-118">-Confirm</span></span>
<span data-ttu-id="a77a3-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a77a3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a77a3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a77a3-120">-DefaultProfile</span></span>
<span data-ttu-id="a77a3-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a77a3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a77a3-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="a77a3-122">-FilterData</span></span>
<span data-ttu-id="a77a3-123">Filter Optionen für die Start-Paketerfassung auf dem virtuellen Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="a77a3-123">Filter options for start packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="a77a3-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a77a3-124">-InputObject</span></span>
<span data-ttu-id="a77a3-125">Das virtuelle Netzwerkgateway-Objekt, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a77a3-125">The virtual network gateway object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a77a3-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a77a3-126">-Name</span></span>
<span data-ttu-id="a77a3-127">Der Name des virtuellen Netzwerkgateways, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a77a3-127">The virtual network gateway name where packet capture is to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a77a3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a77a3-128">-ResourceGroupName</span></span>
<span data-ttu-id="a77a3-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a77a3-129">The resource group name.</span></span>

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

### <span data-ttu-id="a77a3-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a77a3-130">-ResourceId</span></span>
<span data-ttu-id="a77a3-131">Die Azure-Ressourcen-ID des VirtualNetworkGateway, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a77a3-131">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="a77a3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a77a3-132">-WhatIf</span></span>
<span data-ttu-id="a77a3-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a77a3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a77a3-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a77a3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a77a3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a77a3-135">CommonParameters</span></span>
<span data-ttu-id="a77a3-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a77a3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a77a3-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a77a3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a77a3-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a77a3-138">INPUTS</span></span>

### <span data-ttu-id="a77a3-139">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a77a3-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="a77a3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a77a3-140">System.String</span></span>

## <span data-ttu-id="a77a3-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a77a3-141">OUTPUTS</span></span>

### <span data-ttu-id="a77a3-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="a77a3-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="a77a3-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="a77a3-143">NOTES</span></span>

## <span data-ttu-id="a77a3-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a77a3-144">RELATED LINKS</span></span>
[<span data-ttu-id="a77a3-145">Stopp-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a77a3-145">Stop-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)