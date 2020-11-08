---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75010b9591b4211f32c5665aa969bae28d69aaea
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006891"
---
# <span data-ttu-id="821d7-101">Remove-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="821d7-101">Remove-AzsPlan</span></span>

## <span data-ttu-id="821d7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="821d7-102">SYNOPSIS</span></span>
<span data-ttu-id="821d7-103">Entfernt den angegebenen Plan</span><span class="sxs-lookup"><span data-stu-id="821d7-103">Removes the specified plan</span></span>

## <span data-ttu-id="821d7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="821d7-104">SYNTAX</span></span>

### <span data-ttu-id="821d7-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="821d7-105">Delete (Default)</span></span>
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="821d7-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="821d7-106">ResourceId</span></span>
```
Remove-AzsPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="821d7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="821d7-107">DESCRIPTION</span></span>
<span data-ttu-id="821d7-108">Entfernt den angegebenen Plan</span><span class="sxs-lookup"><span data-stu-id="821d7-108">Removes the specified plan</span></span>

## <span data-ttu-id="821d7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="821d7-109">EXAMPLES</span></span>

### <span data-ttu-id="821d7-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="821d7-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlan -Name plan1 -ResourceGroupName "rg1"
```

<span data-ttu-id="821d7-111">Entfernt den angegebenen Plan</span><span class="sxs-lookup"><span data-stu-id="821d7-111">Removes the specified plan</span></span>

## <span data-ttu-id="821d7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="821d7-112">PARAMETERS</span></span>

### <span data-ttu-id="821d7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="821d7-113">-Force</span></span>
<span data-ttu-id="821d7-114">Kennzeichnen, um das Element ohne Bestätigung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="821d7-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="821d7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="821d7-115">-Name</span></span>
<span data-ttu-id="821d7-116">Der Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="821d7-116">Name of the plan.</span></span>

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

### <span data-ttu-id="821d7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="821d7-117">-ResourceGroupName</span></span>
<span data-ttu-id="821d7-118">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="821d7-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="821d7-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="821d7-119">-ResourceId</span></span>
<span data-ttu-id="821d7-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="821d7-120">The resource id.</span></span>

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

### <span data-ttu-id="821d7-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="821d7-121">-Confirm</span></span>
<span data-ttu-id="821d7-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="821d7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="821d7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="821d7-123">-WhatIf</span></span>
<span data-ttu-id="821d7-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="821d7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="821d7-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="821d7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="821d7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="821d7-126">CommonParameters</span></span>
<span data-ttu-id="821d7-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="821d7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="821d7-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="821d7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="821d7-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="821d7-129">INPUTS</span></span>

## <span data-ttu-id="821d7-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="821d7-130">OUTPUTS</span></span>

## <span data-ttu-id="821d7-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="821d7-131">NOTES</span></span>

## <span data-ttu-id="821d7-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="821d7-132">RELATED LINKS</span></span>

