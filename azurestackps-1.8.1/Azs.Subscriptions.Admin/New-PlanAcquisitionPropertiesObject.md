---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 199d9fb2ce88c149965d488b55bce669f364a615
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828132"
---
# <span data-ttu-id="55ece-101">New-PlanAcquisitionPropertiesObject</span><span class="sxs-lookup"><span data-stu-id="55ece-101">New-PlanAcquisitionPropertiesObject</span></span>

## <span data-ttu-id="55ece-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="55ece-102">SYNOPSIS</span></span>
<span data-ttu-id="55ece-103">Stellt den Erwerb eines Add-on-Plans für ein Abonnement dar.</span><span class="sxs-lookup"><span data-stu-id="55ece-103">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="55ece-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="55ece-104">SYNTAX</span></span>

```
New-PlanAcquisitionPropertiesObject [[-ProvisioningState] <String>] [[-AcquisitionTime] <String>]
 [[-Id] <String>] [[-PlanId] <String>] [[-AcquisitionId] <String>] [[-ExternalReferenceId] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="55ece-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55ece-105">DESCRIPTION</span></span>
<span data-ttu-id="55ece-106">Stellt den Erwerb eines Add-on-Plans für ein Abonnement dar.</span><span class="sxs-lookup"><span data-stu-id="55ece-106">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="55ece-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55ece-107">EXAMPLES</span></span>

### <span data-ttu-id="55ece-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="55ece-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="55ece-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="55ece-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="55ece-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="55ece-110">PARAMETERS</span></span>

### <span data-ttu-id="55ece-111">-Akquisitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="55ece-111">-AcquisitionId</span></span>
<span data-ttu-id="55ece-112">Akquisitions-ID.</span><span class="sxs-lookup"><span data-stu-id="55ece-112">Acquisition identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ece-113">-Erwerbszeitpunkt</span><span class="sxs-lookup"><span data-stu-id="55ece-113">-AcquisitionTime</span></span>
<span data-ttu-id="55ece-114">Akquisitions Zeit.</span><span class="sxs-lookup"><span data-stu-id="55ece-114">Acquisition time.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ece-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="55ece-115">-ExternalReferenceId</span></span>
<span data-ttu-id="55ece-116">Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="55ece-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ece-117">-ID</span><span class="sxs-lookup"><span data-stu-id="55ece-117">-Id</span></span>
<span data-ttu-id="55ece-118">Bezeichner im Mandanten Abonnement Kontext.</span><span class="sxs-lookup"><span data-stu-id="55ece-118">Identifier in the tenant subscription context.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ece-119">-Plan-Nr.</span><span class="sxs-lookup"><span data-stu-id="55ece-119">-PlanId</span></span>
<span data-ttu-id="55ece-120">Plan-ID im Kontext des Mandanten Abonnements</span><span class="sxs-lookup"><span data-stu-id="55ece-120">Plan identifier in the tenant subscription context.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ece-121">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="55ece-121">-ProvisioningState</span></span>
<span data-ttu-id="55ece-122">Der Zustand der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="55ece-122">State of the provisioning.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ece-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55ece-123">CommonParameters</span></span>
<span data-ttu-id="55ece-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55ece-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55ece-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55ece-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55ece-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="55ece-126">INPUTS</span></span>

## <span data-ttu-id="55ece-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="55ece-127">OUTPUTS</span></span>

## <span data-ttu-id="55ece-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="55ece-128">NOTES</span></span>

## <span data-ttu-id="55ece-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="55ece-129">RELATED LINKS</span></span>

