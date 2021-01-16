---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 657ffd65bd6dd477700002862060b931979de456
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379937"
---
# <span data-ttu-id="1b1dc-101">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="1b1dc-101">Get-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="1b1dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b1dc-102">SYNOPSIS</span></span>
<span data-ttu-id="1b1dc-103">Holen Sie sich virtuelle Geräte im Netzwerk, oder listen Sie sie auf.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-103">Get or List Network Virtual Appliances.</span></span>

## <span data-ttu-id="1b1dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b1dc-104">SYNTAX</span></span>

### <span data-ttu-id="1b1dc-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1b1dc-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzNetworkVirtualAppliance [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b1dc-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b1dc-106">ResourceIdParameterSet</span></span>
```
Get-AzNetworkVirtualAppliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b1dc-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b1dc-107">DESCRIPTION</span></span>
<span data-ttu-id="1b1dc-108">Die Get-AzNetworkVirtualAppliance ruft Ressourcen für virtuelle Geräte von Network ab oder listet diese auf.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-108">The Get-AzNetworkVirtualAppliance commands gets or lists Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="1b1dc-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1b1dc-109">EXAMPLES</span></span>

### <span data-ttu-id="1b1dc-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1b1dc-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva                                                                                                                      

BootStrapConfigurationBlobs : {}
VirtualHub                  : Microsoft.Azure.Commands.Network.Models.PSResourceId
CloudInitConfigurationBlobs : {}
CloudInitConfiguration      : echo hi
VirtualApplianceAsn         : 1270
VirtualApplianceNics        : {privatenicipconfig, publicnicipconfig, privatenicipconfig, publicnicipconfig}
VirtualApplianceSites       : {}
ProvisioningState           : Succeeded
Identity                    :
NvaSku                      : Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
ResourceGroupName           : testrg
Location                    : eastus2
ResourceGuid                :
Type                        : Microsoft.Network/NetworkVirtualAppliances
Tag                         :
TagsTable                   :
Name                        : nva
Etag                        : 00000000-0000-0000-0000-000000000000
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva
```

<span data-ttu-id="1b1dc-111">Holen Sie sich eine Network Virtual Appliance-Ressource.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-111">Get a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="1b1dc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b1dc-112">PARAMETERS</span></span>

### <span data-ttu-id="1b1dc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b1dc-113">-DefaultProfile</span></span>
<span data-ttu-id="1b1dc-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b1dc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1b1dc-115">-Name</span></span>
<span data-ttu-id="1b1dc-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b1dc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b1dc-117">-ResourceGroupName</span></span>
<span data-ttu-id="1b1dc-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b1dc-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b1dc-119">-ResourceId</span></span>
<span data-ttu-id="1b1dc-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-120">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b1dc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b1dc-121">CommonParameters</span></span>
<span data-ttu-id="1b1dc-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b1dc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b1dc-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b1dc-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b1dc-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1b1dc-124">INPUTS</span></span>

### <span data-ttu-id="1b1dc-125">System.String</span><span class="sxs-lookup"><span data-stu-id="1b1dc-125">System.String</span></span>

## <span data-ttu-id="1b1dc-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1b1dc-126">OUTPUTS</span></span>

### <span data-ttu-id="1b1dc-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="1b1dc-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="1b1dc-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1b1dc-128">NOTES</span></span>

## <span data-ttu-id="1b1dc-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1b1dc-129">RELATED LINKS</span></span>
