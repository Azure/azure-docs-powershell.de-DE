---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81bdb6a75e10af30b6febe9bbbf0989933818aec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822700"
---
# <span data-ttu-id="1d82f-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="1d82f-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="1d82f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1d82f-102">SYNOPSIS</span></span>
<span data-ttu-id="1d82f-103">Abbrechen eines Container Migrationsauftrags</span><span class="sxs-lookup"><span data-stu-id="1d82f-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="1d82f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d82f-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d82f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d82f-105">DESCRIPTION</span></span>
<span data-ttu-id="1d82f-106">Abbrechen eines Container Migrationsauftrags</span><span class="sxs-lookup"><span data-stu-id="1d82f-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="1d82f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1d82f-107">EXAMPLES</span></span>

### <span data-ttu-id="1d82f-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1d82f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="1d82f-109">Abbrechen der Container Migration</span><span class="sxs-lookup"><span data-stu-id="1d82f-109">Cancel container migration.</span></span>

## <span data-ttu-id="1d82f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d82f-110">PARAMETERS</span></span>

### <span data-ttu-id="1d82f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d82f-111">-AsJob</span></span>
<span data-ttu-id="1d82f-112">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="1d82f-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="1d82f-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="1d82f-113">-FarmName</span></span>
<span data-ttu-id="1d82f-114">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="1d82f-114">Farm Id.</span></span>

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

### <span data-ttu-id="1d82f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1d82f-115">-Force</span></span>
<span data-ttu-id="1d82f-116">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="1d82f-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1d82f-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="1d82f-117">-JobId</span></span>
<span data-ttu-id="1d82f-118">Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="1d82f-118">Operation Id.</span></span>

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

### <span data-ttu-id="1d82f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d82f-119">-ResourceGroupName</span></span>
<span data-ttu-id="1d82f-120">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1d82f-120">Resource group name.</span></span>

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

### <span data-ttu-id="1d82f-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1d82f-121">-Confirm</span></span>
<span data-ttu-id="1d82f-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1d82f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d82f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d82f-123">-WhatIf</span></span>
<span data-ttu-id="1d82f-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d82f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d82f-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d82f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d82f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d82f-126">CommonParameters</span></span>
<span data-ttu-id="1d82f-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d82f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d82f-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d82f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d82f-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1d82f-129">INPUTS</span></span>

## <span data-ttu-id="1d82f-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1d82f-130">OUTPUTS</span></span>

## <span data-ttu-id="1d82f-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="1d82f-131">NOTES</span></span>

## <span data-ttu-id="1d82f-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1d82f-132">RELATED LINKS</span></span>

