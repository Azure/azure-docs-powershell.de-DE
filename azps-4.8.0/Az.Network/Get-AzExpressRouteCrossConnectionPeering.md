---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 15aed0e5a4cca1b67c85cbe651453d64cecc13ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165792"
---
# <span data-ttu-id="b7ab0-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="b7ab0-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="b7ab0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7ab0-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ab0-103">Ruft eine Express Route-quer Verbindungs Peering-Konfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="b7ab0-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="b7ab0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7ab0-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7ab0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7ab0-105">DESCRIPTION</span></span>
<span data-ttu-id="b7ab0-106">Das Cmdlet " **Get-AzExpressRouteCrossConnectionPeering** " Ruft die Konfiguration einer Peering-Beziehung für eine Express Route-Querverbindung ab.</span><span class="sxs-lookup"><span data-stu-id="b7ab0-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="b7ab0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7ab0-107">EXAMPLES</span></span>

### <span data-ttu-id="b7ab0-108">Beispiel 1: Anzeigen der Peering-Konfiguration für eine Express Route-Querverbindung</span><span class="sxs-lookup"><span data-stu-id="b7ab0-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="b7ab0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7ab0-109">PARAMETERS</span></span>

### <span data-ttu-id="b7ab0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ab0-110">-DefaultProfile</span></span>
<span data-ttu-id="b7ab0-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b7ab0-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7ab0-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="b7ab0-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="b7ab0-113">Das Express Route-Kreuz Verbindungsobjekt, das die Peering-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="b7ab0-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

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

### <span data-ttu-id="b7ab0-114">-Name</span><span class="sxs-lookup"><span data-stu-id="b7ab0-114">-Name</span></span>
<span data-ttu-id="b7ab0-115">Der Name der Peering-Konfiguration, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7ab0-115">The name of the peering configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7ab0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ab0-116">CommonParameters</span></span>
<span data-ttu-id="b7ab0-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7ab0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ab0-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7ab0-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ab0-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7ab0-119">INPUTS</span></span>

### <span data-ttu-id="b7ab0-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="b7ab0-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="b7ab0-121">Der Parameter "ExpressRouteCrossConnection" akzeptiert den Wert vom Typ "PSExpressRouteCrossConnection" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b7ab0-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="b7ab0-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7ab0-122">OUTPUTS</span></span>

### <span data-ttu-id="b7ab0-123">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="b7ab0-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="b7ab0-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7ab0-124">NOTES</span></span>

## <span data-ttu-id="b7ab0-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7ab0-125">RELATED LINKS</span></span>

[<span data-ttu-id="b7ab0-126">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="b7ab0-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="b7ab0-127">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="b7ab0-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="b7ab0-128">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="b7ab0-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="b7ab0-129">Satz-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="b7ab0-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
