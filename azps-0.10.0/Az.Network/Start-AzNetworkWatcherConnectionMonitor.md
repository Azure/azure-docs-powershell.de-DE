---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 61b23db6cfc634b318aa0070b5f784ad7067a234
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843536"
---
# <span data-ttu-id="67362-101">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="67362-101">Start-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="67362-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67362-102">SYNOPSIS</span></span>
<span data-ttu-id="67362-103">Starten eines Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="67362-103">Start a connection monitor</span></span>

## <span data-ttu-id="67362-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67362-104">SYNTAX</span></span>

### <span data-ttu-id="67362-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="67362-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="67362-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="67362-106">SetByName</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="67362-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="67362-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="67362-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="67362-108">SetByResourceId</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="67362-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="67362-109">SetByInputObject</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="67362-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67362-110">DESCRIPTION</span></span>
<span data-ttu-id="67362-111">Mit dem Start-AzNetworkWatcherConnectionMonitor-Cmdlet wird der angegebene Verbindungsmonitor gestartet.</span><span class="sxs-lookup"><span data-stu-id="67362-111">The Start-AzNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="67362-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67362-112">EXAMPLES</span></span>

### <span data-ttu-id="67362-113">---------------Beispiel 1: Starten eines Verbindungs Monitors---------------</span><span class="sxs-lookup"><span data-stu-id="67362-113">---------------  Example 1: Start a connection monitor ---------------</span></span>
```
PS C:\> Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="67362-114">In diesem Beispiel wird der vom Namen und Netzwerkmonitor angegebene Verbindungsmonitor gestartet.</span><span class="sxs-lookup"><span data-stu-id="67362-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="67362-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="67362-115">PARAMETERS</span></span>

### <span data-ttu-id="67362-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67362-116">-AsJob</span></span>
<span data-ttu-id="67362-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="67362-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67362-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="67362-118">-Confirm</span></span>
<span data-ttu-id="67362-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="67362-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67362-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67362-120">-DefaultProfile</span></span>
<span data-ttu-id="67362-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="67362-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67362-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="67362-122">-InputObject</span></span>
<span data-ttu-id="67362-123">Connection Monitor-Objekt.</span><span class="sxs-lookup"><span data-stu-id="67362-123">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67362-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="67362-124">-Location</span></span>
<span data-ttu-id="67362-125">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="67362-125">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67362-126">-Name</span><span class="sxs-lookup"><span data-stu-id="67362-126">-Name</span></span>
<span data-ttu-id="67362-127">Name des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="67362-127">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67362-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="67362-128">-NetworkWatcher</span></span>
<span data-ttu-id="67362-129">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="67362-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="67362-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="67362-130">-NetworkWatcherName</span></span>
<span data-ttu-id="67362-131">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="67362-131">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67362-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67362-132">-PassThru</span></span>
<span data-ttu-id="67362-133">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="67362-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="67362-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67362-134">-ResourceGroupName</span></span>
<span data-ttu-id="67362-135">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="67362-135">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67362-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="67362-136">-ResourceId</span></span>
<span data-ttu-id="67362-137">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="67362-137">Resource ID.</span></span>

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

### <span data-ttu-id="67362-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67362-138">-WhatIf</span></span>
<span data-ttu-id="67362-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67362-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67362-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="67362-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="67362-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67362-141">INPUTS</span></span>

### <span data-ttu-id="67362-142">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="67362-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="67362-143">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="67362-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="67362-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67362-144">OUTPUTS</span></span>

### <span data-ttu-id="67362-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="67362-145">System.Boolean</span></span>


## <span data-ttu-id="67362-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="67362-146">NOTES</span></span>
<span data-ttu-id="67362-147">Schlüsselwörter: Azure, azurerm, arm, Ressource, Konnektivität, Verwaltung, Manager, Netzwerk, Netzwerke, Netzwerkmonitor, Verbindungsmonitor</span><span class="sxs-lookup"><span data-stu-id="67362-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="67362-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67362-148">RELATED LINKS</span></span>
<span data-ttu-id="67362-149">[Neu – AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="67362-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="67362-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="67362-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="67362-151">[Neu – AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Neu – AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stopp-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="67362-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="67362-152">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Satz-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Stopp-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="67362-152">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)</span></span>