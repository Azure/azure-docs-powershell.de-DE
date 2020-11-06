---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 4d9442ba87ba46704aaa93b31f41f111519c980b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504366"
---
# <span data-ttu-id="374a0-101">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="374a0-101">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="374a0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="374a0-102">SYNOPSIS</span></span>
<span data-ttu-id="374a0-103">Ruft eine Express Route Circuit Connection-Konfiguration ab, die mit Private Peering von ExpressRouteCircuit verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="374a0-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="374a0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="374a0-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="374a0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="374a0-105">DESCRIPTION</span></span>
<span data-ttu-id="374a0-106">Das Cmdlet " **Get-AzureRmExpressRouteCircuitConnectionConfig** " Ruft die Konfiguration einer Circuit-Verbindung ab, die mit Private Peering für einen Express Route-Schaltkreis verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="374a0-106">The **Get-AzureRmExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="374a0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="374a0-107">EXAMPLES</span></span>

### <span data-ttu-id="374a0-108">Beispiel 1: Anzeigen der Schaltungs Verbindungskonfiguration für einen Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="374a0-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="374a0-109">Beispiel 2: Abrufen der Schaltkreis Verbindungsressource, die mit einem Express Route-Schaltkreis verbunden ist, mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="374a0-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="374a0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="374a0-110">PARAMETERS</span></span>

### <span data-ttu-id="374a0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="374a0-111">-DefaultProfile</span></span>
<span data-ttu-id="374a0-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="374a0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="374a0-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="374a0-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="374a0-114">Das Express Route-Schaltkreis Objekt, das die Leitungs Verbindungskonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="374a0-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="374a0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="374a0-115">-Name</span></span>
<span data-ttu-id="374a0-116">Der Name der Verbindungskonfiguration, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="374a0-116">The name of the circuit connection configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="374a0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="374a0-117">CommonParameters</span></span>
<span data-ttu-id="374a0-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="374a0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="374a0-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="374a0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="374a0-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="374a0-120">INPUTS</span></span>

### <span data-ttu-id="374a0-121">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="374a0-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="374a0-122">Parameter: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="374a0-122">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="374a0-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="374a0-123">OUTPUTS</span></span>

### <span data-ttu-id="374a0-124">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="374a0-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="374a0-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="374a0-125">NOTES</span></span>

## <span data-ttu-id="374a0-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="374a0-126">RELATED LINKS</span></span>

[<span data-ttu-id="374a0-127">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="374a0-127">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="374a0-128">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="374a0-128">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Add-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="374a0-129">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="374a0-129">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="374a0-130">Satz-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="374a0-130">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="374a0-131">Neu – AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="374a0-131">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)
