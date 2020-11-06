---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f7f40982a4c7d24e02e7e365163cc6250ff8791
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475546"
---
# <span data-ttu-id="854f7-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="854f7-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="854f7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="854f7-102">SYNOPSIS</span></span>
<span data-ttu-id="854f7-103">Löschen eines Kontingents nach Name</span><span class="sxs-lookup"><span data-stu-id="854f7-103">Delete a quota by name.</span></span>

## <span data-ttu-id="854f7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="854f7-104">SYNTAX</span></span>

### <span data-ttu-id="854f7-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="854f7-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="854f7-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="854f7-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="854f7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="854f7-107">DESCRIPTION</span></span>
<span data-ttu-id="854f7-108">Löschen eines Kontingents nach Name</span><span class="sxs-lookup"><span data-stu-id="854f7-108">Delete a quota by name.</span></span>

## <span data-ttu-id="854f7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="854f7-109">EXAMPLES</span></span>

### <span data-ttu-id="854f7-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="854f7-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="854f7-111">Entfernen eines Netzwerk Kontingents nach Namen</span><span class="sxs-lookup"><span data-stu-id="854f7-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="854f7-112">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="854f7-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="854f7-113">Entfernen eines Netzwerk Kontingents mithilfe einer Pipe</span><span class="sxs-lookup"><span data-stu-id="854f7-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="854f7-114">--------------------------Beispiel 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="854f7-114">-------------------------- EXAMPLE 3 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="854f7-115">Entfernen eines Netzwerk Kontingents</span><span class="sxs-lookup"><span data-stu-id="854f7-115">Remove a network quota.</span></span>

## <span data-ttu-id="854f7-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="854f7-116">PARAMETERS</span></span>

### <span data-ttu-id="854f7-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="854f7-117">-AsJob</span></span>
<span data-ttu-id="854f7-118">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="854f7-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="854f7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="854f7-119">-Force</span></span>
<span data-ttu-id="854f7-120">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="854f7-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="854f7-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="854f7-121">-Location</span></span>
<span data-ttu-id="854f7-122">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="854f7-122">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="854f7-123">-Name</span><span class="sxs-lookup"><span data-stu-id="854f7-123">-Name</span></span>
<span data-ttu-id="854f7-124">Der Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="854f7-124">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="854f7-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="854f7-125">-ResourceId</span></span>
<span data-ttu-id="854f7-126">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="854f7-126">The resource id.</span></span>

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

### <span data-ttu-id="854f7-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="854f7-127">-Confirm</span></span>
<span data-ttu-id="854f7-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="854f7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="854f7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="854f7-129">-WhatIf</span></span>
<span data-ttu-id="854f7-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="854f7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="854f7-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="854f7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="854f7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="854f7-132">CommonParameters</span></span>
<span data-ttu-id="854f7-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="854f7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="854f7-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="854f7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="854f7-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="854f7-135">INPUTS</span></span>

## <span data-ttu-id="854f7-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="854f7-136">OUTPUTS</span></span>

## <span data-ttu-id="854f7-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="854f7-137">NOTES</span></span>

## <span data-ttu-id="854f7-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="854f7-138">RELATED LINKS</span></span>

