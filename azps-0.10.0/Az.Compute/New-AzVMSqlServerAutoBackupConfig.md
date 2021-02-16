---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: ecff02643dd6d0e017d56af01792a06dc7b8d998
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398273"
---
# <span data-ttu-id="fa74c-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="fa74c-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="fa74c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa74c-102">SYNOPSIS</span></span>
<span data-ttu-id="fa74c-103">Erstellt ein Konfigurationsobjekt für SQL Server Sicherung.</span><span class="sxs-lookup"><span data-stu-id="fa74c-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="fa74c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa74c-104">SYNTAX</span></span>

### <span data-ttu-id="fa74c-105">StorageUriSqlServerAutoBackup (Standard)</span><span class="sxs-lookup"><span data-stu-id="fa74c-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa74c-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="fa74c-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs]
 [-BackupScheduleType <String>] [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>]
 [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa74c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa74c-107">DESCRIPTION</span></span>
<span data-ttu-id="fa74c-108">Das **Cmdlet "New-AzVMSqlServerAutoBackupConfig"** erstellt ein Konfigurationsobjekt für SQL Server Sicherung.</span><span class="sxs-lookup"><span data-stu-id="fa74c-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="fa74c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fa74c-109">EXAMPLES</span></span>

### <span data-ttu-id="fa74c-110">Beispiel 1: Erstellen einer automatischen Sicherungskonfiguration mit Speicher-URI und Kontoschlüssel</span><span class="sxs-lookup"><span data-stu-id="fa74c-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="fa74c-111">Mit diesem Befehl wird ein automatisches Sicherungskonfigurationsobjekt erstellt, indem Speicher-URI und Kontoschlüssel angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fa74c-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="fa74c-112">Automatische Sicherungen sind aktiviert, und automatische Sicherungen werden 10 Tage lang aufbewahrt.</span><span class="sxs-lookup"><span data-stu-id="fa74c-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="fa74c-113">Der Befehl speichert das Ergebnis in der $AutoBackupConfig Variable.</span><span class="sxs-lookup"><span data-stu-id="fa74c-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="fa74c-114">Sie können dieses Konfigurationselement für andere Cmdlets angeben, z. B. Set-AzVMSqlServerExtension Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa74c-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="fa74c-115">Beispiel 2: Erstellen einer automatischen Sicherungskonfiguration mithilfe des Speicherkontexts</span><span class="sxs-lookup"><span data-stu-id="fa74c-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="fa74c-116">Der erste Befehl erstellt einen Speicherkontext und speichert ihn dann in der $StorageContext Variable.</span><span class="sxs-lookup"><span data-stu-id="fa74c-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="fa74c-117">Weitere Informationen finden Sie unter "New-AzureStorageContext".</span><span class="sxs-lookup"><span data-stu-id="fa74c-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="fa74c-118">Der zweite Befehl erstellt ein automatisches Sicherungskonfigurationsobjekt, indem er den Speicherkontext in der $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="fa74c-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="fa74c-119">Automatische Sicherungen sind aktiviert, und automatische Sicherungen werden 10 Tage lang aufbewahrt.</span><span class="sxs-lookup"><span data-stu-id="fa74c-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="fa74c-120">Beispiel 3: Erstellen einer automatischen Sicherungskonfiguration mithilfe des Speicherkontexts mit Verschlüsselung und Kennwort</span><span class="sxs-lookup"><span data-stu-id="fa74c-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="fa74c-121">Mit diesem Befehl wird ein automatisches Sicherungskonfigurationsobjekt erstellt und gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fa74c-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="fa74c-122">Der Befehl gibt den in einem vorherigen Beispiel erstellten Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="fa74c-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="fa74c-123">Der Befehl ermöglicht die Verschlüsselung mit Kennwort.</span><span class="sxs-lookup"><span data-stu-id="fa74c-123">The command enables encryption with password.</span></span>
<span data-ttu-id="fa74c-124">Das Kennwort wurde zuvor als sichere Zeichenfolge in der Variablen $CertificatePassword gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fa74c-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="fa74c-125">Verwenden Sie zum Erstellen einer sicheren Zeichenfolge das ConvertTo-SecureString Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa74c-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="fa74c-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa74c-126">PARAMETERS</span></span>

### <span data-ttu-id="fa74c-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="fa74c-127">-BackupScheduleType</span></span>
<span data-ttu-id="fa74c-128">Sicherungsplantyp, manuell oder automatisiert</span><span class="sxs-lookup"><span data-stu-id="fa74c-128">Backup schedule type, manual or automated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa74c-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="fa74c-129">-BackupSystemDbs</span></span>
<span data-ttu-id="fa74c-130">Sichern von Systemdatenbanken</span><span class="sxs-lookup"><span data-stu-id="fa74c-130">Backup system databases</span></span>

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

### <span data-ttu-id="fa74c-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="fa74c-131">-CertificatePassword</span></span>
<span data-ttu-id="fa74c-132">Gibt ein Kennwort zum Verschlüsseln des Zertifikats an, das zum Ausführen verschlüsselter SQL Server Sicherungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fa74c-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa74c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa74c-133">-DefaultProfile</span></span>
<span data-ttu-id="fa74c-134">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa74c-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa74c-135">-Enable</span><span class="sxs-lookup"><span data-stu-id="fa74c-135">-Enable</span></span>
<span data-ttu-id="fa74c-136">Gibt an, dass die automatische Sicherung für SQL Server virtuellen Computer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fa74c-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="fa74c-137">Wenn Sie diesen Parameter angeben, legt die automatische Sicherung einen Sicherungszeitplan für alle aktuellen und neuen Datenbanken fest.</span><span class="sxs-lookup"><span data-stu-id="fa74c-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="fa74c-138">Dadurch werden die Einstellungen für verwaltete Sicherungen aktualisiert, um diesen Zeitplan zu befolgen.</span><span class="sxs-lookup"><span data-stu-id="fa74c-138">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa74c-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="fa74c-139">-EnableEncryption</span></span>
<span data-ttu-id="fa74c-140">Gibt an, dass dieses Cmdlet Verschlüsselung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="fa74c-140">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa74c-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="fa74c-141">-FullBackupFrequency</span></span>
<span data-ttu-id="fa74c-142">Sql Server: vollständige Sicherungshäufigkeit, täglich oder wöchentlich</span><span class="sxs-lookup"><span data-stu-id="fa74c-142">Sql Server Full Backup frequency, daily or weekly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa74c-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="fa74c-143">-FullBackupStartHour</span></span>
<span data-ttu-id="fa74c-144">Tageszeit (0-23), zu der die vollständige Sql Server-Sicherung gestartet werden soll</span><span class="sxs-lookup"><span data-stu-id="fa74c-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="fa74c-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="fa74c-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="fa74c-146">Sql Server Vollsicherung Fenster in Stunden</span><span class="sxs-lookup"><span data-stu-id="fa74c-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="fa74c-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="fa74c-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="fa74c-148">Häufigkeit der Sql Server-Protokollsicherung, einmal alle 1-60 Minuten</span><span class="sxs-lookup"><span data-stu-id="fa74c-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="fa74c-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa74c-149">-ResourceGroupName</span></span>
<span data-ttu-id="fa74c-150">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="fa74c-150">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa74c-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="fa74c-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="fa74c-152">Gibt die Anzahl der Tage an, die eine Sicherung erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="fa74c-152">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa74c-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="fa74c-153">-StorageContext</span></span>
<span data-ttu-id="fa74c-154">Gibt das Speicherkonto an, das zum Speichern von Sicherungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fa74c-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="fa74c-155">Verwenden Sie zum Abrufen **eines AzureStorageContext-Objekts** das New-AzureStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa74c-155">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="fa74c-156">Die Standardeinstellung ist das Speicherkonto, das dem virtuellen SQL Server zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fa74c-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa74c-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="fa74c-157">-StorageKey</span></span>
<span data-ttu-id="fa74c-158">Gibt den Speicherschlüssel des BLOB-Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="fa74c-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="fa74c-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="fa74c-159">-StorageUri</span></span>
<span data-ttu-id="fa74c-160">Gibt den URI (Uniform Resource Identifier) des BLOB-Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="fa74c-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="fa74c-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa74c-161">CommonParameters</span></span>
<span data-ttu-id="fa74c-162">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa74c-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa74c-163">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa74c-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa74c-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fa74c-164">INPUTS</span></span>

### <span data-ttu-id="fa74c-165">Keine</span><span class="sxs-lookup"><span data-stu-id="fa74c-165">None</span></span>
<span data-ttu-id="fa74c-166">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="fa74c-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fa74c-167">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fa74c-167">OUTPUTS</span></span>

### <span data-ttu-id="fa74c-168">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="fa74c-168">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="fa74c-169">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fa74c-169">NOTES</span></span>

## <span data-ttu-id="fa74c-170">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fa74c-170">RELATED LINKS</span></span>

[<span data-ttu-id="fa74c-171">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="fa74c-171">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="fa74c-172">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="fa74c-172">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


