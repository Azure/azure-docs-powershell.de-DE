---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: d01fad830b9edcd8eced13a4f1e9317bb4930f9c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160553"
---
# <span data-ttu-id="2f872-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f872-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="2f872-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f872-102">SYNOPSIS</span></span>
<span data-ttu-id="2f872-103">Startet den Paketerfassungsvorgang für eine Virtuelle Netzwerkgatewayverbindung.</span><span class="sxs-lookup"><span data-stu-id="2f872-103">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="2f872-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f872-104">SYNTAX</span></span>

### <span data-ttu-id="2f872-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2f872-105">ByName (Default)</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f872-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2f872-106">ByInputObject</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f872-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2f872-107">ByResourceId</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f872-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f872-108">DESCRIPTION</span></span>
<span data-ttu-id="2f872-109">Startet den Paketerfassungsvorgang für eine Virtuelle Netzwerkgatewayverbindung.</span><span class="sxs-lookup"><span data-stu-id="2f872-109">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="2f872-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2f872-110">EXAMPLES</span></span>

### <span data-ttu-id="2f872-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2f872-111">Example 1</span></span>
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
### <span data-ttu-id="2f872-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2f872-112">Example 2</span></span>
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
### <span data-ttu-id="2f872-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2f872-113">Example 3</span></span>
<span data-ttu-id="2f872-114">Beispiel für die Paketerfassung zum Erfassen aller inneren und äußeren Pakete</span><span class="sxs-lookup"><span data-stu-id="2f872-114">Packet Capture example for capture all inner and outer packets</span></span>
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

## <span data-ttu-id="2f872-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f872-115">PARAMETERS</span></span>

### <span data-ttu-id="2f872-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f872-116">-AsJob</span></span>
<span data-ttu-id="2f872-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2f872-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f872-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f872-118">-Confirm</span></span>
<span data-ttu-id="2f872-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2f872-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f872-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f872-120">-DefaultProfile</span></span>
<span data-ttu-id="2f872-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f872-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f872-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="2f872-122">-FilterData</span></span>
<span data-ttu-id="2f872-123">Filteroptionen für das Starten der Paketerfassung auf einer virtuellen Netzwerkgatewayverbindung.</span><span class="sxs-lookup"><span data-stu-id="2f872-123">Filter options for start packet capture on virtual network gateway connection.</span></span>

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

### <span data-ttu-id="2f872-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f872-124">-InputObject</span></span>
<span data-ttu-id="2f872-125">Das Objekt der virtuellen Netzwerkgateway-Verbindung, in dem die Paketaufzeichnung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f872-125">The virtual network gateway connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="2f872-126">-Name</span><span class="sxs-lookup"><span data-stu-id="2f872-126">-Name</span></span>
<span data-ttu-id="2f872-127">Der Name der virtuellen Netzwerkgatewayverbindung, in dem die Paketaufzeichnung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f872-127">The virtual network gateway connection name where packet capture to be started.</span></span>

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

### <span data-ttu-id="2f872-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f872-128">-ResourceGroupName</span></span>
<span data-ttu-id="2f872-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2f872-129">The resource group name.</span></span>

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

### <span data-ttu-id="2f872-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f872-130">-ResourceId</span></span>
<span data-ttu-id="2f872-131">Die Azure-Ressourcen-ID der VirtualNetworkGatewayConnection, in der die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f872-131">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="2f872-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2f872-132">-WhatIf</span></span>
<span data-ttu-id="2f872-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f872-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f872-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f872-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f872-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f872-135">CommonParameters</span></span>
<span data-ttu-id="2f872-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f872-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f872-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f872-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f872-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2f872-138">INPUTS</span></span>

### <span data-ttu-id="2f872-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2f872-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="2f872-140">System.String</span><span class="sxs-lookup"><span data-stu-id="2f872-140">System.String</span></span>

## <span data-ttu-id="2f872-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2f872-141">OUTPUTS</span></span>

### <span data-ttu-id="2f872-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="2f872-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="2f872-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2f872-143">NOTES</span></span>

## <span data-ttu-id="2f872-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2f872-144">RELATED LINKS</span></span>
[<span data-ttu-id="2f872-145">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f872-145">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>](./Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md)