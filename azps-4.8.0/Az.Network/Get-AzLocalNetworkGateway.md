---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 14c0ec31f10a6405fb2a3f412f004d53dbdeb9a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165280"
---
# <span data-ttu-id="5325b-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5325b-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="5325b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5325b-102">SYNOPSIS</span></span>
<span data-ttu-id="5325b-103">Ruft ein lokales Netzwerk Gateway ab</span><span class="sxs-lookup"><span data-stu-id="5325b-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="5325b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5325b-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5325b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5325b-105">DESCRIPTION</span></span>
<span data-ttu-id="5325b-106">Das lokale Netzwerk Gateway ist das Objekt, das Ihr VPN-Gerät lokal darstellt.</span><span class="sxs-lookup"><span data-stu-id="5325b-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="5325b-107">Das Cmdlet " **Get-AzLocalNetworkGateway** " gibt das Objekt zurück, das ihr auf-Prem-Gateway basierend auf Name und Ressourcengruppenname darstellt.</span><span class="sxs-lookup"><span data-stu-id="5325b-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="5325b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5325b-108">EXAMPLES</span></span>

### <span data-ttu-id="5325b-109">Beispiel 1: Abrufen eines lokalen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="5325b-109">Example 1: Get a Local Network Gateway</span></span>
```powershell
Get-AzLocalNetworkGateway -Name myLocalGW1 -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

<span data-ttu-id="5325b-110">Gibt das Objekt des lokalen Netzwerkgateways mit dem Namen "myLocalGW1" innerhalb der Ressourcengruppe "myRG" zurück.</span><span class="sxs-lookup"><span data-stu-id="5325b-110">Returns the object of the Local Network Gateway with the name "myLocalGW1" within the resource group "myRG"</span></span>

### <span data-ttu-id="5325b-111">Beispiel 2: Abrufen von lokalen Netzwerkgateways mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="5325b-111">Example 2: Get Local Network Gateways using filtering</span></span>
```powershell
Get-AzLocalNetworkGateway -Name myLocalGW* -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null

Name                     : myLocalGW2
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

<span data-ttu-id="5325b-112">Gibt das Objekt des lokalen Netzwerkgateways mit dem Namen ab "myLocalGW" innerhalb der Ressourcengruppe "myRG" zurück.</span><span class="sxs-lookup"><span data-stu-id="5325b-112">Returns the object of the Local Network Gateway with name starting with "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="5325b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5325b-113">PARAMETERS</span></span>

### <span data-ttu-id="5325b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5325b-114">-DefaultProfile</span></span>
<span data-ttu-id="5325b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5325b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5325b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5325b-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="5325b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5325b-117">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="5325b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5325b-118">CommonParameters</span></span>
<span data-ttu-id="5325b-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5325b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5325b-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5325b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5325b-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5325b-121">INPUTS</span></span>

### <span data-ttu-id="5325b-122">System. String</span><span class="sxs-lookup"><span data-stu-id="5325b-122">System.String</span></span>

## <span data-ttu-id="5325b-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5325b-123">OUTPUTS</span></span>

### <span data-ttu-id="5325b-124">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5325b-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="5325b-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="5325b-125">NOTES</span></span>

## <span data-ttu-id="5325b-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5325b-126">RELATED LINKS</span></span>

[<span data-ttu-id="5325b-127">Neu – AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5325b-127">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="5325b-128">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5325b-128">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="5325b-129">Satz-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5325b-129">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
