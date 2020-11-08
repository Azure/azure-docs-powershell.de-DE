---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
ms.openlocfilehash: 6dba24ae79d051668e88a718402c5e01e81a7461
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007969"
---
# <span data-ttu-id="43007-101">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="43007-101">New-AzFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="43007-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43007-102">SYNOPSIS</span></span>
<span data-ttu-id="43007-103">Erstellen eines PSBackendPool-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="43007-103">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="43007-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43007-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43007-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43007-105">DESCRIPTION</span></span>
<span data-ttu-id="43007-106">Erstellen eines PSBackendPool-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="43007-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="43007-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43007-107">EXAMPLES</span></span>

### <span data-ttu-id="43007-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="43007-108">Example 1</span></span>
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

<span data-ttu-id="43007-109">Erstellen eines PSBackendPool-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="43007-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="43007-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="43007-110">PARAMETERS</span></span>

### <span data-ttu-id="43007-111">-Back-End</span><span class="sxs-lookup"><span data-stu-id="43007-111">-Backend</span></span>
<span data-ttu-id="43007-112">Der Satz der Backends für diesen Pool.</span><span class="sxs-lookup"><span data-stu-id="43007-112">The set of backends for this pool.</span></span>

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

### <span data-ttu-id="43007-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43007-113">-DefaultProfile</span></span>
<span data-ttu-id="43007-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="43007-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43007-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="43007-115">-FrontDoorName</span></span>
<span data-ttu-id="43007-116">Der Name der Haustür, zu der diese Routingregel gehört.</span><span class="sxs-lookup"><span data-stu-id="43007-116">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="43007-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="43007-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="43007-118">Der Name der Integritäts Prüfungseinstellungen für diesen Back-End-Pool</span><span class="sxs-lookup"><span data-stu-id="43007-118">The name of the health probe settings for this backend pool</span></span>

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

### <span data-ttu-id="43007-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="43007-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="43007-120">Der Name der Lastenausgleichseinstellungen für diesen Back-End-Pool</span><span class="sxs-lookup"><span data-stu-id="43007-120">The name of the load balancing settings for this backend pool</span></span>

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

### <span data-ttu-id="43007-121">-Name</span><span class="sxs-lookup"><span data-stu-id="43007-121">-Name</span></span>
<span data-ttu-id="43007-122">BackendPool-Name.</span><span class="sxs-lookup"><span data-stu-id="43007-122">BackendPool name.</span></span>

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

### <span data-ttu-id="43007-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43007-123">-ResourceGroupName</span></span>
<span data-ttu-id="43007-124">Der Ressourcengruppenname, in dem der RoutingRule erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="43007-124">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="43007-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43007-125">CommonParameters</span></span>
<span data-ttu-id="43007-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43007-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43007-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43007-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43007-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43007-128">INPUTS</span></span>

### <span data-ttu-id="43007-129">Keine</span><span class="sxs-lookup"><span data-stu-id="43007-129">None</span></span>

## <span data-ttu-id="43007-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43007-130">OUTPUTS</span></span>

### <span data-ttu-id="43007-131">Microsoft. Azure. Commands. Haustür. Models. PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="43007-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="43007-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="43007-132">NOTES</span></span>

## <span data-ttu-id="43007-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43007-133">RELATED LINKS</span></span>

<span data-ttu-id="43007-134">[Neu – AzFrontDoor](./New-AzFrontDoor.md) 
 [Satz-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Neu – AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="43007-134">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span></span>
