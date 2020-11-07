---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2ac9f85896c1ae0a8eb7e060600ba5b4eb0e792
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661959"
---
# <span data-ttu-id="5da7e-101">Remove-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="5da7e-101">Remove-AzsOffer</span></span>

## <span data-ttu-id="5da7e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5da7e-102">SYNOPSIS</span></span>
<span data-ttu-id="5da7e-103">Löschen des angegebenen Angebots</span><span class="sxs-lookup"><span data-stu-id="5da7e-103">Delete the specified offer.</span></span>

## <span data-ttu-id="5da7e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5da7e-104">SYNTAX</span></span>

### <span data-ttu-id="5da7e-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="5da7e-105">Delete (Default)</span></span>
```
Remove-AzsOffer -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5da7e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5da7e-106">ResourceId</span></span>
```
Remove-AzsOffer -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5da7e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5da7e-107">DESCRIPTION</span></span>
<span data-ttu-id="5da7e-108">Löschen des angegebenen Angebots</span><span class="sxs-lookup"><span data-stu-id="5da7e-108">Delete the specified offer.</span></span>

## <span data-ttu-id="5da7e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5da7e-109">EXAMPLES</span></span>

### <span data-ttu-id="5da7e-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5da7e-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOffer -Name offername1 -ResourceGroupName rg1
```

<span data-ttu-id="5da7e-111">Löschen des angegebenen Angebots</span><span class="sxs-lookup"><span data-stu-id="5da7e-111">Delete the specified offer.</span></span>

## <span data-ttu-id="5da7e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5da7e-112">PARAMETERS</span></span>

### <span data-ttu-id="5da7e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5da7e-113">-Force</span></span>
<span data-ttu-id="5da7e-114">Kennzeichnen, um das Element ohne Bestätigung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="5da7e-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="5da7e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5da7e-115">-Name</span></span>
<span data-ttu-id="5da7e-116">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="5da7e-116">Name of an offer.</span></span>

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

### <span data-ttu-id="5da7e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5da7e-117">-ResourceGroupName</span></span>
<span data-ttu-id="5da7e-118">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="5da7e-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="5da7e-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5da7e-119">-ResourceId</span></span>
<span data-ttu-id="5da7e-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="5da7e-120">The resource id.</span></span>

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

### <span data-ttu-id="5da7e-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5da7e-121">-Confirm</span></span>
<span data-ttu-id="5da7e-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5da7e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5da7e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5da7e-123">-WhatIf</span></span>
<span data-ttu-id="5da7e-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5da7e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5da7e-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5da7e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5da7e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5da7e-126">CommonParameters</span></span>
<span data-ttu-id="5da7e-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5da7e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5da7e-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5da7e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5da7e-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5da7e-129">INPUTS</span></span>

## <span data-ttu-id="5da7e-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5da7e-130">OUTPUTS</span></span>

## <span data-ttu-id="5da7e-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="5da7e-131">NOTES</span></span>

## <span data-ttu-id="5da7e-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5da7e-132">RELATED LINKS</span></span>

