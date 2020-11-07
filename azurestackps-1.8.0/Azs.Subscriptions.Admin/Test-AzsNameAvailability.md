---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4bd00dc1709a3060da9777ab4755ae1c6a28ec4
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827455"
---
# <span data-ttu-id="40fbd-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="40fbd-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="40fbd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="40fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="40fbd-103">Gibt den avaialbility des angegebenen Abonnements Ressourcentyps und-Namens zurück.</span><span class="sxs-lookup"><span data-stu-id="40fbd-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="40fbd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="40fbd-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="40fbd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40fbd-105">DESCRIPTION</span></span>
<span data-ttu-id="40fbd-106">Gibt den avaialbility des angegebenen Abonnements Ressourcentyps und-Namens zurück.</span><span class="sxs-lookup"><span data-stu-id="40fbd-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="40fbd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="40fbd-107">EXAMPLES</span></span>

### <span data-ttu-id="40fbd-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="40fbd-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="40fbd-109">Gibt den avaialbility des angegebenen Abonnements Ressourcentyps und-Namens zurück.</span><span class="sxs-lookup"><span data-stu-id="40fbd-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="40fbd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="40fbd-110">PARAMETERS</span></span>

### <span data-ttu-id="40fbd-111">-Name</span><span class="sxs-lookup"><span data-stu-id="40fbd-111">-Name</span></span>
<span data-ttu-id="40fbd-112">Der zu überprüfende Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="40fbd-112">The resource name to verify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40fbd-113">-</span><span class="sxs-lookup"><span data-stu-id="40fbd-113">-ResourceType</span></span>
<span data-ttu-id="40fbd-114">Der zu überprüfende Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="40fbd-114">The resource type to verify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40fbd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40fbd-115">CommonParameters</span></span>
<span data-ttu-id="40fbd-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40fbd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40fbd-117">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40fbd-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40fbd-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="40fbd-118">INPUTS</span></span>

## <span data-ttu-id="40fbd-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="40fbd-119">OUTPUTS</span></span>

### <span data-ttu-id="40fbd-120">Microsoft. AzureStack. Management. Subscriptions. admin. Models. CheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="40fbd-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="40fbd-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="40fbd-121">NOTES</span></span>

## <span data-ttu-id="40fbd-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="40fbd-122">RELATED LINKS</span></span>

