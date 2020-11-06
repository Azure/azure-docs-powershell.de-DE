---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 267a5bf4c3f864c987c0bc747eefce9dd3ffe6b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475090"
---
# <span data-ttu-id="9d5f0-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="9d5f0-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="9d5f0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d5f0-102">SYNOPSIS</span></span>
<span data-ttu-id="9d5f0-103">Gibt den avaialbility des angegebenen Abonnements Ressourcentyps und-Namens zurück.</span><span class="sxs-lookup"><span data-stu-id="9d5f0-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="9d5f0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d5f0-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="9d5f0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d5f0-105">DESCRIPTION</span></span>
<span data-ttu-id="9d5f0-106">Gibt den avaialbility des angegebenen Abonnements Ressourcentyps und-Namens zurück.</span><span class="sxs-lookup"><span data-stu-id="9d5f0-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="9d5f0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d5f0-107">EXAMPLES</span></span>

### <span data-ttu-id="9d5f0-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9d5f0-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="9d5f0-109">Gibt den avaialbility des angegebenen Abonnements Ressourcentyps und-Namens zurück.</span><span class="sxs-lookup"><span data-stu-id="9d5f0-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="9d5f0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d5f0-110">PARAMETERS</span></span>

### <span data-ttu-id="9d5f0-111">-Name</span><span class="sxs-lookup"><span data-stu-id="9d5f0-111">-Name</span></span>
<span data-ttu-id="9d5f0-112">Der zu überprüfende Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="9d5f0-112">The resource name to verify.</span></span>

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

### <span data-ttu-id="9d5f0-113">-</span><span class="sxs-lookup"><span data-stu-id="9d5f0-113">-ResourceType</span></span>
<span data-ttu-id="9d5f0-114">Der zu überprüfende Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="9d5f0-114">The resource type to verify.</span></span>

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

### <span data-ttu-id="9d5f0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d5f0-115">CommonParameters</span></span>
<span data-ttu-id="9d5f0-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d5f0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d5f0-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d5f0-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d5f0-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d5f0-118">INPUTS</span></span>

## <span data-ttu-id="9d5f0-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d5f0-119">OUTPUTS</span></span>

### <span data-ttu-id="9d5f0-120">Microsoft. AzureStack. Management. Subscriptions. admin. Models. CheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="9d5f0-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="9d5f0-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d5f0-121">NOTES</span></span>

## <span data-ttu-id="9d5f0-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d5f0-122">RELATED LINKS</span></span>

