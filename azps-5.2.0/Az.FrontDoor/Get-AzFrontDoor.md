---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
ms.openlocfilehash: 8c378d7f0b1ac7a753f7f270fd3969eb881c7aec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307368"
---
# <span data-ttu-id="5fbc8-101">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="5fbc8-101">Get-AzFrontDoor</span></span>

## <span data-ttu-id="5fbc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fbc8-102">SYNOPSIS</span></span>
<span data-ttu-id="5fbc8-103">Lastenausgleich bei Front Door</span><span class="sxs-lookup"><span data-stu-id="5fbc8-103">Get Front Door load balancer</span></span>

## <span data-ttu-id="5fbc8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5fbc8-104">SYNTAX</span></span>

```
Get-AzFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5fbc8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fbc8-105">DESCRIPTION</span></span>
<span data-ttu-id="5fbc8-106">Das **CmdletGet Get-AzFrontDments** ruft alle vorhandenen Front Doors im aktuellen Abonnement ab, die den bereitgestellten Informationen entspricht.</span><span class="sxs-lookup"><span data-stu-id="5fbc8-106">The **Get-AzFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="5fbc8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5fbc8-107">EXAMPLES</span></span>

### <span data-ttu-id="5fbc8-108">Beispiel 1: Alle FrontDoors im aktuellen Abonnement erhalten.</span><span class="sxs-lookup"><span data-stu-id="5fbc8-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
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

<span data-ttu-id="5fbc8-109">Holen Sie sich alle FrontDoors im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5fbc8-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="5fbc8-110">Beispiel 2: Alle FrontDoors in der Ressourcengruppe "rg1" im aktuellen Abonnement erhalten.</span><span class="sxs-lookup"><span data-stu-id="5fbc8-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
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

<span data-ttu-id="5fbc8-111">Alle FrontDoors in der Ressourcengruppe "rg1" im aktuellen Abonnement erhalten.</span><span class="sxs-lookup"><span data-stu-id="5fbc8-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="5fbc8-112">Beispiel 3: Erhalten Sie die FrontDoors in der Ressourcengruppe "rg1" mit dem Namen "frontDdot1" im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5fbc8-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
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

<span data-ttu-id="5fbc8-113">Holen Sie sich die FrontDoors in der Ressourcengruppe "rg1" mit dem Namen "frontDdot1" im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5fbc8-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="5fbc8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fbc8-114">PARAMETERS</span></span>

### <span data-ttu-id="5fbc8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fbc8-115">-DefaultProfile</span></span>
<span data-ttu-id="5fbc8-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5fbc8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fbc8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5fbc8-117">-Name</span></span>
<span data-ttu-id="5fbc8-118">Name der Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="5fbc8-118">Front Door name.</span></span>

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

### <span data-ttu-id="5fbc8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fbc8-119">-ResourceGroupName</span></span>
<span data-ttu-id="5fbc8-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5fbc8-120">The resource group name.</span></span>

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

### <span data-ttu-id="5fbc8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fbc8-121">CommonParameters</span></span>
<span data-ttu-id="5fbc8-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fbc8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fbc8-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5fbc8-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fbc8-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5fbc8-124">INPUTS</span></span>

### <span data-ttu-id="5fbc8-125">Keine</span><span class="sxs-lookup"><span data-stu-id="5fbc8-125">None</span></span>

## <span data-ttu-id="5fbc8-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5fbc8-126">OUTPUTS</span></span>

### <span data-ttu-id="5fbc8-127">Microsoft.Azure.Commands.Frontdando.Models.PSFrontDando</span><span class="sxs-lookup"><span data-stu-id="5fbc8-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="5fbc8-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5fbc8-128">NOTES</span></span>

## <span data-ttu-id="5fbc8-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5fbc8-129">RELATED LINKS</span></span>

<span data-ttu-id="5fbc8-130">[New-AzFrontD verankert](./New-AzFrontDoor.md) 
 [Set-AzFrontD verankert](./Set-AzFrontDoor.md) 
 [Remove-AzFrontD verankert](./Remove-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="5fbc8-130">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span></span>
