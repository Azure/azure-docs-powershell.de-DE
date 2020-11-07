---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: a67dde4b1e8f3f97038304086b63d02d75ff8fec
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848688"
---
# <span data-ttu-id="a2e7d-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a2e7d-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="a2e7d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a2e7d-102">SYNOPSIS</span></span>
<span data-ttu-id="a2e7d-103">Beenden eines Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="a2e7d-103">Stop a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2e7d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2e7d-104">SYNTAX</span></span>

### <span data-ttu-id="a2e7d-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="a2e7d-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a2e7d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a2e7d-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a2e7d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a2e7d-107">SetByLocation</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a2e7d-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a2e7d-108">SetByResourceId</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a2e7d-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="a2e7d-109">SetByInputObject</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a2e7d-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2e7d-110">DESCRIPTION</span></span>
<span data-ttu-id="a2e7d-111">Das Stop-AzureRmNetworkWatcherConnectionMonitor-Cmdlet beendet den angegebenen Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="a2e7d-111">The Stop-AzureRmNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="a2e7d-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2e7d-112">EXAMPLES</span></span>

### <span data-ttu-id="a2e7d-113">---------------Beispiel 1: Beenden eines Verbindungs Monitors---------------</span><span class="sxs-lookup"><span data-stu-id="a2e7d-113">---------------  Example 1: Stop a connection monitor ---------------</span></span>
```
PS C:\> Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="a2e7d-114">In diesem Beispiel wird der vom Namen und Netzwerkmonitor angegebene Verbindungsmonitor beendet</span><span class="sxs-lookup"><span data-stu-id="a2e7d-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="a2e7d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2e7d-115">PARAMETERS</span></span>

### <span data-ttu-id="a2e7d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2e7d-116">-AsJob</span></span>
<span data-ttu-id="a2e7d-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a2e7d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2e7d-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a2e7d-118">-Confirm</span></span>
<span data-ttu-id="a2e7d-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2e7d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2e7d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2e7d-120">-DefaultProfile</span></span>
<span data-ttu-id="a2e7d-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a2e7d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2e7d-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a2e7d-122">-InputObject</span></span>
<span data-ttu-id="a2e7d-123">Connection Monitor-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a2e7d-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="a2e7d-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="a2e7d-124">-Location</span></span>
<span data-ttu-id="a2e7d-125">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="a2e7d-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a2e7d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a2e7d-126">-Name</span></span>
<span data-ttu-id="a2e7d-127">Name des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="a2e7d-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="a2e7d-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2e7d-128">-NetworkWatcher</span></span>
<span data-ttu-id="a2e7d-129">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="a2e7d-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="a2e7d-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a2e7d-130">-NetworkWatcherName</span></span>
<span data-ttu-id="a2e7d-131">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="a2e7d-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="a2e7d-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2e7d-132">-PassThru</span></span>
<span data-ttu-id="a2e7d-133">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="a2e7d-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a2e7d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2e7d-134">-ResourceGroupName</span></span>
<span data-ttu-id="a2e7d-135">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a2e7d-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a2e7d-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a2e7d-136">-ResourceId</span></span>
<span data-ttu-id="a2e7d-137">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a2e7d-137">Resource ID.</span></span>

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

### <span data-ttu-id="a2e7d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2e7d-138">-WhatIf</span></span>
<span data-ttu-id="a2e7d-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2e7d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2e7d-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2e7d-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="a2e7d-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a2e7d-141">INPUTS</span></span>

### <span data-ttu-id="a2e7d-142">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2e7d-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a2e7d-143">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="a2e7d-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="a2e7d-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a2e7d-144">OUTPUTS</span></span>

### <span data-ttu-id="a2e7d-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a2e7d-145">System.Boolean</span></span>


## <span data-ttu-id="a2e7d-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="a2e7d-146">NOTES</span></span>
<span data-ttu-id="a2e7d-147">Schlüsselwörter: Azure, azurerm, arm, Ressource, Konnektivität, Verwaltung, Manager, Netzwerk, Netzwerke, Netzwerkmonitor, Verbindungsmonitor</span><span class="sxs-lookup"><span data-stu-id="a2e7d-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="a2e7d-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a2e7d-148">RELATED LINKS</span></span>
<span data-ttu-id="a2e7d-149">[Neu – AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="a2e7d-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="a2e7d-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="a2e7d-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="a2e7d-151">[Neu – AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Neu – AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stopp-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="a2e7d-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="a2e7d-152">[Neu – AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Satz-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Anfang-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="a2e7d-152">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)
[Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md)
[Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>
