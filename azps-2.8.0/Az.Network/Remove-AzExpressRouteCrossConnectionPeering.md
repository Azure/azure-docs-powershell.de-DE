---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: d1d506d0be75650d5404d7efc0f96abbcbd2683e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410224"
---
# <span data-ttu-id="eb261-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="eb261-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="eb261-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb261-102">SYNOPSIS</span></span>
<span data-ttu-id="eb261-103">Entfernt eine ExpressRoute-Verbindungs-Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="eb261-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="eb261-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb261-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb261-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb261-105">DESCRIPTION</span></span>
<span data-ttu-id="eb261-106">Das **Cmdlet "Remove-AzExpressRouteCrossConnectionPeering"** entfernt eine ExpressRoute-Verbindungspeeringkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="eb261-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="eb261-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eb261-107">EXAMPLES</span></span>

### <span data-ttu-id="eb261-108">Beispiel 1: Entfernen einer Peeringkonfiguration aus einer ExpressRoute-Kreuzverbindung</span><span class="sxs-lookup"><span data-stu-id="eb261-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="eb261-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb261-109">PARAMETERS</span></span>

### <span data-ttu-id="eb261-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb261-110">-DefaultProfile</span></span>
<span data-ttu-id="eb261-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb261-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb261-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="eb261-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="eb261-113">Die ExpressRoute-Überleitungsverbindung, die die zu entfernende Peeringkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="eb261-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="eb261-114">-Force</span><span class="sxs-lookup"><span data-stu-id="eb261-114">-Force</span></span>
<span data-ttu-id="eb261-115">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="eb261-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="eb261-116">-Name</span><span class="sxs-lookup"><span data-stu-id="eb261-116">-Name</span></span>
<span data-ttu-id="eb261-117">Der Name der Peeringkonfiguration, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb261-117">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="eb261-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="eb261-118">-PeerAddressType</span></span>
<span data-ttu-id="eb261-119">Die Adressfamilie des Peerings</span><span class="sxs-lookup"><span data-stu-id="eb261-119">The Address family of the peering</span></span>

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

### <span data-ttu-id="eb261-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb261-120">-Confirm</span></span>
<span data-ttu-id="eb261-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eb261-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb261-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="eb261-122">-WhatIf</span></span>
<span data-ttu-id="eb261-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eb261-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb261-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eb261-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb261-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb261-125">CommonParameters</span></span>
<span data-ttu-id="eb261-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb261-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb261-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb261-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb261-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eb261-128">INPUTS</span></span>

### <span data-ttu-id="eb261-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="eb261-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="eb261-130">Der Parameter 'ExpressRouteCrossConnection' akzeptiert den Wert des Typs 'PSExpressRouteCrossConnection' aus der Pipeline</span><span class="sxs-lookup"><span data-stu-id="eb261-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="eb261-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eb261-131">OUTPUTS</span></span>

### <span data-ttu-id="eb261-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="eb261-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="eb261-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="eb261-133">NOTES</span></span>

## <span data-ttu-id="eb261-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="eb261-134">RELATED LINKS</span></span>

[<span data-ttu-id="eb261-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="eb261-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)



[<span data-ttu-id="eb261-136">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="eb261-136">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="eb261-137">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="eb261-137">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
