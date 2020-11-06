---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 57d7037f6deb669531bb03c3bf4f2e504586f832
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474754"
---
# <span data-ttu-id="01fba-101">New-AzsAddonPlanDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="01fba-101">New-AzsAddonPlanDefinitionObject</span></span>

## <span data-ttu-id="01fba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="01fba-102">SYNOPSIS</span></span>
<span data-ttu-id="01fba-103">Enthält den Namen des gewünschten Plans, mit dem ein Angebot verknüpft oder dessen Verknüpfung aufgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="01fba-103">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="01fba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="01fba-104">SYNTAX</span></span>

```
New-AzsAddonPlanDefinitionObject [[-PlanId] <String>] [[-MaxAcquisitionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="01fba-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="01fba-105">DESCRIPTION</span></span>
<span data-ttu-id="01fba-106">Enthält den Namen des gewünschten Plans, mit dem ein Angebot verknüpft oder dessen Verknüpfung aufgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="01fba-106">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="01fba-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="01fba-107">EXAMPLES</span></span>

### <span data-ttu-id="01fba-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="01fba-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsAddonPlanDefinitionObject -PlanId $planIdentifier -MaxAcquisitionCount 500
```

<span data-ttu-id="01fba-109">Erstellen Sie ein neues Plan Definitionsobjekt für den angegebenen Plan mit dem Erfassungs Grenzwert von 500.</span><span class="sxs-lookup"><span data-stu-id="01fba-109">Create a new plan definition object for the specified plan with the acquisition limit of 500.</span></span>

## <span data-ttu-id="01fba-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="01fba-110">PARAMETERS</span></span>

### <span data-ttu-id="01fba-111">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="01fba-111">-MaxAcquisitionCount</span></span>
<span data-ttu-id="01fba-112">Die maximale Anzahl von Instanzen, die von einem einzelnen Abonnement abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="01fba-112">Maximum number of instances that can be acquired by a single subscription.</span></span>
<span data-ttu-id="01fba-113">Wenn keine Angabe erfolgt, lautet der angenommene Wert 1.</span><span class="sxs-lookup"><span data-stu-id="01fba-113">If not specified, the assumed value is 1.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01fba-114">-Plan-Nr.</span><span class="sxs-lookup"><span data-stu-id="01fba-114">-PlanId</span></span>
<span data-ttu-id="01fba-115">Plan-ID.</span><span class="sxs-lookup"><span data-stu-id="01fba-115">Plan identifier.</span></span>

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

### <span data-ttu-id="01fba-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01fba-116">CommonParameters</span></span>
<span data-ttu-id="01fba-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01fba-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01fba-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01fba-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01fba-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="01fba-119">INPUTS</span></span>

## <span data-ttu-id="01fba-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="01fba-120">OUTPUTS</span></span>

## <span data-ttu-id="01fba-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="01fba-121">NOTES</span></span>

## <span data-ttu-id="01fba-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="01fba-122">RELATED LINKS</span></span>

