---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94609250696a99a337153e9e0d3a1d092e380c40
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007376"
---
# <span data-ttu-id="5bdef-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="5bdef-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="5bdef-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5bdef-102">SYNOPSIS</span></span>
<span data-ttu-id="5bdef-103">Löschen eines Kontingents nach Name</span><span class="sxs-lookup"><span data-stu-id="5bdef-103">Delete a quota by name.</span></span>

## <span data-ttu-id="5bdef-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bdef-104">SYNTAX</span></span>

### <span data-ttu-id="5bdef-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="5bdef-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5bdef-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bdef-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bdef-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5bdef-107">DESCRIPTION</span></span>
<span data-ttu-id="5bdef-108">Löschen eines Kontingents nach Name</span><span class="sxs-lookup"><span data-stu-id="5bdef-108">Delete a quota by name.</span></span>

## <span data-ttu-id="5bdef-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5bdef-109">EXAMPLES</span></span>

### <span data-ttu-id="5bdef-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5bdef-110">EXAMPLE 1</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="5bdef-111">Entfernen eines Netzwerk Kontingents nach Namen</span><span class="sxs-lookup"><span data-stu-id="5bdef-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="5bdef-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5bdef-112">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="5bdef-113">Entfernen eines Netzwerk Kontingents mithilfe einer Pipe</span><span class="sxs-lookup"><span data-stu-id="5bdef-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="5bdef-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5bdef-114">EXAMPLE 3</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="5bdef-115">Entfernen eines Netzwerk Kontingents</span><span class="sxs-lookup"><span data-stu-id="5bdef-115">Remove a network quota.</span></span>

## <span data-ttu-id="5bdef-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="5bdef-116">PARAMETERS</span></span>

### <span data-ttu-id="5bdef-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5bdef-117">-Name</span></span>
<span data-ttu-id="5bdef-118">Der Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="5bdef-118">Name of the resource.</span></span>

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

### <span data-ttu-id="5bdef-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="5bdef-119">-Location</span></span>
<span data-ttu-id="5bdef-120">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="5bdef-120">Location of the resource.</span></span>

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

### <span data-ttu-id="5bdef-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5bdef-121">-ResourceId</span></span>
<span data-ttu-id="5bdef-122">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="5bdef-122">The resource id.</span></span>

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

### <span data-ttu-id="5bdef-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5bdef-123">-AsJob</span></span>
<span data-ttu-id="5bdef-124">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="5bdef-124">Run asynchronous as a job and return the job object.</span></span>


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

### <span data-ttu-id="5bdef-125">-Force</span><span class="sxs-lookup"><span data-stu-id="5bdef-125">-Force</span></span>
<span data-ttu-id="5bdef-126">Parameter wechseln, um die Bestätigung nicht zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="5bdef-126">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="5bdef-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bdef-127">-WhatIf</span></span>
<span data-ttu-id="5bdef-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5bdef-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bdef-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5bdef-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bdef-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5bdef-130">-Confirm</span></span>
<span data-ttu-id="5bdef-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5bdef-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bdef-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bdef-132">CommonParameters</span></span>
<span data-ttu-id="5bdef-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bdef-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bdef-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bdef-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bdef-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5bdef-135">INPUTS</span></span>

## <span data-ttu-id="5bdef-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5bdef-136">OUTPUTS</span></span>

## <span data-ttu-id="5bdef-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="5bdef-137">NOTES</span></span>

## <span data-ttu-id="5bdef-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5bdef-138">RELATED LINKS</span></span>
