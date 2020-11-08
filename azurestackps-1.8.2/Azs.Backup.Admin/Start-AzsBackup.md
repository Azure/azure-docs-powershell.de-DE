---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bf583c30d2faff1055debf366a84a0739789467
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007010"
---
# <span data-ttu-id="5fe2f-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="5fe2f-101">Start-AzsBackup</span></span>

## <span data-ttu-id="5fe2f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5fe2f-102">SYNOPSIS</span></span>
<span data-ttu-id="5fe2f-103">Sichern eines bestimmten Speicherorts</span><span class="sxs-lookup"><span data-stu-id="5fe2f-103">Back up a specific location.</span></span>

## <span data-ttu-id="5fe2f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fe2f-104">SYNTAX</span></span>

### <span data-ttu-id="5fe2f-105">CreateBackup (Standard)</span><span class="sxs-lookup"><span data-stu-id="5fe2f-105">CreateBackup (Default)</span></span>
```
Start-AzsBackup [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fe2f-106">CreateBackup_FromResourceId</span><span class="sxs-lookup"><span data-stu-id="5fe2f-106">CreateBackup_FromResourceId</span></span>
```
Start-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fe2f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5fe2f-107">DESCRIPTION</span></span>
<span data-ttu-id="5fe2f-108">Sichern eines bestimmten Speicherorts</span><span class="sxs-lookup"><span data-stu-id="5fe2f-108">Back up a specific location.</span></span>

## <span data-ttu-id="5fe2f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5fe2f-109">EXAMPLES</span></span>

### <span data-ttu-id="5fe2f-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5fe2f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsBackup
```

<span data-ttu-id="5fe2f-111">Starten Sie eine Azure Stack-Sicherung.</span><span class="sxs-lookup"><span data-stu-id="5fe2f-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="5fe2f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5fe2f-112">PARAMETERS</span></span>

### <span data-ttu-id="5fe2f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fe2f-113">-AsJob</span></span>
<span data-ttu-id="5fe2f-114">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="5fe2f-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="5fe2f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5fe2f-115">-Force</span></span>
<span data-ttu-id="5fe2f-116">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="5fe2f-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="5fe2f-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="5fe2f-117">-Location</span></span>
<span data-ttu-id="5fe2f-118">Der Name des Sicherungsspeicherorts.</span><span class="sxs-lookup"><span data-stu-id="5fe2f-118">Name of the backup location.</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe2f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fe2f-119">-ResourceGroupName</span></span>
<span data-ttu-id="5fe2f-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5fe2f-120">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe2f-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5fe2f-121">-ResourceId</span></span>
<span data-ttu-id="5fe2f-122">{{Fill resourcel Description}}</span><span class="sxs-lookup"><span data-stu-id="5fe2f-122">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup_FromResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fe2f-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5fe2f-123">-Confirm</span></span>
<span data-ttu-id="5fe2f-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5fe2f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fe2f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fe2f-125">-WhatIf</span></span>
<span data-ttu-id="5fe2f-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5fe2f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fe2f-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5fe2f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fe2f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe2f-128">CommonParameters</span></span>
<span data-ttu-id="5fe2f-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fe2f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe2f-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fe2f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe2f-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5fe2f-131">INPUTS</span></span>

## <span data-ttu-id="5fe2f-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5fe2f-132">OUTPUTS</span></span>

### <span data-ttu-id="5fe2f-133">Microsoft. AzureStack. Management. Backup. admin. Models. LongRunningOperationStatus</span><span class="sxs-lookup"><span data-stu-id="5fe2f-133">Microsoft.AzureStack.Management.Backup.Admin.Models.LongRunningOperationStatus</span></span>

## <span data-ttu-id="5fe2f-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="5fe2f-134">NOTES</span></span>

## <span data-ttu-id="5fe2f-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5fe2f-135">RELATED LINKS</span></span>

