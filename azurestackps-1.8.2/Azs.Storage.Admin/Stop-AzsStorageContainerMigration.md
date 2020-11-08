---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8c9a27b1722c1c7f08d9daeab0205dd20d9ba8b9
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006809"
---
# <span data-ttu-id="398b2-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="398b2-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="398b2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="398b2-102">SYNOPSIS</span></span>
<span data-ttu-id="398b2-103">Abbrechen eines Container Migrationsauftrags</span><span class="sxs-lookup"><span data-stu-id="398b2-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="398b2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="398b2-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="398b2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="398b2-105">DESCRIPTION</span></span>
<span data-ttu-id="398b2-106">Abbrechen eines Container Migrationsauftrags</span><span class="sxs-lookup"><span data-stu-id="398b2-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="398b2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="398b2-107">EXAMPLES</span></span>

### <span data-ttu-id="398b2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="398b2-108">EXAMPLE 1</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="398b2-109">Abbrechen der Container Migration</span><span class="sxs-lookup"><span data-stu-id="398b2-109">Cancel container migration.</span></span>

## <span data-ttu-id="398b2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="398b2-110">PARAMETERS</span></span>

### <span data-ttu-id="398b2-111">-JobId</span><span class="sxs-lookup"><span data-stu-id="398b2-111">-JobId</span></span>
<span data-ttu-id="398b2-112">Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="398b2-112">Operation Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="398b2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="398b2-113">-ResourceGroupName</span></span>
<span data-ttu-id="398b2-114">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="398b2-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="398b2-115">-Farmname</span><span class="sxs-lookup"><span data-stu-id="398b2-115">-FarmName</span></span>
<span data-ttu-id="398b2-116">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="398b2-116">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="398b2-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="398b2-117">-AsJob</span></span>
<span data-ttu-id="398b2-118">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="398b2-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="398b2-119">-Force</span><span class="sxs-lookup"><span data-stu-id="398b2-119">-Force</span></span>
<span data-ttu-id="398b2-120">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="398b2-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="398b2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="398b2-121">-WhatIf</span></span>
<span data-ttu-id="398b2-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="398b2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="398b2-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="398b2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="398b2-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="398b2-124">-Confirm</span></span>
<span data-ttu-id="398b2-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="398b2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="398b2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="398b2-126">CommonParameters</span></span>
<span data-ttu-id="398b2-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="398b2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="398b2-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="398b2-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="398b2-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="398b2-129">INPUTS</span></span>

## <span data-ttu-id="398b2-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="398b2-130">OUTPUTS</span></span>

## <span data-ttu-id="398b2-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="398b2-131">NOTES</span></span>

## <span data-ttu-id="398b2-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="398b2-132">RELATED LINKS</span></span>
