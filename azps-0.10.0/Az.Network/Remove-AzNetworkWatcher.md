---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: 276cd57a51b6b457f2f4d205932cdbfabd7613b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843799"
---
# <span data-ttu-id="4f802-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4f802-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="4f802-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4f802-102">SYNOPSIS</span></span>
<span data-ttu-id="4f802-103">Entfernt einen Netzwerkmonitor.</span><span class="sxs-lookup"><span data-stu-id="4f802-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="4f802-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f802-104">SYNTAX</span></span>

```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f802-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f802-105">DESCRIPTION</span></span>
<span data-ttu-id="4f802-106">Das Remove-AzNetworkWatcher-Cmdlet entfernt eine Network Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="4f802-106">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="4f802-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f802-107">EXAMPLES</span></span>

### <span data-ttu-id="4f802-108">--------------------------Beispiel 1: Erstellen und Löschen eines Netzwerkmonitors--------------------------</span><span class="sxs-lookup"><span data-stu-id="4f802-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="4f802-109">In diesem Beispiel wird ein Netzwerkmonitor in einer Ressourcengruppe erstellt und anschließend sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4f802-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="4f802-110">Beachten Sie, dass pro Abonnement nur ein Netzwerkmonitor pro Region erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="4f802-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="4f802-111">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen des virtuellen Netzwerks zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="4f802-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="4f802-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f802-112">PARAMETERS</span></span>

### <span data-ttu-id="4f802-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f802-113">-AsJob</span></span>
<span data-ttu-id="4f802-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4f802-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f802-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f802-115">-DefaultProfile</span></span>
<span data-ttu-id="4f802-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4f802-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f802-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4f802-117">-Name</span></span>
<span data-ttu-id="4f802-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="4f802-118">The resource name.</span></span>

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

### <span data-ttu-id="4f802-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f802-119">-PassThru</span></span>
<span data-ttu-id="4f802-120">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="4f802-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4f802-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f802-121">-ResourceGroupName</span></span>
<span data-ttu-id="4f802-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4f802-122">The resource group name.</span></span>

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

### <span data-ttu-id="4f802-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4f802-123">-Confirm</span></span>
<span data-ttu-id="4f802-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f802-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f802-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f802-125">-WhatIf</span></span>
<span data-ttu-id="4f802-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f802-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f802-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f802-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f802-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f802-128">CommonParameters</span></span>
<span data-ttu-id="4f802-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f802-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f802-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f802-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f802-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4f802-131">INPUTS</span></span>

### <span data-ttu-id="4f802-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4f802-132">System.String</span></span>

## <span data-ttu-id="4f802-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4f802-133">OUTPUTS</span></span>

### <span data-ttu-id="4f802-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="4f802-134">System.Object</span></span>

## <span data-ttu-id="4f802-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="4f802-135">NOTES</span></span>
<span data-ttu-id="4f802-136">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke, Netzwerkmonitor</span><span class="sxs-lookup"><span data-stu-id="4f802-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="4f802-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4f802-137">RELATED LINKS</span></span>

[<span data-ttu-id="4f802-138">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4f802-138">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="4f802-139">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4f802-139">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4f802-140">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4f802-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4f802-141">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4f802-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4f802-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4f802-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4f802-143">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4f802-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4f802-144">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4f802-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4f802-145">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4f802-145">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4f802-146">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4f802-146">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4f802-147">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4f802-147">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4f802-148">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4f802-148">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="4f802-149">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4f802-149">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
