---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd5f27a942a33082b9488f74cac2779107f7371f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827327"
---
# <span data-ttu-id="15ed2-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="15ed2-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="15ed2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="15ed2-102">SYNOPSIS</span></span>
<span data-ttu-id="15ed2-103">Legen Sie die Sicherungskonfiguration am angegebenen Speicherort fest.</span><span class="sxs-lookup"><span data-stu-id="15ed2-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="15ed2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="15ed2-104">SYNTAX</span></span>

### <span data-ttu-id="15ed2-105">Update (Standard)</span><span class="sxs-lookup"><span data-stu-id="15ed2-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionCertPath <String>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15ed2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="15ed2-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionCertPath <String>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15ed2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="15ed2-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionCertPath <String>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15ed2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15ed2-108">DESCRIPTION</span></span>
<span data-ttu-id="15ed2-109">Legen Sie die Sicherungskonfiguration am angegebenen Speicherort fest.</span><span class="sxs-lookup"><span data-stu-id="15ed2-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="15ed2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15ed2-110">EXAMPLES</span></span>

### <span data-ttu-id="15ed2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="15ed2-111">EXAMPLE 1</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionCertPath $encryptionCertPath
```

<span data-ttu-id="15ed2-112">Konfigurieren Sie die Azure Stack-Sicherungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="15ed2-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="15ed2-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="15ed2-113">PARAMETERS</span></span>

### <span data-ttu-id="15ed2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15ed2-114">-AsJob</span></span>
<span data-ttu-id="15ed2-115">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="15ed2-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="15ed2-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="15ed2-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="15ed2-117">Das Intervall in Stunden für die Häufigkeit, mit der der Planer eine Sicherung ausführt.</span><span class="sxs-lookup"><span data-stu-id="15ed2-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15ed2-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="15ed2-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="15ed2-119">Der Aufbewahrungszeitraum in Tagen für Sicherungen am Speicherort.</span><span class="sxs-lookup"><span data-stu-id="15ed2-119">The retention period, in days, for backups in the storage location.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15ed2-120">-EncryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="15ed2-120">-EncryptionCertPath</span></span>
<span data-ttu-id="15ed2-121">Pfad zur Verschlüsselungs-CERT-Datei mit öffentlichem Schlüssel (. cer).</span><span class="sxs-lookup"><span data-stu-id="15ed2-121">Path to the encryption cert file with public key (.cer).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15ed2-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="15ed2-122">-InputObject</span></span>
<span data-ttu-id="15ed2-123">Von Get-AzsBackupConfiguration zurückgegebene Backup-Standortkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="15ed2-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

```yaml
Type: Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15ed2-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="15ed2-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="15ed2-125">Gibt an, ob der Sicherungszeitplan aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="15ed2-125">Whether the backup scheduler should be enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15ed2-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="15ed2-126">-Location</span></span>
<span data-ttu-id="15ed2-127">Der Speicherort, den Sie konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="15ed2-127">Location to configure.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15ed2-128">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="15ed2-128">-Password</span></span>
<span data-ttu-id="15ed2-129">Kennwort, das für den Zugriff auf den Sicherungsspeicherort erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="15ed2-129">Password required to access backup location.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15ed2-130">-Path</span><span class="sxs-lookup"><span data-stu-id="15ed2-130">-Path</span></span>
<span data-ttu-id="15ed2-131">Der Speicherort, an dem Sicherungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="15ed2-131">Location where backups will be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupShare

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15ed2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15ed2-132">-ResourceGroupName</span></span>
<span data-ttu-id="15ed2-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="15ed2-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15ed2-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="15ed2-134">-ResourceId</span></span>
<span data-ttu-id="15ed2-135">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="15ed2-135">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15ed2-136">-Username</span><span class="sxs-lookup"><span data-stu-id="15ed2-136">-Username</span></span>
<span data-ttu-id="15ed2-137">Der für den Zugriff auf den Sicherungsspeicherort erforderliche Benutzername.</span><span class="sxs-lookup"><span data-stu-id="15ed2-137">Username required to access backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15ed2-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="15ed2-138">-Confirm</span></span>
<span data-ttu-id="15ed2-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="15ed2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15ed2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15ed2-140">-WhatIf</span></span>
<span data-ttu-id="15ed2-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15ed2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15ed2-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15ed2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15ed2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15ed2-143">CommonParameters</span></span>
<span data-ttu-id="15ed2-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15ed2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15ed2-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15ed2-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15ed2-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="15ed2-146">INPUTS</span></span>

## <span data-ttu-id="15ed2-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="15ed2-147">OUTPUTS</span></span>

### <span data-ttu-id="15ed2-148">Microsoft. AzureStack. Management. Backup. admin. Models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="15ed2-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="15ed2-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="15ed2-149">NOTES</span></span>

## <span data-ttu-id="15ed2-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="15ed2-150">RELATED LINKS</span></span>
