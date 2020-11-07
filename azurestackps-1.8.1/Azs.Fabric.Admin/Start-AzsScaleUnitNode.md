---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c51249856d9cd8c8fc47d4968b1bc011040610e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840904"
---
# <span data-ttu-id="69ded-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="69ded-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="69ded-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="69ded-102">SYNOPSIS</span></span>
<span data-ttu-id="69ded-103">Schalten Sie den Knoten einer Skalierungseinheit ein.</span><span class="sxs-lookup"><span data-stu-id="69ded-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="69ded-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="69ded-104">SYNTAX</span></span>

### <span data-ttu-id="69ded-105">PowerOn (Standard)</span><span class="sxs-lookup"><span data-stu-id="69ded-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69ded-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="69ded-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69ded-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69ded-107">DESCRIPTION</span></span>
<span data-ttu-id="69ded-108">Schalten Sie den Knoten einer Skalierungseinheit ein.</span><span class="sxs-lookup"><span data-stu-id="69ded-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="69ded-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="69ded-109">EXAMPLES</span></span>

### <span data-ttu-id="69ded-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="69ded-110">EXAMPLE 1</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="69ded-111">ProvisioningState: erfolgreich</span><span class="sxs-lookup"><span data-stu-id="69ded-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="69ded-112">Schalten Sie den Knoten einer Skalierungseinheit ein.</span><span class="sxs-lookup"><span data-stu-id="69ded-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="69ded-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="69ded-113">PARAMETERS</span></span>

### <span data-ttu-id="69ded-114">-Name</span><span class="sxs-lookup"><span data-stu-id="69ded-114">-Name</span></span>
<span data-ttu-id="69ded-115">Name des Knotens der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="69ded-115">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="69ded-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="69ded-116">-Location</span></span>
<span data-ttu-id="69ded-117">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="69ded-117">Location of the resource.</span></span>

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

### <span data-ttu-id="69ded-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69ded-118">-ResourceGroupName</span></span>
<span data-ttu-id="69ded-119">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="69ded-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="69ded-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="69ded-120">-ResourceId</span></span>
<span data-ttu-id="69ded-121">Ressourcen-ID des Skalierungseinheit-Knotens</span><span class="sxs-lookup"><span data-stu-id="69ded-121">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="69ded-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69ded-122">-AsJob</span></span>
<span data-ttu-id="69ded-123">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="69ded-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="69ded-124">-Force</span><span class="sxs-lookup"><span data-stu-id="69ded-124">-Force</span></span>
<span data-ttu-id="69ded-125">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="69ded-125">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="69ded-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69ded-126">-WhatIf</span></span>
<span data-ttu-id="69ded-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69ded-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69ded-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69ded-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69ded-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="69ded-129">-Confirm</span></span>
<span data-ttu-id="69ded-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="69ded-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69ded-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ded-131">CommonParameters</span></span>
<span data-ttu-id="69ded-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69ded-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ded-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69ded-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ded-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="69ded-134">INPUTS</span></span>

## <span data-ttu-id="69ded-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="69ded-135">OUTPUTS</span></span>

## <span data-ttu-id="69ded-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="69ded-136">NOTES</span></span>

## <span data-ttu-id="69ded-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="69ded-137">RELATED LINKS</span></span>
