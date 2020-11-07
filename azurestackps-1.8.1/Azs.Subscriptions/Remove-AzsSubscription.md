---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e6588eed555062aaf6dbb4075dffd9506c05503
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840647"
---
# <span data-ttu-id="9fd7c-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="9fd7c-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="9fd7c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9fd7c-102">SYNOPSIS</span></span>
<span data-ttu-id="9fd7c-103">Löschen Sie das angegebene-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9fd7c-103">Delete the specifed subscription.</span></span>

## <span data-ttu-id="9fd7c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fd7c-104">SYNTAX</span></span>

```
Remove-AzsSubscription [-SubscriptionId] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fd7c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9fd7c-105">DESCRIPTION</span></span>
<span data-ttu-id="9fd7c-106">Löschen Sie das angegebene-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9fd7c-106">Delete the specifed subscription.</span></span>

## <span data-ttu-id="9fd7c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9fd7c-107">EXAMPLES</span></span>

### <span data-ttu-id="9fd7c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9fd7c-108">EXAMPLE 1</span></span>
```
Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9
```

<span data-ttu-id="9fd7c-109">Löschen Sie das angegebene-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9fd7c-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="9fd7c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fd7c-110">PARAMETERS</span></span>

### <span data-ttu-id="9fd7c-111">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="9fd7c-111">-SubscriptionId</span></span>
<span data-ttu-id="9fd7c-112">Die ID des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="9fd7c-112">Id of the subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fd7c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9fd7c-113">-Force</span></span>
<span data-ttu-id="9fd7c-114">Entfernen eines Abonnements ohne Aufforderung</span><span class="sxs-lookup"><span data-stu-id="9fd7c-114">Remove subscription without prompting</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fd7c-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fd7c-115">-WhatIf</span></span>
<span data-ttu-id="9fd7c-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9fd7c-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fd7c-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9fd7c-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fd7c-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9fd7c-118">-Confirm</span></span>
<span data-ttu-id="9fd7c-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9fd7c-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fd7c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fd7c-120">CommonParameters</span></span>
<span data-ttu-id="9fd7c-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fd7c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fd7c-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fd7c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fd7c-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9fd7c-123">INPUTS</span></span>

## <span data-ttu-id="9fd7c-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9fd7c-124">OUTPUTS</span></span>

## <span data-ttu-id="9fd7c-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="9fd7c-125">NOTES</span></span>

## <span data-ttu-id="9fd7c-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9fd7c-126">RELATED LINKS</span></span>
