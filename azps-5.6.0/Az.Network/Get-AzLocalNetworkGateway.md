---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 961edb46c71b60f0c3c43523d8d88486f1414d3d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945988"
---
# <span data-ttu-id="47f7f-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="47f7f-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="47f7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47f7f-102">SYNOPSIS</span></span>
<span data-ttu-id="47f7f-103">Ruft ein lokales Netzwerkgateway ab</span><span class="sxs-lookup"><span data-stu-id="47f7f-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="47f7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47f7f-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47f7f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47f7f-105">DESCRIPTION</span></span>
<span data-ttu-id="47f7f-106">Das Lokale Netzwerkgateway ist das Objekt, das Ihr VPN-Gerät lokal darstellt.</span><span class="sxs-lookup"><span data-stu-id="47f7f-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="47f7f-107">Das **Get-AzLocalNetworkGateway-Cmdlet** gibt das -Objekt zurück, das ihr lokales Gateway basierend auf Name und Ressourcengruppenname darstellt.</span><span class="sxs-lookup"><span data-stu-id="47f7f-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="47f7f-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="47f7f-108">EXAMPLES</span></span>

### <span data-ttu-id="47f7f-109">Beispiel 1: Ein lokales Netzwerkgateway erhalten</span><span class="sxs-lookup"><span data-stu-id="47f7f-109">Example 1: Get a Local Network Gateway</span></span>
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

<span data-ttu-id="47f7f-110">Gibt das Objekt des lokalen Netzwerkgateways mit dem Namen "myLocalGW1" innerhalb der Ressourcengruppe "myRG" zurück.</span><span class="sxs-lookup"><span data-stu-id="47f7f-110">Returns the object of the Local Network Gateway with the name "myLocalGW1" within the resource group "myRG"</span></span>

### <span data-ttu-id="47f7f-111">Beispiel 2: Erhalten lokaler Netzwerkgateways mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="47f7f-111">Example 2: Get Local Network Gateways using filtering</span></span>
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

<span data-ttu-id="47f7f-112">Gibt das -Objekt des Lokalen Netzwerkgateways zurück, und der Name beginnt mit "myLocalGW" innerhalb der Ressourcengruppe "myRG".</span><span class="sxs-lookup"><span data-stu-id="47f7f-112">Returns the object of the Local Network Gateway with name starting with "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="47f7f-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="47f7f-113">PARAMETERS</span></span>

### <span data-ttu-id="47f7f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47f7f-114">-DefaultProfile</span></span>
<span data-ttu-id="47f7f-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47f7f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47f7f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="47f7f-116">-Name</span></span>
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

### <span data-ttu-id="47f7f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47f7f-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="47f7f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47f7f-118">CommonParameters</span></span>
<span data-ttu-id="47f7f-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47f7f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47f7f-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47f7f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47f7f-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="47f7f-121">INPUTS</span></span>

### <span data-ttu-id="47f7f-122">System.String</span><span class="sxs-lookup"><span data-stu-id="47f7f-122">System.String</span></span>

## <span data-ttu-id="47f7f-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="47f7f-123">OUTPUTS</span></span>

### <span data-ttu-id="47f7f-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="47f7f-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="47f7f-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="47f7f-125">NOTES</span></span>

## <span data-ttu-id="47f7f-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="47f7f-126">RELATED LINKS</span></span>

[<span data-ttu-id="47f7f-127">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="47f7f-127">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="47f7f-128">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="47f7f-128">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="47f7f-129">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="47f7f-129">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
