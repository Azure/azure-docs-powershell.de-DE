---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 55E097F4-1F49-4196-9A8B-949FD5D9108A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4035487fa0363e6a7802966d9bc6422429723d94
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006405"
---
# <span data-ttu-id="ea53f-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="ea53f-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="ea53f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ea53f-102">SYNOPSIS</span></span>
<span data-ttu-id="ea53f-103">Erstellt ein Configuration-Objekt für die automatische Sicherung von SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ea53f-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="ea53f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea53f-104">SYNTAX</span></span>

### <span data-ttu-id="ea53f-105">StorageUriSqlServerAutoBackup (Standard)</span><span class="sxs-lookup"><span data-stu-id="ea53f-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>]
 [-BackupSystemDbs] [-BackupScheduleType <String>] [-FullBackupFrequency <String>]
 [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea53f-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="ea53f-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageContext] <AzureStorageContext>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ea53f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea53f-107">DESCRIPTION</span></span>
<span data-ttu-id="ea53f-108">Das Cmdlet **New-AzureVMSqlServerAutoBackupConfig** erstellt ein Configuration-Objekt für die automatische Sicherung von SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ea53f-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="ea53f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea53f-109">EXAMPLES</span></span>

### <span data-ttu-id="ea53f-110">Beispiel 1: Erstellen einer automatischen Sicherungskonfiguration mithilfe von Speicher-URI und Kontoschlüssel</span><span class="sxs-lookup"><span data-stu-id="ea53f-110">Example 1: Create an auto-backup configuration using storage URI and account key</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="ea53f-111">Dieser Befehl erstellt ein Konfigurationsobjekt für die automatische Sicherung, indem Sie die Speicher-URL und den Kontoschlüssel angeben.</span><span class="sxs-lookup"><span data-stu-id="ea53f-111">This command creates an auto-backup configuration object by specifying storage URL and account key.</span></span>

### <span data-ttu-id="ea53f-112">Beispiel 2: Erstellen einer automatischen Sicherungskonfiguration mithilfe des Speicher Kontexts</span><span class="sxs-lookup"><span data-stu-id="ea53f-112">Example 2: Create an auto-backup configuration using storage context</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="ea53f-113">Mit diesem Befehl wird ein Konfigurationsobjekt für die automatische Sicherung erstellt, indem der Speicherkontext angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ea53f-113">This command creates an auto-backup configuration object by specifying storage context.</span></span>

### <span data-ttu-id="ea53f-114">Beispiel 3: Erstellen einer automatischen Sicherungskonfiguration mithilfe des Speicher Kontexts mit Verschlüsselung und Kennwort</span><span class="sxs-lookup"><span data-stu-id="ea53f-114">Example 3: Create an auto-backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertPasswd
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="ea53f-115">Mit diesem Befehl wird ein Konfigurationsobjekt für die automatische Sicherung erstellt, indem der Speicherkontext angegeben und die Verschlüsselungsoption mit Kennwort aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="ea53f-115">This command creates an auto-backup configuration object by specifying Storage context and enabling encryption option with password.</span></span>
<span data-ttu-id="ea53f-116">Die CertificatePassword ist in der Variablen mit dem Namen $CertPasswd gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ea53f-116">The certificatepassword ist stored in the variable named $CertPasswd.</span></span>

## <span data-ttu-id="ea53f-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea53f-117">PARAMETERS</span></span>

### <span data-ttu-id="ea53f-118">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="ea53f-118">-BackupScheduleType</span></span>
<span data-ttu-id="ea53f-119">Sicherungszeitplan, manuell oder automatisiert</span><span class="sxs-lookup"><span data-stu-id="ea53f-119">Backup schedule type, manual or automated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea53f-120">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="ea53f-120">-BackupSystemDbs</span></span>
<span data-ttu-id="ea53f-121">Sicherungssystem Datenbanken</span><span class="sxs-lookup"><span data-stu-id="ea53f-121">Backup system databases</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea53f-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="ea53f-122">-CertificatePassword</span></span>
<span data-ttu-id="ea53f-123">Gibt ein Kennwort zum Verschlüsseln des Zertifikats an, mit dem SQL Server-verschlüsselte Sicherungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ea53f-123">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea53f-124">-Enable</span><span class="sxs-lookup"><span data-stu-id="ea53f-124">-Enable</span></span>
<span data-ttu-id="ea53f-125">Gibt an, dass die automatische Sicherung für den virtuellen SQL Server-Computer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ea53f-125">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="ea53f-126">Wenn Sie diesen Parameter verwenden, legt automatisiertes Backup einen Sicherungszeitplan für alle aktuellen und neuen Datenbanken fest.</span><span class="sxs-lookup"><span data-stu-id="ea53f-126">If you use this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="ea53f-127">Damit werden die Einstellungen für verwaltete Sicherungen so aktualisiert, dass Sie diesem Zeitplan folgen.</span><span class="sxs-lookup"><span data-stu-id="ea53f-127">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea53f-128">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="ea53f-128">-EnableEncryption</span></span>
<span data-ttu-id="ea53f-129">Gibt an, dass die Verschlüsselung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ea53f-129">Indicates that encryption is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea53f-130">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="ea53f-130">-FullBackupFrequency</span></span>
<span data-ttu-id="ea53f-131">Vollständige SQL Server-Backup-Häufigkeit, täglich oder Woche</span><span class="sxs-lookup"><span data-stu-id="ea53f-131">Sql Server Full Backup frequency, daily or week</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea53f-132">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="ea53f-132">-FullBackupStartHour</span></span>
<span data-ttu-id="ea53f-133">Stunde des Tages (0-23), wenn die vollständige Sicherung von SQL Server gestartet werden soll</span><span class="sxs-lookup"><span data-stu-id="ea53f-133">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea53f-134">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="ea53f-134">-FullBackupWindowInHours</span></span>
<span data-ttu-id="ea53f-135">Vollständiges SQL Server-Sicherungsfenster in Stunden</span><span class="sxs-lookup"><span data-stu-id="ea53f-135">Sql Server Full Backup window in hours</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea53f-136">-Information</span><span class="sxs-lookup"><span data-stu-id="ea53f-136">-InformationAction</span></span>
<span data-ttu-id="ea53f-137">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="ea53f-137">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ea53f-138">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ea53f-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ea53f-139">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="ea53f-139">Continue</span></span>
- <span data-ttu-id="ea53f-140">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="ea53f-140">Ignore</span></span>
- <span data-ttu-id="ea53f-141">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="ea53f-141">Inquire</span></span>
- <span data-ttu-id="ea53f-142">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ea53f-142">SilentlyContinue</span></span>
- <span data-ttu-id="ea53f-143">Beenden</span><span class="sxs-lookup"><span data-stu-id="ea53f-143">Stop</span></span>
- <span data-ttu-id="ea53f-144">Anhalten</span><span class="sxs-lookup"><span data-stu-id="ea53f-144">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea53f-145">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ea53f-145">-InformationVariable</span></span>
<span data-ttu-id="ea53f-146">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="ea53f-146">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea53f-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="ea53f-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="ea53f-148">SQL Server-Protokoll Sicherungshäufigkeit, einmal alle 1-60 Minuten</span><span class="sxs-lookup"><span data-stu-id="ea53f-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea53f-149">-Profil</span><span class="sxs-lookup"><span data-stu-id="ea53f-149">-Profile</span></span>
<span data-ttu-id="ea53f-150">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="ea53f-150">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ea53f-151">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="ea53f-151">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea53f-152">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="ea53f-152">-RetentionPeriodInDays</span></span>
<span data-ttu-id="ea53f-153">Gibt die Länge des Aufbewahrungszeitraums in Tagen an.</span><span class="sxs-lookup"><span data-stu-id="ea53f-153">Specifies the length of the retention period in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea53f-154">-Storagecontext</span><span class="sxs-lookup"><span data-stu-id="ea53f-154">-StorageContext</span></span>
<span data-ttu-id="ea53f-155">Gibt das zum Speichern von Sicherungen zu verwendende Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="ea53f-155">Specifies the storage account to be used to store backups.</span></span>
<span data-ttu-id="ea53f-156">Standard ist das dem SQL Server-virtuellen Computer zugeordnete Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="ea53f-156">Default is the storage account associated with the SQL Server virtual machine.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea53f-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="ea53f-157">-StorageKey</span></span>
<span data-ttu-id="ea53f-158">Gibt den Speicherschlüssel des BLOB-speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="ea53f-158">Specifies the storage key of the blob storage account.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea53f-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="ea53f-159">-StorageUri</span></span>
<span data-ttu-id="ea53f-160">Gibt einen URI für das BLOB-Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="ea53f-160">Specifies a URI to the blob storage account.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea53f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea53f-161">CommonParameters</span></span>
<span data-ttu-id="ea53f-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea53f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea53f-163">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea53f-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea53f-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ea53f-164">INPUTS</span></span>

## <span data-ttu-id="ea53f-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ea53f-165">OUTPUTS</span></span>

## <span data-ttu-id="ea53f-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="ea53f-166">NOTES</span></span>

## <span data-ttu-id="ea53f-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ea53f-167">RELATED LINKS</span></span>

[<span data-ttu-id="ea53f-168">Neu – AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="ea53f-168">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)


