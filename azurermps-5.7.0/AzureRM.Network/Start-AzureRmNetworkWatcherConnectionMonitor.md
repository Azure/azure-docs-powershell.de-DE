---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: cf67e27a8f502a753cded74f0cb5bf48ceb2d4ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662572"
---
# <span data-ttu-id="3ce2e-101">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3ce2e-101">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="3ce2e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3ce2e-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce2e-103">Starten eines Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="3ce2e-103">Start a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ce2e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ce2e-104">SYNTAX</span></span>

### <span data-ttu-id="3ce2e-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3ce2e-105">SetByName (Default)</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ce2e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3ce2e-106">SetByResource</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ce2e-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3ce2e-107">SetByLocation</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ce2e-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3ce2e-108">SetByResourceId</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ce2e-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="3ce2e-109">SetByInputObject</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ce2e-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3ce2e-110">DESCRIPTION</span></span>
<span data-ttu-id="3ce2e-111">Mit dem Start-AzureRmNetworkWatcherConnectionMonitor-Cmdlet wird der angegebene Verbindungsmonitor gestartet.</span><span class="sxs-lookup"><span data-stu-id="3ce2e-111">The Start-AzureRmNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="3ce2e-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3ce2e-112">EXAMPLES</span></span>

### <span data-ttu-id="3ce2e-113">Beispiel 1: Starten eines Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="3ce2e-113">Example 1: Start a connection monitor</span></span>
```
PS C:\> Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="3ce2e-114">In diesem Beispiel wird der vom Namen und Netzwerkmonitor angegebene Verbindungsmonitor gestartet.</span><span class="sxs-lookup"><span data-stu-id="3ce2e-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="3ce2e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ce2e-115">PARAMETERS</span></span>

### <span data-ttu-id="3ce2e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ce2e-116">-AsJob</span></span>
<span data-ttu-id="3ce2e-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3ce2e-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce2e-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3ce2e-118">-Confirm</span></span>
<span data-ttu-id="3ce2e-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3ce2e-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce2e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ce2e-120">-DefaultProfile</span></span>
<span data-ttu-id="3ce2e-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3ce2e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce2e-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3ce2e-122">-InputObject</span></span>
<span data-ttu-id="3ce2e-123">Connection Monitor-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3ce2e-123">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce2e-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="3ce2e-124">-Location</span></span>
<span data-ttu-id="3ce2e-125">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="3ce2e-125">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce2e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="3ce2e-126">-Name</span></span>
<span data-ttu-id="3ce2e-127">Name des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="3ce2e-127">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce2e-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3ce2e-128">-NetworkWatcher</span></span>
<span data-ttu-id="3ce2e-129">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="3ce2e-129">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce2e-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3ce2e-130">-NetworkWatcherName</span></span>
<span data-ttu-id="3ce2e-131">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="3ce2e-131">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce2e-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ce2e-132">-PassThru</span></span>
<span data-ttu-id="3ce2e-133">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="3ce2e-133">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce2e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ce2e-134">-ResourceGroupName</span></span>
<span data-ttu-id="3ce2e-135">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="3ce2e-135">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce2e-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3ce2e-136">-ResourceId</span></span>
<span data-ttu-id="3ce2e-137">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="3ce2e-137">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce2e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ce2e-138">-WhatIf</span></span>
<span data-ttu-id="3ce2e-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3ce2e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ce2e-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3ce2e-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce2e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce2e-141">CommonParameters</span></span>
<span data-ttu-id="3ce2e-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ce2e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3ce2e-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ce2e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce2e-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3ce2e-144">INPUTS</span></span>

### <span data-ttu-id="3ce2e-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3ce2e-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="3ce2e-146">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="3ce2e-146">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="3ce2e-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3ce2e-147">OUTPUTS</span></span>

### <span data-ttu-id="3ce2e-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3ce2e-148">System.Boolean</span></span>

## <span data-ttu-id="3ce2e-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="3ce2e-149">NOTES</span></span>
<span data-ttu-id="3ce2e-150">Schlüsselwörter: Azure, azurerm, arm, Ressource, Konnektivität, Verwaltung, Manager, Netzwerk, Netzwerke, Netzwerkmonitor, Verbindungsmonitor</span><span class="sxs-lookup"><span data-stu-id="3ce2e-150">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="3ce2e-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3ce2e-151">RELATED LINKS</span></span>

[<span data-ttu-id="3ce2e-152">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3ce2e-152">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="3ce2e-153">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3ce2e-153">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="3ce2e-154">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3ce2e-154">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="3ce2e-155">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3ce2e-155">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="3ce2e-156">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3ce2e-156">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="3ce2e-157">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3ce2e-157">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="3ce2e-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3ce2e-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="3ce2e-159">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3ce2e-159">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="3ce2e-160">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3ce2e-160">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="3ce2e-161">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3ce2e-161">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="3ce2e-162">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3ce2e-162">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="3ce2e-163">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3ce2e-163">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="3ce2e-164">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3ce2e-164">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="3ce2e-165">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="3ce2e-165">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="3ce2e-166">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3ce2e-166">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="3ce2e-167">Satz-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3ce2e-167">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="3ce2e-168">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3ce2e-168">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="3ce2e-169">Neu – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3ce2e-169">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
