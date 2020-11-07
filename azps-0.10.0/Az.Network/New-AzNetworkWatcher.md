---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: cace33dd9831dcfcc01f2a57eefb5f28367966d9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841296"
---
# <span data-ttu-id="c2eb9-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c2eb9-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="c2eb9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="c2eb9-103">Erstellt eine neue Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="c2eb9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2eb9-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2eb9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2eb9-105">DESCRIPTION</span></span>
<span data-ttu-id="c2eb9-106">Das New-AzNetworkWatcher-Cmdlet erstellt eine neue Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="c2eb9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2eb9-107">EXAMPLES</span></span>

### <span data-ttu-id="c2eb9-108">Beispiel 1: Erstellen eines Netzwerkmonitors</span><span class="sxs-lookup"><span data-stu-id="c2eb9-108">Example 1: Create a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="c2eb9-109">In diesem Beispiel wird ein neuer Netzwerkmonitor in einer neu erstellten Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="c2eb9-110">Beachten Sie, dass pro Abonnement nur ein Netzwerkmonitor pro Region erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="c2eb9-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2eb9-111">PARAMETERS</span></span>

### <span data-ttu-id="c2eb9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2eb9-112">-DefaultProfile</span></span>
<span data-ttu-id="c2eb9-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2eb9-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="c2eb9-114">-Location</span></span>
<span data-ttu-id="c2eb9-115">Lage.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-115">Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2eb9-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c2eb9-116">-Name</span></span>
<span data-ttu-id="c2eb9-117">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-117">The network watcher name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2eb9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2eb9-118">-ResourceGroupName</span></span>
<span data-ttu-id="c2eb9-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2eb9-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="c2eb9-120">-Tag</span></span>
<span data-ttu-id="c2eb9-121">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="c2eb9-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c2eb9-122">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c2eb9-122">For example:</span></span>

<span data-ttu-id="c2eb9-123">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="c2eb9-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2eb9-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c2eb9-124">-Confirm</span></span>
<span data-ttu-id="c2eb9-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2eb9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2eb9-126">-WhatIf</span></span>
<span data-ttu-id="c2eb9-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2eb9-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2eb9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2eb9-129">CommonParameters</span></span>
<span data-ttu-id="c2eb9-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2eb9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2eb9-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2eb9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2eb9-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2eb9-132">INPUTS</span></span>

### <span data-ttu-id="c2eb9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c2eb9-133">System.String</span></span>
<span data-ttu-id="c2eb9-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c2eb9-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c2eb9-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2eb9-135">OUTPUTS</span></span>

### <span data-ttu-id="c2eb9-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c2eb9-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="c2eb9-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2eb9-137">NOTES</span></span>
<span data-ttu-id="c2eb9-138">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke, Netzwerkmonitor</span><span class="sxs-lookup"><span data-stu-id="c2eb9-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="c2eb9-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2eb9-139">RELATED LINKS</span></span>

[<span data-ttu-id="c2eb9-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c2eb9-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c2eb9-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c2eb9-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c2eb9-142">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c2eb9-142">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c2eb9-143">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c2eb9-143">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c2eb9-144">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c2eb9-144">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c2eb9-145">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c2eb9-145">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c2eb9-146">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c2eb9-146">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c2eb9-147">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c2eb9-147">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c2eb9-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c2eb9-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c2eb9-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c2eb9-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c2eb9-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c2eb9-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c2eb9-151">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c2eb9-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
