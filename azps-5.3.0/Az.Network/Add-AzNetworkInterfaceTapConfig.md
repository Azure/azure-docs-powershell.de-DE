---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 1b51b7d086af738e356d7a6b65c17bdb45cbb518
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467451"
---
# <span data-ttu-id="2767c-101">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2767c-101">Add-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="2767c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2767c-102">SYNOPSIS</span></span>
<span data-ttu-id="2767c-103">Erstellt eine TapConfiguration-Ressource, die einem NetworkInterface zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2767c-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="2767c-104">Dadurch wird auf eine vorhandene VirtualNetworkTap-Ressource verwiesen.</span><span class="sxs-lookup"><span data-stu-id="2767c-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="2767c-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2767c-105">SYNTAX</span></span>

### <span data-ttu-id="2767c-106">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="2767c-106">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2767c-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2767c-107">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2767c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2767c-108">DESCRIPTION</span></span>
<span data-ttu-id="2767c-109">Das **Cmdlet "Add-AzNetworkInterfaceTapConfig"** erstellt eine TapConfiguration-Ressource, die einem NetworkInterface zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2767c-109">The **Add-AzNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="2767c-110">Dadurch wird auf eine vorhandene VirtualNetworkTap-Ressource verwiesen.</span><span class="sxs-lookup"><span data-stu-id="2767c-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="2767c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2767c-111">EXAMPLES</span></span>

### <span data-ttu-id="2767c-112">Beispiel 1: Hinzufügen von "TapConfiguration" zu einem bestimmten NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2767c-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="2767c-113">Fügen Sie "TapConfiguration" zu einer sourceNic hinzu.</span><span class="sxs-lookup"><span data-stu-id="2767c-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="2767c-114">Der Datenverkehr von sourceNic VM wird an die Ziel-VM gespiegelt, die in der vVirtualNetworkTap-Ressource bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="2767c-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="2767c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2767c-115">PARAMETERS</span></span>

### <span data-ttu-id="2767c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2767c-116">-DefaultProfile</span></span>
<span data-ttu-id="2767c-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2767c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2767c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2767c-118">-Name</span></span>
<span data-ttu-id="2767c-119">Name der Tippkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="2767c-119">Name of the tap configuration.</span></span>

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

### <span data-ttu-id="2767c-120">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2767c-120">-NetworkInterface</span></span>
<span data-ttu-id="2767c-121">Der Verweis auf die Netzwerkschnittstellenressource.</span><span class="sxs-lookup"><span data-stu-id="2767c-121">The reference of the network interface resource.</span></span>

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

### <span data-ttu-id="2767c-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2767c-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="2767c-123">Der Verweis auf die Anzapfressource des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="2767c-123">The reference of the virtual network tap resource.</span></span>

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

### <span data-ttu-id="2767c-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="2767c-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="2767c-125">Der Verweis auf die Anzapfressource des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="2767c-125">The reference of the virtual network tap resource.</span></span>

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

### <span data-ttu-id="2767c-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2767c-126">-Confirm</span></span>
<span data-ttu-id="2767c-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2767c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2767c-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2767c-128">-WhatIf</span></span>
<span data-ttu-id="2767c-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2767c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2767c-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2767c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2767c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2767c-131">CommonParameters</span></span>
<span data-ttu-id="2767c-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2767c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2767c-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2767c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2767c-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2767c-134">INPUTS</span></span>

### <span data-ttu-id="2767c-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2767c-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="2767c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2767c-136">System.String</span></span>

### <span data-ttu-id="2767c-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2767c-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="2767c-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2767c-138">OUTPUTS</span></span>

### <span data-ttu-id="2767c-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2767c-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="2767c-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2767c-140">NOTES</span></span>

## <span data-ttu-id="2767c-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2767c-141">RELATED LINKS</span></span>

[<span data-ttu-id="2767c-142">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2767c-142">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="2767c-143">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2767c-143">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="2767c-144">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2767c-144">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
