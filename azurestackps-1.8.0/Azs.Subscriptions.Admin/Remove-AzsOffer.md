---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 74772615551979a9ab0cdba3603305489698e212
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827479"
---
# <span data-ttu-id="59849-101">Remove-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="59849-101">Remove-AzsOffer</span></span>

## <span data-ttu-id="59849-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59849-102">SYNOPSIS</span></span>
<span data-ttu-id="59849-103">Löschen des angegebenen Angebots</span><span class="sxs-lookup"><span data-stu-id="59849-103">Delete the specified offer.</span></span>

## <span data-ttu-id="59849-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59849-104">SYNTAX</span></span>

### <span data-ttu-id="59849-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="59849-105">Delete (Default)</span></span>
```
Remove-AzsOffer -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59849-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="59849-106">ResourceId</span></span>
```
Remove-AzsOffer -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59849-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59849-107">DESCRIPTION</span></span>
<span data-ttu-id="59849-108">Löschen des angegebenen Angebots</span><span class="sxs-lookup"><span data-stu-id="59849-108">Delete the specified offer.</span></span>

## <span data-ttu-id="59849-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59849-109">EXAMPLES</span></span>

### <span data-ttu-id="59849-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="59849-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOffer -Name offername1 -ResourceGroupName rg1
```

<span data-ttu-id="59849-111">Löschen des angegebenen Angebots</span><span class="sxs-lookup"><span data-stu-id="59849-111">Delete the specified offer.</span></span>

## <span data-ttu-id="59849-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="59849-112">PARAMETERS</span></span>

### <span data-ttu-id="59849-113">-Force</span><span class="sxs-lookup"><span data-stu-id="59849-113">-Force</span></span>
<span data-ttu-id="59849-114">Kennzeichnen, um das Element ohne Bestätigung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="59849-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="59849-115">-Name</span><span class="sxs-lookup"><span data-stu-id="59849-115">-Name</span></span>
<span data-ttu-id="59849-116">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="59849-116">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59849-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59849-117">-ResourceGroupName</span></span>
<span data-ttu-id="59849-118">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="59849-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59849-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="59849-119">-ResourceId</span></span>
<span data-ttu-id="59849-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="59849-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59849-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="59849-121">-Confirm</span></span>
<span data-ttu-id="59849-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="59849-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59849-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59849-123">-WhatIf</span></span>
<span data-ttu-id="59849-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59849-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59849-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59849-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59849-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59849-126">CommonParameters</span></span>
<span data-ttu-id="59849-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59849-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59849-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59849-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59849-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59849-129">INPUTS</span></span>

## <span data-ttu-id="59849-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59849-130">OUTPUTS</span></span>

## <span data-ttu-id="59849-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="59849-131">NOTES</span></span>

## <span data-ttu-id="59849-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59849-132">RELATED LINKS</span></span>

