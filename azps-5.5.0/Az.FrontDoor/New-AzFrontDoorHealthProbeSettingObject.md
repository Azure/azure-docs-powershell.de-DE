---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 850db31354ebe4a717a5064c7fed56dc94bf1f0d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147897"
---
# <span data-ttu-id="117cf-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="117cf-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="117cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="117cf-102">SYNOPSIS</span></span>
<span data-ttu-id="117cf-103">Erstellen eines "PSHealthProbeSetting"-Objekts für die Erstellung von "Front Door"</span><span class="sxs-lookup"><span data-stu-id="117cf-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="117cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="117cf-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="117cf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="117cf-105">DESCRIPTION</span></span>
<span data-ttu-id="117cf-106">Erstellen eines "PSHealthProbeSetting"-Objekts für die Erstellung von "Front Door"</span><span class="sxs-lookup"><span data-stu-id="117cf-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="117cf-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="117cf-107">EXAMPLES</span></span>

### <span data-ttu-id="117cf-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="117cf-108">Example 1</span></span>
```powershell
PS C:\>  New-AzFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
HealthProbeMethod : Head
EnabledState      : Enabled
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="117cf-109">Hinweis: Bei der Einstellung "HealthProbeMethod" wird die Zwischenschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="117cf-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="117cf-110">Erstellen eines "PSHealthProbeSetting"-Objekts für die Erstellung von "Front Door"</span><span class="sxs-lookup"><span data-stu-id="117cf-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="117cf-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="117cf-111">PARAMETERS</span></span>

### <span data-ttu-id="117cf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="117cf-112">-DefaultProfile</span></span>
<span data-ttu-id="117cf-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="117cf-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="117cf-114">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="117cf-114">-EnabledState</span></span>
<span data-ttu-id="117cf-115">Gibt an, ob Integritätssonden für Back-End-Funktionen aktiviert werden sollen, die unter Back-End-Pools definiert sind.</span><span class="sxs-lookup"><span data-stu-id="117cf-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="117cf-116">Integritätstest können nur deaktiviert werden, wenn ein einzelnes aktiviertes Back-End im einzelnen aktivierten Back-End-Pool verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="117cf-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="117cf-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="117cf-117">-HealthProbeMethod</span></span>
<span data-ttu-id="117cf-118">Konfiguriert, welche HTTP-Methode verwendet werden soll, um die unter "Back-EndPools" definierten Back-End-Back-Ends zu finden.</span><span class="sxs-lookup"><span data-stu-id="117cf-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

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

### <span data-ttu-id="117cf-119">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="117cf-119">-IntervalInSeconds</span></span>
<span data-ttu-id="117cf-120">Die Anzahl von Sekunden zwischen Integritätstest.</span><span class="sxs-lookup"><span data-stu-id="117cf-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="117cf-121">Der Standardwert ist 30.</span><span class="sxs-lookup"><span data-stu-id="117cf-121">Default value is 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="117cf-122">-Name</span><span class="sxs-lookup"><span data-stu-id="117cf-122">-Name</span></span>
<span data-ttu-id="117cf-123">Name der Integritätstesteinstellung.</span><span class="sxs-lookup"><span data-stu-id="117cf-123">Health probe setting name.</span></span>

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

### <span data-ttu-id="117cf-124">-Path</span><span class="sxs-lookup"><span data-stu-id="117cf-124">-Path</span></span>
<span data-ttu-id="117cf-125">Der Pfad, der für die Integritätssonde verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="117cf-125">The path to use for the health probe.</span></span>
<span data-ttu-id="117cf-126">Der Standardwert ist /.</span><span class="sxs-lookup"><span data-stu-id="117cf-126">Default is /</span></span>

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

### <span data-ttu-id="117cf-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="117cf-127">-Protocol</span></span>
<span data-ttu-id="117cf-128">Für diese Sonde zu verwendende Protokollschema Standardwert ist HTTP</span><span class="sxs-lookup"><span data-stu-id="117cf-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="117cf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="117cf-129">CommonParameters</span></span>
<span data-ttu-id="117cf-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="117cf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="117cf-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="117cf-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="117cf-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="117cf-132">INPUTS</span></span>

### <span data-ttu-id="117cf-133">Keine</span><span class="sxs-lookup"><span data-stu-id="117cf-133">None</span></span>
## <span data-ttu-id="117cf-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="117cf-134">OUTPUTS</span></span>

### <span data-ttu-id="117cf-135">Microsoft.Azure.Commands.FrontDando.Models.PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="117cf-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="117cf-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="117cf-136">NOTES</span></span>

## <span data-ttu-id="117cf-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="117cf-137">RELATED LINKS</span></span>

<span data-ttu-id="117cf-138">[New-AzFrontD verankert](./New-AzFrontDoor.md) 
 [Set-AzFrontD verankert](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="117cf-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
