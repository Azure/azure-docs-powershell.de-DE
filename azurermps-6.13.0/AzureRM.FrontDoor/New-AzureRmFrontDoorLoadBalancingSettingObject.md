---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: de13a33aeaf60dbd83fcacebb8380bee27c18c46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480329"
---
# <span data-ttu-id="cd580-101">New-AzureRmFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="cd580-101">New-AzureRmFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="cd580-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cd580-102">SYNOPSIS</span></span>
<span data-ttu-id="cd580-103">Erstellen eines PSLoadBalancingSetting-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="cd580-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd580-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd580-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd580-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd580-105">DESCRIPTION</span></span>
<span data-ttu-id="cd580-106">Erstellen eines PSLoadBalancingSetting-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="cd580-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="cd580-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd580-107">EXAMPLES</span></span>

### <span data-ttu-id="cd580-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cd580-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorLoadBalancingSettingObject -Name "loadbalancingsetting1"


SampleSize                    : 4
AdditionalLatencyMilliseconds : 0
SuccessfulSamplesRequired     : 2
ResourceState                 :
Id                            :
Name                          : loadbalancingsetting1
Type                          :
```

<span data-ttu-id="cd580-109">Erstellen eines PSLoadBalancingSetting-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="cd580-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="cd580-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd580-110">PARAMETERS</span></span>

### <span data-ttu-id="cd580-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="cd580-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="cd580-112">Die zusätzliche Wartezeit in Millisekunden für Prüfpunkte, die in den niedrigsten Latenz Bucket fallen.</span><span class="sxs-lookup"><span data-stu-id="cd580-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="cd580-113">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="cd580-113">Default value is 0</span></span>

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

### <span data-ttu-id="cd580-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd580-114">-DefaultProfile</span></span>
<span data-ttu-id="cd580-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cd580-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd580-116">-Name</span><span class="sxs-lookup"><span data-stu-id="cd580-116">-Name</span></span>
<span data-ttu-id="cd580-117">Name für Integritäts Prüf Punkt Einstellung.</span><span class="sxs-lookup"><span data-stu-id="cd580-117">health probe setting name.</span></span>

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

### <span data-ttu-id="cd580-118">-Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd580-118">-SampleSize</span></span>
<span data-ttu-id="cd580-119">Die Anzahl der Beispiele, die für Lastenausgleichs Entscheidungen berücksichtigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cd580-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="cd580-120">Standardwert ist 4</span><span class="sxs-lookup"><span data-stu-id="cd580-120">Default value is 4</span></span>

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

### <span data-ttu-id="cd580-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="cd580-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="cd580-122">Die Anzahl der Stichproben innerhalb des Beispielzeitraums, die erfolgreich sein müssen, ist der Standardwert 2.</span><span class="sxs-lookup"><span data-stu-id="cd580-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

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

### <span data-ttu-id="cd580-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd580-123">CommonParameters</span></span>
<span data-ttu-id="cd580-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd580-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd580-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd580-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd580-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cd580-126">INPUTS</span></span>

### <span data-ttu-id="cd580-127">Keine</span><span class="sxs-lookup"><span data-stu-id="cd580-127">None</span></span>

## <span data-ttu-id="cd580-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cd580-128">OUTPUTS</span></span>

### <span data-ttu-id="cd580-129">Microsoft. Azure. Commands. Haustür. Models. PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="cd580-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="cd580-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="cd580-130">NOTES</span></span>

## <span data-ttu-id="cd580-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cd580-131">RELATED LINKS</span></span>

<span data-ttu-id="cd580-132">[Neu – AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Satz-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="cd580-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
