---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: eb90b668bf0466c44e3fde0ef0a8d6777074fb37
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004261"
---
# <span data-ttu-id="3c2f4-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="3c2f4-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="3c2f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3c2f4-102">SYNOPSIS</span></span>
<span data-ttu-id="3c2f4-103">Entfernt eine Express Route-quer Verbindungs Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3c2f4-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="3c2f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c2f4-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c2f4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c2f4-105">DESCRIPTION</span></span>
<span data-ttu-id="3c2f4-106">Das Cmdlet **Remove-AzExpressRouteCrossConnectionPeering** entfernt eine Express Route-Peering-Konfiguration für Querverbindungen.</span><span class="sxs-lookup"><span data-stu-id="3c2f4-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="3c2f4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3c2f4-107">EXAMPLES</span></span>

### <span data-ttu-id="3c2f4-108">Beispiel 1: Entfernen einer Peering-Konfiguration aus einer Express Route-Querverbindung</span><span class="sxs-lookup"><span data-stu-id="3c2f4-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="3c2f4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c2f4-109">PARAMETERS</span></span>

### <span data-ttu-id="3c2f4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c2f4-110">-DefaultProfile</span></span>
<span data-ttu-id="3c2f4-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3c2f4-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c2f4-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="3c2f4-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="3c2f4-113">Die Express Route-Querverbindung, die die zu entfernende Peering-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="3c2f4-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c2f4-114">-Force</span><span class="sxs-lookup"><span data-stu-id="3c2f4-114">-Force</span></span>
<span data-ttu-id="3c2f4-115">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="3c2f4-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c2f4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="3c2f4-116">-Name</span></span>
<span data-ttu-id="3c2f4-117">Der Name der zu entfernende Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3c2f4-117">The name of the peering configuration to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c2f4-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="3c2f4-118">-PeerAddressType</span></span>
<span data-ttu-id="3c2f4-119">Die Adressfamilie des Peerings</span><span class="sxs-lookup"><span data-stu-id="3c2f4-119">The Address family of the peering</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c2f4-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3c2f4-120">-Confirm</span></span>
<span data-ttu-id="3c2f4-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3c2f4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c2f4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c2f4-122">-WhatIf</span></span>
<span data-ttu-id="3c2f4-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c2f4-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c2f4-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3c2f4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c2f4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c2f4-125">CommonParameters</span></span>
<span data-ttu-id="3c2f4-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c2f4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c2f4-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c2f4-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c2f4-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3c2f4-128">INPUTS</span></span>

### <span data-ttu-id="3c2f4-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="3c2f4-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="3c2f4-130">Der Parameter "ExpressRouteCrossConnection" akzeptiert den Wert vom Typ "PSExpressRouteCrossConnection" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3c2f4-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="3c2f4-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3c2f4-131">OUTPUTS</span></span>

### <span data-ttu-id="3c2f4-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="3c2f4-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="3c2f4-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="3c2f4-133">NOTES</span></span>

## <span data-ttu-id="3c2f4-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3c2f4-134">RELATED LINKS</span></span>

[<span data-ttu-id="3c2f4-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="3c2f4-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="3c2f4-136">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="3c2f4-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](New-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="3c2f4-137">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="3c2f4-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="3c2f4-138">Satz-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="3c2f4-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
