---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c5de84b66283d683d121c99c0cf2e0ea27a4a66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827247"
---
# <span data-ttu-id="a2ec9-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="a2ec9-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="a2ec9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a2ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="a2ec9-103">Schalten Sie den Knoten einer Skalierungseinheit ein.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="a2ec9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2ec9-104">SYNTAX</span></span>

### <span data-ttu-id="a2ec9-105">PowerOn (Standard)</span><span class="sxs-lookup"><span data-stu-id="a2ec9-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2ec9-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2ec9-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2ec9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2ec9-107">DESCRIPTION</span></span>
<span data-ttu-id="a2ec9-108">Schalten Sie den Knoten einer Skalierungseinheit ein.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="a2ec9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2ec9-109">EXAMPLES</span></span>

### <span data-ttu-id="a2ec9-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a2ec9-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="a2ec9-111">ProvisioningState: erfolgreich</span><span class="sxs-lookup"><span data-stu-id="a2ec9-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="a2ec9-112">Schalten Sie den Knoten einer Skalierungseinheit ein.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="a2ec9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2ec9-113">PARAMETERS</span></span>

### <span data-ttu-id="a2ec9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2ec9-114">-AsJob</span></span>
<span data-ttu-id="a2ec9-115">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="a2ec9-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a2ec9-116">-Force</span></span>
<span data-ttu-id="a2ec9-117">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="a2ec9-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="a2ec9-118">-Location</span></span>
<span data-ttu-id="a2ec9-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-119">Location of the resource.</span></span>

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

### <span data-ttu-id="a2ec9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a2ec9-120">-Name</span></span>
<span data-ttu-id="a2ec9-121">Name des Knotens der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="a2ec9-121">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="a2ec9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2ec9-122">-ResourceGroupName</span></span>
<span data-ttu-id="a2ec9-123">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="a2ec9-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a2ec9-124">-ResourceId</span></span>
<span data-ttu-id="a2ec9-125">Ressourcen-ID des Skalierungseinheit-Knotens</span><span class="sxs-lookup"><span data-stu-id="a2ec9-125">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="a2ec9-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a2ec9-126">-Confirm</span></span>
<span data-ttu-id="a2ec9-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2ec9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2ec9-128">-WhatIf</span></span>
<span data-ttu-id="a2ec9-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2ec9-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2ec9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2ec9-131">CommonParameters</span></span>
<span data-ttu-id="a2ec9-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2ec9-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2ec9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2ec9-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a2ec9-134">INPUTS</span></span>

## <span data-ttu-id="a2ec9-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a2ec9-135">OUTPUTS</span></span>

## <span data-ttu-id="a2ec9-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="a2ec9-136">NOTES</span></span>

## <span data-ttu-id="a2ec9-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a2ec9-137">RELATED LINKS</span></span>

