---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d77229892da63973513dd8870a949ff296f5538
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827616"
---
# <span data-ttu-id="19f2a-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="19f2a-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="19f2a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="19f2a-103">Beenden des Wartungsmodus für einen Knoten der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="19f2a-103">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="19f2a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19f2a-104">SYNTAX</span></span>

### <span data-ttu-id="19f2a-105">Aktivieren (Standard)</span><span class="sxs-lookup"><span data-stu-id="19f2a-105">Enable (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19f2a-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="19f2a-106">ResourceId</span></span>
```
Enable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19f2a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19f2a-107">DESCRIPTION</span></span>
<span data-ttu-id="19f2a-108">Beenden des Wartungsmodus für einen Knoten der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="19f2a-108">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="19f2a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19f2a-109">EXAMPLES</span></span>

### <span data-ttu-id="19f2a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="19f2a-110">EXAMPLE 1</span></span>
```
Enable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="19f2a-111">Beenden des Wartungsmodus auf einem Skalierungseinheiten Knoten</span><span class="sxs-lookup"><span data-stu-id="19f2a-111">Stop maintenance mode on a scale unit node.</span></span>

## <span data-ttu-id="19f2a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="19f2a-112">PARAMETERS</span></span>

### <span data-ttu-id="19f2a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="19f2a-113">-Name</span></span>
<span data-ttu-id="19f2a-114">Name des Knotens der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="19f2a-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f2a-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="19f2a-115">-Location</span></span>
<span data-ttu-id="19f2a-116">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="19f2a-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f2a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19f2a-117">-ResourceGroupName</span></span>
<span data-ttu-id="19f2a-118">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="19f2a-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f2a-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="19f2a-119">-ResourceId</span></span>
<span data-ttu-id="19f2a-120">Ressourcen-ID des Skalierungseinheit-Knotens</span><span class="sxs-lookup"><span data-stu-id="19f2a-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="19f2a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19f2a-121">-AsJob</span></span>
<span data-ttu-id="19f2a-122">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="19f2a-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="19f2a-123">-Force</span><span class="sxs-lookup"><span data-stu-id="19f2a-123">-Force</span></span>
<span data-ttu-id="19f2a-124">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="19f2a-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="19f2a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19f2a-125">-WhatIf</span></span>
<span data-ttu-id="19f2a-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="19f2a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19f2a-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="19f2a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19f2a-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="19f2a-128">-Confirm</span></span>
<span data-ttu-id="19f2a-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="19f2a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19f2a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19f2a-130">CommonParameters</span></span>
<span data-ttu-id="19f2a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19f2a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19f2a-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19f2a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19f2a-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19f2a-133">INPUTS</span></span>

## <span data-ttu-id="19f2a-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19f2a-134">OUTPUTS</span></span>

## <span data-ttu-id="19f2a-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="19f2a-135">NOTES</span></span>

## <span data-ttu-id="19f2a-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19f2a-136">RELATED LINKS</span></span>
