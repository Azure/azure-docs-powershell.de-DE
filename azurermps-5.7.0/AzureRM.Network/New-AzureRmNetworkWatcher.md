---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
ms.openlocfilehash: e1e0714c070c47d4be2cff0893a4428bdf0949c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664642"
---
# <span data-ttu-id="bca72-101">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bca72-101">New-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="bca72-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bca72-102">SYNOPSIS</span></span>
<span data-ttu-id="bca72-103">Erstellt eine neue Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="bca72-103">Creates a new Network Watcher resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bca72-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bca72-104">SYNTAX</span></span>

```
New-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bca72-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bca72-105">DESCRIPTION</span></span>
<span data-ttu-id="bca72-106">Das New-AzureRmNetworkWatcher-Cmdlet erstellt eine neue Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="bca72-106">The New-AzureRmNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="bca72-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bca72-107">EXAMPLES</span></span>

### <span data-ttu-id="bca72-108">Beispiel 1: Erstellen eines Netzwerkmonitors</span><span class="sxs-lookup"><span data-stu-id="bca72-108">Example 1: Create a Network Watcher</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="bca72-109">In diesem Beispiel wird ein neuer Netzwerkmonitor in einer neu erstellten Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="bca72-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="bca72-110">Beachten Sie, dass pro Abonnement nur ein Netzwerkmonitor pro Region erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="bca72-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="bca72-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="bca72-111">PARAMETERS</span></span>

### <span data-ttu-id="bca72-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bca72-112">-DefaultProfile</span></span>
<span data-ttu-id="bca72-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bca72-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bca72-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="bca72-114">-Location</span></span>
<span data-ttu-id="bca72-115">Lage.</span><span class="sxs-lookup"><span data-stu-id="bca72-115">Location.</span></span>

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

### <span data-ttu-id="bca72-116">-Name</span><span class="sxs-lookup"><span data-stu-id="bca72-116">-Name</span></span>
<span data-ttu-id="bca72-117">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="bca72-117">The network watcher name.</span></span>

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

### <span data-ttu-id="bca72-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bca72-118">-ResourceGroupName</span></span>
<span data-ttu-id="bca72-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bca72-119">The resource group name.</span></span>

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

### <span data-ttu-id="bca72-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="bca72-120">-Tag</span></span>
<span data-ttu-id="bca72-121">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="bca72-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bca72-122">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="bca72-122">For example:</span></span>

<span data-ttu-id="bca72-123">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="bca72-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bca72-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bca72-124">-Confirm</span></span>
<span data-ttu-id="bca72-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bca72-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bca72-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bca72-126">-WhatIf</span></span>
<span data-ttu-id="bca72-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bca72-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bca72-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bca72-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bca72-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bca72-129">CommonParameters</span></span>
<span data-ttu-id="bca72-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bca72-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bca72-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bca72-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bca72-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bca72-132">INPUTS</span></span>

### <span data-ttu-id="bca72-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bca72-133">System.String</span></span>
<span data-ttu-id="bca72-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bca72-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bca72-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bca72-135">OUTPUTS</span></span>

### <span data-ttu-id="bca72-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bca72-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="bca72-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="bca72-137">NOTES</span></span>
<span data-ttu-id="bca72-138">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke, Netzwerkmonitor</span><span class="sxs-lookup"><span data-stu-id="bca72-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="bca72-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bca72-139">RELATED LINKS</span></span>

[<span data-ttu-id="bca72-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bca72-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="bca72-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bca72-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="bca72-142">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bca72-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bca72-143">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="bca72-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="bca72-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bca72-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bca72-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bca72-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bca72-146">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bca72-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bca72-147">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="bca72-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="bca72-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="bca72-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="bca72-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="bca72-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="bca72-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="bca72-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="bca72-151">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="bca72-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
