---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 385947ead1039103933cb7e752dc5dee768b388a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475581"
---
# <span data-ttu-id="9ae9f-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="9ae9f-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="9ae9f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ae9f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ae9f-103">Wiederherstellen einer Sicherung</span><span class="sxs-lookup"><span data-stu-id="9ae9f-103">Restore a backup.</span></span>

## <span data-ttu-id="9ae9f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ae9f-104">SYNTAX</span></span>

### <span data-ttu-id="9ae9f-105">Backups_Restore (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ae9f-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ae9f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ae9f-106">ResourceId</span></span>
```
Restore-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ae9f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ae9f-107">DESCRIPTION</span></span>
<span data-ttu-id="9ae9f-108">Wiederherstellen einer Sicherung</span><span class="sxs-lookup"><span data-stu-id="9ae9f-108">Restore a backup.</span></span>

## <span data-ttu-id="9ae9f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ae9f-109">EXAMPLES</span></span>

### <span data-ttu-id="9ae9f-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9ae9f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsBackup -Backup 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e
```

<span data-ttu-id="9ae9f-111">Wiederherstellen aus einer Azure Stack-Sicherung</span><span class="sxs-lookup"><span data-stu-id="9ae9f-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="9ae9f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ae9f-112">PARAMETERS</span></span>

### <span data-ttu-id="9ae9f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ae9f-113">-AsJob</span></span>
<span data-ttu-id="9ae9f-114">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="9ae9f-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="9ae9f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9ae9f-115">-Force</span></span>
<span data-ttu-id="9ae9f-116">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="9ae9f-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="9ae9f-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="9ae9f-117">-Location</span></span>
<span data-ttu-id="9ae9f-118">Name des zu sichernden Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="9ae9f-118">Name of location to backup.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ae9f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9ae9f-119">-Name</span></span>
<span data-ttu-id="9ae9f-120">Der Name der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="9ae9f-120">Name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ae9f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ae9f-121">-ResourceGroupName</span></span>
<span data-ttu-id="9ae9f-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9ae9f-122">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ae9f-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9ae9f-123">-ResourceId</span></span>
<span data-ttu-id="9ae9f-124">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="9ae9f-124">The resource id.</span></span>

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

### <span data-ttu-id="9ae9f-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9ae9f-125">-Confirm</span></span>
<span data-ttu-id="9ae9f-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ae9f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ae9f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ae9f-127">-WhatIf</span></span>
<span data-ttu-id="9ae9f-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ae9f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ae9f-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ae9f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ae9f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ae9f-130">CommonParameters</span></span>
<span data-ttu-id="9ae9f-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ae9f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ae9f-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ae9f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ae9f-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ae9f-133">INPUTS</span></span>

## <span data-ttu-id="9ae9f-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ae9f-134">OUTPUTS</span></span>

## <span data-ttu-id="9ae9f-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ae9f-135">NOTES</span></span>

## <span data-ttu-id="9ae9f-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ae9f-136">RELATED LINKS</span></span>

