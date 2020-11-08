---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 1b51b7d086af738e356d7a6b65c17bdb45cbb518
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173268"
---
# <span data-ttu-id="0b89c-101">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="0b89c-101">Add-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="0b89c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b89c-102">SYNOPSIS</span></span>
<span data-ttu-id="0b89c-103">Erstellt eine TapConfiguration-Ressource, die einem Network Interface zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0b89c-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="0b89c-104">Dieser Verweis bezieht sich auf eine vorhandene VirtualNetworkTap-Ressource.</span><span class="sxs-lookup"><span data-stu-id="0b89c-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="0b89c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b89c-105">SYNTAX</span></span>

### <span data-ttu-id="0b89c-106">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="0b89c-106">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b89c-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0b89c-107">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b89c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b89c-108">DESCRIPTION</span></span>
<span data-ttu-id="0b89c-109">Das Cmdlet **Add-AzNetworkInterfaceTapConfig** erstellt eine TapConfiguration-Ressource, die einem Network Interface zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0b89c-109">The **Add-AzNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="0b89c-110">Dieser Verweis bezieht sich auf eine vorhandene VirtualNetworkTap-Ressource.</span><span class="sxs-lookup"><span data-stu-id="0b89c-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="0b89c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b89c-111">EXAMPLES</span></span>

### <span data-ttu-id="0b89c-112">Beispiel 1: Hinzufügen von TapConfiguration zu einem bestimmten Network Interface</span><span class="sxs-lookup"><span data-stu-id="0b89c-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="0b89c-113">Fügen Sie TapConfiguration zu einem sourceNic hinzu.</span><span class="sxs-lookup"><span data-stu-id="0b89c-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="0b89c-114">Der Datenverkehr von sourceNic VM wird auf die Ziel-VM gespiegelt, die in vVirtualNetworkTap-Ressource bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="0b89c-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="0b89c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b89c-115">PARAMETERS</span></span>

### <span data-ttu-id="0b89c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b89c-116">-DefaultProfile</span></span>
<span data-ttu-id="0b89c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b89c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b89c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0b89c-118">-Name</span></span>
<span data-ttu-id="0b89c-119">Der Name der TAP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0b89c-119">Name of the tap configuration.</span></span>

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

### <span data-ttu-id="0b89c-120">-Network Interface</span><span class="sxs-lookup"><span data-stu-id="0b89c-120">-NetworkInterface</span></span>
<span data-ttu-id="0b89c-121">Der Verweis der Netzwerkschnittstellenressource.</span><span class="sxs-lookup"><span data-stu-id="0b89c-121">The reference of the network interface resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b89c-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0b89c-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="0b89c-123">Der Verweis der virtuellen Netzwerk-Tap-Ressource.</span><span class="sxs-lookup"><span data-stu-id="0b89c-123">The reference of the virtual network tap resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b89c-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="0b89c-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="0b89c-125">Der Verweis der virtuellen Netzwerk-Tap-Ressource.</span><span class="sxs-lookup"><span data-stu-id="0b89c-125">The reference of the virtual network tap resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b89c-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b89c-126">-Confirm</span></span>
<span data-ttu-id="0b89c-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b89c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b89c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b89c-128">-WhatIf</span></span>
<span data-ttu-id="0b89c-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b89c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b89c-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b89c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b89c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b89c-131">CommonParameters</span></span>
<span data-ttu-id="0b89c-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b89c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b89c-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b89c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b89c-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b89c-134">INPUTS</span></span>

### <span data-ttu-id="0b89c-135">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0b89c-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="0b89c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0b89c-136">System.String</span></span>

### <span data-ttu-id="0b89c-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0b89c-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="0b89c-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b89c-138">OUTPUTS</span></span>

### <span data-ttu-id="0b89c-139">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0b89c-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="0b89c-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b89c-140">NOTES</span></span>

## <span data-ttu-id="0b89c-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b89c-141">RELATED LINKS</span></span>

[<span data-ttu-id="0b89c-142">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="0b89c-142">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="0b89c-143">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="0b89c-143">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="0b89c-144">Satz-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="0b89c-144">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
