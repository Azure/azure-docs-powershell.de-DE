---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: e9195a60b06f206a5b3133834f19cfdab68db31b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175436"
---
# <span data-ttu-id="420e4-101">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="420e4-101">New-AzFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="420e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="420e4-102">SYNOPSIS</span></span>
<span data-ttu-id="420e4-103">Erstellen eines "PSLoadBalancingSetting"-Objekts für die Erstellung von "Front Door"</span><span class="sxs-lookup"><span data-stu-id="420e4-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="420e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="420e4-104">SYNTAX</span></span>

```
New-AzFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="420e4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="420e4-105">DESCRIPTION</span></span>
<span data-ttu-id="420e4-106">Erstellen eines "PSLoadBalancingSetting"-Objekts für die Erstellung von "Front Door"</span><span class="sxs-lookup"><span data-stu-id="420e4-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="420e4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="420e4-107">EXAMPLES</span></span>

### <span data-ttu-id="420e4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="420e4-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorLoadBalancingSettingObject -Name "loadbalancingsetting1"


SampleSize                    : 4
AdditionalLatencyMilliseconds : 0
SuccessfulSamplesRequired     : 2
ResourceState                 :
Id                            :
Name                          : loadbalancingsetting1
Type                          :
```

<span data-ttu-id="420e4-109">Erstellen eines "PSLoadBalancingSetting"-Objekts für die Erstellung von "Front Door"</span><span class="sxs-lookup"><span data-stu-id="420e4-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="420e4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="420e4-110">PARAMETERS</span></span>

### <span data-ttu-id="420e4-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="420e4-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="420e4-112">Die zusätzliche Latenz in Millisekunden, über die Sonden in den Bucket mit der niedrigsten Latenz fallen.</span><span class="sxs-lookup"><span data-stu-id="420e4-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="420e4-113">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="420e4-113">Default value is 0</span></span>

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

### <span data-ttu-id="420e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="420e4-114">-DefaultProfile</span></span>
<span data-ttu-id="420e4-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="420e4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="420e4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="420e4-116">-Name</span></span>
<span data-ttu-id="420e4-117">name der Integritätsintepunkteinstellung.</span><span class="sxs-lookup"><span data-stu-id="420e4-117">health probe setting name.</span></span>

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

### <span data-ttu-id="420e4-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="420e4-118">-SampleSize</span></span>
<span data-ttu-id="420e4-119">Die Anzahl von Beispielen, die bei Entscheidungen zum Lastenausgleich zu berücksichtigen sind.</span><span class="sxs-lookup"><span data-stu-id="420e4-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="420e4-120">Der Standardwert ist 4.</span><span class="sxs-lookup"><span data-stu-id="420e4-120">Default value is 4</span></span>

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

### <span data-ttu-id="420e4-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="420e4-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="420e4-122">Die Anzahl von Beispielen innerhalb des Beispielzeitraums, für die der Standardwert erfolgreich sein muss, beträgt 2.</span><span class="sxs-lookup"><span data-stu-id="420e4-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

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

### <span data-ttu-id="420e4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="420e4-123">CommonParameters</span></span>
<span data-ttu-id="420e4-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="420e4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="420e4-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="420e4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="420e4-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="420e4-126">INPUTS</span></span>

### <span data-ttu-id="420e4-127">Keine</span><span class="sxs-lookup"><span data-stu-id="420e4-127">None</span></span>

## <span data-ttu-id="420e4-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="420e4-128">OUTPUTS</span></span>

### <span data-ttu-id="420e4-129">Microsoft.Azure.Commands.FrontD selbst.Models.PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="420e4-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="420e4-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="420e4-130">NOTES</span></span>

## <span data-ttu-id="420e4-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="420e4-131">RELATED LINKS</span></span>

<span data-ttu-id="420e4-132">[New-AzFrontD verankert](./New-AzFrontDoor.md) 
 [Set-AzFrontD verankert](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="420e4-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
