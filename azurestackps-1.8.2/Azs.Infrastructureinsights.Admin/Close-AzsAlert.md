---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14885871139eaed1c901312b9540a90d385795e5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007128"
---
# <span data-ttu-id="302a9-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="302a9-101">Close-AzsAlert</span></span>

## <span data-ttu-id="302a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="302a9-102">SYNOPSIS</span></span>
<span data-ttu-id="302a9-103">Schließt die angegebene Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="302a9-103">Closes the given alert.</span></span>

## <span data-ttu-id="302a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="302a9-104">SYNTAX</span></span>

### <span data-ttu-id="302a9-105">Schließen (Standard)</span><span class="sxs-lookup"><span data-stu-id="302a9-105">Close (Default)</span></span>
```
Close-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="302a9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="302a9-106">InputObject</span></span>
```
Close-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="302a9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="302a9-107">ResourceId</span></span>
```
Close-AzsAlert -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="302a9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="302a9-108">DESCRIPTION</span></span>
<span data-ttu-id="302a9-109">Schließt die angegebene Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="302a9-109">Closes the given alert.</span></span>

## <span data-ttu-id="302a9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="302a9-110">EXAMPLES</span></span>

### <span data-ttu-id="302a9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="302a9-111">EXAMPLE 1</span></span>
```
Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="302a9-112">Schließen Sie eine Benachrichtigung nach Namen.</span><span class="sxs-lookup"><span data-stu-id="302a9-112">Close an alert by Name.</span></span>

### <span data-ttu-id="302a9-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="302a9-113">EXAMPLE 2</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="302a9-114">Schließen Sie eine Benachrichtigung über Piping.</span><span class="sxs-lookup"><span data-stu-id="302a9-114">Close an alert through piping.</span></span>

## <span data-ttu-id="302a9-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="302a9-115">PARAMETERS</span></span>

### <span data-ttu-id="302a9-116">-Name</span><span class="sxs-lookup"><span data-stu-id="302a9-116">-Name</span></span>
<span data-ttu-id="302a9-117">Der Warnungs Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="302a9-117">The alert identifier.</span></span>

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

### <span data-ttu-id="302a9-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="302a9-118">-Location</span></span>
<span data-ttu-id="302a9-119">Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="302a9-119">Name of the location.</span></span>

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

### <span data-ttu-id="302a9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="302a9-120">-ResourceGroupName</span></span>
<span data-ttu-id="302a9-121">Der Ressourcengruppenname der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="302a9-121">Resource group name of the alert.</span></span>

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

### <span data-ttu-id="302a9-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="302a9-122">-InputObject</span></span>
<span data-ttu-id="302a9-123">Eine von Get-AzsAlert zurückgegebene Warnung.</span><span class="sxs-lookup"><span data-stu-id="302a9-123">An alert returned from Get-AzsAlert.</span></span>

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

### <span data-ttu-id="302a9-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="302a9-124">-ResourceId</span></span>
<span data-ttu-id="302a9-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="302a9-125">The resource id.</span></span>

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

### <span data-ttu-id="302a9-126">-Force</span><span class="sxs-lookup"><span data-stu-id="302a9-126">-Force</span></span>
<span data-ttu-id="302a9-127">Parameter wechseln, um die Bestätigung nicht zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="302a9-127">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="302a9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="302a9-128">-WhatIf</span></span>
<span data-ttu-id="302a9-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="302a9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="302a9-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="302a9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="302a9-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="302a9-131">-Confirm</span></span>
<span data-ttu-id="302a9-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="302a9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="302a9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="302a9-133">CommonParameters</span></span>
<span data-ttu-id="302a9-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="302a9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="302a9-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="302a9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="302a9-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="302a9-136">INPUTS</span></span>

## <span data-ttu-id="302a9-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="302a9-137">OUTPUTS</span></span>

### <span data-ttu-id="302a9-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. Alert</span><span class="sxs-lookup"><span data-stu-id="302a9-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="302a9-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="302a9-139">NOTES</span></span>

## <span data-ttu-id="302a9-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="302a9-140">RELATED LINKS</span></span>
