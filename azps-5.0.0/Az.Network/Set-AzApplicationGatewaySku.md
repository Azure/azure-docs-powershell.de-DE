---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
ms.openlocfilehash: bfaf9773582b201de8f6066a30a55c0fd5f5b7ac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176269"
---
# <span data-ttu-id="6860d-101">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="6860d-101">Set-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="6860d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6860d-102">SYNOPSIS</span></span>
<span data-ttu-id="6860d-103">Ändert die SKU eines Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="6860d-103">Modifies the SKU of an application gateway.</span></span>

## <span data-ttu-id="6860d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6860d-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 [-Capacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6860d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6860d-105">DESCRIPTION</span></span>
<span data-ttu-id="6860d-106">Das Cmdlet " **Satz-AzApplicationGatewaySku** " ändert die Lagerhaltungs Einheit (SKU) eines Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="6860d-106">The **Set-AzApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="6860d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6860d-107">EXAMPLES</span></span>

### <span data-ttu-id="6860d-108">Beispiel 1: Aktualisieren der SKU des Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="6860d-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="6860d-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="6860d-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6860d-110">Der zweite Befehl aktualisiert die SKU des Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="6860d-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="6860d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6860d-111">PARAMETERS</span></span>

### <span data-ttu-id="6860d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6860d-112">-ApplicationGateway</span></span>
<span data-ttu-id="6860d-113">Gibt das Application Gateway-Objekt an, mit dem dieses Cmdlet die SKU verknüpft.</span><span class="sxs-lookup"><span data-stu-id="6860d-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="6860d-114">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="6860d-114">-Capacity</span></span>
<span data-ttu-id="6860d-115">Gibt die Anzahl der Instanzen des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="6860d-115">Specifies the instance count of the application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6860d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6860d-116">-DefaultProfile</span></span>
<span data-ttu-id="6860d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6860d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6860d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6860d-118">-Name</span></span>
<span data-ttu-id="6860d-119">Gibt den Namen des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="6860d-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="6860d-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6860d-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6860d-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="6860d-121">Standard_Small</span></span>
- <span data-ttu-id="6860d-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="6860d-122">Standard_Medium</span></span>
- <span data-ttu-id="6860d-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="6860d-123">Standard_Large</span></span>
- <span data-ttu-id="6860d-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="6860d-124">WAF_Medium</span></span>
- <span data-ttu-id="6860d-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="6860d-125">WAF_Large</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6860d-126">-Tier</span><span class="sxs-lookup"><span data-stu-id="6860d-126">-Tier</span></span>
<span data-ttu-id="6860d-127">Gibt die Ebene des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="6860d-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="6860d-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6860d-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6860d-129">Standard</span><span class="sxs-lookup"><span data-stu-id="6860d-129">Standard</span></span>
- <span data-ttu-id="6860d-130">WAF</span><span class="sxs-lookup"><span data-stu-id="6860d-130">WAF</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, WAF, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6860d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6860d-131">CommonParameters</span></span>
<span data-ttu-id="6860d-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6860d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6860d-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6860d-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6860d-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6860d-134">INPUTS</span></span>

### <span data-ttu-id="6860d-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6860d-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6860d-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6860d-136">OUTPUTS</span></span>

### <span data-ttu-id="6860d-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6860d-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6860d-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="6860d-138">NOTES</span></span>

## <span data-ttu-id="6860d-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6860d-139">RELATED LINKS</span></span>

[<span data-ttu-id="6860d-140">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="6860d-140">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="6860d-141">Neu – AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="6860d-141">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)


