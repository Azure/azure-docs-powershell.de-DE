---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/Stop-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: d61b12a5a46abbba95919bb747966caf14d61538
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918491"
---
# <span data-ttu-id="e5341-101">Stop-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e5341-101">Stop-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="e5341-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5341-102">SYNOPSIS</span></span>
<span data-ttu-id="e5341-103">Beendet den Paketaufnahmevorgang in einem Vpn-Gateway.</span><span class="sxs-lookup"><span data-stu-id="e5341-103">Stops Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="e5341-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5341-104">SYNTAX</span></span>

### <span data-ttu-id="e5341-105">ByVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e5341-105">ByVpnGatewayName (Default)</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5341-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="e5341-106">ByVpnGatewayObject</span></span>
```
Stop-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5341-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="e5341-107">ByVpnGatewayResourceId</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5341-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5341-108">DESCRIPTION</span></span>
<span data-ttu-id="e5341-109">Beendet den Paketaufnahmevorgang auf einem Vpn-Gateway und hochgeladen das Ergebnis auf den angegebenen SasUrl des Speichercontainers.</span><span class="sxs-lookup"><span data-stu-id="e5341-109">Stops Packet Capture Operation on a Vpn Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="e5341-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e5341-110">EXAMPLES</span></span>

### <span data-ttu-id="e5341-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5341-111">Example 1</span></span>
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

### <span data-ttu-id="e5341-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e5341-112">Example 2</span></span>
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

## <span data-ttu-id="e5341-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e5341-113">PARAMETERS</span></span>

### <span data-ttu-id="e5341-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5341-114">-AsJob</span></span>
<span data-ttu-id="e5341-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e5341-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5341-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5341-116">-DefaultProfile</span></span>
<span data-ttu-id="e5341-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5341-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5341-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5341-118">-InputObject</span></span>
<span data-ttu-id="e5341-119">Das Vpn Gateway-Objekt, in dem die Paketaufnahme gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e5341-119">The Vpn Gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="e5341-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e5341-120">-Name</span></span>
<span data-ttu-id="e5341-121">Der Name des Vpn-Gateways, in dem die Paketaufnahme gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e5341-121">The Vpn Gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="e5341-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5341-122">-ResourceGroupName</span></span>
<span data-ttu-id="e5341-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e5341-123">The resource group name.</span></span>

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

### <span data-ttu-id="e5341-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5341-124">-ResourceId</span></span>
<span data-ttu-id="e5341-125">Die Azure-Ressourcen-ID des VpnGateways, auf dem die Paketaufnahme gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e5341-125">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="e5341-126">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="e5341-126">-SasUrl</span></span>
<span data-ttu-id="e5341-127">SAS-URL-Paketerfassung auf dem Vpn Gateway.</span><span class="sxs-lookup"><span data-stu-id="e5341-127">SAS URL packet capture on Vpn Gateway.</span></span>

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

### <span data-ttu-id="e5341-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e5341-128">-Confirm</span></span>
<span data-ttu-id="e5341-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e5341-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5341-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5341-130">-WhatIf</span></span>
<span data-ttu-id="e5341-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e5341-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5341-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e5341-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5341-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5341-133">CommonParameters</span></span>
<span data-ttu-id="e5341-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5341-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5341-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5341-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5341-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e5341-136">INPUTS</span></span>

### <span data-ttu-id="e5341-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e5341-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="e5341-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e5341-138">System.String</span></span>

## <span data-ttu-id="e5341-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e5341-139">OUTPUTS</span></span>

### <span data-ttu-id="e5341-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="e5341-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="e5341-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e5341-141">NOTES</span></span>

## <span data-ttu-id="e5341-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e5341-142">RELATED LINKS</span></span>

[<span data-ttu-id="e5341-143">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e5341-143">Start-AzVpnGatewayPacketCapture</span></span>](./Start-AzVpnGatewayPacketCapture.md)