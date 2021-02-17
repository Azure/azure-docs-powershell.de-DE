---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: f80543b245c59cee7261d062c741788489fb5cb7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172397"
---
# <span data-ttu-id="6245f-101">Stop-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6245f-101">Stop-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="6245f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6245f-102">SYNOPSIS</span></span>
<span data-ttu-id="6245f-103">Beendet den Paketerfassungsvorgang in einer Vpn-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="6245f-103">Stops Packet Capture Operation on a Vpn connection</span></span>

## <span data-ttu-id="6245f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6245f-104">SYNTAX</span></span>

### <span data-ttu-id="6245f-105">ByVpnConnectionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6245f-105">ByVpnConnectionName (Default)</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -LinkConnectionName <String> -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6245f-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="6245f-106">ByVpnConnectionObject</span></span>
```
Stop-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> -LinkConnectionName <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6245f-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="6245f-107">ByVpnConnectionResourceId</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceId <String> -LinkConnectionName <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6245f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6245f-108">DESCRIPTION</span></span>
<span data-ttu-id="6245f-109">Beendet den Paketerfassungsvorgang für eine Vpn-Verbindung und uploadt das Ergebnis auf den angegebenen SasUrl-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="6245f-109">Stops Packet Capture Operation on a Vpn connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="6245f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6245f-110">EXAMPLES</span></span>

### <span data-ttu-id="6245f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6245f-111">Example 1</span></span>
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
PS C:\> Stop-AzVpnConnectionPacketCapture -ResourceGroupName $rgname -Name "testconn" -ParentResourceName "VpnGw1" -LinkConnectionName "SiteLink1,SiteLink2" -SasUrl $sasurl
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
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

### <span data-ttu-id="6245f-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6245f-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $conn = Get-AzVpnConnection -name "testconn" -ResourceGroupName $rgname
PS C:\> Stop-AzVpnConnectionPacketCapture -InputObject $conn -SasUrl $sasurl -LinkConnectionName "SiteLink1,SiteLink2"
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
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

## <span data-ttu-id="6245f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6245f-113">PARAMETERS</span></span>

### <span data-ttu-id="6245f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6245f-114">-AsJob</span></span>
<span data-ttu-id="6245f-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6245f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6245f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6245f-116">-DefaultProfile</span></span>
<span data-ttu-id="6245f-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6245f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6245f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6245f-118">-InputObject</span></span>
<span data-ttu-id="6245f-119">Das Vpn-Verbindungsobjekt, in dem die Paketaufzeichnung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6245f-119">The Vpn connection object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6245f-120">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="6245f-120">-LinkConnectionName</span></span>
<span data-ttu-id="6245f-121">Die Namen von SiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="6245f-121">The names of the SiteLinkConnection.</span></span>

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

### <span data-ttu-id="6245f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6245f-122">-Name</span></span>
<span data-ttu-id="6245f-123">Der Name der VPN-Verbindung, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6245f-123">The Vpn connection name where packet capture is to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6245f-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="6245f-124">-ParentResourceName</span></span>
<span data-ttu-id="6245f-125">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="6245f-125">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6245f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6245f-126">-ResourceGroupName</span></span>
<span data-ttu-id="6245f-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6245f-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6245f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6245f-128">-ResourceId</span></span>
<span data-ttu-id="6245f-129">Die Azure-Ressourcen-ID des VpnConnection-Kontos, in dem die Paketerfassung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6245f-129">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6245f-130">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="6245f-130">-SasUrl</span></span>
<span data-ttu-id="6245f-131">SAS-URL zum Beenden der Paketerfassung in Vpn.</span><span class="sxs-lookup"><span data-stu-id="6245f-131">SAS Url for stop packet capture on Vpn.</span></span>

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

### <span data-ttu-id="6245f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6245f-132">-Confirm</span></span>
<span data-ttu-id="6245f-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6245f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6245f-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6245f-134">-WhatIf</span></span>
<span data-ttu-id="6245f-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6245f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6245f-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6245f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6245f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6245f-137">CommonParameters</span></span>
<span data-ttu-id="6245f-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6245f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6245f-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6245f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6245f-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6245f-140">INPUTS</span></span>

### <span data-ttu-id="6245f-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="6245f-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="6245f-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6245f-142">System.String</span></span>

## <span data-ttu-id="6245f-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6245f-143">OUTPUTS</span></span>

### <span data-ttu-id="6245f-144">Microsoft.Azure.Commands.Network.Models.PSVpnPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="6245f-144">Microsoft.Azure.Commands.Network.Models.PSVpnPacketCaptureResult</span></span>

## <span data-ttu-id="6245f-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6245f-145">NOTES</span></span>

## <span data-ttu-id="6245f-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6245f-146">RELATED LINKS</span></span>

[<span data-ttu-id="6245f-147">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6245f-147">Start-AzVpnConnectionPacketCapture</span></span>](./Start-AzVpnConnectionPacketCapture.md)