---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfrontendendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
ms.openlocfilehash: cc07dd366d5c82705a23e3b9276ee9d681c6ae2c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175452"
---
# <span data-ttu-id="397e2-101">Get-AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="397e2-101">Get-AzFrontDoorFrontendEndpoint</span></span>

## <span data-ttu-id="397e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="397e2-102">SYNOPSIS</span></span>
<span data-ttu-id="397e2-103">Erhalten Sie einen Eingangseingangsendpunkt.</span><span class="sxs-lookup"><span data-stu-id="397e2-103">Get a front door frontend endpoint.</span></span>

## <span data-ttu-id="397e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="397e2-104">SYNTAX</span></span>

### <span data-ttu-id="397e2-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="397e2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="397e2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="397e2-106">ByObjectParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint [-Name <String>] -FrontDoorObject <PSFrontDoor>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="397e2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="397e2-107">ByResourceIdParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="397e2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="397e2-108">DESCRIPTION</span></span>
<span data-ttu-id="397e2-109">Das **Cmdlet "Get-AzFrontDsourceFrontendEndpoint"** ruft alle vorhandenen Frontend-Endpunkte in der aktuellen Ressource "Front Door" ab, die den bereitgestellten Informationen entspricht.</span><span class="sxs-lookup"><span data-stu-id="397e2-109">The **Get-AzFrontDoorFrontendEndpoint** cmdlet gets all existing frontend endpoints in the current Front Door resource that matches provided information.</span></span>

## <span data-ttu-id="397e2-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="397e2-110">EXAMPLES</span></span>

### <span data-ttu-id="397e2-111">Beispiel 1: Erhalten Sie alle Frontend-Endpunkte in Front Door "frontd door1", das zur Ressourcengruppe "rg1" gehört.</span><span class="sxs-lookup"><span data-stu-id="397e2-111">Example 1: Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>
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

<span data-ttu-id="397e2-112">Erhalten Sie alle Frontend-Endpunkte in Front Door "frontd dann 1", das zur Ressourcengruppe "rg1" gehört.</span><span class="sxs-lookup"><span data-stu-id="397e2-112">Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>

### <span data-ttu-id="397e2-113">Beispiel 2: Erhalten des Frontend-Endpunkts mit dem Namen "frontdsource1-azurefd-net" in Front Door "frontd dann1", das zur Ressourcengruppe "rg1" gehört</span><span class="sxs-lookup"><span data-stu-id="397e2-113">Example 2: Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>
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

<span data-ttu-id="397e2-114">Erhalten Sie den Frontend-Endpunkt mit dem Namen "frontdsource1-azurefd-net" in Front Door "frontd door1", der zur Ressourcengruppe "rg1" gehört.</span><span class="sxs-lookup"><span data-stu-id="397e2-114">Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>

## <span data-ttu-id="397e2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="397e2-115">PARAMETERS</span></span>

### <span data-ttu-id="397e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="397e2-116">-DefaultProfile</span></span>
<span data-ttu-id="397e2-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="397e2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="397e2-118">-FrontD ernennenName</span><span class="sxs-lookup"><span data-stu-id="397e2-118">-FrontDoorName</span></span>
<span data-ttu-id="397e2-119">Name der Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="397e2-119">Front Door name.</span></span>

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

### <span data-ttu-id="397e2-120">-FrontDobjectObject</span><span class="sxs-lookup"><span data-stu-id="397e2-120">-FrontDoorObject</span></span>
<span data-ttu-id="397e2-121">Das FrontDoor-Objekt.</span><span class="sxs-lookup"><span data-stu-id="397e2-121">The FrontDoor object.</span></span>

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

### <span data-ttu-id="397e2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="397e2-122">-Name</span></span>
<span data-ttu-id="397e2-123">Name des Frontend-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="397e2-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="397e2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="397e2-124">-ResourceGroupName</span></span>
<span data-ttu-id="397e2-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="397e2-125">The resource group name.</span></span>

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

### <span data-ttu-id="397e2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="397e2-126">-ResourceId</span></span>
<span data-ttu-id="397e2-127">Ressourcen-ID der Eingangstür</span><span class="sxs-lookup"><span data-stu-id="397e2-127">Resource Id of the Front Door</span></span>

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

### <span data-ttu-id="397e2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="397e2-128">CommonParameters</span></span>
<span data-ttu-id="397e2-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="397e2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="397e2-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="397e2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="397e2-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="397e2-131">INPUTS</span></span>

### <span data-ttu-id="397e2-132">Keine</span><span class="sxs-lookup"><span data-stu-id="397e2-132">None</span></span>

## <span data-ttu-id="397e2-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="397e2-133">OUTPUTS</span></span>

### <span data-ttu-id="397e2-134">Microsoft.Azure.Commands.FrontDando.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="397e2-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="397e2-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="397e2-135">NOTES</span></span>

## <span data-ttu-id="397e2-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="397e2-136">RELATED LINKS</span></span>
