---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 74772615551979a9ab0cdba3603305489698e212
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007358"
---
# <span data-ttu-id="262c5-101">Remove-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="262c5-101">Remove-AzsOffer</span></span>

## <span data-ttu-id="262c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="262c5-102">SYNOPSIS</span></span>
<span data-ttu-id="262c5-103">Löschen des angegebenen Angebots</span><span class="sxs-lookup"><span data-stu-id="262c5-103">Delete the specified offer.</span></span>

## <span data-ttu-id="262c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="262c5-104">SYNTAX</span></span>

### <span data-ttu-id="262c5-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="262c5-105">Delete (Default)</span></span>
```
Remove-AzsOffer -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="262c5-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="262c5-106">ResourceId</span></span>
```
Remove-AzsOffer -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="262c5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="262c5-107">DESCRIPTION</span></span>
<span data-ttu-id="262c5-108">Löschen des angegebenen Angebots</span><span class="sxs-lookup"><span data-stu-id="262c5-108">Delete the specified offer.</span></span>

## <span data-ttu-id="262c5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="262c5-109">EXAMPLES</span></span>

### <span data-ttu-id="262c5-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="262c5-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOffer -Name offername1 -ResourceGroupName rg1
```

<span data-ttu-id="262c5-111">Löschen des angegebenen Angebots</span><span class="sxs-lookup"><span data-stu-id="262c5-111">Delete the specified offer.</span></span>

## <span data-ttu-id="262c5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="262c5-112">PARAMETERS</span></span>

### <span data-ttu-id="262c5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="262c5-113">-Force</span></span>
<span data-ttu-id="262c5-114">Kennzeichnen, um das Element ohne Bestätigung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="262c5-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="262c5-115">-Name</span><span class="sxs-lookup"><span data-stu-id="262c5-115">-Name</span></span>
<span data-ttu-id="262c5-116">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="262c5-116">Name of an offer.</span></span>

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

### <span data-ttu-id="262c5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="262c5-117">-ResourceGroupName</span></span>
<span data-ttu-id="262c5-118">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="262c5-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="262c5-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="262c5-119">-ResourceId</span></span>
<span data-ttu-id="262c5-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="262c5-120">The resource id.</span></span>

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

### <span data-ttu-id="262c5-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="262c5-121">-Confirm</span></span>
<span data-ttu-id="262c5-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="262c5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="262c5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="262c5-123">-WhatIf</span></span>
<span data-ttu-id="262c5-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="262c5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="262c5-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="262c5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="262c5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="262c5-126">CommonParameters</span></span>
<span data-ttu-id="262c5-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="262c5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="262c5-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="262c5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="262c5-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="262c5-129">INPUTS</span></span>

## <span data-ttu-id="262c5-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="262c5-130">OUTPUTS</span></span>

## <span data-ttu-id="262c5-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="262c5-131">NOTES</span></span>

## <span data-ttu-id="262c5-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="262c5-132">RELATED LINKS</span></span>

