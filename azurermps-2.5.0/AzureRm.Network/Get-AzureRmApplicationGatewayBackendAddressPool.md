---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 4ce1f2d1c388b531ee960688ba8296ef1632ac25
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849248"
---
# <span data-ttu-id="4cbf9-101">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4cbf9-101">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="4cbf9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4cbf9-102">SYNOPSIS</span></span>
<span data-ttu-id="4cbf9-103">Ruft einen Back-End-Adresspool für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="4cbf9-103">Gets a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cbf9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cbf9-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cbf9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4cbf9-105">DESCRIPTION</span></span>

## <span data-ttu-id="4cbf9-106">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4cbf9-106">EXAMPLES</span></span>

### <span data-ttu-id="4cbf9-107">Beispiel 1: Abrufen eines angegebenen Back-End-Server Pools</span><span class="sxs-lookup"><span data-stu-id="4cbf9-107">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="4cbf9-108">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="4cbf9-108">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4cbf9-109">Der zweite Befehl ruft den Back-End-Adresspool ab, der $AppGw benannten Pool01 zugeordnet ist, und speichert ihn in der $BackendPool-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4cbf9-109">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="4cbf9-110">Beispiel 2: Abrufen einer Liste des Back-End-Server Pools</span><span class="sxs-lookup"><span data-stu-id="4cbf9-110">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="4cbf9-111">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="4cbf9-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4cbf9-112">Der zweite Befehl ruft eine Liste der dem $AppGw zugeordneten Back-End-Adresspools ab und speichert die Liste in der $BackendPools Variablen.</span><span class="sxs-lookup"><span data-stu-id="4cbf9-112">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="4cbf9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cbf9-113">PARAMETERS</span></span>

### <span data-ttu-id="4cbf9-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4cbf9-114">-ApplicationGateway</span></span>
<span data-ttu-id="4cbf9-115">Das Cmdlet " **Get-AzureRmApplicationGatewayBackendAddressPool** " Ruft einen Back-End-Adresspool für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="4cbf9-115">The **Get-AzureRmApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="4cbf9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cbf9-116">-DefaultProfile</span></span>
<span data-ttu-id="4cbf9-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4cbf9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cbf9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4cbf9-118">-Name</span></span>
<span data-ttu-id="4cbf9-119">Gibt den Namen des Back-End-Adresspools an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="4cbf9-119">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cbf9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cbf9-120">CommonParameters</span></span>
<span data-ttu-id="4cbf9-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cbf9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cbf9-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cbf9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cbf9-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4cbf9-123">INPUTS</span></span>

### <span data-ttu-id="4cbf9-124">System. String</span><span class="sxs-lookup"><span data-stu-id="4cbf9-124">System.String</span></span>

## <span data-ttu-id="4cbf9-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4cbf9-125">OUTPUTS</span></span>

### <span data-ttu-id="4cbf9-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4cbf9-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="4cbf9-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="4cbf9-127">NOTES</span></span>

## <span data-ttu-id="4cbf9-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4cbf9-128">RELATED LINKS</span></span>

[<span data-ttu-id="4cbf9-129">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4cbf9-129">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4cbf9-130">Neu – AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4cbf9-130">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4cbf9-131">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4cbf9-131">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4cbf9-132">Satz-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4cbf9-132">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


