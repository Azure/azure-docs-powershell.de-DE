---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: aa4bd73f9300daf8ca17e3a11d884e06e9852234
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475598"
---
# <span data-ttu-id="ea1d1-101">Remove-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="ea1d1-101">Remove-AzsPlan</span></span>

## <span data-ttu-id="ea1d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ea1d1-102">SYNOPSIS</span></span>
<span data-ttu-id="ea1d1-103">Entfernt den angegebenen Plan</span><span class="sxs-lookup"><span data-stu-id="ea1d1-103">Removes the specified plan</span></span>

## <span data-ttu-id="ea1d1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea1d1-104">SYNTAX</span></span>

### <span data-ttu-id="ea1d1-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="ea1d1-105">Delete (Default)</span></span>
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea1d1-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea1d1-106">ResourceId</span></span>
```
Remove-AzsPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea1d1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea1d1-107">DESCRIPTION</span></span>
<span data-ttu-id="ea1d1-108">Entfernt den angegebenen Plan</span><span class="sxs-lookup"><span data-stu-id="ea1d1-108">Removes the specified plan</span></span>

## <span data-ttu-id="ea1d1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea1d1-109">EXAMPLES</span></span>

### <span data-ttu-id="ea1d1-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ea1d1-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlan -Name plan1 -ResourceGroupName "rg1"
```

<span data-ttu-id="ea1d1-111">Entfernt den angegebenen Plan</span><span class="sxs-lookup"><span data-stu-id="ea1d1-111">Removes the specified plan</span></span>

## <span data-ttu-id="ea1d1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea1d1-112">PARAMETERS</span></span>

### <span data-ttu-id="ea1d1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ea1d1-113">-Force</span></span>
<span data-ttu-id="ea1d1-114">Kennzeichnen, um das Element ohne Bestätigung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="ea1d1-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="ea1d1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ea1d1-115">-Name</span></span>
<span data-ttu-id="ea1d1-116">Der Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="ea1d1-116">Name of the plan.</span></span>

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

### <span data-ttu-id="ea1d1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea1d1-117">-ResourceGroupName</span></span>
<span data-ttu-id="ea1d1-118">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="ea1d1-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="ea1d1-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ea1d1-119">-ResourceId</span></span>
<span data-ttu-id="ea1d1-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ea1d1-120">The resource id.</span></span>

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

### <span data-ttu-id="ea1d1-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ea1d1-121">-Confirm</span></span>
<span data-ttu-id="ea1d1-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ea1d1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea1d1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea1d1-123">-WhatIf</span></span>
<span data-ttu-id="ea1d1-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea1d1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea1d1-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ea1d1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea1d1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea1d1-126">CommonParameters</span></span>
<span data-ttu-id="ea1d1-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea1d1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea1d1-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea1d1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea1d1-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ea1d1-129">INPUTS</span></span>

## <span data-ttu-id="ea1d1-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ea1d1-130">OUTPUTS</span></span>

## <span data-ttu-id="ea1d1-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="ea1d1-131">NOTES</span></span>

## <span data-ttu-id="ea1d1-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ea1d1-132">RELATED LINKS</span></span>

