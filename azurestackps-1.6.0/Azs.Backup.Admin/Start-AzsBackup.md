---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c7dff6c2d9c191d852420ab2c2017a0b9d1cf8d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475577"
---
# <span data-ttu-id="35435-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="35435-101">Start-AzsBackup</span></span>

## <span data-ttu-id="35435-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35435-102">SYNOPSIS</span></span>
<span data-ttu-id="35435-103">Sichern eines bestimmten Speicherorts</span><span class="sxs-lookup"><span data-stu-id="35435-103">Back up a specific location.</span></span>

## <span data-ttu-id="35435-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35435-104">SYNTAX</span></span>

### <span data-ttu-id="35435-105">CreateBackup (Standard)</span><span class="sxs-lookup"><span data-stu-id="35435-105">CreateBackup (Default)</span></span>
```
Start-AzsBackup [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35435-106">CreateBackup_FromResourceId</span><span class="sxs-lookup"><span data-stu-id="35435-106">CreateBackup_FromResourceId</span></span>
```
Start-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35435-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35435-107">DESCRIPTION</span></span>
<span data-ttu-id="35435-108">Sichern eines bestimmten Speicherorts</span><span class="sxs-lookup"><span data-stu-id="35435-108">Back up a specific location.</span></span>

## <span data-ttu-id="35435-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35435-109">EXAMPLES</span></span>

### <span data-ttu-id="35435-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="35435-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsBackup
```

<span data-ttu-id="35435-111">Starten Sie eine Azure Stack-Sicherung.</span><span class="sxs-lookup"><span data-stu-id="35435-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="35435-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="35435-112">PARAMETERS</span></span>

### <span data-ttu-id="35435-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35435-113">-AsJob</span></span>
<span data-ttu-id="35435-114">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="35435-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="35435-115">-Force</span><span class="sxs-lookup"><span data-stu-id="35435-115">-Force</span></span>
<span data-ttu-id="35435-116">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="35435-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="35435-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="35435-117">-Location</span></span>
<span data-ttu-id="35435-118">Der Name des Sicherungsspeicherorts.</span><span class="sxs-lookup"><span data-stu-id="35435-118">Name of the backup location.</span></span>

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

### <span data-ttu-id="35435-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35435-119">-ResourceGroupName</span></span>
<span data-ttu-id="35435-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="35435-120">Name of the resource group.</span></span>

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

### <span data-ttu-id="35435-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="35435-121">-ResourceId</span></span>
<span data-ttu-id="35435-122">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="35435-122">The resource id.</span></span>

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

### <span data-ttu-id="35435-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="35435-123">-Confirm</span></span>
<span data-ttu-id="35435-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="35435-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35435-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35435-125">-WhatIf</span></span>
<span data-ttu-id="35435-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="35435-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35435-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="35435-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35435-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35435-128">CommonParameters</span></span>
<span data-ttu-id="35435-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35435-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35435-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35435-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35435-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35435-131">INPUTS</span></span>

## <span data-ttu-id="35435-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35435-132">OUTPUTS</span></span>

### <span data-ttu-id="35435-133">Microsoft. AzureStack. Management. Backup. admin. Models. LongRunningOperationStatus</span><span class="sxs-lookup"><span data-stu-id="35435-133">Microsoft.AzureStack.Management.Backup.Admin.Models.LongRunningOperationStatus</span></span>

## <span data-ttu-id="35435-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="35435-134">NOTES</span></span>

## <span data-ttu-id="35435-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35435-135">RELATED LINKS</span></span>

