---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 498374f19f83befc5697395eb58bb191555b10ca
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006969"
---
# <span data-ttu-id="c3001-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="c3001-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="c3001-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3001-102">SYNOPSIS</span></span>
<span data-ttu-id="c3001-103">Repariert einen Knoten des Clusters.</span><span class="sxs-lookup"><span data-stu-id="c3001-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="c3001-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3001-104">SYNTAX</span></span>

### <span data-ttu-id="c3001-105">Reparieren (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3001-105">Repair (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BMCIPv4Address <String> [-Location <String>]
 [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3001-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3001-106">ResourceId</span></span>
```
Repair-AzsScaleUnitNode -BMCIPv4Address <String> -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c3001-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3001-107">DESCRIPTION</span></span>
<span data-ttu-id="c3001-108">Repariert einen Knoten des Clusters.</span><span class="sxs-lookup"><span data-stu-id="c3001-108">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="c3001-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3001-109">EXAMPLES</span></span>

### <span data-ttu-id="c3001-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c3001-110">EXAMPLE 1</span></span>
```
Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***
```

<span data-ttu-id="c3001-111">Reparieren eines Knotens einer Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="c3001-111">Repair a scale unit node.</span></span>

## <span data-ttu-id="c3001-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3001-112">PARAMETERS</span></span>

### <span data-ttu-id="c3001-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c3001-113">-Name</span></span>
<span data-ttu-id="c3001-114">Name des Knotens der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="c3001-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3001-115">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="c3001-115">-BMCIPv4Address</span></span>
<span data-ttu-id="c3001-116">BMC-Adresse des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="c3001-116">BMC address of the physical machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3001-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="c3001-117">-Location</span></span>
<span data-ttu-id="c3001-118">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="c3001-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3001-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3001-119">-ResourceGroupName</span></span>
<span data-ttu-id="c3001-120">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="c3001-120">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3001-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c3001-121">-ResourceId</span></span>
<span data-ttu-id="c3001-122">Ressourcen-ID des Skalierungseinheit-Knotens</span><span class="sxs-lookup"><span data-stu-id="c3001-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="c3001-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3001-123">-AsJob</span></span>
<span data-ttu-id="c3001-124">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c3001-124">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="c3001-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c3001-125">-Force</span></span>
<span data-ttu-id="c3001-126">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="c3001-126">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c3001-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3001-127">-WhatIf</span></span>
<span data-ttu-id="c3001-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3001-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3001-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3001-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3001-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c3001-130">-Confirm</span></span>
<span data-ttu-id="c3001-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3001-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3001-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3001-132">CommonParameters</span></span>
<span data-ttu-id="c3001-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3001-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3001-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3001-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3001-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3001-135">INPUTS</span></span>

## <span data-ttu-id="c3001-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3001-136">OUTPUTS</span></span>

## <span data-ttu-id="c3001-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3001-137">NOTES</span></span>

## <span data-ttu-id="c3001-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3001-138">RELATED LINKS</span></span>
