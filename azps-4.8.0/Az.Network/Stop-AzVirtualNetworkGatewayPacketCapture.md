---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
ms.openlocfilehash: 46d097d2985b39e1d757e2d530e67775c1b8a28d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165093"
---
# <span data-ttu-id="402ab-101">Stop-AzVirtualNetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="402ab-101">Stop-AzVirtualNetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="402ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="402ab-102">SYNOPSIS</span></span>
<span data-ttu-id="402ab-103">Beendet den Paket Erfassungsvorgang auf einem virtuellen Netzwerk Gateway.</span><span class="sxs-lookup"><span data-stu-id="402ab-103">Stops Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="402ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="402ab-104">SYNTAX</span></span>

### <span data-ttu-id="402ab-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="402ab-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="402ab-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="402ab-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="402ab-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="402ab-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="402ab-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="402ab-108">DESCRIPTION</span></span>
<span data-ttu-id="402ab-109">Beendet den Paket Erfassungsvorgang auf einem virtuellen Netzwerk Gateway und lädt das Ergebnis auf der angegebenen SasUrl des Speichercontainers hoch.</span><span class="sxs-lookup"><span data-stu-id="402ab-109">Stops Packet Capture Operation on a Virtual Network Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="402ab-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="402ab-110">EXAMPLES</span></span>

### <span data-ttu-id="402ab-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="402ab-111">Example 1</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 New-AzStorageContainer -Name $containerName -Context $context
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName $rgname -Name "testgw" -SasUrl $sasurl

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

### <span data-ttu-id="402ab-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="402ab-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $gw = Get-AzVirtualNetworkGateway -ResourceGroupName $rgname -name "testGw"
PS C:\> Stop-AzVirtualNetworkGatewayPacketCapture -InputObject $gw -SasUrl $sasurl

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

## <span data-ttu-id="402ab-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="402ab-113">PARAMETERS</span></span>

### <span data-ttu-id="402ab-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="402ab-114">-AsJob</span></span>
<span data-ttu-id="402ab-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="402ab-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="402ab-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="402ab-116">-Confirm</span></span>
<span data-ttu-id="402ab-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="402ab-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="402ab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="402ab-118">-DefaultProfile</span></span>
<span data-ttu-id="402ab-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="402ab-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="402ab-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="402ab-120">-InputObject</span></span>
<span data-ttu-id="402ab-121">Das virtuelle Netzwerkgateway-Objekt, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="402ab-121">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="402ab-122">-Name</span><span class="sxs-lookup"><span data-stu-id="402ab-122">-Name</span></span>
<span data-ttu-id="402ab-123">Der Name des virtuellen Netzwerkgateways, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="402ab-123">The virtual network gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="402ab-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="402ab-124">-ResourceGroupName</span></span>
<span data-ttu-id="402ab-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="402ab-125">The resource group name.</span></span>

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

### <span data-ttu-id="402ab-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="402ab-126">-ResourceId</span></span>
<span data-ttu-id="402ab-127">Die Azure-Ressourcen-ID des VirtualNetworkGateway, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="402ab-127">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="402ab-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="402ab-128">-SasUrl</span></span>
<span data-ttu-id="402ab-129">SAS-URL-Paketerfassung auf dem virtuellen Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="402ab-129">SAS URL packet capture on virtual network gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="402ab-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="402ab-130">-WhatIf</span></span>
<span data-ttu-id="402ab-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="402ab-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="402ab-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="402ab-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="402ab-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="402ab-133">CommonParameters</span></span>
<span data-ttu-id="402ab-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="402ab-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="402ab-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="402ab-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="402ab-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="402ab-136">INPUTS</span></span>

### <span data-ttu-id="402ab-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="402ab-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="402ab-138">System. String</span><span class="sxs-lookup"><span data-stu-id="402ab-138">System.String</span></span>

## <span data-ttu-id="402ab-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="402ab-139">OUTPUTS</span></span>

### <span data-ttu-id="402ab-140">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="402ab-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="402ab-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="402ab-141">NOTES</span></span>

## <span data-ttu-id="402ab-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="402ab-142">RELATED LINKS</span></span>
[<span data-ttu-id="402ab-143">Anfang-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="402ab-143">Start-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)
