---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: fdceee36319d1c9ea950dbf5573b4ba0e3c614ee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475521"
---
# <span data-ttu-id="b6258-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="b6258-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="b6258-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b6258-102">SYNOPSIS</span></span>
<span data-ttu-id="b6258-103">Löschen Sie das angegebene-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b6258-103">Delete the specifed subscription.</span></span>

## <span data-ttu-id="b6258-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6258-104">SYNTAX</span></span>

```
Remove-AzsSubscription [-SubscriptionId] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6258-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6258-105">DESCRIPTION</span></span>
<span data-ttu-id="b6258-106">Löschen Sie das angegebene-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b6258-106">Delete the specifed subscription.</span></span>

## <span data-ttu-id="b6258-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6258-107">EXAMPLES</span></span>

### <span data-ttu-id="b6258-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b6258-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9
```

<span data-ttu-id="b6258-109">Löschen Sie das angegebene-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b6258-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="b6258-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6258-110">PARAMETERS</span></span>

### <span data-ttu-id="b6258-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b6258-111">-Force</span></span>
<span data-ttu-id="b6258-112">Entfernen eines Abonnements ohne Aufforderung</span><span class="sxs-lookup"><span data-stu-id="b6258-112">Remove subscription without prompting</span></span>

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

### <span data-ttu-id="b6258-113">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="b6258-113">-SubscriptionId</span></span>
<span data-ttu-id="b6258-114">Die ID des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="b6258-114">Id of the subscription.</span></span>

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

### <span data-ttu-id="b6258-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b6258-115">-Confirm</span></span>
<span data-ttu-id="b6258-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b6258-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6258-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6258-117">-WhatIf</span></span>
<span data-ttu-id="b6258-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b6258-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6258-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b6258-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6258-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6258-120">CommonParameters</span></span>
<span data-ttu-id="b6258-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6258-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6258-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6258-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6258-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b6258-123">INPUTS</span></span>

## <span data-ttu-id="b6258-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b6258-124">OUTPUTS</span></span>

## <span data-ttu-id="b6258-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="b6258-125">NOTES</span></span>

## <span data-ttu-id="b6258-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b6258-126">RELATED LINKS</span></span>

