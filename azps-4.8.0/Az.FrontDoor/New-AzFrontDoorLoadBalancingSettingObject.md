---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: e9195a60b06f206a5b3133834f19cfdab68db31b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008480"
---
# <span data-ttu-id="bf301-101">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="bf301-101">New-AzFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="bf301-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf301-102">SYNOPSIS</span></span>
<span data-ttu-id="bf301-103">Erstellen eines PSLoadBalancingSetting-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="bf301-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="bf301-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf301-104">SYNTAX</span></span>

```
New-AzFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf301-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf301-105">DESCRIPTION</span></span>
<span data-ttu-id="bf301-106">Erstellen eines PSLoadBalancingSetting-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="bf301-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="bf301-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf301-107">EXAMPLES</span></span>

### <span data-ttu-id="bf301-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bf301-108">Example 1</span></span>
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

<span data-ttu-id="bf301-109">Erstellen eines PSLoadBalancingSetting-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="bf301-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="bf301-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf301-110">PARAMETERS</span></span>

### <span data-ttu-id="bf301-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="bf301-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="bf301-112">Die zusätzliche Wartezeit in Millisekunden für Prüfpunkte, die in den niedrigsten Latenz Bucket fallen.</span><span class="sxs-lookup"><span data-stu-id="bf301-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="bf301-113">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="bf301-113">Default value is 0</span></span>

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

### <span data-ttu-id="bf301-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf301-114">-DefaultProfile</span></span>
<span data-ttu-id="bf301-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bf301-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf301-116">-Name</span><span class="sxs-lookup"><span data-stu-id="bf301-116">-Name</span></span>
<span data-ttu-id="bf301-117">Name für Integritäts Prüf Punkt Einstellung.</span><span class="sxs-lookup"><span data-stu-id="bf301-117">health probe setting name.</span></span>

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

### <span data-ttu-id="bf301-118">-Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf301-118">-SampleSize</span></span>
<span data-ttu-id="bf301-119">Die Anzahl der Beispiele, die für Lastenausgleichs Entscheidungen berücksichtigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bf301-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="bf301-120">Standardwert ist 4</span><span class="sxs-lookup"><span data-stu-id="bf301-120">Default value is 4</span></span>

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

### <span data-ttu-id="bf301-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="bf301-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="bf301-122">Die Anzahl der Stichproben innerhalb des Beispielzeitraums, die erfolgreich sein müssen, ist der Standardwert 2.</span><span class="sxs-lookup"><span data-stu-id="bf301-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

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

### <span data-ttu-id="bf301-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf301-123">CommonParameters</span></span>
<span data-ttu-id="bf301-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf301-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf301-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf301-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf301-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf301-126">INPUTS</span></span>

### <span data-ttu-id="bf301-127">Keine</span><span class="sxs-lookup"><span data-stu-id="bf301-127">None</span></span>

## <span data-ttu-id="bf301-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf301-128">OUTPUTS</span></span>

### <span data-ttu-id="bf301-129">Microsoft. Azure. Commands. Haustür. Models. PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="bf301-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="bf301-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf301-130">NOTES</span></span>

## <span data-ttu-id="bf301-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf301-131">RELATED LINKS</span></span>

<span data-ttu-id="bf301-132">[Neu – AzFrontDoor](./New-AzFrontDoor.md) 
 [Satz-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="bf301-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
