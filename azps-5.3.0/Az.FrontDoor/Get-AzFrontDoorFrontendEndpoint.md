---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfrontendendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
ms.openlocfilehash: cc07dd366d5c82705a23e3b9276ee9d681c6ae2c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458664"
---
# <span data-ttu-id="3ce0c-101">Get-AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ce0c-101">Get-AzFrontDoorFrontendEndpoint</span></span>

## <span data-ttu-id="3ce0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ce0c-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce0c-103">Erhalten Sie einen Eingangseingangsendpunkt.</span><span class="sxs-lookup"><span data-stu-id="3ce0c-103">Get a front door frontend endpoint.</span></span>

## <span data-ttu-id="3ce0c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ce0c-104">SYNTAX</span></span>

### <span data-ttu-id="3ce0c-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3ce0c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ce0c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ce0c-106">ByObjectParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint [-Name <String>] -FrontDoorObject <PSFrontDoor>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ce0c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ce0c-107">ByResourceIdParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ce0c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ce0c-108">DESCRIPTION</span></span>
<span data-ttu-id="3ce0c-109">Das **Cmdlet "Get-AzFrontDsourceFrontendEndpoint"** ruft alle vorhandenen Frontend-Endpunkte in der aktuellen Ressource "Front Door" ab, die bereitgestellten Informationen entspricht.</span><span class="sxs-lookup"><span data-stu-id="3ce0c-109">The **Get-AzFrontDoorFrontendEndpoint** cmdlet gets all existing frontend endpoints in the current Front Door resource that matches provided information.</span></span>

## <span data-ttu-id="3ce0c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3ce0c-110">EXAMPLES</span></span>

### <span data-ttu-id="3ce0c-111">Beispiel 1: Erhalten Sie alle Frontend-Endpunkte in Front Door "frontd dann1", das zur Ressourcengruppe "rg1" gehört.</span><span class="sxs-lookup"><span data-stu-id="3ce0c-111">Example 1: Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "rg1" -FrontDoorName "frontdoor1"


HostName                         : frontdoor1.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontdoor1-azurefd-net
Name                             : frontdoor1-azurefd-net
Type                             : Microsoft.Network/frontdoors/frontendendpoints

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="3ce0c-112">Erhalten Sie alle Frontend-Endpunkte in Front Door "frontd dann 1", das zur Ressourcengruppe "rg1" gehört.</span><span class="sxs-lookup"><span data-stu-id="3ce0c-112">Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>

### <span data-ttu-id="3ce0c-113">Beispiel 2: Erhalten des Frontend-Endpunkts mit dem Namen "frontdsource1-azurefd-net" in Front Door "frontd dann1", das zur Ressourcengruppe "rg1" gehört</span><span class="sxs-lookup"><span data-stu-id="3ce0c-113">Example 2: Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "rg1" -FrontDoorName "frontdoor1" -Name "frontdoor1-azurefd-net"


HostName                         : frontdoor1.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontdoor1-azurefd-net
Name                             : frontdoor1-azurefd-net
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="3ce0c-114">Erhalten Sie den Frontend-Endpunkt mit dem Namen "frontdsource1-azurefd-net" in Front Door "frontd door1", der zur Ressourcengruppe "rg1" gehört.</span><span class="sxs-lookup"><span data-stu-id="3ce0c-114">Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>

## <span data-ttu-id="3ce0c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ce0c-115">PARAMETERS</span></span>

### <span data-ttu-id="3ce0c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ce0c-116">-DefaultProfile</span></span>
<span data-ttu-id="3ce0c-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ce0c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ce0c-118">-FrontD anderenName</span><span class="sxs-lookup"><span data-stu-id="3ce0c-118">-FrontDoorName</span></span>
<span data-ttu-id="3ce0c-119">Name der Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="3ce0c-119">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0c-120">-FrontDobjectObject</span><span class="sxs-lookup"><span data-stu-id="3ce0c-120">-FrontDoorObject</span></span>
<span data-ttu-id="3ce0c-121">Das FrontD dann-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3ce0c-121">The FrontDoor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3ce0c-122">-Name</span></span>
<span data-ttu-id="3ce0c-123">Name des Frontend-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="3ce0c-123">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ce0c-124">-ResourceGroupName</span></span>
<span data-ttu-id="3ce0c-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3ce0c-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ce0c-126">-ResourceId</span></span>
<span data-ttu-id="3ce0c-127">Ressourcen-ID der Eingangstür</span><span class="sxs-lookup"><span data-stu-id="3ce0c-127">Resource Id of the Front Door</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce0c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce0c-128">CommonParameters</span></span>
<span data-ttu-id="3ce0c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ce0c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce0c-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ce0c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce0c-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3ce0c-131">INPUTS</span></span>

### <span data-ttu-id="3ce0c-132">Keine</span><span class="sxs-lookup"><span data-stu-id="3ce0c-132">None</span></span>

## <span data-ttu-id="3ce0c-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3ce0c-133">OUTPUTS</span></span>

### <span data-ttu-id="3ce0c-134">Microsoft.Azure.Commands.FrontDando.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ce0c-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="3ce0c-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3ce0c-135">NOTES</span></span>

## <span data-ttu-id="3ce0c-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3ce0c-136">RELATED LINKS</span></span>
