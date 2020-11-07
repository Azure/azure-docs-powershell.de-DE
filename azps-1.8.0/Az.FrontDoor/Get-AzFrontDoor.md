---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
ms.openlocfilehash: 6dd40ff6bdf94d95b9fe31ead7ce6bde53c7042b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820068"
---
# <span data-ttu-id="2d777-101">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d777-101">Get-AzFrontDoor</span></span>

## <span data-ttu-id="2d777-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d777-102">SYNOPSIS</span></span>
<span data-ttu-id="2d777-103">Herunterladen des Front-Door-Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="2d777-103">Get Front Door load balancer</span></span>

## <span data-ttu-id="2d777-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d777-104">SYNTAX</span></span>

```
Get-AzFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d777-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d777-105">DESCRIPTION</span></span>
<span data-ttu-id="2d777-106">Die **Get-AzFrontDoor-** cmdletGet Ruft alle vorhandenen Front Türen im aktuellen Abonnement ab, die den angegebenen Informationen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="2d777-106">The **Get-AzFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="2d777-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d777-107">EXAMPLES</span></span>

### <span data-ttu-id="2d777-108">Beispiel 1: Abrufen aller FrontDoors im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2d777-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid1}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid2}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="2d777-109">Abrufen aller FrontDoors im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="2d777-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="2d777-110">Beispiel 2: Abrufen aller FrontDoors in der Ressourcengruppe "RG1" im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2d777-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1"

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor2
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="2d777-111">Abrufen aller FrontDoors in der Ressourcengruppe "RG1" im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2d777-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="2d777-112">Beispiel 3: Abrufen der FrontDoors in der Ressourcengruppe "RG1" mit dem Namen "frontDoor1" im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2d777-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="2d777-113">Rufen Sie die FrontDoors in der Ressourcengruppe "RG1" mit dem Namen "frontDoor1" im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="2d777-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="2d777-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d777-114">PARAMETERS</span></span>

### <span data-ttu-id="2d777-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d777-115">-DefaultProfile</span></span>
<span data-ttu-id="2d777-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2d777-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d777-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2d777-117">-Name</span></span>
<span data-ttu-id="2d777-118">Name der Haustüre</span><span class="sxs-lookup"><span data-stu-id="2d777-118">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d777-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d777-119">-ResourceGroupName</span></span>
<span data-ttu-id="2d777-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2d777-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d777-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d777-121">CommonParameters</span></span>
<span data-ttu-id="2d777-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d777-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d777-123">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d777-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d777-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d777-124">INPUTS</span></span>

### <span data-ttu-id="2d777-125">Keine</span><span class="sxs-lookup"><span data-stu-id="2d777-125">None</span></span>

## <span data-ttu-id="2d777-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d777-126">OUTPUTS</span></span>

### <span data-ttu-id="2d777-127">Microsoft. Azure. Commands. Haustür. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d777-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="2d777-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d777-128">NOTES</span></span>

## <span data-ttu-id="2d777-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d777-129">RELATED LINKS</span></span>

<span data-ttu-id="2d777-130">[Neu – AzFrontDoor](./New-AzFrontDoor.md) 
 [Satz-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="2d777-130">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span></span>
