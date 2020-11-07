---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c60245b9e6b8d44d8c465427c41c69e5cd442bb0
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828295"
---
# <span data-ttu-id="1e3d4-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="1e3d4-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="1e3d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e3d4-102">SYNOPSIS</span></span>
<span data-ttu-id="1e3d4-103">Starten Sie den Wartungsmodus für einen Skalierungseinheit-Knoten.</span><span class="sxs-lookup"><span data-stu-id="1e3d4-103">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="1e3d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e3d4-104">SYNTAX</span></span>

### <span data-ttu-id="1e3d4-105">Deaktivieren (Standard)</span><span class="sxs-lookup"><span data-stu-id="1e3d4-105">Disable (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e3d4-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e3d4-106">ResourceId</span></span>
```
Disable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e3d4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e3d4-107">DESCRIPTION</span></span>
<span data-ttu-id="1e3d4-108">Starten Sie den Wartungsmodus für einen Skalierungseinheit-Knoten.</span><span class="sxs-lookup"><span data-stu-id="1e3d4-108">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="1e3d4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e3d4-109">EXAMPLES</span></span>

### <span data-ttu-id="1e3d4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1e3d4-110">EXAMPLE 1</span></span>
```
Disable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="1e3d4-111">Aktivieren des Wartungsmodus für einen Knoten der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="1e3d4-111">Enable maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="1e3d4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e3d4-112">PARAMETERS</span></span>

### <span data-ttu-id="1e3d4-113">-Name</span><span class="sxs-lookup"><span data-stu-id="1e3d4-113">-Name</span></span>
<span data-ttu-id="1e3d4-114">Name des Knotens der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="1e3d4-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3d4-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="1e3d4-115">-Location</span></span>
<span data-ttu-id="1e3d4-116">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="1e3d4-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3d4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e3d4-117">-ResourceGroupName</span></span>
<span data-ttu-id="1e3d4-118">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="1e3d4-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3d4-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1e3d4-119">-ResourceId</span></span>
<span data-ttu-id="1e3d4-120">Ressourcen-ID des Skalierungseinheit-Knotens</span><span class="sxs-lookup"><span data-stu-id="1e3d4-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="1e3d4-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e3d4-121">-AsJob</span></span>
<span data-ttu-id="1e3d4-122">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="1e3d4-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="1e3d4-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1e3d4-123">-Force</span></span>
<span data-ttu-id="1e3d4-124">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="1e3d4-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="1e3d4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e3d4-125">-WhatIf</span></span>
<span data-ttu-id="1e3d4-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e3d4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e3d4-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e3d4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e3d4-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1e3d4-128">-Confirm</span></span>
<span data-ttu-id="1e3d4-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e3d4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e3d4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e3d4-130">CommonParameters</span></span>
<span data-ttu-id="1e3d4-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e3d4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e3d4-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e3d4-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e3d4-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e3d4-133">INPUTS</span></span>

## <span data-ttu-id="1e3d4-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e3d4-134">OUTPUTS</span></span>

## <span data-ttu-id="1e3d4-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e3d4-135">NOTES</span></span>

## <span data-ttu-id="1e3d4-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e3d4-136">RELATED LINKS</span></span>
