---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6de990526330cdd192cd99707aacc1e06ad49c5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661965"
---
# <span data-ttu-id="c500d-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="c500d-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="c500d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c500d-102">SYNOPSIS</span></span>
<span data-ttu-id="c500d-103">Schalten Sie einen Skalierungseinheit-Knoten aus.</span><span class="sxs-lookup"><span data-stu-id="c500d-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="c500d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c500d-104">SYNTAX</span></span>

### <span data-ttu-id="c500d-105">Stopp (Standard)</span><span class="sxs-lookup"><span data-stu-id="c500d-105">Stop (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Shutdown] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c500d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c500d-106">ResourceId</span></span>
```
Stop-AzsScaleUnitNode -ResourceId <String> [-Shutdown] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c500d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c500d-107">DESCRIPTION</span></span>
<span data-ttu-id="c500d-108">Schalten Sie einen Skalierungseinheit-Knoten aus.</span><span class="sxs-lookup"><span data-stu-id="c500d-108">Power off a scale unit node.</span></span>

## <span data-ttu-id="c500d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c500d-109">EXAMPLES</span></span>

### <span data-ttu-id="c500d-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c500d-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236" -Shutdown
```

<span data-ttu-id="c500d-111">Herunterfahren des Knotens einer Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="c500d-111">Shutdown a scale unit node.</span></span>

### <span data-ttu-id="c500d-112">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c500d-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="c500d-113">Schalten Sie einen Knoten der Skalierungseinheit herunter.</span><span class="sxs-lookup"><span data-stu-id="c500d-113">Power down a scale unit node.</span></span>

## <span data-ttu-id="c500d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c500d-114">PARAMETERS</span></span>

### <span data-ttu-id="c500d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c500d-115">-AsJob</span></span>
<span data-ttu-id="c500d-116">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c500d-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="c500d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c500d-117">-Force</span></span>
<span data-ttu-id="c500d-118">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="c500d-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c500d-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="c500d-119">-Location</span></span>
<span data-ttu-id="c500d-120">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="c500d-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c500d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c500d-121">-Name</span></span>
<span data-ttu-id="c500d-122">Name des Knotens der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="c500d-122">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c500d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c500d-123">-ResourceGroupName</span></span>
<span data-ttu-id="c500d-124">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="c500d-124">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c500d-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c500d-125">-ResourceId</span></span>
<span data-ttu-id="c500d-126">Ressourcen-ID des Skalierungseinheit-Knotens</span><span class="sxs-lookup"><span data-stu-id="c500d-126">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="c500d-127">-Shutdown</span><span class="sxs-lookup"><span data-stu-id="c500d-127">-Shutdown</span></span>
<span data-ttu-id="c500d-128">Wenn der Knoten Skalierungseinheit ordnungsgemäß heruntergefahren wird; Andernfalls wird der Knoten Skalierungseinheit stark ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="c500d-128">If set gracefully shutdown the scale unit node; otherwise hard power off the scale unit node.</span></span>

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

### <span data-ttu-id="c500d-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c500d-129">-Confirm</span></span>
<span data-ttu-id="c500d-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c500d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c500d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c500d-131">-WhatIf</span></span>
<span data-ttu-id="c500d-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c500d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c500d-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c500d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c500d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c500d-134">CommonParameters</span></span>
<span data-ttu-id="c500d-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c500d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c500d-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c500d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c500d-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c500d-137">INPUTS</span></span>

## <span data-ttu-id="c500d-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c500d-138">OUTPUTS</span></span>

## <span data-ttu-id="c500d-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="c500d-139">NOTES</span></span>

## <span data-ttu-id="c500d-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c500d-140">RELATED LINKS</span></span>

