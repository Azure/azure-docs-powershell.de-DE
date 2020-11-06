---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b04ce97fe1fc7e21f166b1bb86db52bc8ad6e29e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475017"
---
# <span data-ttu-id="14a70-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="14a70-101">Close-AzsAlert</span></span>

## <span data-ttu-id="14a70-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="14a70-102">SYNOPSIS</span></span>
<span data-ttu-id="14a70-103">Schließt die angegebene Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="14a70-103">Closes the given alert.</span></span>

## <span data-ttu-id="14a70-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="14a70-104">SYNTAX</span></span>

### <span data-ttu-id="14a70-105">Schließen (Standard)</span><span class="sxs-lookup"><span data-stu-id="14a70-105">Close (Default)</span></span>
```
Close-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14a70-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="14a70-106">InputObject</span></span>
```
Close-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14a70-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="14a70-107">ResourceId</span></span>
```
Close-AzsAlert -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14a70-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14a70-108">DESCRIPTION</span></span>
<span data-ttu-id="14a70-109">Schließt die angegebene Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="14a70-109">Closes the given alert.</span></span>

## <span data-ttu-id="14a70-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="14a70-110">EXAMPLES</span></span>

### <span data-ttu-id="14a70-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="14a70-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="14a70-112">Schließen Sie eine Benachrichtigung nach Namen.</span><span class="sxs-lookup"><span data-stu-id="14a70-112">Close an alert by Name.</span></span>

### <span data-ttu-id="14a70-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="14a70-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="14a70-114">Schließen Sie eine Benachrichtigung über Piping.</span><span class="sxs-lookup"><span data-stu-id="14a70-114">Close an alert through piping.</span></span>

## <span data-ttu-id="14a70-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="14a70-115">PARAMETERS</span></span>

### <span data-ttu-id="14a70-116">-Force</span><span class="sxs-lookup"><span data-stu-id="14a70-116">-Force</span></span>
<span data-ttu-id="14a70-117">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="14a70-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="14a70-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="14a70-118">-InputObject</span></span>
<span data-ttu-id="14a70-119">Eine von Get-AzsAlert zurückgegebene Warnung.</span><span class="sxs-lookup"><span data-stu-id="14a70-119">An alert returned from Get-AzsAlert.</span></span>

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

### <span data-ttu-id="14a70-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="14a70-120">-Location</span></span>
<span data-ttu-id="14a70-121">Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="14a70-121">Name of the location.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a70-122">-Name</span><span class="sxs-lookup"><span data-stu-id="14a70-122">-Name</span></span>
<span data-ttu-id="14a70-123">Der Warnungs Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="14a70-123">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a70-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14a70-124">-ResourceGroupName</span></span>
<span data-ttu-id="14a70-125">Der Ressourcengruppenname, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="14a70-125">Resource group name which the resource resides.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a70-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="14a70-126">-ResourceId</span></span>
<span data-ttu-id="14a70-127">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="14a70-127">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14a70-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="14a70-128">-Confirm</span></span>
<span data-ttu-id="14a70-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="14a70-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14a70-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14a70-130">-WhatIf</span></span>
<span data-ttu-id="14a70-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="14a70-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14a70-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="14a70-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14a70-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14a70-133">CommonParameters</span></span>
<span data-ttu-id="14a70-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14a70-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14a70-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14a70-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14a70-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="14a70-136">INPUTS</span></span>

## <span data-ttu-id="14a70-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="14a70-137">OUTPUTS</span></span>

### <span data-ttu-id="14a70-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. Alert</span><span class="sxs-lookup"><span data-stu-id="14a70-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="14a70-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="14a70-139">NOTES</span></span>

## <span data-ttu-id="14a70-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="14a70-140">RELATED LINKS</span></span>

