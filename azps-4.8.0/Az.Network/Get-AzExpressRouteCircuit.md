---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: 7997949db725d50dd656479852b10d12094b8da7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165809"
---
# <span data-ttu-id="7f794-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7f794-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="7f794-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f794-102">SYNOPSIS</span></span>
<span data-ttu-id="7f794-103">Ruft eine Azure Express Route-Schaltkreis aus Azure ab.</span><span class="sxs-lookup"><span data-stu-id="7f794-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="7f794-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f794-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f794-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f794-105">DESCRIPTION</span></span>
<span data-ttu-id="7f794-106">Das Cmdlet " **Get-AzExpressRouteCircuit** " wird verwendet, um ein Express Route-Schaltkreis Objekt aus Ihrem Abonnement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7f794-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="7f794-107">Das zurückgegebene Circuit-Objekt kann als Eingabe für andere Cmdlets verwendet werden, die auf Express Route-Schaltkreisen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7f794-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="7f794-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f794-108">EXAMPLES</span></span>

### <span data-ttu-id="7f794-109">Beispiel 1: Abrufen des Express Route-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="7f794-109">Example 1: Get the ExpressRoute circuit</span></span>
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

<span data-ttu-id="7f794-110">Abrufen eines bestimmten Express Route-Schaltkreises mit dem Namen "testrg" und ResourceGroupName "Test"</span><span class="sxs-lookup"><span data-stu-id="7f794-110">Get a specific ExpressRoute circuit with Name "testrg" and ResourceGroupName "test"</span></span>

### <span data-ttu-id="7f794-111">Beispiel 2: Auflisten der Express Route-Schaltkreise mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="7f794-111">Example 2: List the ExpressRoute circuits using filtering</span></span>
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

<span data-ttu-id="7f794-112">Rufen Sie alle Express Route-Schaltkreise ab, deren Name mit "Test" beginnt.</span><span class="sxs-lookup"><span data-stu-id="7f794-112">Get all ExpressRoute circuits whose name starts with "test".</span></span>

## <span data-ttu-id="7f794-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f794-113">PARAMETERS</span></span>

### <span data-ttu-id="7f794-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f794-114">-DefaultProfile</span></span>
<span data-ttu-id="7f794-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7f794-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f794-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7f794-116">-Name</span></span>
<span data-ttu-id="7f794-117">Der Name des Express Route-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="7f794-117">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="7f794-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f794-118">-ResourceGroupName</span></span>
<span data-ttu-id="7f794-119">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="7f794-119">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="7f794-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f794-120">CommonParameters</span></span>
<span data-ttu-id="7f794-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f794-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f794-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f794-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f794-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f794-123">INPUTS</span></span>

### <span data-ttu-id="7f794-124">System. String</span><span class="sxs-lookup"><span data-stu-id="7f794-124">System.String</span></span>

## <span data-ttu-id="7f794-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f794-125">OUTPUTS</span></span>

### <span data-ttu-id="7f794-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7f794-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7f794-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f794-127">NOTES</span></span>

## <span data-ttu-id="7f794-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f794-128">RELATED LINKS</span></span>

[<span data-ttu-id="7f794-129">Verschieben-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7f794-129">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="7f794-130">Neu – AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7f794-130">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="7f794-131">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7f794-131">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="7f794-132">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7f794-132">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
