---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
ms.openlocfilehash: 5cfe83c48950fff7f300b07cf43ba32ff9739606
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925568"
---
# <span data-ttu-id="30019-101">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="30019-101">New-AzFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="30019-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30019-102">SYNOPSIS</span></span>
<span data-ttu-id="30019-103">Erstellen eines PSBackendPool-Objekts für die Erstellung von Vordertüren</span><span class="sxs-lookup"><span data-stu-id="30019-103">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="30019-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30019-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30019-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30019-105">DESCRIPTION</span></span>
<span data-ttu-id="30019-106">Erstellen eines PSBackendPool-Objekts für die Erstellung von Vordertüren</span><span class="sxs-lookup"><span data-stu-id="30019-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="30019-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="30019-107">EXAMPLES</span></span>

### <span data-ttu-id="30019-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="30019-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendPoolObject -Name "backendpool1" -FrontDoorName $Name -ResourceGroupName $resourceGroupName -Backend $backend1 -He
althProbeSettingsName "healthProbeSetting1" -LoadBalancingSettingsName "loadBalancingSetting1"


Backends                : {Microsoft.Azure.Commands.FrontDoor.Models.PSBackend}
LoadBalancingSettingRef : /subscriptions/{subid}/resourceGroups/{resourceGroupName}/providers
                          /Microsoft.Network/frontDoors/frontdoor5/LoadBalancingSettings/loadBalancingSetting1
HealthProbeSettingRef   : /subscriptions/{subid}/resourceGroups/{resourceGroupName}/providers
                          /Microsoft.Network/frontDoors/frontdoor5/HealthProbeSettings/healthProbeSetting1
EnabledState            : Enabled
ResourceState           :
Id                      :
Name                    : backendpool1
Type                    :
```

<span data-ttu-id="30019-109">Erstellen eines PSBackendPool-Objekts für die Erstellung von Vordertüren</span><span class="sxs-lookup"><span data-stu-id="30019-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="30019-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="30019-110">PARAMETERS</span></span>

### <span data-ttu-id="30019-111">-Back-End</span><span class="sxs-lookup"><span data-stu-id="30019-111">-Backend</span></span>
<span data-ttu-id="30019-112">Die Gruppe von Back-Ends für diesen Pool.</span><span class="sxs-lookup"><span data-stu-id="30019-112">The set of backends for this pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackend[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30019-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30019-113">-DefaultProfile</span></span>
<span data-ttu-id="30019-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="30019-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30019-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="30019-115">-FrontDoorName</span></span>
<span data-ttu-id="30019-116">Der Name der Eingangstür, zu der diese Routingregel gehört.</span><span class="sxs-lookup"><span data-stu-id="30019-116">The name of the Front Door to which this routing rule belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30019-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="30019-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="30019-118">Der Name der Integritätstesteinstellungen für diesen Back-End-Pool</span><span class="sxs-lookup"><span data-stu-id="30019-118">The name of the health probe settings for this backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30019-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="30019-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="30019-120">Der Name der Einstellungen für den Lastenausgleich für diesen Back-End-Pool</span><span class="sxs-lookup"><span data-stu-id="30019-120">The name of the load balancing settings for this backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30019-121">-Name</span><span class="sxs-lookup"><span data-stu-id="30019-121">-Name</span></span>
<span data-ttu-id="30019-122">Name des Back-EndPools.</span><span class="sxs-lookup"><span data-stu-id="30019-122">BackendPool name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30019-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30019-123">-ResourceGroupName</span></span>
<span data-ttu-id="30019-124">Der Ressourcengruppenname, in dem die RoutingRule erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="30019-124">The resource group name that the RoutingRule will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30019-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30019-125">CommonParameters</span></span>
<span data-ttu-id="30019-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30019-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30019-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30019-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30019-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="30019-128">INPUTS</span></span>

### <span data-ttu-id="30019-129">Keine</span><span class="sxs-lookup"><span data-stu-id="30019-129">None</span></span>

## <span data-ttu-id="30019-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="30019-130">OUTPUTS</span></span>

### <span data-ttu-id="30019-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="30019-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="30019-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="30019-132">NOTES</span></span>

## <span data-ttu-id="30019-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="30019-133">RELATED LINKS</span></span>

<span data-ttu-id="30019-134">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="30019-134">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span></span>
