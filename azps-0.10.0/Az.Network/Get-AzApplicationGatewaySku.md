---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: e8ad9974096f633cd829c4d933f092fd869a4103
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841719"
---
# <span data-ttu-id="7f928-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7f928-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="7f928-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f928-102">SYNOPSIS</span></span>
<span data-ttu-id="7f928-103">Ruft die SKU eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="7f928-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="7f928-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f928-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f928-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f928-105">DESCRIPTION</span></span>
<span data-ttu-id="7f928-106">Das Cmdlet " **Get-AzApplicationGatewaySku** " Ruft die Lagerhaltungs Einheit (SKU) eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="7f928-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="7f928-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f928-107">EXAMPLES</span></span>

### <span data-ttu-id="7f928-108">Beispiel 1: Abrufen einer SKU für das Anwendungs-Gateway</span><span class="sxs-lookup"><span data-stu-id="7f928-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="7f928-109">Der erste Befehl ruft das Anwendungs Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $AppGW.</span><span class="sxs-lookup"><span data-stu-id="7f928-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="7f928-110">Der zweite Befehl ruft die SKU eines Anwendungs Gateways mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $SKU.</span><span class="sxs-lookup"><span data-stu-id="7f928-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="7f928-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f928-111">PARAMETERS</span></span>

### <span data-ttu-id="7f928-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f928-112">-ApplicationGateway</span></span>
<span data-ttu-id="7f928-113">Gibt das Application Gateway-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="7f928-113">Specifies the application gateway object.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f928-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f928-114">-DefaultProfile</span></span>
<span data-ttu-id="7f928-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7f928-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f928-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f928-116">CommonParameters</span></span>
<span data-ttu-id="7f928-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f928-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f928-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f928-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f928-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f928-119">INPUTS</span></span>

### <span data-ttu-id="7f928-120">System. String</span><span class="sxs-lookup"><span data-stu-id="7f928-120">System.String</span></span>

## <span data-ttu-id="7f928-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f928-121">OUTPUTS</span></span>

### <span data-ttu-id="7f928-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7f928-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="7f928-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f928-123">NOTES</span></span>

## <span data-ttu-id="7f928-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f928-124">RELATED LINKS</span></span>

[<span data-ttu-id="7f928-125">Neu – AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7f928-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="7f928-126">Satz-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7f928-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


