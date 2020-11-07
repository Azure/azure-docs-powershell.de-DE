---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 84b92468f4945cbe25404b81f4c6403254a23ad3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849563"
---
# <span data-ttu-id="d50ee-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d50ee-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="d50ee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d50ee-102">SYNOPSIS</span></span>
<span data-ttu-id="d50ee-103">Entfernt einen Netzwerkmonitor.</span><span class="sxs-lookup"><span data-stu-id="d50ee-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d50ee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d50ee-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d50ee-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d50ee-105">DESCRIPTION</span></span>
<span data-ttu-id="d50ee-106">Das Remove-AzureRmNetworkWatcher-Cmdlet entfernt eine Network Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="d50ee-106">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="d50ee-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d50ee-107">EXAMPLES</span></span>

### <span data-ttu-id="d50ee-108">--------------------------Beispiel 1: Erstellen und Löschen eines Netzwerkmonitors--------------------------</span><span class="sxs-lookup"><span data-stu-id="d50ee-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="d50ee-109">In diesem Beispiel wird ein Netzwerkmonitor in einer Ressourcengruppe erstellt und anschließend sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d50ee-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="d50ee-110">Beachten Sie, dass pro Abonnement nur ein Netzwerkmonitor pro Region erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d50ee-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="d50ee-111">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen des virtuellen Netzwerks zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="d50ee-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="d50ee-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d50ee-112">PARAMETERS</span></span>

### <span data-ttu-id="d50ee-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d50ee-113">-AsJob</span></span>
<span data-ttu-id="d50ee-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d50ee-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d50ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d50ee-115">-DefaultProfile</span></span>
<span data-ttu-id="d50ee-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d50ee-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d50ee-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d50ee-117">-Name</span></span>
<span data-ttu-id="d50ee-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="d50ee-118">The resource name.</span></span>

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

### <span data-ttu-id="d50ee-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d50ee-119">-PassThru</span></span>
<span data-ttu-id="d50ee-120">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="d50ee-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d50ee-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d50ee-121">-ResourceGroupName</span></span>
<span data-ttu-id="d50ee-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d50ee-122">The resource group name.</span></span>

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

### <span data-ttu-id="d50ee-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d50ee-123">-Confirm</span></span>
<span data-ttu-id="d50ee-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d50ee-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d50ee-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d50ee-125">-WhatIf</span></span>
<span data-ttu-id="d50ee-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d50ee-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d50ee-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d50ee-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d50ee-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d50ee-128">CommonParameters</span></span>
<span data-ttu-id="d50ee-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d50ee-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d50ee-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d50ee-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d50ee-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d50ee-131">INPUTS</span></span>

### <span data-ttu-id="d50ee-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d50ee-132">System.String</span></span>

## <span data-ttu-id="d50ee-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d50ee-133">OUTPUTS</span></span>

### <span data-ttu-id="d50ee-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="d50ee-134">System.Object</span></span>

## <span data-ttu-id="d50ee-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="d50ee-135">NOTES</span></span>
<span data-ttu-id="d50ee-136">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke, Netzwerkmonitor</span><span class="sxs-lookup"><span data-stu-id="d50ee-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="d50ee-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d50ee-137">RELATED LINKS</span></span>

[<span data-ttu-id="d50ee-138">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d50ee-138">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d50ee-139">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d50ee-139">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d50ee-140">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d50ee-140">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d50ee-141">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d50ee-141">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="d50ee-142">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d50ee-142">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d50ee-143">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d50ee-143">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d50ee-144">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d50ee-144">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d50ee-145">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d50ee-145">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="d50ee-146">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d50ee-146">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="d50ee-147">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d50ee-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d50ee-148">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d50ee-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="d50ee-149">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d50ee-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
