---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ab432625ab6af4a8fbd23895cb82e1d9f83954c8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007137"
---
# <span data-ttu-id="4391a-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="4391a-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="4391a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4391a-102">SYNOPSIS</span></span>
<span data-ttu-id="4391a-103">Wenden Sie ein bestimmtes Update an einem Aktualisierungsspeicherort an.</span><span class="sxs-lookup"><span data-stu-id="4391a-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="4391a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4391a-104">SYNTAX</span></span>

### <span data-ttu-id="4391a-105">Übernehmen (Standard)</span><span class="sxs-lookup"><span data-stu-id="4391a-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4391a-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4391a-106">ResourceId</span></span>
```
Install-AzsUpdate [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4391a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4391a-107">DESCRIPTION</span></span>
<span data-ttu-id="4391a-108">Wenden Sie ein bestimmtes Update an einem Aktualisierungsspeicherort an.</span><span class="sxs-lookup"><span data-stu-id="4391a-108">Apply a specific update at an update location.</span></span> <span data-ttu-id="4391a-109">Nach dem aufrufen kann Get-AzsUpdateRun verwendet werden, um den Fortschritt des Updates zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4391a-109">After invoked, Get-AzsUpdateRun may be used to modify the progress of the update.</span></span>

## <span data-ttu-id="4391a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4391a-110">EXAMPLES</span></span>

### <span data-ttu-id="4391a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4391a-111">EXAMPLE 1</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1 | Install-AzsUpdate
```

<span data-ttu-id="4391a-112">Wenden Sie ein bestimmtes Update an einem Aktualisierungsspeicherort an.</span><span class="sxs-lookup"><span data-stu-id="4391a-112">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="4391a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4391a-113">PARAMETERS</span></span>

### <span data-ttu-id="4391a-114">-Name</span><span class="sxs-lookup"><span data-stu-id="4391a-114">-Name</span></span>
<span data-ttu-id="4391a-115">Der Name des Updates.</span><span class="sxs-lookup"><span data-stu-id="4391a-115">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4391a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4391a-116">-ResourceGroupName</span></span>
<span data-ttu-id="4391a-117">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="4391a-117">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4391a-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="4391a-118">-Location</span></span>
<span data-ttu-id="4391a-119">Der Name des Update Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="4391a-119">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4391a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4391a-120">-AsJob</span></span>
<span data-ttu-id="4391a-121">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="4391a-121">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="4391a-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4391a-122">-ResourceId</span></span>
<span data-ttu-id="4391a-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="4391a-123">The resource id.</span></span>

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

### <span data-ttu-id="4391a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="4391a-124">-Force</span></span>
<span data-ttu-id="4391a-125">Kennzeichnen, um das Element ohne Bestätigung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="4391a-125">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="4391a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4391a-126">-WhatIf</span></span>
<span data-ttu-id="4391a-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4391a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4391a-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4391a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4391a-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4391a-129">-Confirm</span></span>
<span data-ttu-id="4391a-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4391a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4391a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4391a-131">CommonParameters</span></span>
<span data-ttu-id="4391a-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4391a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4391a-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4391a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4391a-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4391a-134">INPUTS</span></span>

## <span data-ttu-id="4391a-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4391a-135">OUTPUTS</span></span>

### <span data-ttu-id="4391a-136">Microsoft. AzureStack. Management. Update. admin. Models. Update</span><span class="sxs-lookup"><span data-stu-id="4391a-136">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="4391a-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="4391a-137">NOTES</span></span>

## <span data-ttu-id="4391a-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4391a-138">RELATED LINKS</span></span>
