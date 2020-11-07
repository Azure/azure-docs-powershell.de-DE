---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 542056ecfb17254802b8ae06ae3fda8a5995f444
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822904"
---
# <span data-ttu-id="91495-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="91495-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="91495-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91495-102">SYNOPSIS</span></span>
<span data-ttu-id="91495-103">Entfernt eine Express Route-quer Verbindungs Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="91495-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="91495-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91495-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91495-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91495-105">DESCRIPTION</span></span>
<span data-ttu-id="91495-106">Das Cmdlet **Remove-AzExpressRouteCrossConnectionPeering** entfernt eine Express Route-Peering-Konfiguration für Querverbindungen.</span><span class="sxs-lookup"><span data-stu-id="91495-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="91495-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91495-107">EXAMPLES</span></span>

### <span data-ttu-id="91495-108">Beispiel 1: Entfernen einer Peering-Konfiguration aus einer Express Route-Querverbindung</span><span class="sxs-lookup"><span data-stu-id="91495-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="91495-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="91495-109">PARAMETERS</span></span>

### <span data-ttu-id="91495-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91495-110">-DefaultProfile</span></span>
<span data-ttu-id="91495-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="91495-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91495-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="91495-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="91495-113">Die Express Route-Querverbindung, die die zu entfernende Peering-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="91495-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="91495-114">-Force</span><span class="sxs-lookup"><span data-stu-id="91495-114">-Force</span></span>
<span data-ttu-id="91495-115">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="91495-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="91495-116">-Name</span><span class="sxs-lookup"><span data-stu-id="91495-116">-Name</span></span>
<span data-ttu-id="91495-117">Der Name der zu entfernende Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="91495-117">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="91495-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="91495-118">-PeerAddressType</span></span>
<span data-ttu-id="91495-119">Die Adressfamilie des Peerings</span><span class="sxs-lookup"><span data-stu-id="91495-119">The Address family of the peering</span></span>

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

### <span data-ttu-id="91495-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="91495-120">-Confirm</span></span>
<span data-ttu-id="91495-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="91495-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91495-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91495-122">-WhatIf</span></span>
<span data-ttu-id="91495-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91495-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91495-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91495-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91495-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91495-125">CommonParameters</span></span>
<span data-ttu-id="91495-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91495-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91495-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91495-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91495-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91495-128">INPUTS</span></span>

### <span data-ttu-id="91495-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="91495-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="91495-130">Der Parameter "ExpressRouteCrossConnection" akzeptiert den Wert vom Typ "PSExpressRouteCrossConnection" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="91495-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="91495-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91495-131">OUTPUTS</span></span>

### <span data-ttu-id="91495-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="91495-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="91495-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="91495-133">NOTES</span></span>

## <span data-ttu-id="91495-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91495-134">RELATED LINKS</span></span>

[<span data-ttu-id="91495-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="91495-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="91495-136">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="91495-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](New-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="91495-137">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="91495-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="91495-138">Satz-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="91495-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
