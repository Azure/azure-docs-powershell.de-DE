---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 6ca7bc3e5d1af477c7d6750f674272ff64d54889
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178566"
---
# <span data-ttu-id="ef308-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ef308-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="ef308-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef308-102">SYNOPSIS</span></span>
<span data-ttu-id="ef308-103">Ruft einen Back-End-Adresspool für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="ef308-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="ef308-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef308-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef308-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef308-105">DESCRIPTION</span></span>
<span data-ttu-id="ef308-106">Das Cmdlet " **Get-AzApplicationGatewayBackendAddressPool** " ruft mindestens eine Back-End-Adresspool Konfiguration von einem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="ef308-106">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets one or more backend address pool configurations from an application gateway.</span></span>

## <span data-ttu-id="ef308-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef308-107">EXAMPLES</span></span>

### <span data-ttu-id="ef308-108">Beispiel 1: Abrufen eines angegebenen Back-End-Server Pools</span><span class="sxs-lookup"><span data-stu-id="ef308-108">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="ef308-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="ef308-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ef308-110">Der zweite Befehl ruft den Back-End-Adresspool ab, der $AppGw benannten Pool01 zugeordnet ist, und speichert ihn in der $BackendPool-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ef308-110">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="ef308-111">Beispiel 2: Abrufen einer Liste des Back-End-Server Pools</span><span class="sxs-lookup"><span data-stu-id="ef308-111">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="ef308-112">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="ef308-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ef308-113">Der zweite Befehl ruft eine Liste der dem $AppGw zugeordneten Back-End-Adresspools ab und speichert die Liste in der $BackendPools Variablen.</span><span class="sxs-lookup"><span data-stu-id="ef308-113">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="ef308-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef308-114">PARAMETERS</span></span>

### <span data-ttu-id="ef308-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef308-115">-ApplicationGateway</span></span>
<span data-ttu-id="ef308-116">Das Cmdlet " **Get-AzApplicationGatewayBackendAddressPool** " Ruft einen Back-End-Adresspool für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="ef308-116">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="ef308-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef308-117">-DefaultProfile</span></span>
<span data-ttu-id="ef308-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ef308-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef308-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ef308-119">-Name</span></span>
<span data-ttu-id="ef308-120">Gibt den Namen des Back-End-Adresspools an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ef308-120">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef308-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef308-121">CommonParameters</span></span>
<span data-ttu-id="ef308-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef308-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef308-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef308-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef308-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef308-124">INPUTS</span></span>

### <span data-ttu-id="ef308-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef308-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ef308-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef308-126">OUTPUTS</span></span>

### <span data-ttu-id="ef308-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ef308-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="ef308-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef308-128">NOTES</span></span>

## <span data-ttu-id="ef308-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef308-129">RELATED LINKS</span></span>

[<span data-ttu-id="ef308-130">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ef308-130">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ef308-131">Neu – AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ef308-131">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ef308-132">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ef308-132">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ef308-133">Satz-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ef308-133">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


