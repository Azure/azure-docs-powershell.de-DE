---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 932d0b77fc6df9a88a2ee13ad92856727db82f06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827307"
---
# <span data-ttu-id="40c97-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="40c97-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="40c97-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="40c97-102">SYNOPSIS</span></span>
<span data-ttu-id="40c97-103">Beenden des Wartungsmodus für einen Knoten der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="40c97-103">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="40c97-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="40c97-104">SYNTAX</span></span>

### <span data-ttu-id="40c97-105">Aktivieren (Standard)</span><span class="sxs-lookup"><span data-stu-id="40c97-105">Enable (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40c97-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="40c97-106">ResourceId</span></span>
```
Enable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40c97-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40c97-107">DESCRIPTION</span></span>
<span data-ttu-id="40c97-108">Beenden des Wartungsmodus für einen Knoten der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="40c97-108">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="40c97-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="40c97-109">EXAMPLES</span></span>

### <span data-ttu-id="40c97-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="40c97-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Enable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="40c97-111">Beenden des Wartungsmodus auf einem Skalierungseinheiten Knoten</span><span class="sxs-lookup"><span data-stu-id="40c97-111">Stop maintenance mode on a scale unit node.</span></span>

## <span data-ttu-id="40c97-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="40c97-112">PARAMETERS</span></span>

### <span data-ttu-id="40c97-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40c97-113">-AsJob</span></span>
<span data-ttu-id="40c97-114">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="40c97-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="40c97-115">-Force</span><span class="sxs-lookup"><span data-stu-id="40c97-115">-Force</span></span>
<span data-ttu-id="40c97-116">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="40c97-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="40c97-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="40c97-117">-Location</span></span>
<span data-ttu-id="40c97-118">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="40c97-118">Location of the resource.</span></span>

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

### <span data-ttu-id="40c97-119">-Name</span><span class="sxs-lookup"><span data-stu-id="40c97-119">-Name</span></span>
<span data-ttu-id="40c97-120">Name des Knotens der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="40c97-120">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="40c97-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40c97-121">-ResourceGroupName</span></span>
<span data-ttu-id="40c97-122">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="40c97-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="40c97-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="40c97-123">-ResourceId</span></span>
<span data-ttu-id="40c97-124">Ressourcen-ID des Skalierungseinheit-Knotens</span><span class="sxs-lookup"><span data-stu-id="40c97-124">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="40c97-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="40c97-125">-Confirm</span></span>
<span data-ttu-id="40c97-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="40c97-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40c97-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40c97-127">-WhatIf</span></span>
<span data-ttu-id="40c97-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="40c97-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40c97-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="40c97-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40c97-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40c97-130">CommonParameters</span></span>
<span data-ttu-id="40c97-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40c97-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40c97-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40c97-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40c97-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="40c97-133">INPUTS</span></span>

## <span data-ttu-id="40c97-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="40c97-134">OUTPUTS</span></span>

## <span data-ttu-id="40c97-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="40c97-135">NOTES</span></span>

## <span data-ttu-id="40c97-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="40c97-136">RELATED LINKS</span></span>

