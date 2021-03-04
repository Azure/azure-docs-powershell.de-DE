---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
ms.openlocfilehash: 8b2e8902257566256ed41c38c90c31cb430d12d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919696"
---
# <span data-ttu-id="4712b-101">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4712b-101">Get-AzPrivateLinkService</span></span>

## <span data-ttu-id="4712b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4712b-102">SYNOPSIS</span></span>
<span data-ttu-id="4712b-103">Ruft privaten Linkdienst ab</span><span class="sxs-lookup"><span data-stu-id="4712b-103">Gets private link service</span></span>

## <span data-ttu-id="4712b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4712b-104">SYNTAX</span></span>

### <span data-ttu-id="4712b-105">NoExpand (Standard)</span><span class="sxs-lookup"><span data-stu-id="4712b-105">NoExpand (Default)</span></span>
```
Get-AzPrivateLinkService [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4712b-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="4712b-106">Expand</span></span>
```
Get-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4712b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4712b-107">DESCRIPTION</span></span>
<span data-ttu-id="4712b-108">Das **Get-AzPrivateLinkService-Cmdlet** ruft einen oder mehrere private Linkdienste ab.</span><span class="sxs-lookup"><span data-stu-id="4712b-108">The **Get-AzPrivateLinkService** cmdlet gets one or more private link services.</span></span>

## <span data-ttu-id="4712b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4712b-109">EXAMPLES</span></span>

### <span data-ttu-id="4712b-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4712b-110">Example</span></span>
```
Get-AzPrivateLinkService -Name MyPLS -ResourceGroupName TestResourceGroup

Name                                 : MyPLS
ResourceGroupName                    : TestResourceGroup
Id                                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/prov
                                       iders/Microsoft.Network/privateLinkServices/MyPLS
Location                             : eastus2euap
Type                                 : Microsoft.Network/privateLinkServices
Etag                                 : W/"00000000-0000-0000-0000-000000000000"
Tag                                  : {}
ProvisioningState                    : Succeeded
Visibility                           : 
AutoApproval                         : 
Alias                                :
LoadBalancerFrontendIpConfigurations : []
IpConfigurations                     : [
                                         {
                                           "PrivateIPAddress": "10.0.2.5",
                                           "PrivateIPAllocationMethod": "Static",
                                           "ProvisioningState": "Failed",
                                           "PrivateIPAddressVersion": "IPv4",
                                           "Name": "IP-Config",
                                           "Subnet": {
                                             "Delegations": [],
                                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/
                                       TestResourceGroup/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/backendSubne
                                       t",
                                             "ServiceAssociationLinks": []
                                           }
                                         }
                                       ]
PrivateEndpointConnections           : []
NetworkInterfaces                    : [
                                         {
                                           "TapConfigurations": [],
                                           "HostedWorkloads": [],
                                           "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/mytestinterface"
                                         }
                                       ]
```

<span data-ttu-id="4712b-111">Dieses Commandlet ruft einen privaten Linkdienst in der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="4712b-111">This commandlet gets a private link service in the resource group.</span></span>

## <span data-ttu-id="4712b-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4712b-112">PARAMETERS</span></span>

### <span data-ttu-id="4712b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4712b-113">-DefaultProfile</span></span>
<span data-ttu-id="4712b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4712b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4712b-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="4712b-115">-ExpandResource</span></span>
<span data-ttu-id="4712b-116">Der Ressourcenbezug, der erweitert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4712b-116">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4712b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4712b-117">-Name</span></span>
<span data-ttu-id="4712b-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="4712b-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4712b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4712b-119">-ResourceGroupName</span></span>
<span data-ttu-id="4712b-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4712b-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4712b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4712b-121">CommonParameters</span></span>
<span data-ttu-id="4712b-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4712b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4712b-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4712b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4712b-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4712b-124">INPUTS</span></span>

### <span data-ttu-id="4712b-125">System.String</span><span class="sxs-lookup"><span data-stu-id="4712b-125">System.String</span></span>

## <span data-ttu-id="4712b-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4712b-126">OUTPUTS</span></span>

### <span data-ttu-id="4712b-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4712b-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="4712b-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4712b-128">NOTES</span></span>

## <span data-ttu-id="4712b-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4712b-129">RELATED LINKS</span></span>
