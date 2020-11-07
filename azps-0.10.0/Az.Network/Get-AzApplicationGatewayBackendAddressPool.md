---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: b10863cf5e4af09ded0e98dbed76aff37dc48677
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841756"
---
# <span data-ttu-id="959a6-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="959a6-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="959a6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="959a6-102">SYNOPSIS</span></span>
<span data-ttu-id="959a6-103">Ruft einen Back-End-Adresspool für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="959a6-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="959a6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="959a6-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="959a6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="959a6-105">DESCRIPTION</span></span>

## <span data-ttu-id="959a6-106">Beispiele</span><span class="sxs-lookup"><span data-stu-id="959a6-106">EXAMPLES</span></span>

### <span data-ttu-id="959a6-107">Beispiel 1: Abrufen eines angegebenen Back-End-Server Pools</span><span class="sxs-lookup"><span data-stu-id="959a6-107">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="959a6-108">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="959a6-108">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="959a6-109">Der zweite Befehl ruft den Back-End-Adresspool ab, der $AppGw benannten Pool01 zugeordnet ist, und speichert ihn in der $BackendPool-Variablen.</span><span class="sxs-lookup"><span data-stu-id="959a6-109">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="959a6-110">Beispiel 2: Abrufen einer Liste des Back-End-Server Pools</span><span class="sxs-lookup"><span data-stu-id="959a6-110">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="959a6-111">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="959a6-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="959a6-112">Der zweite Befehl ruft eine Liste der dem $AppGw zugeordneten Back-End-Adresspools ab und speichert die Liste in der $BackendPools Variablen.</span><span class="sxs-lookup"><span data-stu-id="959a6-112">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="959a6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="959a6-113">PARAMETERS</span></span>

### <span data-ttu-id="959a6-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="959a6-114">-ApplicationGateway</span></span>
<span data-ttu-id="959a6-115">Das Cmdlet " **Get-AzApplicationGatewayBackendAddressPool** " Ruft einen Back-End-Adresspool für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="959a6-115">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="959a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="959a6-116">-DefaultProfile</span></span>
<span data-ttu-id="959a6-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="959a6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="959a6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="959a6-118">-Name</span></span>
<span data-ttu-id="959a6-119">Gibt den Namen des Back-End-Adresspools an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="959a6-119">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="959a6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="959a6-120">CommonParameters</span></span>
<span data-ttu-id="959a6-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="959a6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="959a6-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="959a6-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="959a6-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="959a6-123">INPUTS</span></span>

### <span data-ttu-id="959a6-124">System. String</span><span class="sxs-lookup"><span data-stu-id="959a6-124">System.String</span></span>

## <span data-ttu-id="959a6-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="959a6-125">OUTPUTS</span></span>

### <span data-ttu-id="959a6-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="959a6-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="959a6-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="959a6-127">NOTES</span></span>

## <span data-ttu-id="959a6-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="959a6-128">RELATED LINKS</span></span>

[<span data-ttu-id="959a6-129">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="959a6-129">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="959a6-130">Neu – AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="959a6-130">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="959a6-131">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="959a6-131">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="959a6-132">Satz-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="959a6-132">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


