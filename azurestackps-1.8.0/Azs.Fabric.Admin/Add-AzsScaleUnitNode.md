---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ced1207f07360c0a18674d6f8ae4170be9b87beb
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827628"
---
# <span data-ttu-id="e9cb6-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="e9cb6-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="e9cb6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e9cb6-102">SYNOPSIS</span></span>
<span data-ttu-id="e9cb6-103">Hinzufügen einer neuen Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="e9cb6-103">Add a new scale unit.</span></span>

## <span data-ttu-id="e9cb6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9cb6-104">SYNTAX</span></span>

### <span data-ttu-id="e9cb6-105">Skalieren (Standard)</span><span class="sxs-lookup"><span data-stu-id="e9cb6-105">ScaleOut (Default)</span></span>
```
Add-AzsScaleUnitNode -Name <String> -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence]
 [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9cb6-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9cb6-106">ResourceId</span></span>
```
Add-AzsScaleUnitNode -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence] -ResourceId <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9cb6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9cb6-107">DESCRIPTION</span></span>
<span data-ttu-id="e9cb6-108">Hinzufügen einer neuen Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="e9cb6-108">Add a new scale unit.</span></span>

## <span data-ttu-id="e9cb6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9cb6-109">EXAMPLES</span></span>

### <span data-ttu-id="e9cb6-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e9cb6-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsScaleUnitNode -ScaleUnitName "Azs-ERC03" -NodeList $nodeList
```

<span data-ttu-id="e9cb6-111">Hinzufügen eines neuen Skalierungseinheiten Knotens</span><span class="sxs-lookup"><span data-stu-id="e9cb6-111">Add a new scale unit node.</span></span>

## <span data-ttu-id="e9cb6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9cb6-112">PARAMETERS</span></span>

### <span data-ttu-id="e9cb6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9cb6-113">-AsJob</span></span>
<span data-ttu-id="e9cb6-114">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="e9cb6-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="e9cb6-115">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="e9cb6-115">-AwaitStorageConvergence</span></span>
<span data-ttu-id="e9cb6-116">Flag gibt an, ob der Vorgang auf eine Konvergenz des Speichers warten soll, bevor er zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="e9cb6-116">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

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

### <span data-ttu-id="e9cb6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e9cb6-117">-Force</span></span>
<span data-ttu-id="e9cb6-118">Keine Bestätigung anfordern</span><span class="sxs-lookup"><span data-stu-id="e9cb6-118">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="e9cb6-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="e9cb6-119">-Location</span></span>
<span data-ttu-id="e9cb6-120">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="e9cb6-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9cb6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e9cb6-121">-Name</span></span>
<span data-ttu-id="e9cb6-122">{{Fill Name Description}}</span><span class="sxs-lookup"><span data-stu-id="e9cb6-122">{{Fill Name Description}}</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9cb6-123">-Nodeliste</span><span class="sxs-lookup"><span data-stu-id="e9cb6-123">-NodeList</span></span>
<span data-ttu-id="e9cb6-124">Liste der Knoten in der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="e9cb6-124">List of nodes in the scale unit.</span></span>

```yaml
Type: ScaleOutScaleUnitParameters[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9cb6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9cb6-125">-ResourceGroupName</span></span>
<span data-ttu-id="e9cb6-126">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="e9cb6-126">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9cb6-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e9cb6-127">-ResourceId</span></span>
<span data-ttu-id="e9cb6-128">Ressourcen-ID des Skalierungseinheit-Knotens</span><span class="sxs-lookup"><span data-stu-id="e9cb6-128">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="e9cb6-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e9cb6-129">-Confirm</span></span>
<span data-ttu-id="e9cb6-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e9cb6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9cb6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9cb6-131">-WhatIf</span></span>
<span data-ttu-id="e9cb6-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9cb6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9cb6-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e9cb6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9cb6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9cb6-134">CommonParameters</span></span>
<span data-ttu-id="e9cb6-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9cb6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9cb6-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9cb6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9cb6-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e9cb6-137">INPUTS</span></span>

## <span data-ttu-id="e9cb6-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e9cb6-138">OUTPUTS</span></span>

## <span data-ttu-id="e9cb6-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="e9cb6-139">NOTES</span></span>

## <span data-ttu-id="e9cb6-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e9cb6-140">RELATED LINKS</span></span>

