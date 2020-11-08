---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNatGateway.md
ms.openlocfilehash: 650ffdfd557780727a4f3bc4c69a7be6f2783cb3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003532"
---
# <span data-ttu-id="156ff-101">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="156ff-101">Get-AzNatGateway</span></span>

## <span data-ttu-id="156ff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="156ff-102">SYNOPSIS</span></span>
<span data-ttu-id="156ff-103">Ruft eine NAT-Gateway-Ressource in einer Ressourcengruppe nach Name oder NatGateway-ID oder alle NAT-Gateway-Ressourcen in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="156ff-103">Gets a Nat Gateway resource in a resource group by name or NatGateway Id  or all Nat Gateway resources in a resource group.</span></span>

## <span data-ttu-id="156ff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="156ff-104">SYNTAX</span></span>

### <span data-ttu-id="156ff-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="156ff-105">ListParameterSet (Default)</span></span>
```
Get-AzNatGateway [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="156ff-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="156ff-106">GetByNameParameterSet</span></span>
```
Get-AzNatGateway -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="156ff-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="156ff-107">GetByResourceIdParameterSet</span></span>
```
Get-AzNatGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="156ff-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="156ff-108">DESCRIPTION</span></span>
<span data-ttu-id="156ff-109">Ruft eine NAT-Gateway-Ressource in einer Ressourcengruppe nach Name oder NatGateway-ID oder alle NAT-Gateway-Ressourcen in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="156ff-109">Gets a Nat Gateway resource in a resource group by name OR NatGateway Id OR all Nat Gateway resources in a resource group.</span></span>

## <span data-ttu-id="156ff-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="156ff-110">EXAMPLES</span></span>

### <span data-ttu-id="156ff-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="156ff-111">Example 1</span></span>
```powershell
PS C:> Get-AzNatGateway -ResourceGroupName "natgateway_test"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway

IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : []
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : ng1
Etag                  : W/"bdf98e30-d6c6-4af2-8f62-10d1fdaa6e84"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/ng1


PS C:> Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway

PS C:> Get-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway
```

## <span data-ttu-id="156ff-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="156ff-112">PARAMETERS</span></span>

### <span data-ttu-id="156ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="156ff-113">-DefaultProfile</span></span>
<span data-ttu-id="156ff-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="156ff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="156ff-115">-Name</span><span class="sxs-lookup"><span data-stu-id="156ff-115">-Name</span></span>
<span data-ttu-id="156ff-116">Der Name des NAT-Gateways.</span><span class="sxs-lookup"><span data-stu-id="156ff-116">The name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="156ff-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="156ff-117">-ResourceGroupName</span></span>
<span data-ttu-id="156ff-118">Der Ressourcengruppenname des NAT-Gateways.</span><span class="sxs-lookup"><span data-stu-id="156ff-118">The resource group name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="156ff-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="156ff-119">-ResourceId</span></span>
<span data-ttu-id="156ff-120">NAT-Gateway-ID</span><span class="sxs-lookup"><span data-stu-id="156ff-120">Nat Gateway Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="156ff-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="156ff-121">CommonParameters</span></span>
<span data-ttu-id="156ff-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="156ff-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="156ff-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="156ff-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="156ff-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="156ff-124">INPUTS</span></span>

### <span data-ttu-id="156ff-125">System. String</span><span class="sxs-lookup"><span data-stu-id="156ff-125">System.String</span></span>

## <span data-ttu-id="156ff-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="156ff-126">OUTPUTS</span></span>

### <span data-ttu-id="156ff-127">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="156ff-127">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="156ff-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="156ff-128">NOTES</span></span>

## <span data-ttu-id="156ff-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="156ff-129">RELATED LINKS</span></span>
