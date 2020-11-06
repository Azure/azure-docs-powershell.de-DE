---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4406dc4cadecd1945e82b8a90e9937df2183b4da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475513"
---
# <span data-ttu-id="2e634-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="2e634-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="2e634-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2e634-102">SYNOPSIS</span></span>
<span data-ttu-id="2e634-103">Wenden Sie ein bestimmtes Update an einem Aktualisierungsspeicherort an.</span><span class="sxs-lookup"><span data-stu-id="2e634-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="2e634-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e634-104">SYNTAX</span></span>

### <span data-ttu-id="2e634-105">Übernehmen (Standard)</span><span class="sxs-lookup"><span data-stu-id="2e634-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e634-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e634-106">ResourceId</span></span>
```
Install-AzsUpdate [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e634-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e634-107">DESCRIPTION</span></span>
<span data-ttu-id="2e634-108">Wenden Sie ein bestimmtes Update an einem Aktualisierungsspeicherort an.</span><span class="sxs-lookup"><span data-stu-id="2e634-108">Apply a specific update at an update location.</span></span> <span data-ttu-id="2e634-109">Nach dem aufrufen kann Get-AzsUpdateRun verwendet werden, um den Fortschritt des Updates zu ändern.</span><span class="sxs-lookup"><span data-stu-id="2e634-109">After invoked, Get-AzsUpdateRun may be used to modify the progress of the update.</span></span>

## <span data-ttu-id="2e634-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e634-110">EXAMPLES</span></span>

### <span data-ttu-id="2e634-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2e634-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1 | Install-AzsUpdate
```

<span data-ttu-id="2e634-112">Wenden Sie ein bestimmtes Update an einem Aktualisierungsspeicherort an.</span><span class="sxs-lookup"><span data-stu-id="2e634-112">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="2e634-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e634-113">PARAMETERS</span></span>

### <span data-ttu-id="2e634-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e634-114">-AsJob</span></span>
<span data-ttu-id="2e634-115">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="2e634-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="2e634-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2e634-116">-Force</span></span>
<span data-ttu-id="2e634-117">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="2e634-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2e634-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="2e634-118">-Location</span></span>
<span data-ttu-id="2e634-119">Der Name des Update Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="2e634-119">The name of the update location.</span></span>

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

### <span data-ttu-id="2e634-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2e634-120">-Name</span></span>
<span data-ttu-id="2e634-121">Der Name des Updates.</span><span class="sxs-lookup"><span data-stu-id="2e634-121">Name of the update.</span></span>

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

### <span data-ttu-id="2e634-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e634-122">-ResourceGroupName</span></span>
<span data-ttu-id="2e634-123">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="2e634-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="2e634-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2e634-124">-ResourceId</span></span>
<span data-ttu-id="2e634-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="2e634-125">The resource id.</span></span>

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

### <span data-ttu-id="2e634-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2e634-126">-Confirm</span></span>
<span data-ttu-id="2e634-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2e634-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e634-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e634-128">-WhatIf</span></span>
<span data-ttu-id="2e634-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2e634-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e634-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2e634-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e634-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e634-131">CommonParameters</span></span>
<span data-ttu-id="2e634-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e634-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e634-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e634-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e634-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2e634-134">INPUTS</span></span>

## <span data-ttu-id="2e634-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2e634-135">OUTPUTS</span></span>

### <span data-ttu-id="2e634-136">Microsoft. AzureStack. Management. Update. admin. Models. Update</span><span class="sxs-lookup"><span data-stu-id="2e634-136">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="2e634-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="2e634-137">NOTES</span></span>

## <span data-ttu-id="2e634-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2e634-138">RELATED LINKS</span></span>

