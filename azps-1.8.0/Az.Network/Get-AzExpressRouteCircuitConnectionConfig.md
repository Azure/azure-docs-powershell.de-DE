---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 70badaebf0b6b8a35fd96cc20a54aab1ff316bef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660807"
---
# <span data-ttu-id="e6c63-101">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e6c63-101">Get-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="e6c63-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e6c63-102">SYNOPSIS</span></span>
<span data-ttu-id="e6c63-103">Ruft eine Express Route Circuit Connection-Konfiguration ab, die mit Private Peering von ExpressRouteCircuit verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="e6c63-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

## <span data-ttu-id="e6c63-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6c63-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6c63-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6c63-105">DESCRIPTION</span></span>
<span data-ttu-id="e6c63-106">Das Cmdlet " **Get-AzExpressRouteCircuitConnectionConfig** " Ruft die Konfiguration einer Circuit-Verbindung ab, die mit Private Peering für einen Express Route-Schaltkreis verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="e6c63-106">The **Get-AzExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="e6c63-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6c63-107">EXAMPLES</span></span>

### <span data-ttu-id="e6c63-108">Beispiel 1: Anzeigen der Schaltungs Verbindungskonfiguration für einen Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="e6c63-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="e6c63-109">Beispiel 2: Abrufen der Schaltkreis Verbindungsressource, die mit einem Express Route-Schaltkreis verbunden ist, mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="e6c63-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="e6c63-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6c63-110">PARAMETERS</span></span>

### <span data-ttu-id="e6c63-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6c63-111">-DefaultProfile</span></span>
<span data-ttu-id="e6c63-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e6c63-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6c63-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e6c63-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="e6c63-114">Das Express Route-Schaltkreis Objekt, das die Leitungs Verbindungskonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="e6c63-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

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

### <span data-ttu-id="e6c63-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e6c63-115">-Name</span></span>
<span data-ttu-id="e6c63-116">Der Name der Verbindungskonfiguration, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e6c63-116">The name of the circuit connection configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c63-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6c63-117">CommonParameters</span></span>
<span data-ttu-id="e6c63-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6c63-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6c63-119">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6c63-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6c63-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e6c63-120">INPUTS</span></span>

### <span data-ttu-id="e6c63-121">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e6c63-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e6c63-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e6c63-122">OUTPUTS</span></span>

### <span data-ttu-id="e6c63-123">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="e6c63-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="e6c63-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="e6c63-124">NOTES</span></span>

## <span data-ttu-id="e6c63-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e6c63-125">RELATED LINKS</span></span>

[<span data-ttu-id="e6c63-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e6c63-126">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="e6c63-127">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e6c63-127">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="e6c63-128">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e6c63-128">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="e6c63-129">Satz-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e6c63-129">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="e6c63-130">Neu – AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e6c63-130">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)