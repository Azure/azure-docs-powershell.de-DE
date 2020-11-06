---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
ms.openlocfilehash: ee92fd78d3a69b38620b2af543e01db7569d3b70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477133"
---
# <span data-ttu-id="ec9e7-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ec9e7-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="ec9e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec9e7-102">SYNOPSIS</span></span>
<span data-ttu-id="ec9e7-103">Entfernt einen Netzwerkmonitor.</span><span class="sxs-lookup"><span data-stu-id="ec9e7-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec9e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec9e7-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec9e7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec9e7-105">DESCRIPTION</span></span>
<span data-ttu-id="ec9e7-106">Das Remove-AzureRmNetworkWatcher-Cmdlet entfernt eine Network Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="ec9e7-106">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="ec9e7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec9e7-107">EXAMPLES</span></span>

### <span data-ttu-id="ec9e7-108">--------------------------Beispiel 1: Erstellen und Löschen eines Netzwerkmonitors--------------------------</span><span class="sxs-lookup"><span data-stu-id="ec9e7-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="ec9e7-109">In diesem Beispiel wird ein Netzwerkmonitor in einer Ressourcengruppe erstellt und anschließend sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ec9e7-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="ec9e7-110">Beachten Sie, dass pro Abonnement nur ein Netzwerkmonitor pro Region erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ec9e7-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="ec9e7-111">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen des virtuellen Netzwerks zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="ec9e7-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="ec9e7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec9e7-112">PARAMETERS</span></span>

### <span data-ttu-id="ec9e7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ec9e7-113">-Name</span></span>
<span data-ttu-id="ec9e7-114">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="ec9e7-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec9e7-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec9e7-115">-PassThru</span></span>
<span data-ttu-id="ec9e7-116">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="ec9e7-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec9e7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec9e7-117">-ResourceGroupName</span></span>
<span data-ttu-id="ec9e7-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ec9e7-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec9e7-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ec9e7-119">-Confirm</span></span>
<span data-ttu-id="ec9e7-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec9e7-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec9e7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec9e7-121">-WhatIf</span></span>
<span data-ttu-id="ec9e7-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ec9e7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec9e7-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ec9e7-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec9e7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec9e7-124">-DefaultProfile</span></span>
<span data-ttu-id="ec9e7-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ec9e7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec9e7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec9e7-126">CommonParameters</span></span>
<span data-ttu-id="ec9e7-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec9e7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec9e7-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec9e7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec9e7-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec9e7-129">INPUTS</span></span>

### <span data-ttu-id="ec9e7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ec9e7-130">System.String</span></span>

## <span data-ttu-id="ec9e7-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec9e7-131">OUTPUTS</span></span>

### <span data-ttu-id="ec9e7-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="ec9e7-132">System.Object</span></span>

## <span data-ttu-id="ec9e7-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec9e7-133">NOTES</span></span>
<span data-ttu-id="ec9e7-134">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke, Netzwerkmonitor</span><span class="sxs-lookup"><span data-stu-id="ec9e7-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="ec9e7-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec9e7-135">RELATED LINKS</span></span>

[<span data-ttu-id="ec9e7-136">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ec9e7-136">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ec9e7-137">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ec9e7-137">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ec9e7-138">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ec9e7-138">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ec9e7-139">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ec9e7-139">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="ec9e7-140">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ec9e7-140">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ec9e7-141">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ec9e7-141">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ec9e7-142">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ec9e7-142">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ec9e7-143">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ec9e7-143">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="ec9e7-144">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ec9e7-144">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="ec9e7-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ec9e7-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ec9e7-146">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ec9e7-146">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="ec9e7-147">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ec9e7-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
