---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: dbcccaa1c0a17a616d474135be253ebb7ecc0396
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652056"
---
# <span data-ttu-id="1e49d-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="1e49d-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="1e49d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e49d-102">SYNOPSIS</span></span>
<span data-ttu-id="1e49d-103">Erstellt ein Configuration-Objekt für die automatische Sicherung von SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1e49d-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="1e49d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e49d-104">SYNTAX</span></span>

### <span data-ttu-id="1e49d-105">StorageUriSqlServerAutoBackup (Standard)</span><span class="sxs-lookup"><span data-stu-id="1e49d-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e49d-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="1e49d-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e49d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e49d-107">DESCRIPTION</span></span>
<span data-ttu-id="1e49d-108">Das Cmdlet **New-AzVMSqlServerAutoBackupConfig** erstellt ein Configuration-Objekt für die automatische Sicherung von SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1e49d-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="1e49d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e49d-109">EXAMPLES</span></span>

### <span data-ttu-id="1e49d-110">Beispiel 1: Erstellen einer automatischen Sicherungskonfiguration mithilfe von Speicher-URI und Kontoschlüssel</span><span class="sxs-lookup"><span data-stu-id="1e49d-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="1e49d-111">Mit diesem Befehl wird ein Automatisches Backup-Konfigurationsobjekt erstellt, indem Sie den Speicher-URI und den Kontoschlüssel angeben.</span><span class="sxs-lookup"><span data-stu-id="1e49d-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="1e49d-112">Die automatische Sicherung ist aktiviert, und automatische Sicherungen werden 10 Tage lang aufbewahrt.</span><span class="sxs-lookup"><span data-stu-id="1e49d-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="1e49d-113">Der Befehl speichert das Ergebnis in der $AutoBackupConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1e49d-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="1e49d-114">Sie können dieses Konfigurationselement für andere Cmdlets angeben, beispielsweise das Cmdlet "Set-AzVMSqlServerExtension".</span><span class="sxs-lookup"><span data-stu-id="1e49d-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="1e49d-115">Beispiel 2: Erstellen einer automatischen Sicherungskonfiguration mithilfe des Speicher Kontexts</span><span class="sxs-lookup"><span data-stu-id="1e49d-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="1e49d-116">Der erste Befehl erstellt einen Speicherkontext und speichert ihn dann in der $StorageContext-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1e49d-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="1e49d-117">Weitere Informationen finden Sie unter New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1e49d-117">For more information, see New-AzStorageContext.</span></span>
<span data-ttu-id="1e49d-118">Mit dem zweiten Befehl wird ein Automatisches Backup-Konfigurationsobjekt erstellt, indem der Speicherkontext in $StorageContext angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1e49d-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="1e49d-119">Die automatische Sicherung ist aktiviert, und automatische Sicherungen werden 10 Tage lang aufbewahrt.</span><span class="sxs-lookup"><span data-stu-id="1e49d-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="1e49d-120">Beispiel 3: Erstellen einer automatischen Sicherungskonfiguration mithilfe des Speicher Kontexts mit Verschlüsselung und Kennwort</span><span class="sxs-lookup"><span data-stu-id="1e49d-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="1e49d-121">Mit diesem Befehl wird ein Automatisches Backup-Konfigurationsobjekt erstellt und gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1e49d-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="1e49d-122">Der Befehl gibt den in einem vorherigen Beispiel erstellten Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="1e49d-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="1e49d-123">Der Befehl ermöglicht die Verschlüsselung mit einem Kennwort.</span><span class="sxs-lookup"><span data-stu-id="1e49d-123">The command enables encryption with password.</span></span>
<span data-ttu-id="1e49d-124">Das Kennwort wurde zuvor als sichere Zeichenfolge in der $CertificatePassword Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1e49d-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="1e49d-125">Verwenden Sie zum Erstellen einer sicheren Zeichenfolge das ConvertTo-SecureString-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e49d-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="1e49d-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e49d-126">PARAMETERS</span></span>

### <span data-ttu-id="1e49d-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="1e49d-127">-BackupScheduleType</span></span>
<span data-ttu-id="1e49d-128">Sicherungszeitplan, manuell oder automatisiert</span><span class="sxs-lookup"><span data-stu-id="1e49d-128">Backup schedule type, manual or automated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e49d-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="1e49d-129">-BackupSystemDbs</span></span>
<span data-ttu-id="1e49d-130">Sicherungssystem Datenbanken</span><span class="sxs-lookup"><span data-stu-id="1e49d-130">Backup system databases</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e49d-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="1e49d-131">-CertificatePassword</span></span>
<span data-ttu-id="1e49d-132">Gibt ein Kennwort zum Verschlüsseln des Zertifikats an, mit dem SQL Server-verschlüsselte Sicherungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1e49d-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e49d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e49d-133">-DefaultProfile</span></span>
<span data-ttu-id="1e49d-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1e49d-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e49d-135">-Enable</span><span class="sxs-lookup"><span data-stu-id="1e49d-135">-Enable</span></span>
<span data-ttu-id="1e49d-136">Gibt an, dass die automatische Sicherung für den virtuellen SQL Server-Computer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1e49d-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="1e49d-137">Wenn Sie diesen Parameter angeben, legt automatisiertes Backup einen Sicherungszeitplan für alle aktuellen und neuen Datenbanken fest.</span><span class="sxs-lookup"><span data-stu-id="1e49d-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="1e49d-138">Damit werden die Einstellungen für verwaltete Sicherungen so aktualisiert, dass Sie diesem Zeitplan folgen.</span><span class="sxs-lookup"><span data-stu-id="1e49d-138">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e49d-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="1e49d-139">-EnableEncryption</span></span>
<span data-ttu-id="1e49d-140">Gibt an, dass dieses Cmdlet die Verschlüsselung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1e49d-140">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e49d-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="1e49d-141">-FullBackupFrequency</span></span>
<span data-ttu-id="1e49d-142">Vollständige SQL Server-Backup-Häufigkeit, täglich oder wöchentlich</span><span class="sxs-lookup"><span data-stu-id="1e49d-142">Sql Server Full Backup frequency, daily or weekly</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e49d-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="1e49d-143">-FullBackupStartHour</span></span>
<span data-ttu-id="1e49d-144">Stunde des Tages (0-23), wenn die vollständige Sicherung von SQL Server gestartet werden soll</span><span class="sxs-lookup"><span data-stu-id="1e49d-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e49d-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="1e49d-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="1e49d-146">Vollständiges SQL Server-Sicherungsfenster in Stunden</span><span class="sxs-lookup"><span data-stu-id="1e49d-146">Sql Server Full Backup window in hours</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e49d-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="1e49d-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="1e49d-148">SQL Server-Protokoll Sicherungshäufigkeit, einmal alle 1-60 Minuten</span><span class="sxs-lookup"><span data-stu-id="1e49d-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e49d-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e49d-149">-ResourceGroupName</span></span>
<span data-ttu-id="1e49d-150">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="1e49d-150">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e49d-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="1e49d-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="1e49d-152">Gibt die Anzahl der Tage an, für die eine Sicherung aufbewahrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1e49d-152">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e49d-153">-Storagecontext</span><span class="sxs-lookup"><span data-stu-id="1e49d-153">-StorageContext</span></span>
<span data-ttu-id="1e49d-154">Gibt das Speicherkonto an, das zum Speichern von Sicherungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1e49d-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="1e49d-155">Verwenden Sie das New-AzStorageContext-Cmdlet, um ein **AzureStorageContext** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1e49d-155">To obtain an **AzureStorageContext** object, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="1e49d-156">Der Standardwert ist das Speicherkonto, das dem virtuellen SQL Server-Computer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1e49d-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e49d-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="1e49d-157">-StorageKey</span></span>
<span data-ttu-id="1e49d-158">Gibt den Speicherschlüssel des BLOB-speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="1e49d-158">Specifies the storage key of the blob storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e49d-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="1e49d-159">-StorageUri</span></span>
<span data-ttu-id="1e49d-160">Gibt den Uniform Resource Identifier (URI) des BLOB-speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="1e49d-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e49d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e49d-161">CommonParameters</span></span>
<span data-ttu-id="1e49d-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e49d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e49d-163">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e49d-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e49d-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e49d-164">INPUTS</span></span>

### <span data-ttu-id="1e49d-165">System. String</span><span class="sxs-lookup"><span data-stu-id="1e49d-165">System.String</span></span>

### <span data-ttu-id="1e49d-166">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="1e49d-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1e49d-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1e49d-167">System.Int32</span></span>

### <span data-ttu-id="1e49d-168">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1e49d-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="1e49d-169">System. Uri</span><span class="sxs-lookup"><span data-stu-id="1e49d-169">System.Uri</span></span>

### <span data-ttu-id="1e49d-170">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="1e49d-170">System.Security.SecureString</span></span>

### <span data-ttu-id="1e49d-171">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1e49d-171">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1e49d-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e49d-172">OUTPUTS</span></span>

### <span data-ttu-id="1e49d-173">Microsoft. Azure. Commands. Compute. AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="1e49d-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="1e49d-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e49d-174">NOTES</span></span>

## <span data-ttu-id="1e49d-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e49d-175">RELATED LINKS</span></span>

[<span data-ttu-id="1e49d-176">Neu – AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="1e49d-176">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="1e49d-177">Satz-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="1e49d-177">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


