---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: 487a3cd096f1d27852f4472d478977ac0cbe2ccc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664527"
---
# <span data-ttu-id="11eb7-101">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="11eb7-101">Set-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="11eb7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="11eb7-102">SYNOPSIS</span></span>
<span data-ttu-id="11eb7-103">Ändert die SKU eines Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="11eb7-103">Modifies the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11eb7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="11eb7-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 [-Capacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11eb7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11eb7-105">DESCRIPTION</span></span>
<span data-ttu-id="11eb7-106">Das Cmdlet " **Satz-AzureRmApplicationGatewaySku** " ändert die Lagerhaltungs Einheit (SKU) eines Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="11eb7-106">The **Set-AzureRmApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="11eb7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11eb7-107">EXAMPLES</span></span>

### <span data-ttu-id="11eb7-108">Beispiel 1: Aktualisieren der SKU des Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="11eb7-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="11eb7-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="11eb7-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="11eb7-110">Der zweite Befehl aktualisiert die SKU des Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="11eb7-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="11eb7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="11eb7-111">PARAMETERS</span></span>

### <span data-ttu-id="11eb7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11eb7-112">-ApplicationGateway</span></span>
<span data-ttu-id="11eb7-113">Gibt das Application Gateway-Objekt an, mit dem dieses Cmdlet die SKU verknüpft.</span><span class="sxs-lookup"><span data-stu-id="11eb7-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="11eb7-114">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="11eb7-114">-Capacity</span></span>
<span data-ttu-id="11eb7-115">Gibt die Anzahl der Instanzen des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="11eb7-115">Specifies the instance count of the application gateway.</span></span>

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

### <span data-ttu-id="11eb7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11eb7-116">-DefaultProfile</span></span>
<span data-ttu-id="11eb7-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="11eb7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11eb7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="11eb7-118">-Name</span></span>
<span data-ttu-id="11eb7-119">Gibt den Namen des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="11eb7-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="11eb7-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="11eb7-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="11eb7-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="11eb7-121">Standard_Small</span></span>
- <span data-ttu-id="11eb7-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="11eb7-122">Standard_Medium</span></span>
- <span data-ttu-id="11eb7-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="11eb7-123">Standard_Large</span></span>
- <span data-ttu-id="11eb7-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="11eb7-124">WAF_Medium</span></span>
- <span data-ttu-id="11eb7-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="11eb7-125">WAF_Large</span></span>

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

### <span data-ttu-id="11eb7-126">-Tier</span><span class="sxs-lookup"><span data-stu-id="11eb7-126">-Tier</span></span>
<span data-ttu-id="11eb7-127">Gibt die Ebene des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="11eb7-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="11eb7-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="11eb7-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="11eb7-129">Standard</span><span class="sxs-lookup"><span data-stu-id="11eb7-129">Standard</span></span>
- <span data-ttu-id="11eb7-130">WAF</span><span class="sxs-lookup"><span data-stu-id="11eb7-130">WAF</span></span>

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

### <span data-ttu-id="11eb7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11eb7-131">CommonParameters</span></span>
<span data-ttu-id="11eb7-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11eb7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11eb7-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11eb7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11eb7-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="11eb7-134">INPUTS</span></span>

### <span data-ttu-id="11eb7-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11eb7-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="11eb7-136">Parameter: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="11eb7-136">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="11eb7-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="11eb7-137">OUTPUTS</span></span>

### <span data-ttu-id="11eb7-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11eb7-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="11eb7-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="11eb7-139">NOTES</span></span>

## <span data-ttu-id="11eb7-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="11eb7-140">RELATED LINKS</span></span>

[<span data-ttu-id="11eb7-141">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="11eb7-141">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="11eb7-142">Neu – AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="11eb7-142">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)


