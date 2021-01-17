---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: 7997949db725d50dd656479852b10d12094b8da7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467368"
---
# <span data-ttu-id="86994-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="86994-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="86994-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86994-102">SYNOPSIS</span></span>
<span data-ttu-id="86994-103">Ruft einen Azure -ExpressRoute-Schaltkreis aus Azure ab.</span><span class="sxs-lookup"><span data-stu-id="86994-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="86994-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86994-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86994-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86994-105">DESCRIPTION</span></span>
<span data-ttu-id="86994-106">Das **Cmdlet "Get-AzExpressRouteCircuit"** wird verwendet, um ein ExpressRoute-Schaltkreisobjekt aus Ihrem Abonnement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="86994-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="86994-107">Das zurückgegebene Schaltkreisobjekt kann als Eingabe für andere Cmdlets verwendet werden, die mit ExpressRoute-Schaltkreisen arbeiten.</span><span class="sxs-lookup"><span data-stu-id="86994-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="86994-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="86994-108">EXAMPLES</span></span>

### <span data-ttu-id="86994-109">Beispiel 1: Ableiten des ExpressRoute-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="86994-109">Example 1: Get the ExpressRoute circuit</span></span>
```
Get-AzExpressRouteCircuit -ResourceGroupName testrg -Name test

Name                             : test
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :
```

<span data-ttu-id="86994-110">Einen bestimmten "ExpressRoute"-Schaltkreis mit Name "testrg" und "ResourceGroupName"test"</span><span class="sxs-lookup"><span data-stu-id="86994-110">Get a specific ExpressRoute circuit with Name "testrg" and ResourceGroupName "test"</span></span>

### <span data-ttu-id="86994-111">Beispiel 2: Auflisten der "ExpressRoute"-Schaltkreise mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="86994-111">Example 2: List the ExpressRoute circuits using filtering</span></span>
```
Get-AzExpressRouteCircuit -Name test*

Name                             : test1
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test1
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :

Name                             : test2
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test2
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :
```

<span data-ttu-id="86994-112">Erhalten Sie alle ExpressRoute-Schaltkreise, deren Name mit "test" beginnt.</span><span class="sxs-lookup"><span data-stu-id="86994-112">Get all ExpressRoute circuits whose name starts with "test".</span></span>

## <span data-ttu-id="86994-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86994-113">PARAMETERS</span></span>

### <span data-ttu-id="86994-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86994-114">-DefaultProfile</span></span>
<span data-ttu-id="86994-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="86994-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86994-116">-Name</span><span class="sxs-lookup"><span data-stu-id="86994-116">-Name</span></span>
<span data-ttu-id="86994-117">Der Name des ExpressRoute-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="86994-117">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="86994-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86994-118">-ResourceGroupName</span></span>
<span data-ttu-id="86994-119">Der Name der Ressourcengruppe, die den "ExpressRoute"-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="86994-119">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="86994-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86994-120">CommonParameters</span></span>
<span data-ttu-id="86994-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86994-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86994-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86994-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86994-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="86994-123">INPUTS</span></span>

### <span data-ttu-id="86994-124">System.String</span><span class="sxs-lookup"><span data-stu-id="86994-124">System.String</span></span>

## <span data-ttu-id="86994-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="86994-125">OUTPUTS</span></span>

### <span data-ttu-id="86994-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="86994-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="86994-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="86994-127">NOTES</span></span>

## <span data-ttu-id="86994-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="86994-128">RELATED LINKS</span></span>

[<span data-ttu-id="86994-129">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="86994-129">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="86994-130">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="86994-130">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="86994-131">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="86994-131">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="86994-132">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="86994-132">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
