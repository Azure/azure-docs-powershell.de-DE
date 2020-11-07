---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
ms.openlocfilehash: 39bb650333c59bd7d7185449025de7bdd6254fab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823728"
---
# <span data-ttu-id="54038-101">Stop-AzVirtualNetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="54038-101">Stop-AzVirtualNetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="54038-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="54038-102">SYNOPSIS</span></span>
<span data-ttu-id="54038-103">Beendet den Paket Erfassungsvorgang auf einem virtuellen Netzwerk Gateway.</span><span class="sxs-lookup"><span data-stu-id="54038-103">Stops Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="54038-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="54038-104">SYNTAX</span></span>

### <span data-ttu-id="54038-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="54038-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54038-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="54038-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54038-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="54038-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54038-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54038-108">DESCRIPTION</span></span>
<span data-ttu-id="54038-109">Beendet den Paket Erfassungsvorgang auf einem virtuellen Netzwerk Gateway und lädt das Ergebnis auf der angegebenen SasUrl des Speichercontainers hoch.</span><span class="sxs-lookup"><span data-stu-id="54038-109">Stops Packet Capture Operation on a Virtual Network Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="54038-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54038-110">EXAMPLES</span></span>

### <span data-ttu-id="54038-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="54038-111">Example 1</span></span>
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

### <span data-ttu-id="54038-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="54038-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
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

## <span data-ttu-id="54038-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="54038-113">PARAMETERS</span></span>

### <span data-ttu-id="54038-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54038-114">-AsJob</span></span>
<span data-ttu-id="54038-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="54038-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54038-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="54038-116">-Confirm</span></span>
<span data-ttu-id="54038-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="54038-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54038-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54038-118">-DefaultProfile</span></span>
<span data-ttu-id="54038-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="54038-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54038-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="54038-120">-InputObject</span></span>
<span data-ttu-id="54038-121">Das virtuelle Netzwerkgateway-Objekt, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="54038-121">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="54038-122">-Name</span><span class="sxs-lookup"><span data-stu-id="54038-122">-Name</span></span>
<span data-ttu-id="54038-123">Der Name des virtuellen Netzwerkgateways, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="54038-123">The virtual network gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="54038-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54038-124">-ResourceGroupName</span></span>
<span data-ttu-id="54038-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="54038-125">The resource group name.</span></span>

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

### <span data-ttu-id="54038-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="54038-126">-ResourceId</span></span>
<span data-ttu-id="54038-127">Die Azure-Ressourcen-ID des VirtualNetworkGateway, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="54038-127">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="54038-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="54038-128">-SasUrl</span></span>
<span data-ttu-id="54038-129">SAS-URL-Paketerfassung auf dem virtuellen Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="54038-129">SAS URL packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="54038-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54038-130">-WhatIf</span></span>
<span data-ttu-id="54038-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54038-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54038-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54038-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54038-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54038-133">CommonParameters</span></span>
<span data-ttu-id="54038-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54038-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54038-135">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54038-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54038-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="54038-136">INPUTS</span></span>

### <span data-ttu-id="54038-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="54038-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="54038-138">System. String</span><span class="sxs-lookup"><span data-stu-id="54038-138">System.String</span></span>

## <span data-ttu-id="54038-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="54038-139">OUTPUTS</span></span>

### <span data-ttu-id="54038-140">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="54038-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="54038-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="54038-141">NOTES</span></span>

## <span data-ttu-id="54038-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="54038-142">RELATED LINKS</span></span>
[<span data-ttu-id="54038-143">Anfang-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="54038-143">Start-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)