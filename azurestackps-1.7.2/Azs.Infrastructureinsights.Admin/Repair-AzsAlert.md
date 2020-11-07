---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b06ae4189b427686f4237c1a6eae841fcaba5c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827400"
---
# <span data-ttu-id="cd484-101">Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="cd484-101">Repair-AzsAlert</span></span>

## <span data-ttu-id="cd484-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cd484-102">SYNOPSIS</span></span>
<span data-ttu-id="cd484-103">Repariert die angegebene Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="cd484-103">Repairs the given alert.</span></span>

## <span data-ttu-id="cd484-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd484-104">SYNTAX</span></span>

### <span data-ttu-id="cd484-105">Reparieren (Standard)</span><span class="sxs-lookup"><span data-stu-id="cd484-105">Repair (Default)</span></span>
```
Repair-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd484-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="cd484-106">InputObject</span></span>
```
Repair-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd484-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd484-107">DESCRIPTION</span></span>
<span data-ttu-id="cd484-108">Repariert die angegebene Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="cd484-108">Repairs the given alert.</span></span>

## <span data-ttu-id="cd484-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd484-109">EXAMPLES</span></span>

### <span data-ttu-id="cd484-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cd484-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Repair-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="cd484-111">Repariert eine Benachrichtigung nach Namen.</span><span class="sxs-lookup"><span data-stu-id="cd484-111">Repairs an alert by Name.</span></span>

### <span data-ttu-id="cd484-112">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="cd484-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Repair-AzsAlert
```

<span data-ttu-id="cd484-113">Repariert eine Warnung durch Rohrleitungen.</span><span class="sxs-lookup"><span data-stu-id="cd484-113">Repairs an alert through piping.</span></span>

## <span data-ttu-id="cd484-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd484-114">PARAMETERS</span></span>

### <span data-ttu-id="cd484-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cd484-115">-Force</span></span>
<span data-ttu-id="cd484-116">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="cd484-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="cd484-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cd484-117">-InputObject</span></span>
<span data-ttu-id="cd484-118">Eine von Get-AzsAlert zurückgegebene Warnung.</span><span class="sxs-lookup"><span data-stu-id="cd484-118">An alert returned from Get-AzsAlert.</span></span>

```yaml
Type: Alert
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd484-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="cd484-119">-Location</span></span>
<span data-ttu-id="cd484-120">Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="cd484-120">Name of the location.</span></span>

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

### <span data-ttu-id="cd484-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cd484-121">-Name</span></span>
<span data-ttu-id="cd484-122">Der Warnungs Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="cd484-122">The alert identifier.</span></span>

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

### <span data-ttu-id="cd484-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd484-123">-ResourceGroupName</span></span>
<span data-ttu-id="cd484-124">Der Ressourcengruppenname, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="cd484-124">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="cd484-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cd484-125">-Confirm</span></span>
<span data-ttu-id="cd484-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cd484-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd484-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd484-127">-WhatIf</span></span>
<span data-ttu-id="cd484-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cd484-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd484-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd484-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd484-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd484-130">CommonParameters</span></span>
<span data-ttu-id="cd484-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd484-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd484-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd484-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd484-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cd484-133">INPUTS</span></span>

## <span data-ttu-id="cd484-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cd484-134">OUTPUTS</span></span>

## <span data-ttu-id="cd484-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="cd484-135">NOTES</span></span>

## <span data-ttu-id="cd484-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cd484-136">RELATED LINKS</span></span>

