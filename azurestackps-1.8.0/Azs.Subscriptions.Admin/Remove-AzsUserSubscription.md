---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25411a71a6d8233be55ab25ac99487da0b44bd0b
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827472"
---
# <span data-ttu-id="df7e7-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="df7e7-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="df7e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="df7e7-102">SYNOPSIS</span></span>
<span data-ttu-id="df7e7-103">Entfernt das angegebene Mandanten Abonnement.</span><span class="sxs-lookup"><span data-stu-id="df7e7-103">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="df7e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="df7e7-104">SYNTAX</span></span>

```
Remove-AzsUserSubscription [-SubscriptionId] <Guid> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df7e7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df7e7-105">DESCRIPTION</span></span>
<span data-ttu-id="df7e7-106">Entfernt das angegebene Mandanten Abonnement.</span><span class="sxs-lookup"><span data-stu-id="df7e7-106">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="df7e7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df7e7-107">EXAMPLES</span></span>

### <span data-ttu-id="df7e7-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="df7e7-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="df7e7-109">Entfernen des angegebenen Mandanten Abonnements</span><span class="sxs-lookup"><span data-stu-id="df7e7-109">Remove the specified tenant subscription.</span></span>

## <span data-ttu-id="df7e7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="df7e7-110">PARAMETERS</span></span>

### <span data-ttu-id="df7e7-111">-Force</span><span class="sxs-lookup"><span data-stu-id="df7e7-111">-Force</span></span>
<span data-ttu-id="df7e7-112">Kennzeichnen, um das Element ohne Bestätigung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="df7e7-112">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="df7e7-113">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="df7e7-113">-SubscriptionId</span></span>
<span data-ttu-id="df7e7-114">Parameter für die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="df7e7-114">Subscription Id parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df7e7-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="df7e7-115">-Confirm</span></span>
<span data-ttu-id="df7e7-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="df7e7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df7e7-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df7e7-117">-WhatIf</span></span>
<span data-ttu-id="df7e7-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="df7e7-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df7e7-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="df7e7-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df7e7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df7e7-120">CommonParameters</span></span>
<span data-ttu-id="df7e7-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df7e7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df7e7-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df7e7-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df7e7-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="df7e7-123">INPUTS</span></span>

## <span data-ttu-id="df7e7-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="df7e7-124">OUTPUTS</span></span>

## <span data-ttu-id="df7e7-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="df7e7-125">NOTES</span></span>

## <span data-ttu-id="df7e7-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="df7e7-126">RELATED LINKS</span></span>

