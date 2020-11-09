---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 4309550557480211560e108489b14850672ee1f8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301425"
---
# <span data-ttu-id="d7323-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="d7323-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="d7323-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7323-102">SYNOPSIS</span></span>
<span data-ttu-id="d7323-103">Entfernt eine Express Route-quer Verbindungs Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d7323-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="d7323-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7323-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7323-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7323-105">DESCRIPTION</span></span>
<span data-ttu-id="d7323-106">Das Cmdlet **Remove-AzExpressRouteCrossConnectionPeering** entfernt eine Express Route-Peering-Konfiguration für Querverbindungen.</span><span class="sxs-lookup"><span data-stu-id="d7323-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="d7323-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7323-107">EXAMPLES</span></span>

### <span data-ttu-id="d7323-108">Beispiel 1: Entfernen einer Peering-Konfiguration aus einer Express Route-Querverbindung</span><span class="sxs-lookup"><span data-stu-id="d7323-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="d7323-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7323-109">PARAMETERS</span></span>

### <span data-ttu-id="d7323-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7323-110">-DefaultProfile</span></span>
<span data-ttu-id="d7323-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d7323-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7323-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d7323-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="d7323-113">Die Express Route-Querverbindung, die die zu entfernende Peering-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="d7323-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="d7323-114">-Force</span><span class="sxs-lookup"><span data-stu-id="d7323-114">-Force</span></span>
<span data-ttu-id="d7323-115">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="d7323-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d7323-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d7323-116">-Name</span></span>
<span data-ttu-id="d7323-117">Der Name der zu entfernende Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d7323-117">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="d7323-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="d7323-118">-PeerAddressType</span></span>
<span data-ttu-id="d7323-119">Die Adressfamilie des Peerings</span><span class="sxs-lookup"><span data-stu-id="d7323-119">The Address family of the peering</span></span>

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

### <span data-ttu-id="d7323-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d7323-120">-Confirm</span></span>
<span data-ttu-id="d7323-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d7323-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7323-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7323-122">-WhatIf</span></span>
<span data-ttu-id="d7323-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d7323-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7323-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7323-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7323-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7323-125">CommonParameters</span></span>
<span data-ttu-id="d7323-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7323-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7323-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7323-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7323-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7323-128">INPUTS</span></span>

### <span data-ttu-id="d7323-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d7323-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="d7323-130">Der Parameter "ExpressRouteCrossConnection" akzeptiert den Wert vom Typ "PSExpressRouteCrossConnection" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d7323-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="d7323-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7323-131">OUTPUTS</span></span>

### <span data-ttu-id="d7323-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d7323-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="d7323-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7323-133">NOTES</span></span>

## <span data-ttu-id="d7323-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7323-134">RELATED LINKS</span></span>

[<span data-ttu-id="d7323-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="d7323-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="d7323-136">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="d7323-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](./Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="d7323-137">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d7323-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="d7323-138">Satz-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d7323-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
