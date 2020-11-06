---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b3fb659c1d11df734bdc95f554e4c100060e185
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474626"
---
# <span data-ttu-id="49324-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="49324-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="49324-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="49324-102">SYNOPSIS</span></span>
<span data-ttu-id="49324-103">Löscht das angegebene Compute-Kontingent.</span><span class="sxs-lookup"><span data-stu-id="49324-103">Deletes specified compute quota.</span></span>

## <span data-ttu-id="49324-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="49324-104">SYNTAX</span></span>

### <span data-ttu-id="49324-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="49324-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49324-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="49324-106">ResourceId</span></span>
```
Remove-AzsComputeQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49324-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49324-107">DESCRIPTION</span></span>
<span data-ttu-id="49324-108">Löschen eines vorhandenen Kontingents</span><span class="sxs-lookup"><span data-stu-id="49324-108">Delete an existing quota.</span></span>

## <span data-ttu-id="49324-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49324-109">EXAMPLES</span></span>

### <span data-ttu-id="49324-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="49324-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsComputeQuota -Name ComputeQuota
```

<span data-ttu-id="49324-111">Entfernen Sie ein Compute-Kontingent, wenn alle Parameter angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="49324-111">Remove a compute quota given all the parameters.</span></span>

## <span data-ttu-id="49324-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="49324-112">PARAMETERS</span></span>

### <span data-ttu-id="49324-113">-Force</span><span class="sxs-lookup"><span data-stu-id="49324-113">-Force</span></span>
<span data-ttu-id="49324-114">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="49324-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="49324-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="49324-115">-Location</span></span>
<span data-ttu-id="49324-116">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="49324-116">Location of the resource.</span></span> <span data-ttu-id="49324-117">Wenn dies nicht der Fall ist, ist der Standort standardmäßig an das Abonnement von TENAT gebunden.</span><span class="sxs-lookup"><span data-stu-id="49324-117">If not given we default to the location bound to the tenat's subscription.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49324-118">-Name</span><span class="sxs-lookup"><span data-stu-id="49324-118">-Name</span></span>
<span data-ttu-id="49324-119">Der Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="49324-119">Name of the quota.</span></span>

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

### <span data-ttu-id="49324-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="49324-120">-ResourceId</span></span>
<span data-ttu-id="49324-121">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="49324-121">The resource id.</span></span>

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

### <span data-ttu-id="49324-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="49324-122">-Confirm</span></span>
<span data-ttu-id="49324-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="49324-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49324-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49324-124">-WhatIf</span></span>
<span data-ttu-id="49324-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49324-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49324-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="49324-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49324-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49324-127">CommonParameters</span></span>
<span data-ttu-id="49324-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49324-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49324-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49324-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49324-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="49324-130">INPUTS</span></span>

## <span data-ttu-id="49324-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49324-131">OUTPUTS</span></span>

## <span data-ttu-id="49324-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="49324-132">NOTES</span></span>

## <span data-ttu-id="49324-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="49324-133">RELATED LINKS</span></span>

