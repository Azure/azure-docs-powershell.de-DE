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
ms.locfileid: "93827340"
---
# <span data-ttu-id="2b312-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="2b312-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="2b312-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2b312-102">SYNOPSIS</span></span>
<span data-ttu-id="2b312-103">Löscht das angegebene Compute-Kontingent.</span><span class="sxs-lookup"><span data-stu-id="2b312-103">Deletes specified compute quota.</span></span>

## <span data-ttu-id="2b312-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b312-104">SYNTAX</span></span>

### <span data-ttu-id="2b312-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="2b312-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b312-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b312-106">ResourceId</span></span>
```
Remove-AzsComputeQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b312-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b312-107">DESCRIPTION</span></span>
<span data-ttu-id="2b312-108">Löschen eines vorhandenen Kontingents</span><span class="sxs-lookup"><span data-stu-id="2b312-108">Delete an existing quota.</span></span>

## <span data-ttu-id="2b312-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2b312-109">EXAMPLES</span></span>

### <span data-ttu-id="2b312-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2b312-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsComputeQuota -Name ComputeQuota
```

<span data-ttu-id="2b312-111">Entfernen Sie ein Compute-Kontingent, wenn alle Parameter angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="2b312-111">Remove a compute quota given all the parameters.</span></span>

## <span data-ttu-id="2b312-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b312-112">PARAMETERS</span></span>

### <span data-ttu-id="2b312-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2b312-113">-Force</span></span>
<span data-ttu-id="2b312-114">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="2b312-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2b312-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="2b312-115">-Location</span></span>
<span data-ttu-id="2b312-116">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="2b312-116">Location of the resource.</span></span> <span data-ttu-id="2b312-117">Wenn dies nicht der Fall ist, ist der Standort standardmäßig an das Abonnement von TENAT gebunden.</span><span class="sxs-lookup"><span data-stu-id="2b312-117">If not given we default to the location bound to the tenat's subscription.</span></span>

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

### <span data-ttu-id="2b312-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2b312-118">-Name</span></span>
<span data-ttu-id="2b312-119">Der Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="2b312-119">Name of the quota.</span></span>

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

### <span data-ttu-id="2b312-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2b312-120">-ResourceId</span></span>
<span data-ttu-id="2b312-121">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="2b312-121">The resource id.</span></span>

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

### <span data-ttu-id="2b312-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2b312-122">-Confirm</span></span>
<span data-ttu-id="2b312-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b312-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b312-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b312-124">-WhatIf</span></span>
<span data-ttu-id="2b312-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b312-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b312-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b312-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b312-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b312-127">CommonParameters</span></span>
<span data-ttu-id="2b312-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b312-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b312-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b312-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b312-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2b312-130">INPUTS</span></span>

## <span data-ttu-id="2b312-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2b312-131">OUTPUTS</span></span>

## <span data-ttu-id="2b312-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="2b312-132">NOTES</span></span>

## <span data-ttu-id="2b312-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2b312-133">RELATED LINKS</span></span>

