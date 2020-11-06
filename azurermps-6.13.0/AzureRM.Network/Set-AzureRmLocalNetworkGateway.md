---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: a37cb732aed95a2c31c970d83558a3eff8ab31c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476029"
---
# <span data-ttu-id="2bc93-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2bc93-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="2bc93-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2bc93-102">SYNOPSIS</span></span>
<span data-ttu-id="2bc93-103">Ändert ein lokales Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="2bc93-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bc93-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bc93-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2bc93-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2bc93-105">DESCRIPTION</span></span>
<span data-ttu-id="2bc93-106">Das Cmdlet " **Satz-AzureRmLocalNetworkGateway** " ändert ein lokales Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="2bc93-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="2bc93-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2bc93-107">EXAMPLES</span></span>

### <span data-ttu-id="2bc93-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2bc93-108">Example 1</span></span>
<span data-ttu-id="2bc93-109">Einrichten der Konfiguration für ein vorhandenes Gateway</span><span class="sxs-lookup"><span data-stu-id="2bc93-109">Set configuration for an existing gateway</span></span>


```
$lgw = Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway $lgw

Name                     : myLocalGW
ResourceGroupName        : TestRG1
Location                 : westus
Id                       : /subscriptions/81ab786c-56eb-4a4d-bb5f-f60329772466/resourceGroups/TestRG1/providers/Microso
                           ft.Network/localNetworkGateways/myLocalGW
Etag                     : W/"d2de6968-315e-411d-a4b8-a8c335abe61b"
ResourceGuid             : 393acf8b-dbb8-4b08-a9ea-c714570710e1
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : 1.2.3.4
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

## <span data-ttu-id="2bc93-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bc93-110">PARAMETERS</span></span>

### <span data-ttu-id="2bc93-111">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2bc93-111">-AddressPrefix</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bc93-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2bc93-112">-AsJob</span></span>
<span data-ttu-id="2bc93-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2bc93-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bc93-114">-ASN</span><span class="sxs-lookup"><span data-stu-id="2bc93-114">-Asn</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bc93-115">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="2bc93-115">-BgpPeeringAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bc93-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bc93-116">-DefaultProfile</span></span>
<span data-ttu-id="2bc93-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2bc93-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bc93-118">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2bc93-118">-LocalNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bc93-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="2bc93-119">-PeerWeight</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bc93-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bc93-120">CommonParameters</span></span>
<span data-ttu-id="2bc93-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bc93-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bc93-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bc93-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bc93-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2bc93-123">INPUTS</span></span>

### <span data-ttu-id="2bc93-124">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2bc93-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>
<span data-ttu-id="2bc93-125">Parameter: LocalNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2bc93-125">Parameters: LocalNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="2bc93-126">System. Collections. Generic. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2bc93-126">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="2bc93-127">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="2bc93-127">System.UInt32</span></span>

### <span data-ttu-id="2bc93-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2bc93-128">System.String</span></span>

### <span data-ttu-id="2bc93-129">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2bc93-129">System.Int32</span></span>

## <span data-ttu-id="2bc93-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2bc93-130">OUTPUTS</span></span>

### <span data-ttu-id="2bc93-131">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2bc93-131">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="2bc93-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="2bc93-132">NOTES</span></span>

## <span data-ttu-id="2bc93-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2bc93-133">RELATED LINKS</span></span>

[<span data-ttu-id="2bc93-134">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2bc93-134">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="2bc93-135">Neu – AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2bc93-135">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="2bc93-136">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2bc93-136">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


