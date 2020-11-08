---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c51249856d9cd8c8fc47d4968b1bc011040610e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007045"
---
# <span data-ttu-id="83d0e-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="83d0e-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="83d0e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83d0e-102">SYNOPSIS</span></span>
<span data-ttu-id="83d0e-103">Schalten Sie den Knoten einer Skalierungseinheit ein.</span><span class="sxs-lookup"><span data-stu-id="83d0e-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="83d0e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83d0e-104">SYNTAX</span></span>

### <span data-ttu-id="83d0e-105">PowerOn (Standard)</span><span class="sxs-lookup"><span data-stu-id="83d0e-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83d0e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="83d0e-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83d0e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83d0e-107">DESCRIPTION</span></span>
<span data-ttu-id="83d0e-108">Schalten Sie den Knoten einer Skalierungseinheit ein.</span><span class="sxs-lookup"><span data-stu-id="83d0e-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="83d0e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83d0e-109">EXAMPLES</span></span>

### <span data-ttu-id="83d0e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="83d0e-110">EXAMPLE 1</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="83d0e-111">ProvisioningState: erfolgreich</span><span class="sxs-lookup"><span data-stu-id="83d0e-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="83d0e-112">Schalten Sie den Knoten einer Skalierungseinheit ein.</span><span class="sxs-lookup"><span data-stu-id="83d0e-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="83d0e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="83d0e-113">PARAMETERS</span></span>

### <span data-ttu-id="83d0e-114">-Name</span><span class="sxs-lookup"><span data-stu-id="83d0e-114">-Name</span></span>
<span data-ttu-id="83d0e-115">Name des Knotens der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="83d0e-115">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="83d0e-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="83d0e-116">-Location</span></span>
<span data-ttu-id="83d0e-117">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="83d0e-117">Location of the resource.</span></span>

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

### <span data-ttu-id="83d0e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83d0e-118">-ResourceGroupName</span></span>
<span data-ttu-id="83d0e-119">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="83d0e-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="83d0e-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="83d0e-120">-ResourceId</span></span>
<span data-ttu-id="83d0e-121">Ressourcen-ID des Skalierungseinheit-Knotens</span><span class="sxs-lookup"><span data-stu-id="83d0e-121">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="83d0e-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83d0e-122">-AsJob</span></span>
<span data-ttu-id="83d0e-123">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="83d0e-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="83d0e-124">-Force</span><span class="sxs-lookup"><span data-stu-id="83d0e-124">-Force</span></span>
<span data-ttu-id="83d0e-125">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="83d0e-125">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="83d0e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83d0e-126">-WhatIf</span></span>
<span data-ttu-id="83d0e-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83d0e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83d0e-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="83d0e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83d0e-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="83d0e-129">-Confirm</span></span>
<span data-ttu-id="83d0e-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="83d0e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83d0e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d0e-131">CommonParameters</span></span>
<span data-ttu-id="83d0e-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83d0e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d0e-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83d0e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d0e-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83d0e-134">INPUTS</span></span>

## <span data-ttu-id="83d0e-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83d0e-135">OUTPUTS</span></span>

## <span data-ttu-id="83d0e-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="83d0e-136">NOTES</span></span>

## <span data-ttu-id="83d0e-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83d0e-137">RELATED LINKS</span></span>
