---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1a26c22b5714fc7db448935b31b0af685301217
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007031"
---
# <span data-ttu-id="f03e2-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="f03e2-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="f03e2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f03e2-102">SYNOPSIS</span></span>
<span data-ttu-id="f03e2-103">Schalten Sie einen Skalierungseinheit-Knoten aus.</span><span class="sxs-lookup"><span data-stu-id="f03e2-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="f03e2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f03e2-104">SYNTAX</span></span>

### <span data-ttu-id="f03e2-105">Stopp (Standard)</span><span class="sxs-lookup"><span data-stu-id="f03e2-105">Stop (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Shutdown] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f03e2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f03e2-106">ResourceId</span></span>
```
Stop-AzsScaleUnitNode -ResourceId <String> [-Shutdown] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f03e2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f03e2-107">DESCRIPTION</span></span>
<span data-ttu-id="f03e2-108">Schalten Sie einen Skalierungseinheit-Knoten aus.</span><span class="sxs-lookup"><span data-stu-id="f03e2-108">Power off a scale unit node.</span></span>

## <span data-ttu-id="f03e2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f03e2-109">EXAMPLES</span></span>

### <span data-ttu-id="f03e2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f03e2-110">EXAMPLE 1</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236" -Shutdown
```

<span data-ttu-id="f03e2-111">Herunterfahren des Knotens einer Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="f03e2-111">Shutdown a scale unit node.</span></span>

### <span data-ttu-id="f03e2-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f03e2-112">EXAMPLE 2</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="f03e2-113">Schalten Sie einen Knoten der Skalierungseinheit herunter.</span><span class="sxs-lookup"><span data-stu-id="f03e2-113">Power down a scale unit node.</span></span>

## <span data-ttu-id="f03e2-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f03e2-114">PARAMETERS</span></span>

### <span data-ttu-id="f03e2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f03e2-115">-Name</span></span>
<span data-ttu-id="f03e2-116">Name des Knotens der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="f03e2-116">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="f03e2-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="f03e2-117">-Location</span></span>
<span data-ttu-id="f03e2-118">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="f03e2-118">Location of the resource.</span></span>

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

### <span data-ttu-id="f03e2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f03e2-119">-ResourceGroupName</span></span>
<span data-ttu-id="f03e2-120">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="f03e2-120">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="f03e2-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f03e2-121">-ResourceId</span></span>
<span data-ttu-id="f03e2-122">Ressourcen-ID des Skalierungseinheit-Knotens</span><span class="sxs-lookup"><span data-stu-id="f03e2-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="f03e2-123">-Shutdown</span><span class="sxs-lookup"><span data-stu-id="f03e2-123">-Shutdown</span></span>
<span data-ttu-id="f03e2-124">Wenn der Knoten Skalierungseinheit ordnungsgemäß heruntergefahren wird; Andernfalls wird der Knoten Skalierungseinheit stark ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="f03e2-124">If set gracefully shutdown the scale unit node; otherwise hard power off the scale unit node.</span></span>

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

### <span data-ttu-id="f03e2-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f03e2-125">-AsJob</span></span>
<span data-ttu-id="f03e2-126">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="f03e2-126">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="f03e2-127">-Force</span><span class="sxs-lookup"><span data-stu-id="f03e2-127">-Force</span></span>
<span data-ttu-id="f03e2-128">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="f03e2-128">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f03e2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f03e2-129">-WhatIf</span></span>
<span data-ttu-id="f03e2-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f03e2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f03e2-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f03e2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f03e2-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f03e2-132">-Confirm</span></span>
<span data-ttu-id="f03e2-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f03e2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f03e2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f03e2-134">CommonParameters</span></span>
<span data-ttu-id="f03e2-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f03e2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f03e2-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f03e2-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f03e2-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f03e2-137">INPUTS</span></span>

## <span data-ttu-id="f03e2-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f03e2-138">OUTPUTS</span></span>

## <span data-ttu-id="f03e2-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="f03e2-139">NOTES</span></span>

## <span data-ttu-id="f03e2-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f03e2-140">RELATED LINKS</span></span>
