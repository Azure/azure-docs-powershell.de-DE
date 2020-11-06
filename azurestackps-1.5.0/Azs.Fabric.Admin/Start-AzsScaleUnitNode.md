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
ms.locfileid: "93475157"
---
# <span data-ttu-id="91e8f-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="91e8f-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="91e8f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91e8f-102">SYNOPSIS</span></span>
<span data-ttu-id="91e8f-103">Schalten Sie den Knoten einer Skalierungseinheit ein.</span><span class="sxs-lookup"><span data-stu-id="91e8f-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="91e8f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91e8f-104">SYNTAX</span></span>

### <span data-ttu-id="91e8f-105">PowerOn (Standard)</span><span class="sxs-lookup"><span data-stu-id="91e8f-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91e8f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="91e8f-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91e8f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91e8f-107">DESCRIPTION</span></span>
<span data-ttu-id="91e8f-108">Schalten Sie den Knoten einer Skalierungseinheit ein.</span><span class="sxs-lookup"><span data-stu-id="91e8f-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="91e8f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91e8f-109">EXAMPLES</span></span>

### <span data-ttu-id="91e8f-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="91e8f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="91e8f-111">ProvisioningState: erfolgreich</span><span class="sxs-lookup"><span data-stu-id="91e8f-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="91e8f-112">Schalten Sie den Knoten einer Skalierungseinheit ein.</span><span class="sxs-lookup"><span data-stu-id="91e8f-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="91e8f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="91e8f-113">PARAMETERS</span></span>

### <span data-ttu-id="91e8f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91e8f-114">-AsJob</span></span>
<span data-ttu-id="91e8f-115">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="91e8f-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="91e8f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="91e8f-116">-Force</span></span>
<span data-ttu-id="91e8f-117">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="91e8f-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="91e8f-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="91e8f-118">-Location</span></span>
<span data-ttu-id="91e8f-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="91e8f-119">Location of the resource.</span></span>

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

### <span data-ttu-id="91e8f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="91e8f-120">-Name</span></span>
<span data-ttu-id="91e8f-121">Name des Knotens der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="91e8f-121">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="91e8f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91e8f-122">-ResourceGroupName</span></span>
<span data-ttu-id="91e8f-123">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="91e8f-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="91e8f-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="91e8f-124">-ResourceId</span></span>
<span data-ttu-id="91e8f-125">Ressourcen-ID des Skalierungseinheit-Knotens</span><span class="sxs-lookup"><span data-stu-id="91e8f-125">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="91e8f-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="91e8f-126">-Confirm</span></span>
<span data-ttu-id="91e8f-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="91e8f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91e8f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91e8f-128">-WhatIf</span></span>
<span data-ttu-id="91e8f-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91e8f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91e8f-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91e8f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91e8f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91e8f-131">CommonParameters</span></span>
<span data-ttu-id="91e8f-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91e8f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91e8f-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91e8f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91e8f-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91e8f-134">INPUTS</span></span>

## <span data-ttu-id="91e8f-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91e8f-135">OUTPUTS</span></span>

## <span data-ttu-id="91e8f-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="91e8f-136">NOTES</span></span>

## <span data-ttu-id="91e8f-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91e8f-137">RELATED LINKS</span></span>

