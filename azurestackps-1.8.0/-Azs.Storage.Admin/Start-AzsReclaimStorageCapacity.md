---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c7ec31ce2af23a4376f8b5f94deca302345e81
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827687"
---
# <span data-ttu-id="907cb-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="907cb-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="907cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="907cb-102">SYNOPSIS</span></span>
<span data-ttu-id="907cb-103">Starten der Garbage Collection für gelöschte Speicherobjekte</span><span class="sxs-lookup"><span data-stu-id="907cb-103">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="907cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="907cb-104">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [[-ResourceGroupName] <String>] [-FarmName] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="907cb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="907cb-105">DESCRIPTION</span></span>
<span data-ttu-id="907cb-106">Starten der Garbage Collection für gelöschte Speicherobjekte</span><span class="sxs-lookup"><span data-stu-id="907cb-106">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="907cb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="907cb-107">EXAMPLES</span></span>

### <span data-ttu-id="907cb-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="907cb-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsReclaimStorageCapacity -FarmName "44263c10-13b2-4912-9b17-85c1e43b2a30"
```

<span data-ttu-id="907cb-109">Starten Sie die Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="907cb-109">Start garbage collection.</span></span>

## <span data-ttu-id="907cb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="907cb-110">PARAMETERS</span></span>

### <span data-ttu-id="907cb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="907cb-111">-AsJob</span></span>
<span data-ttu-id="907cb-112">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="907cb-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="907cb-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="907cb-113">-FarmName</span></span>
<span data-ttu-id="907cb-114">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="907cb-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907cb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="907cb-115">-Force</span></span>
<span data-ttu-id="907cb-116">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="907cb-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="907cb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="907cb-117">-ResourceGroupName</span></span>
<span data-ttu-id="907cb-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="907cb-118">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907cb-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="907cb-119">-Confirm</span></span>
<span data-ttu-id="907cb-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="907cb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="907cb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="907cb-121">-WhatIf</span></span>
<span data-ttu-id="907cb-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="907cb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="907cb-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="907cb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="907cb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="907cb-124">CommonParameters</span></span>
<span data-ttu-id="907cb-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="907cb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="907cb-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="907cb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="907cb-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="907cb-127">INPUTS</span></span>

## <span data-ttu-id="907cb-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="907cb-128">OUTPUTS</span></span>

## <span data-ttu-id="907cb-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="907cb-129">NOTES</span></span>

## <span data-ttu-id="907cb-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="907cb-130">RELATED LINKS</span></span>

