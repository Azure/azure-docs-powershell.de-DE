---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 262dd4333b2490c5035a00de179b9b2092ccb71e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843651"
---
# <span data-ttu-id="4a15c-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4a15c-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="4a15c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4a15c-102">SYNOPSIS</span></span>
<span data-ttu-id="4a15c-103">Ändert einen Express Route-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="4a15c-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="4a15c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a15c-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a15c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a15c-105">DESCRIPTION</span></span>
<span data-ttu-id="4a15c-106">Das Cmdlet " **Satz-AzExpressRouteCircuit** " speichert den geänderten Express Route-Schaltkreis in Azure.</span><span class="sxs-lookup"><span data-stu-id="4a15c-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="4a15c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a15c-107">EXAMPLES</span></span>

### <span data-ttu-id="4a15c-108">Beispiel 1: Ändern des serviceKey verwenden eines Express Route-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="4a15c-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="4a15c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a15c-109">PARAMETERS</span></span>

### <span data-ttu-id="4a15c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a15c-110">-AsJob</span></span>
<span data-ttu-id="4a15c-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4a15c-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a15c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a15c-112">-DefaultProfile</span></span>
<span data-ttu-id="4a15c-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4a15c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a15c-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4a15c-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="4a15c-115">Gibt das **ExpressRouteCircuit** -Objekt an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4a15c-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a15c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a15c-116">CommonParameters</span></span>
<span data-ttu-id="4a15c-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a15c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a15c-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a15c-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a15c-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4a15c-119">INPUTS</span></span>

### <span data-ttu-id="4a15c-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4a15c-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="4a15c-121">Der Parameter "ExpressRouteCircuit" akzeptiert den Wert vom Typ "PSExpressRouteCircuit" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4a15c-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="4a15c-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4a15c-122">OUTPUTS</span></span>

### <span data-ttu-id="4a15c-123">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4a15c-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4a15c-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="4a15c-124">NOTES</span></span>

## <span data-ttu-id="4a15c-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4a15c-125">RELATED LINKS</span></span>

[<span data-ttu-id="4a15c-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4a15c-126">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="4a15c-127">Verschieben-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4a15c-127">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="4a15c-128">Neu – AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4a15c-128">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="4a15c-129">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4a15c-129">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
