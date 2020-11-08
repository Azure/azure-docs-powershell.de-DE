---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
ms.openlocfilehash: fdbb023c6796a780bfe9e6474191185a58489c91
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165249"
---
# <span data-ttu-id="f380c-101">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f380c-101">Get-AzPrivateLinkService</span></span>

## <span data-ttu-id="f380c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f380c-102">SYNOPSIS</span></span>
<span data-ttu-id="f380c-103">Ruft den privaten Link Dienst ab</span><span class="sxs-lookup"><span data-stu-id="f380c-103">Gets private link service</span></span>

## <span data-ttu-id="f380c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f380c-104">SYNTAX</span></span>

### <span data-ttu-id="f380c-105">NOEXPAND (Standard)</span><span class="sxs-lookup"><span data-stu-id="f380c-105">NoExpand (Default)</span></span>
```
Get-AzPrivateLinkService [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f380c-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="f380c-106">Expand</span></span>
```
Get-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f380c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f380c-107">DESCRIPTION</span></span>
<span data-ttu-id="f380c-108">Das Cmdlet " **Get-AzPrivateLinkService** " Ruft einen oder mehrere private Link Dienste ab.</span><span class="sxs-lookup"><span data-stu-id="f380c-108">The **Get-AzPrivateLinkService** cmdlet gets one or more private link services.</span></span>

## <span data-ttu-id="f380c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f380c-109">EXAMPLES</span></span>

### <span data-ttu-id="f380c-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f380c-110">Example</span></span>
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

<span data-ttu-id="f380c-111">Dieser Unifiedgroup Ruft einen privaten Link Dienst in der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="f380c-111">This commandlet gets a private link service in the resource group.</span></span>

## <span data-ttu-id="f380c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f380c-112">PARAMETERS</span></span>

### <span data-ttu-id="f380c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f380c-113">-DefaultProfile</span></span>
<span data-ttu-id="f380c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f380c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f380c-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="f380c-115">-ExpandResource</span></span>
<span data-ttu-id="f380c-116">Der Ressourcenverweis, der erweitert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f380c-116">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="f380c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f380c-117">-Name</span></span>
<span data-ttu-id="f380c-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="f380c-118">The resource name.</span></span>

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

### <span data-ttu-id="f380c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f380c-119">-ResourceGroupName</span></span>
<span data-ttu-id="f380c-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f380c-120">The resource group name.</span></span>

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

### <span data-ttu-id="f380c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f380c-121">CommonParameters</span></span>
<span data-ttu-id="f380c-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f380c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f380c-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f380c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f380c-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f380c-124">INPUTS</span></span>

### <span data-ttu-id="f380c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f380c-125">System.String</span></span>

## <span data-ttu-id="f380c-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f380c-126">OUTPUTS</span></span>

### <span data-ttu-id="f380c-127">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f380c-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="f380c-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="f380c-128">NOTES</span></span>

## <span data-ttu-id="f380c-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f380c-129">RELATED LINKS</span></span>
