---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b6e8139f201a69684d4236a5e84e89f6607c5c
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007008"
---
# <span data-ttu-id="1bba3-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bba3-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="1bba3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1bba3-102">SYNOPSIS</span></span>
<span data-ttu-id="1bba3-103">Legen Sie die Sicherungskonfiguration am angegebenen Speicherort fest.</span><span class="sxs-lookup"><span data-stu-id="1bba3-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="1bba3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bba3-104">SYNTAX</span></span>

### <span data-ttu-id="1bba3-105">Update (Standard)</span><span class="sxs-lookup"><span data-stu-id="1bba3-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionKey <SecureString>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bba3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1bba3-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1bba3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bba3-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1bba3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1bba3-108">DESCRIPTION</span></span>
<span data-ttu-id="1bba3-109">Legen Sie die Sicherungskonfiguration am angegebenen Speicherort fest.</span><span class="sxs-lookup"><span data-stu-id="1bba3-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="1bba3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1bba3-110">EXAMPLES</span></span>

### <span data-ttu-id="1bba3-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1bba3-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionKey $encryptionKey
```

<span data-ttu-id="1bba3-112">Konfigurieren Sie die Azure Stack-Sicherungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="1bba3-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="1bba3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bba3-113">PARAMETERS</span></span>

### <span data-ttu-id="1bba3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1bba3-114">-AsJob</span></span>
<span data-ttu-id="1bba3-115">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="1bba3-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="1bba3-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="1bba3-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="1bba3-117">Das Intervall in Stunden für die Häufigkeit, mit der der Planer eine Sicherung ausführt.</span><span class="sxs-lookup"><span data-stu-id="1bba3-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

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

### <span data-ttu-id="1bba3-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="1bba3-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="1bba3-119">Der Aufbewahrungszeitraum in Tagen für Sicherungen am Speicherort.</span><span class="sxs-lookup"><span data-stu-id="1bba3-119">The retention period, in days, for backups in the storage location.</span></span>

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

### <span data-ttu-id="1bba3-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1bba3-120">-EncryptionKey</span></span>
<span data-ttu-id="1bba3-121">Verschlüsselungsschlüssel, der zum Verschlüsseln von Sicherungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1bba3-121">Encryption key used to encrypt backups.</span></span>

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

### <span data-ttu-id="1bba3-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1bba3-122">-InputObject</span></span>
<span data-ttu-id="1bba3-123">Von Get-AzsBackupConfiguration zurückgegebene Backup-Standortkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="1bba3-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

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

### <span data-ttu-id="1bba3-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="1bba3-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="1bba3-125">Gibt an, ob der Sicherungszeitplan aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1bba3-125">Whether the backup scheduler should be enabled.</span></span>

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

### <span data-ttu-id="1bba3-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="1bba3-126">-Location</span></span>
<span data-ttu-id="1bba3-127">Der Speicherort, den Sie konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="1bba3-127">Location to configure.</span></span>

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

### <span data-ttu-id="1bba3-128">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="1bba3-128">-Password</span></span>
<span data-ttu-id="1bba3-129">Kennwort, das für den Zugriff auf den Sicherungsspeicherort erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1bba3-129">Password required to access backup location.</span></span>

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

### <span data-ttu-id="1bba3-130">-Path</span><span class="sxs-lookup"><span data-stu-id="1bba3-130">-Path</span></span>
<span data-ttu-id="1bba3-131">Der Speicherort, an dem Sicherungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1bba3-131">Location where backups will be stored.</span></span>

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

### <span data-ttu-id="1bba3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bba3-132">-ResourceGroupName</span></span>
<span data-ttu-id="1bba3-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1bba3-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="1bba3-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1bba3-134">-ResourceId</span></span>
<span data-ttu-id="1bba3-135">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="1bba3-135">The resource id.</span></span>

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

### <span data-ttu-id="1bba3-136">-Username</span><span class="sxs-lookup"><span data-stu-id="1bba3-136">-Username</span></span>
<span data-ttu-id="1bba3-137">Der für den Zugriff auf den Sicherungsspeicherort erforderliche Benutzername.</span><span class="sxs-lookup"><span data-stu-id="1bba3-137">Username required to access backup location.</span></span>

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

### <span data-ttu-id="1bba3-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1bba3-138">-Confirm</span></span>
<span data-ttu-id="1bba3-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1bba3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bba3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bba3-140">-WhatIf</span></span>
<span data-ttu-id="1bba3-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1bba3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bba3-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1bba3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bba3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bba3-143">CommonParameters</span></span>
<span data-ttu-id="1bba3-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bba3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bba3-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bba3-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bba3-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1bba3-146">INPUTS</span></span>

## <span data-ttu-id="1bba3-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1bba3-147">OUTPUTS</span></span>

### <span data-ttu-id="1bba3-148">Microsoft. AzureStack. Management. Backup. admin. Models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="1bba3-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="1bba3-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="1bba3-149">NOTES</span></span>

## <span data-ttu-id="1bba3-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1bba3-150">RELATED LINKS</span></span>

