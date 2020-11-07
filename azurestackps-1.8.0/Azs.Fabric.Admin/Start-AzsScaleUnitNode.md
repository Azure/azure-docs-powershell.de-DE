---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c51249856d9cd8c8fc47d4968b1bc011040610e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827520"
---
# <span data-ttu-id="be201-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="be201-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="be201-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="be201-102">SYNOPSIS</span></span>
<span data-ttu-id="be201-103">Schalten Sie den Knoten einer Skalierungseinheit ein.</span><span class="sxs-lookup"><span data-stu-id="be201-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="be201-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="be201-104">SYNTAX</span></span>

### <span data-ttu-id="be201-105">PowerOn (Standard)</span><span class="sxs-lookup"><span data-stu-id="be201-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be201-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="be201-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be201-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be201-107">DESCRIPTION</span></span>
<span data-ttu-id="be201-108">Schalten Sie den Knoten einer Skalierungseinheit ein.</span><span class="sxs-lookup"><span data-stu-id="be201-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="be201-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be201-109">EXAMPLES</span></span>

### <span data-ttu-id="be201-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="be201-110">EXAMPLE 1</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="be201-111">ProvisioningState: erfolgreich</span><span class="sxs-lookup"><span data-stu-id="be201-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="be201-112">Schalten Sie den Knoten einer Skalierungseinheit ein.</span><span class="sxs-lookup"><span data-stu-id="be201-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="be201-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="be201-113">PARAMETERS</span></span>

### <span data-ttu-id="be201-114">-Name</span><span class="sxs-lookup"><span data-stu-id="be201-114">-Name</span></span>
<span data-ttu-id="be201-115">Name des Knotens der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="be201-115">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be201-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="be201-116">-Location</span></span>
<span data-ttu-id="be201-117">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="be201-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be201-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be201-118">-ResourceGroupName</span></span>
<span data-ttu-id="be201-119">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="be201-119">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be201-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="be201-120">-ResourceId</span></span>
<span data-ttu-id="be201-121">Ressourcen-ID des Skalierungseinheit-Knotens</span><span class="sxs-lookup"><span data-stu-id="be201-121">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="be201-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be201-122">-AsJob</span></span>
<span data-ttu-id="be201-123">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="be201-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="be201-124">-Force</span><span class="sxs-lookup"><span data-stu-id="be201-124">-Force</span></span>
<span data-ttu-id="be201-125">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="be201-125">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="be201-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be201-126">-WhatIf</span></span>
<span data-ttu-id="be201-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="be201-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be201-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="be201-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be201-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="be201-129">-Confirm</span></span>
<span data-ttu-id="be201-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="be201-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be201-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be201-131">CommonParameters</span></span>
<span data-ttu-id="be201-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be201-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be201-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be201-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be201-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="be201-134">INPUTS</span></span>

## <span data-ttu-id="be201-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="be201-135">OUTPUTS</span></span>

## <span data-ttu-id="be201-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="be201-136">NOTES</span></span>

## <span data-ttu-id="be201-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="be201-137">RELATED LINKS</span></span>
