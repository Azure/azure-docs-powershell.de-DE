---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfrontendendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
ms.openlocfilehash: f685bb7bdad663e84a67397c89568d2263d0ed9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820060"
---
# <span data-ttu-id="c7cb1-101">Get-AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7cb1-101">Get-AzFrontDoorFrontendEndpoint</span></span>

## <span data-ttu-id="c7cb1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="c7cb1-103">Besorgen Sie sich einen Frontend-Endpunkt für Haustür.</span><span class="sxs-lookup"><span data-stu-id="c7cb1-103">Get a front door frontend endpoint.</span></span>

## <span data-ttu-id="c7cb1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7cb1-104">SYNTAX</span></span>

### <span data-ttu-id="c7cb1-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c7cb1-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7cb1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7cb1-106">ByObjectParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint [-Name <String>] -FrontDoorObject <PSFrontDoor>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7cb1-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7cb1-107">ByResourceIdParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7cb1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7cb1-108">DESCRIPTION</span></span>
<span data-ttu-id="c7cb1-109">Das Cmdlet " **Get-AzFrontDoorFrontendEndpoint** " ruft alle vorhandenen Frontend-Endpunkte in der aktuellen Haustür Ressource ab, die den bereitgestellten Informationen entspricht.</span><span class="sxs-lookup"><span data-stu-id="c7cb1-109">The **Get-AzFrontDoorFrontendEndpoint** cmdlet gets all existing frontend endpoints in the current Front Door resource that matches provided information.</span></span>

## <span data-ttu-id="c7cb1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7cb1-110">EXAMPLES</span></span>

### <span data-ttu-id="c7cb1-111">Beispiel 1: Abrufen aller Frontend-Endpunkte in der Haustür "frontdoor1", das Teil der Ressourcengruppe "RG1" ist.</span><span class="sxs-lookup"><span data-stu-id="c7cb1-111">Example 1: Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>
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

<span data-ttu-id="c7cb1-112">Rufen Sie alle Frontend-Endpunkte in der Haustür "frontdoor1" ab, die Bestandteil der Ressourcengruppe "RG1" ist.</span><span class="sxs-lookup"><span data-stu-id="c7cb1-112">Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>

### <span data-ttu-id="c7cb1-113">Beispiel 2: Abrufen des Frontend-Endpunkts mit dem Namen "frontdoor1-azurefd-net" im Front Door "frontdoor1", das Teil der Ressourcengruppe "RG1" ist</span><span class="sxs-lookup"><span data-stu-id="c7cb1-113">Example 2: Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>
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

<span data-ttu-id="c7cb1-114">Abrufen des Frontend-Endpunkts mit dem Namen "frontdoor1-azurefd-net" in der Haustür "frontdoor1", das Teil der Ressourcengruppe "RG1" ist</span><span class="sxs-lookup"><span data-stu-id="c7cb1-114">Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>

## <span data-ttu-id="c7cb1-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7cb1-115">PARAMETERS</span></span>

### <span data-ttu-id="c7cb1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7cb1-116">-DefaultProfile</span></span>
<span data-ttu-id="c7cb1-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c7cb1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7cb1-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="c7cb1-118">-FrontDoorName</span></span>
<span data-ttu-id="c7cb1-119">Name der Haustüre</span><span class="sxs-lookup"><span data-stu-id="c7cb1-119">Front Door name.</span></span>

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

### <span data-ttu-id="c7cb1-120">-FrontDoorObject</span><span class="sxs-lookup"><span data-stu-id="c7cb1-120">-FrontDoorObject</span></span>
<span data-ttu-id="c7cb1-121">Das Haustür-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c7cb1-121">The FrontDoor object.</span></span>

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

### <span data-ttu-id="c7cb1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c7cb1-122">-Name</span></span>
<span data-ttu-id="c7cb1-123">Frontend-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="c7cb1-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="c7cb1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7cb1-124">-ResourceGroupName</span></span>
<span data-ttu-id="c7cb1-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c7cb1-125">The resource group name.</span></span>

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

### <span data-ttu-id="c7cb1-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c7cb1-126">-ResourceId</span></span>
<span data-ttu-id="c7cb1-127">Ressourcen-ID der Haustür</span><span class="sxs-lookup"><span data-stu-id="c7cb1-127">Resource Id of the Front Door</span></span>

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

### <span data-ttu-id="c7cb1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7cb1-128">CommonParameters</span></span>
<span data-ttu-id="c7cb1-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7cb1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7cb1-130">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7cb1-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7cb1-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7cb1-131">INPUTS</span></span>

### <span data-ttu-id="c7cb1-132">Keine</span><span class="sxs-lookup"><span data-stu-id="c7cb1-132">None</span></span>

## <span data-ttu-id="c7cb1-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7cb1-133">OUTPUTS</span></span>

### <span data-ttu-id="c7cb1-134">Microsoft. Azure. Commands. Haustür. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7cb1-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="c7cb1-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7cb1-135">NOTES</span></span>

## <span data-ttu-id="c7cb1-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7cb1-136">RELATED LINKS</span></span>
