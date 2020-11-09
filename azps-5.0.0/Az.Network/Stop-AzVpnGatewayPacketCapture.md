---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Stop-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: e5f753d822911abd79e339412741657dae36628f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303106"
---
# <span data-ttu-id="8141e-101">Stop-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8141e-101">Stop-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="8141e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8141e-102">SYNOPSIS</span></span>
<span data-ttu-id="8141e-103">Beendet den Paket Erfassungsvorgang auf einem VPN-Gateway.</span><span class="sxs-lookup"><span data-stu-id="8141e-103">Stops Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="8141e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8141e-104">SYNTAX</span></span>

### <span data-ttu-id="8141e-105">ByVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8141e-105">ByVpnGatewayName (Default)</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8141e-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="8141e-106">ByVpnGatewayObject</span></span>
```
Stop-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8141e-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="8141e-107">ByVpnGatewayResourceId</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8141e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8141e-108">DESCRIPTION</span></span>
<span data-ttu-id="8141e-109">Beendet den Paket Erfassungsvorgang auf einem VPN-Gateway und lädt das Ergebnis auf der angegebenen SasUrl des Speichercontainers hoch.</span><span class="sxs-lookup"><span data-stu-id="8141e-109">Stops Packet Capture Operation on a Vpn Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="8141e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8141e-110">EXAMPLES</span></span>

### <span data-ttu-id="8141e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8141e-111">Example 1</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 New-AzStorageContainer -Name $containerName -Context $context
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> Stop-AzVpnGatewayPacketCapture -ResourceGroupName $rgname -Name "testgw" -SasUrl $sasurl
Code              : Succeeded
EndTime           : 10/1/2019 12:59:37 AM
StartTime         : 10/1/2019 12:58:26 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : testgw
Etag              :
Id                :
```

### <span data-ttu-id="8141e-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8141e-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $gw = Get-AzVpnGateway -ResourceGroupName $rgname -name "testGw"
PS C:\> Stop-AzVpnGatewayPacketCapture -InputObject $gw -SasUrl $sasurl
Code              : Succeeded
EndTime           : 10/1/2019 12:59:37 AM
StartTime         : 10/1/2019 12:58:26 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : testgw
Etag              :
Id                :
```

## <span data-ttu-id="8141e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8141e-113">PARAMETERS</span></span>

### <span data-ttu-id="8141e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8141e-114">-AsJob</span></span>
<span data-ttu-id="8141e-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8141e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8141e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8141e-116">-DefaultProfile</span></span>
<span data-ttu-id="8141e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8141e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8141e-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8141e-118">-InputObject</span></span>
<span data-ttu-id="8141e-119">Das VPN-Gatewayobjekt, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8141e-119">The Vpn Gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="8141e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8141e-120">-Name</span></span>
<span data-ttu-id="8141e-121">Der Name des VPN-Gateways, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8141e-121">The Vpn Gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="8141e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8141e-122">-ResourceGroupName</span></span>
<span data-ttu-id="8141e-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8141e-123">The resource group name.</span></span>

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

### <span data-ttu-id="8141e-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8141e-124">-ResourceId</span></span>
<span data-ttu-id="8141e-125">Die Azure-Ressourcen-ID des VpnGateway, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8141e-125">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="8141e-126">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="8141e-126">-SasUrl</span></span>
<span data-ttu-id="8141e-127">SAS-URL-Paketerfassung auf dem VPN-Gateway</span><span class="sxs-lookup"><span data-stu-id="8141e-127">SAS URL packet capture on Vpn Gateway.</span></span>

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

### <span data-ttu-id="8141e-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8141e-128">-Confirm</span></span>
<span data-ttu-id="8141e-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8141e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8141e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8141e-130">-WhatIf</span></span>
<span data-ttu-id="8141e-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8141e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8141e-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8141e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8141e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8141e-133">CommonParameters</span></span>
<span data-ttu-id="8141e-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8141e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8141e-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8141e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8141e-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8141e-136">INPUTS</span></span>

### <span data-ttu-id="8141e-137">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8141e-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="8141e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8141e-138">System.String</span></span>

## <span data-ttu-id="8141e-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8141e-139">OUTPUTS</span></span>

### <span data-ttu-id="8141e-140">Microsoft. Azure. Commands. Network. Models. PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="8141e-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="8141e-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="8141e-141">NOTES</span></span>

## <span data-ttu-id="8141e-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8141e-142">RELATED LINKS</span></span>

[<span data-ttu-id="8141e-143">Anfang-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8141e-143">Start-AzVpnGatewayPacketCapture</span></span>](./Start-AzVpnGatewayPacketCapture.md)