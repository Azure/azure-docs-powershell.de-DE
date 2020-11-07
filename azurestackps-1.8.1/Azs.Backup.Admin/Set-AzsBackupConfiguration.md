---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b6e8139f201a69684d4236a5e84e89f6607c5c
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840843"
---
# <span data-ttu-id="28d2e-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="28d2e-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="28d2e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="28d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="28d2e-103">Legen Sie die Sicherungskonfiguration am angegebenen Speicherort fest.</span><span class="sxs-lookup"><span data-stu-id="28d2e-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="28d2e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="28d2e-104">SYNTAX</span></span>

### <span data-ttu-id="28d2e-105">Update (Standard)</span><span class="sxs-lookup"><span data-stu-id="28d2e-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionKey <SecureString>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28d2e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="28d2e-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28d2e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="28d2e-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28d2e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28d2e-108">DESCRIPTION</span></span>
<span data-ttu-id="28d2e-109">Legen Sie die Sicherungskonfiguration am angegebenen Speicherort fest.</span><span class="sxs-lookup"><span data-stu-id="28d2e-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="28d2e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="28d2e-110">EXAMPLES</span></span>

### <span data-ttu-id="28d2e-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="28d2e-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionKey $encryptionKey
```

<span data-ttu-id="28d2e-112">Konfigurieren Sie die Azure Stack-Sicherungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="28d2e-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="28d2e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="28d2e-113">PARAMETERS</span></span>

### <span data-ttu-id="28d2e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28d2e-114">-AsJob</span></span>
<span data-ttu-id="28d2e-115">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="28d2e-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="28d2e-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="28d2e-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="28d2e-117">Das Intervall in Stunden für die Häufigkeit, mit der der Planer eine Sicherung ausführt.</span><span class="sxs-lookup"><span data-stu-id="28d2e-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d2e-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="28d2e-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="28d2e-119">Der Aufbewahrungszeitraum in Tagen für Sicherungen am Speicherort.</span><span class="sxs-lookup"><span data-stu-id="28d2e-119">The retention period, in days, for backups in the storage location.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d2e-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="28d2e-120">-EncryptionKey</span></span>
<span data-ttu-id="28d2e-121">Verschlüsselungsschlüssel, der zum Verschlüsseln von Sicherungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="28d2e-121">Encryption key used to encrypt backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d2e-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="28d2e-122">-InputObject</span></span>
<span data-ttu-id="28d2e-123">Von Get-AzsBackupConfiguration zurückgegebene Backup-Standortkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="28d2e-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

```yaml
Type: BackupLocation
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28d2e-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="28d2e-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="28d2e-125">Gibt an, ob der Sicherungszeitplan aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="28d2e-125">Whether the backup scheduler should be enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d2e-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="28d2e-126">-Location</span></span>
<span data-ttu-id="28d2e-127">Der Speicherort, den Sie konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="28d2e-127">Location to configure.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d2e-128">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="28d2e-128">-Password</span></span>
<span data-ttu-id="28d2e-129">Kennwort, das für den Zugriff auf den Sicherungsspeicherort erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="28d2e-129">Password required to access backup location.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d2e-130">-Path</span><span class="sxs-lookup"><span data-stu-id="28d2e-130">-Path</span></span>
<span data-ttu-id="28d2e-131">Der Speicherort, an dem Sicherungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="28d2e-131">Location where backups will be stored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: BackupShare

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d2e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28d2e-132">-ResourceGroupName</span></span>
<span data-ttu-id="28d2e-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="28d2e-133">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d2e-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="28d2e-134">-ResourceId</span></span>
<span data-ttu-id="28d2e-135">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="28d2e-135">The resource id.</span></span>

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

### <span data-ttu-id="28d2e-136">-Username</span><span class="sxs-lookup"><span data-stu-id="28d2e-136">-Username</span></span>
<span data-ttu-id="28d2e-137">Der für den Zugriff auf den Sicherungsspeicherort erforderliche Benutzername.</span><span class="sxs-lookup"><span data-stu-id="28d2e-137">Username required to access backup location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d2e-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="28d2e-138">-Confirm</span></span>
<span data-ttu-id="28d2e-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="28d2e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28d2e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28d2e-140">-WhatIf</span></span>
<span data-ttu-id="28d2e-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28d2e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28d2e-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="28d2e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28d2e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28d2e-143">CommonParameters</span></span>
<span data-ttu-id="28d2e-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28d2e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28d2e-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28d2e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28d2e-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="28d2e-146">INPUTS</span></span>

## <span data-ttu-id="28d2e-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="28d2e-147">OUTPUTS</span></span>

### <span data-ttu-id="28d2e-148">Microsoft. AzureStack. Management. Backup. admin. Models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="28d2e-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="28d2e-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="28d2e-149">NOTES</span></span>

## <span data-ttu-id="28d2e-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="28d2e-150">RELATED LINKS</span></span>

