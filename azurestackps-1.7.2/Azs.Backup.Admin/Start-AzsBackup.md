---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 460d24e091a702cfee32b8c5b7d9c3a8016e73b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827324"
---
# <span data-ttu-id="01ea1-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="01ea1-101">Start-AzsBackup</span></span>

## <span data-ttu-id="01ea1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="01ea1-102">SYNOPSIS</span></span>
<span data-ttu-id="01ea1-103">Sichern eines bestimmten Speicherorts</span><span class="sxs-lookup"><span data-stu-id="01ea1-103">Back up a specific location.</span></span>

## <span data-ttu-id="01ea1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="01ea1-104">SYNTAX</span></span>

### <span data-ttu-id="01ea1-105">CreateBackup (Standard)</span><span class="sxs-lookup"><span data-stu-id="01ea1-105">CreateBackup (Default)</span></span>
```
Start-AzsBackup [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01ea1-106">CreateBackup_FromResourceId</span><span class="sxs-lookup"><span data-stu-id="01ea1-106">CreateBackup_FromResourceId</span></span>
```
Start-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01ea1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="01ea1-107">DESCRIPTION</span></span>
<span data-ttu-id="01ea1-108">Sichern eines bestimmten Speicherorts</span><span class="sxs-lookup"><span data-stu-id="01ea1-108">Back up a specific location.</span></span>

## <span data-ttu-id="01ea1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="01ea1-109">EXAMPLES</span></span>

### <span data-ttu-id="01ea1-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="01ea1-110">EXAMPLE 1</span></span>
```
Start-AzsBackup
```

<span data-ttu-id="01ea1-111">Starten Sie eine Azure Stack-Sicherung.</span><span class="sxs-lookup"><span data-stu-id="01ea1-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="01ea1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="01ea1-112">PARAMETERS</span></span>

### <span data-ttu-id="01ea1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01ea1-113">-AsJob</span></span>
<span data-ttu-id="01ea1-114">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="01ea1-114">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ea1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="01ea1-115">-Force</span></span>
<span data-ttu-id="01ea1-116">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="01ea1-116">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ea1-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="01ea1-117">-Location</span></span>
<span data-ttu-id="01ea1-118">Der Name des Sicherungsspeicherorts.</span><span class="sxs-lookup"><span data-stu-id="01ea1-118">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ea1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01ea1-119">-ResourceGroupName</span></span>
<span data-ttu-id="01ea1-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="01ea1-120">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ea1-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="01ea1-121">-ResourceId</span></span>
<span data-ttu-id="01ea1-122">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="01ea1-122">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBackup_FromResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01ea1-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="01ea1-123">-Confirm</span></span>
<span data-ttu-id="01ea1-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="01ea1-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ea1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01ea1-125">-WhatIf</span></span>
<span data-ttu-id="01ea1-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01ea1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01ea1-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01ea1-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ea1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01ea1-128">CommonParameters</span></span>
<span data-ttu-id="01ea1-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01ea1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01ea1-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01ea1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01ea1-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="01ea1-131">INPUTS</span></span>

## <span data-ttu-id="01ea1-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="01ea1-132">OUTPUTS</span></span>

### <span data-ttu-id="01ea1-133">Microsoft. AzureStack. Management. Backup. admin. Models. LongRunningOperationStatus</span><span class="sxs-lookup"><span data-stu-id="01ea1-133">Microsoft.AzureStack.Management.Backup.Admin.Models.LongRunningOperationStatus</span></span>

## <span data-ttu-id="01ea1-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="01ea1-134">NOTES</span></span>

## <span data-ttu-id="01ea1-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="01ea1-135">RELATED LINKS</span></span>
