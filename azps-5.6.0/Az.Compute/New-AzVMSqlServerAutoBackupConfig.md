---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 6d9047679f4286e0e2212ca8e599237825326dd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930576"
---
# <span data-ttu-id="f6864-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="f6864-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="f6864-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6864-102">SYNOPSIS</span></span>
<span data-ttu-id="f6864-103">Erstellt ein Konfigurationsobjekt für die SQL Server Sicherung.</span><span class="sxs-lookup"><span data-stu-id="f6864-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="f6864-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6864-104">SYNTAX</span></span>

### <span data-ttu-id="f6864-105">StorageUriSqlServerAutoBackup (Standard)</span><span class="sxs-lookup"><span data-stu-id="f6864-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6864-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="f6864-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6864-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6864-107">DESCRIPTION</span></span>
<span data-ttu-id="f6864-108">Das **Cmdlet New-AzVMSqlServerAutoBackupConfig** erstellt ein Konfigurationsobjekt für die SQL Server Sicherung.</span><span class="sxs-lookup"><span data-stu-id="f6864-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="f6864-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f6864-109">EXAMPLES</span></span>

### <span data-ttu-id="f6864-110">Beispiel 1: Erstellen einer automatischen Sicherungskonfiguration mit Speicher-URI und Kontoschlüssel</span><span class="sxs-lookup"><span data-stu-id="f6864-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="f6864-111">Mit diesem Befehl wird ein automatisches Sicherungskonfigurationsobjekt erstellt, indem Speicher-URI und Kontoschlüssel angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f6864-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="f6864-112">Die automatische Sicherung ist aktiviert, und automatische Sicherungen werden 10 Tage lang aufbewahrt.</span><span class="sxs-lookup"><span data-stu-id="f6864-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="f6864-113">Der Befehl speichert das Ergebnis in der $AutoBackupConfig Variablen.</span><span class="sxs-lookup"><span data-stu-id="f6864-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="f6864-114">Sie können dieses Konfigurationselement für andere Cmdlets angeben, z. B. Set-AzVMSqlServerExtension cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6864-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="f6864-115">Beispiel 2: Erstellen einer automatischen Sicherungskonfiguration mithilfe des Speicherkontexts</span><span class="sxs-lookup"><span data-stu-id="f6864-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="f6864-116">Der erste Befehl erstellt einen Speicherkontext und speichert ihn dann in der $StorageContext-Variable.</span><span class="sxs-lookup"><span data-stu-id="f6864-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="f6864-117">Weitere Informationen finden Sie unter New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f6864-117">For more information, see New-AzStorageContext.</span></span>
<span data-ttu-id="f6864-118">Mit dem zweiten Befehl wird ein automatisches Sicherungskonfigurationsobjekt erstellt, indem der Speicherkontext in $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="f6864-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="f6864-119">Die automatische Sicherung ist aktiviert, und automatische Sicherungen werden 10 Tage lang aufbewahrt.</span><span class="sxs-lookup"><span data-stu-id="f6864-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="f6864-120">Beispiel 3: Erstellen einer automatischen Sicherungskonfiguration mithilfe des Speicherkontexts mit Verschlüsselung und Kennwort</span><span class="sxs-lookup"><span data-stu-id="f6864-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="f6864-121">Mit diesem Befehl wird ein automatisches Sicherungskonfigurationsobjekt erstellt und gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f6864-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="f6864-122">Der Befehl gibt den in einem vorherigen Beispiel erstellten Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="f6864-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="f6864-123">Der Befehl aktiviert die Verschlüsselung mit Kennwort.</span><span class="sxs-lookup"><span data-stu-id="f6864-123">The command enables encryption with password.</span></span>
<span data-ttu-id="f6864-124">Das Kennwort wurde zuvor als sichere Zeichenfolge in der Variablen $CertificatePassword gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f6864-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="f6864-125">Verwenden Sie zum Erstellen einer sicheren Zeichenfolge das ConvertTo-SecureString Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6864-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="f6864-126">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f6864-126">PARAMETERS</span></span>

### <span data-ttu-id="f6864-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="f6864-127">-BackupScheduleType</span></span>
<span data-ttu-id="f6864-128">Sicherungszeitplantyp, manuell oder automatisiert</span><span class="sxs-lookup"><span data-stu-id="f6864-128">Backup schedule type, manual or automated</span></span>

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

### <span data-ttu-id="f6864-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="f6864-129">-BackupSystemDbs</span></span>
<span data-ttu-id="f6864-130">Sichern von Systemdatenbanken</span><span class="sxs-lookup"><span data-stu-id="f6864-130">Backup system databases</span></span>

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

### <span data-ttu-id="f6864-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="f6864-131">-CertificatePassword</span></span>
<span data-ttu-id="f6864-132">Gibt ein Kennwort zum Verschlüsseln des Zertifikats an, das zum Ausführen SQL Server Sicherungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f6864-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

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

### <span data-ttu-id="f6864-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6864-133">-DefaultProfile</span></span>
<span data-ttu-id="f6864-134">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6864-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6864-135">-Enable</span><span class="sxs-lookup"><span data-stu-id="f6864-135">-Enable</span></span>
<span data-ttu-id="f6864-136">Gibt an, dass die automatische Sicherung SQL Server virtuellen Computer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f6864-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="f6864-137">Wenn Sie diesen Parameter angeben, legt die automatische Sicherung einen Sicherungszeitplan für alle aktuellen und neuen Datenbanken fest.</span><span class="sxs-lookup"><span data-stu-id="f6864-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="f6864-138">Dadurch werden Ihre Einstellungen für verwaltete Sicherung aktualisiert, um diesen Zeitplan zu befolgen.</span><span class="sxs-lookup"><span data-stu-id="f6864-138">This updates your Managed Backup settings to follow this schedule.</span></span>

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

### <span data-ttu-id="f6864-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="f6864-139">-EnableEncryption</span></span>
<span data-ttu-id="f6864-140">Gibt an, dass dieses Cmdlet die Verschlüsselung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f6864-140">Indicates that this cmdlet enables encryption.</span></span>

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

### <span data-ttu-id="f6864-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="f6864-141">-FullBackupFrequency</span></span>
<span data-ttu-id="f6864-142">Sql Server : Tägliche oder wöchentliche Vollständige Sicherungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="f6864-142">Sql Server Full Backup frequency, daily or weekly</span></span>

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

### <span data-ttu-id="f6864-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="f6864-143">-FullBackupStartHour</span></span>
<span data-ttu-id="f6864-144">Stunde des Tages (0-23), wenn die vollständige Sql Server-Sicherung gestartet werden soll</span><span class="sxs-lookup"><span data-stu-id="f6864-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="f6864-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="f6864-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="f6864-146">Sql Server Full Backup window in hours</span><span class="sxs-lookup"><span data-stu-id="f6864-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="f6864-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="f6864-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="f6864-148">Sql Server-ProtokollSicherungshäufigkeit einmal alle 1-60 Minuten</span><span class="sxs-lookup"><span data-stu-id="f6864-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="f6864-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6864-149">-ResourceGroupName</span></span>
<span data-ttu-id="f6864-150">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="f6864-150">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f6864-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="f6864-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="f6864-152">Gibt die Anzahl der Tage an, in der eine Sicherung beibehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="f6864-152">Specifies the number of days to retain a backup.</span></span>

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

### <span data-ttu-id="f6864-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="f6864-153">-StorageContext</span></span>
<span data-ttu-id="f6864-154">Gibt das Speicherkonto an, das zum Speichern von Sicherungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f6864-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="f6864-155">Zum Abrufen eines **AzureStorageContext-Objekts** verwenden Sie das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6864-155">To obtain an **AzureStorageContext** object, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="f6864-156">Die Standardeinstellung ist das Speicherkonto, das dem virtuellen SQL Server zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f6864-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

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

### <span data-ttu-id="f6864-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="f6864-157">-StorageKey</span></span>
<span data-ttu-id="f6864-158">Gibt den Speicherschlüssel des Blobspeicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="f6864-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="f6864-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="f6864-159">-StorageUri</span></span>
<span data-ttu-id="f6864-160">Gibt den URI (Uniform Resource Identifier) des Blobspeicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="f6864-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="f6864-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6864-161">CommonParameters</span></span>
<span data-ttu-id="f6864-162">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6864-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6864-163">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6864-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6864-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f6864-164">INPUTS</span></span>

### <span data-ttu-id="f6864-165">System.String</span><span class="sxs-lookup"><span data-stu-id="f6864-165">System.String</span></span>

### <span data-ttu-id="f6864-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f6864-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f6864-167">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f6864-167">System.Int32</span></span>

### <span data-ttu-id="f6864-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f6864-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="f6864-169">System.Uri</span><span class="sxs-lookup"><span data-stu-id="f6864-169">System.Uri</span></span>

### <span data-ttu-id="f6864-170">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="f6864-170">System.Security.SecureString</span></span>

### <span data-ttu-id="f6864-171">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f6864-171">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f6864-172">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f6864-172">OUTPUTS</span></span>

### <span data-ttu-id="f6864-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="f6864-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="f6864-174">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f6864-174">NOTES</span></span>

## <span data-ttu-id="f6864-175">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f6864-175">RELATED LINKS</span></span>

[<span data-ttu-id="f6864-176">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="f6864-176">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="f6864-177">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="f6864-177">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


