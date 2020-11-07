---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendPoolObject.md
ms.openlocfilehash: 13b28d236e1c6e758c4f7883285c55017ce5a727
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663138"
---
# <span data-ttu-id="ca73a-101">New-AzureRmFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="ca73a-101">New-AzureRmFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="ca73a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ca73a-102">SYNOPSIS</span></span>
<span data-ttu-id="ca73a-103">Erstellen eines PSBackendPool-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="ca73a-103">Create a PSBackendPool object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca73a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca73a-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca73a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca73a-105">DESCRIPTION</span></span>
<span data-ttu-id="ca73a-106">Erstellen eines PSBackendPool-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="ca73a-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="ca73a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ca73a-107">EXAMPLES</span></span>

### <span data-ttu-id="ca73a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ca73a-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorBackendPoolObject -Name "backendpool1" -FrontDoorName $Name -ResourceGroupName $resourceGroupName -Backend $backend1 -He
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

<span data-ttu-id="ca73a-109">Erstellen eines PSBackendPool-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="ca73a-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="ca73a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca73a-110">PARAMETERS</span></span>

### <span data-ttu-id="ca73a-111">-Back-End</span><span class="sxs-lookup"><span data-stu-id="ca73a-111">-Backend</span></span>
<span data-ttu-id="ca73a-112">Der Satz der Backends für diesen Pool.</span><span class="sxs-lookup"><span data-stu-id="ca73a-112">The set of backends for this pool.</span></span>

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

### <span data-ttu-id="ca73a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca73a-113">-DefaultProfile</span></span>
<span data-ttu-id="ca73a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ca73a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca73a-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="ca73a-115">-FrontDoorName</span></span>
<span data-ttu-id="ca73a-116">Der Name der Haustür, zu der diese Routingregel gehört.</span><span class="sxs-lookup"><span data-stu-id="ca73a-116">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="ca73a-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="ca73a-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="ca73a-118">Der Name der Integritäts Prüfungseinstellungen für diesen Back-End-Pool</span><span class="sxs-lookup"><span data-stu-id="ca73a-118">The name of the health probe settings for this backend pool</span></span>

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

### <span data-ttu-id="ca73a-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="ca73a-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="ca73a-120">Der Name der Lastenausgleichseinstellungen für diesen Back-End-Pool</span><span class="sxs-lookup"><span data-stu-id="ca73a-120">The name of the load balancing settings for this backend pool</span></span>

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

### <span data-ttu-id="ca73a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ca73a-121">-Name</span></span>
<span data-ttu-id="ca73a-122">BackendPool-Name.</span><span class="sxs-lookup"><span data-stu-id="ca73a-122">BackendPool name.</span></span>

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

### <span data-ttu-id="ca73a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca73a-123">-ResourceGroupName</span></span>
<span data-ttu-id="ca73a-124">Der Ressourcengruppenname, in dem der RoutingRule erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ca73a-124">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="ca73a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca73a-125">CommonParameters</span></span>
<span data-ttu-id="ca73a-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca73a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca73a-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca73a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca73a-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ca73a-128">INPUTS</span></span>

### <span data-ttu-id="ca73a-129">Keine</span><span class="sxs-lookup"><span data-stu-id="ca73a-129">None</span></span>

## <span data-ttu-id="ca73a-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ca73a-130">OUTPUTS</span></span>

### <span data-ttu-id="ca73a-131">Microsoft. Azure. Commands. Haustür. Models. PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="ca73a-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="ca73a-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="ca73a-132">NOTES</span></span>

## <span data-ttu-id="ca73a-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ca73a-133">RELATED LINKS</span></span>

<span data-ttu-id="ca73a-134">[Neu – AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Satz-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
 [Neu – AzureRmFrontDoorBackendObject](./New-AzureRmFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="ca73a-134">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorBackendObject](./New-AzureRmFrontDoorBackendObject.md)</span></span>
