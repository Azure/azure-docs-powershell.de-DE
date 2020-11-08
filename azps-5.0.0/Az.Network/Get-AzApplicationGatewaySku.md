---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: c8bd4a0070aa0e5635fad7cb20a627a7d23f5922
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180188"
---
# <span data-ttu-id="c474e-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="c474e-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="c474e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c474e-102">SYNOPSIS</span></span>
<span data-ttu-id="c474e-103">Ruft die SKU eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="c474e-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="c474e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c474e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c474e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c474e-105">DESCRIPTION</span></span>
<span data-ttu-id="c474e-106">Das Cmdlet " **Get-AzApplicationGatewaySku** " Ruft die Lagerhaltungs Einheit (SKU) eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="c474e-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="c474e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c474e-107">EXAMPLES</span></span>

### <span data-ttu-id="c474e-108">Beispiel 1: Abrufen einer SKU für das Anwendungs-Gateway</span><span class="sxs-lookup"><span data-stu-id="c474e-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="c474e-109">Der erste Befehl ruft das Anwendungs Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $AppGW.</span><span class="sxs-lookup"><span data-stu-id="c474e-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="c474e-110">Der zweite Befehl ruft die SKU eines Anwendungs Gateways mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $SKU.</span><span class="sxs-lookup"><span data-stu-id="c474e-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="c474e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c474e-111">PARAMETERS</span></span>

### <span data-ttu-id="c474e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c474e-112">-ApplicationGateway</span></span>
<span data-ttu-id="c474e-113">Gibt das Application Gateway-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="c474e-113">Specifies the application gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c474e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c474e-114">-DefaultProfile</span></span>
<span data-ttu-id="c474e-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c474e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c474e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c474e-116">CommonParameters</span></span>
<span data-ttu-id="c474e-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c474e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c474e-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c474e-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c474e-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c474e-119">INPUTS</span></span>

### <span data-ttu-id="c474e-120">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c474e-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c474e-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c474e-121">OUTPUTS</span></span>

### <span data-ttu-id="c474e-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="c474e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="c474e-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="c474e-123">NOTES</span></span>

## <span data-ttu-id="c474e-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c474e-124">RELATED LINKS</span></span>

[<span data-ttu-id="c474e-125">Neu – AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="c474e-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="c474e-126">Satz-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="c474e-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


