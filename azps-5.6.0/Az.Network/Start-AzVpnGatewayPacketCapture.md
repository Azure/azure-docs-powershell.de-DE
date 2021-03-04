---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/Start-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: ec7307b6bd6d01b7b3f6e2656026eea78e0d3704
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918552"
---
# <span data-ttu-id="88e12-101">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="88e12-101">Start-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="88e12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88e12-102">SYNOPSIS</span></span>
<span data-ttu-id="88e12-103">Startet den Paketaufnahmevorgang auf einem Vpn-Gateway.</span><span class="sxs-lookup"><span data-stu-id="88e12-103">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="88e12-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88e12-104">SYNTAX</span></span>

### <span data-ttu-id="88e12-105">ByVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="88e12-105">ByVpnGatewayName (Default)</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88e12-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="88e12-106">ByVpnGatewayObject</span></span>
```
Start-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88e12-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="88e12-107">ByVpnGatewayResourceId</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88e12-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="88e12-108">DESCRIPTION</span></span>
<span data-ttu-id="88e12-109">Startet den Paketaufnahmevorgang auf einem Vpn-Gateway.</span><span class="sxs-lookup"><span data-stu-id="88e12-109">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="88e12-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="88e12-110">EXAMPLES</span></span>

### <span data-ttu-id="88e12-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="88e12-111">Example 1</span></span>
```powershell
Start-AzVpnGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG"
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

### <span data-ttu-id="88e12-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="88e12-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVpnGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a
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

## <span data-ttu-id="88e12-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="88e12-113">PARAMETERS</span></span>

### <span data-ttu-id="88e12-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88e12-114">-AsJob</span></span>
<span data-ttu-id="88e12-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="88e12-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88e12-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88e12-116">-DefaultProfile</span></span>
<span data-ttu-id="88e12-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88e12-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88e12-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="88e12-118">-FilterData</span></span>
<span data-ttu-id="88e12-119">Filteroptionen zum Starten der Paketaufnahme auf dem Vpn Gateway.</span><span class="sxs-lookup"><span data-stu-id="88e12-119">Filter options for start packet capture on Vpn Gateway.</span></span>

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

### <span data-ttu-id="88e12-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88e12-120">-InputObject</span></span>
<span data-ttu-id="88e12-121">Das Vpn Gateway-Objekt, in dem die Paketaufnahme gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="88e12-121">The Vpn Gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="88e12-122">-Name</span><span class="sxs-lookup"><span data-stu-id="88e12-122">-Name</span></span>
<span data-ttu-id="88e12-123">Der Name des Vpn-Gateways, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="88e12-123">The Vpn Gateway name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="88e12-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88e12-124">-ResourceGroupName</span></span>
<span data-ttu-id="88e12-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="88e12-125">The resource group name.</span></span>

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

### <span data-ttu-id="88e12-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88e12-126">-ResourceId</span></span>
<span data-ttu-id="88e12-127">Die Azure-Ressourcen-ID des VpnGateways, auf dem die Paketaufnahme gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="88e12-127">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="88e12-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="88e12-128">-Confirm</span></span>
<span data-ttu-id="88e12-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="88e12-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88e12-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88e12-130">-WhatIf</span></span>
<span data-ttu-id="88e12-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88e12-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88e12-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88e12-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88e12-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e12-133">CommonParameters</span></span>
<span data-ttu-id="88e12-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88e12-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88e12-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88e12-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e12-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="88e12-136">INPUTS</span></span>

### <span data-ttu-id="88e12-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="88e12-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="88e12-138">System.String</span><span class="sxs-lookup"><span data-stu-id="88e12-138">System.String</span></span>

## <span data-ttu-id="88e12-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="88e12-139">OUTPUTS</span></span>

### <span data-ttu-id="88e12-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="88e12-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="88e12-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="88e12-141">NOTES</span></span>

## <span data-ttu-id="88e12-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="88e12-142">RELATED LINKS</span></span>

[<span data-ttu-id="88e12-143">Stop-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="88e12-143">Stop-AzVpnGatewayPacketCapture</span></span>](./Stop-AzVpnGatewayPacketCapture.md)