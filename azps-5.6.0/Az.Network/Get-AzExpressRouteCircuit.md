---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: 8961948970843873f337fd1625aabfdf878ba15d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926568"
---
# <span data-ttu-id="eac32-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eac32-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="eac32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eac32-102">SYNOPSIS</span></span>
<span data-ttu-id="eac32-103">Ruft einen Azure ExpressRoute-Schaltkreis aus Azure ab.</span><span class="sxs-lookup"><span data-stu-id="eac32-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="eac32-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eac32-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eac32-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eac32-105">DESCRIPTION</span></span>
<span data-ttu-id="eac32-106">Das **Get-AzExpressRouteCircuit-Cmdlet** wird verwendet, um ein ExpressRoute-Schaltkreisobjekt aus Ihrem Abonnement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="eac32-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="eac32-107">Das zurückgegebene Schaltkreisobjekt kann als Eingabe für andere Cmdlets verwendet werden, die auf ExpressRoute-Schaltkreisen funktionieren.</span><span class="sxs-lookup"><span data-stu-id="eac32-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="eac32-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eac32-108">EXAMPLES</span></span>

### <span data-ttu-id="eac32-109">Beispiel 1: Verwenden des ExpressRoute-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="eac32-109">Example 1: Get the ExpressRoute circuit</span></span>
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

<span data-ttu-id="eac32-110">Einen bestimmten ExpressRoute-Schaltkreis mit Name "testrg" und ResourceGroupName "test"</span><span class="sxs-lookup"><span data-stu-id="eac32-110">Get a specific ExpressRoute circuit with Name "testrg" and ResourceGroupName "test"</span></span>

### <span data-ttu-id="eac32-111">Beispiel 2: Auflisten der ExpressRoute-Schaltkreise mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="eac32-111">Example 2: List the ExpressRoute circuits using filtering</span></span>
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

<span data-ttu-id="eac32-112">Hier erhalten Sie alle ExpressRoute-Schaltkreise, deren Name mit "test" beginnt.</span><span class="sxs-lookup"><span data-stu-id="eac32-112">Get all ExpressRoute circuits whose name starts with "test".</span></span>

## <span data-ttu-id="eac32-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="eac32-113">PARAMETERS</span></span>

### <span data-ttu-id="eac32-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eac32-114">-DefaultProfile</span></span>
<span data-ttu-id="eac32-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eac32-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eac32-116">-Name</span><span class="sxs-lookup"><span data-stu-id="eac32-116">-Name</span></span>
<span data-ttu-id="eac32-117">Der Name des ExpressRoute-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="eac32-117">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="eac32-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eac32-118">-ResourceGroupName</span></span>
<span data-ttu-id="eac32-119">Der Name der Ressourcengruppe, die den ExpressRoute-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="eac32-119">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="eac32-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eac32-120">CommonParameters</span></span>
<span data-ttu-id="eac32-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eac32-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eac32-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eac32-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eac32-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eac32-123">INPUTS</span></span>

### <span data-ttu-id="eac32-124">System.String</span><span class="sxs-lookup"><span data-stu-id="eac32-124">System.String</span></span>

## <span data-ttu-id="eac32-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eac32-125">OUTPUTS</span></span>

### <span data-ttu-id="eac32-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eac32-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="eac32-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="eac32-127">NOTES</span></span>

## <span data-ttu-id="eac32-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="eac32-128">RELATED LINKS</span></span>

[<span data-ttu-id="eac32-129">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eac32-129">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="eac32-130">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eac32-130">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="eac32-131">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eac32-131">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="eac32-132">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eac32-132">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
