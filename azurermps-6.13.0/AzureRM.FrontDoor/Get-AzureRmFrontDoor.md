---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/get-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoor.md
ms.openlocfilehash: ca54e2cc86daca89a9872366dea32b375080c63d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663140"
---
# <span data-ttu-id="8be7a-101">Get-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="8be7a-101">Get-AzureRmFrontDoor</span></span>

## <span data-ttu-id="8be7a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8be7a-102">SYNOPSIS</span></span>
<span data-ttu-id="8be7a-103">Herunterladen des Front-Door-Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="8be7a-103">Get Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8be7a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8be7a-104">SYNTAX</span></span>

```
Get-AzureRmFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8be7a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8be7a-105">DESCRIPTION</span></span>
<span data-ttu-id="8be7a-106">Die **Get-AzureRmFrontDoor-** cmdletGet Ruft alle vorhandenen Front Türen im aktuellen Abonnement ab, die den angegebenen Informationen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8be7a-106">The **Get-AzureRmFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="8be7a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8be7a-107">EXAMPLES</span></span>

### <span data-ttu-id="8be7a-108">Beispiel 1: Abrufen aller FrontDoors im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8be7a-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor

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

<span data-ttu-id="8be7a-109">Abrufen aller FrontDoors im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="8be7a-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="8be7a-110">Beispiel 2: Abrufen aller FrontDoors in der Ressourcengruppe "RG1" im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8be7a-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1"

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

<span data-ttu-id="8be7a-111">Abrufen aller FrontDoors in der Ressourcengruppe "RG1" im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8be7a-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="8be7a-112">Beispiel 3: Abrufen der FrontDoors in der Ressourcengruppe "RG1" mit dem Namen "frontDoor1" im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8be7a-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

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

<span data-ttu-id="8be7a-113">Rufen Sie die FrontDoors in der Ressourcengruppe "RG1" mit dem Namen "frontDoor1" im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="8be7a-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="8be7a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8be7a-114">PARAMETERS</span></span>

### <span data-ttu-id="8be7a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8be7a-115">-DefaultProfile</span></span>
<span data-ttu-id="8be7a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8be7a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be7a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8be7a-117">-Name</span></span>
<span data-ttu-id="8be7a-118">Name der Haustüre</span><span class="sxs-lookup"><span data-stu-id="8be7a-118">Front Door name.</span></span>

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

### <span data-ttu-id="8be7a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8be7a-119">-ResourceGroupName</span></span>
<span data-ttu-id="8be7a-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8be7a-120">The resource group name.</span></span>

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

### <span data-ttu-id="8be7a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be7a-121">CommonParameters</span></span>
<span data-ttu-id="8be7a-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8be7a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be7a-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8be7a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be7a-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8be7a-124">INPUTS</span></span>

### <span data-ttu-id="8be7a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8be7a-125">System.String</span></span>

## <span data-ttu-id="8be7a-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8be7a-126">OUTPUTS</span></span>

### <span data-ttu-id="8be7a-127">Microsoft. Azure. Commands. Haustür. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="8be7a-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="8be7a-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="8be7a-128">NOTES</span></span>

## <span data-ttu-id="8be7a-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8be7a-129">RELATED LINKS</span></span>

<span data-ttu-id="8be7a-130">[Neu – AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Satz-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
 [Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="8be7a-130">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)</span></span>
