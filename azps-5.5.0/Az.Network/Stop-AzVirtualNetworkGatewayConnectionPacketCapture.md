---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 1303f8c8d2bb7b1de4401072ce1e968373aed28b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172410"
---
# <span data-ttu-id="d9180-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d9180-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="d9180-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9180-102">SYNOPSIS</span></span>
<span data-ttu-id="d9180-103">Beendet den Paketerfassungsvorgang für eine Verbindung des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="d9180-103">Stops Packet Capture Operation on a Virtual Network Gateway connection</span></span>

## <span data-ttu-id="d9180-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9180-104">SYNTAX</span></span>

### <span data-ttu-id="d9180-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d9180-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9180-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d9180-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9180-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d9180-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9180-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9180-108">DESCRIPTION</span></span>
<span data-ttu-id="d9180-109">Beendet den Paketerfassungsvorgang für eine Verbindung des virtuellen Netzwerkgateways und uploadt das Ergebnis auf den angegebenen SasUrl-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="d9180-109">Stops Packet Capture Operation on a Virtual Network Gateway connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="d9180-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d9180-110">EXAMPLES</span></span>

### <span data-ttu-id="d9180-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d9180-111">Example 1</span></span>
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
PS C:\> Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName $rgname -Name "testconn" -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

### <span data-ttu-id="d9180-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d9180-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $conn = Get-AzVirtualNetworkGatewayConnection -name "testconn" -ResourceGroupName $rgname
PS C:\> Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject $conn -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

## <span data-ttu-id="d9180-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9180-113">PARAMETERS</span></span>

### <span data-ttu-id="d9180-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9180-114">-AsJob</span></span>
<span data-ttu-id="d9180-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d9180-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9180-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9180-116">-Confirm</span></span>
<span data-ttu-id="d9180-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9180-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9180-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9180-118">-DefaultProfile</span></span>
<span data-ttu-id="d9180-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9180-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9180-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9180-120">-InputObject</span></span>
<span data-ttu-id="d9180-121">Das Objekt der virtuellen Netzwerkgateway-Verbindung, in dem die Paketaufzeichnung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9180-121">The virtual network gateway connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="d9180-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d9180-122">-Name</span></span>
<span data-ttu-id="d9180-123">Der Name der virtuellen Netzwerkgateway-Verbindung, in der die Paketaufzeichnung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9180-123">The virtual network gateway connection name where packet capture is to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9180-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9180-124">-ResourceGroupName</span></span>
<span data-ttu-id="d9180-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d9180-125">The resource group name.</span></span>

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

### <span data-ttu-id="d9180-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9180-126">-ResourceId</span></span>
<span data-ttu-id="d9180-127">Die Azure-Ressourcen-ID der VirtualNetworkGatewayConnection, in der die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9180-127">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="d9180-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="d9180-128">-SasUrl</span></span>
<span data-ttu-id="d9180-129">SAS-URL zum Beenden der Paketerfassung auf einem virtuellen Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="d9180-129">SAS Url for stop packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="d9180-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d9180-130">-WhatIf</span></span>
<span data-ttu-id="d9180-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9180-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9180-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9180-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9180-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9180-133">CommonParameters</span></span>
<span data-ttu-id="d9180-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9180-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9180-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9180-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9180-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d9180-136">INPUTS</span></span>

### <span data-ttu-id="d9180-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d9180-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="d9180-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d9180-138">System.String</span></span>

## <span data-ttu-id="d9180-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d9180-139">OUTPUTS</span></span>

### <span data-ttu-id="d9180-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="d9180-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="d9180-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d9180-141">NOTES</span></span>

## <span data-ttu-id="d9180-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d9180-142">RELATED LINKS</span></span>
[<span data-ttu-id="d9180-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d9180-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span></span>](./Start-AzVirtualnetworkGatewayConnectionPacketCapture.md)