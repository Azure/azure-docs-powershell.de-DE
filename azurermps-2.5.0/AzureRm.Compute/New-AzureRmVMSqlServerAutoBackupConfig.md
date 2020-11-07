---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverautobackupconfig
schema: 2.0.0
ms.openlocfilehash: bb00a3e4fc953510d2ec32b7c213d07d6c8801c3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850452"
---
# New-AzureRmVMSqlServerAutoBackupConfig

## Synopsis
Erstellt ein Configuration-Objekt für die automatische Sicherung von SQL Server.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### StorageUriSqlServerAutoBackup (Standard)
```
New-AzureRmVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### StorageContextSqlServerAutoBackup
```
New-AzureRmVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs]
 [-BackupScheduleType <String>] [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>]
 [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmVMSqlServerAutoBackupConfig** erstellt ein Configuration-Objekt für die automatische Sicherung von SQL Server.

## Beispiele

### Beispiel 1: Erstellen einer automatischen Sicherungskonfiguration mithilfe von Speicher-URI und Kontoschlüssel
```
PS C:\> $AutoBackupConfig = New-AzureRmVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

Mit diesem Befehl wird ein Automatisches Backup-Konfigurationsobjekt erstellt, indem Sie den Speicher-URI und den Kontoschlüssel angeben.
Die automatische Sicherung ist aktiviert, und automatische Sicherungen werden 10 Tage lang aufbewahrt.
Der Befehl speichert das Ergebnis in der $AutoBackupConfig-Variablen.
Sie können dieses Konfigurationselement für andere Cmdlets angeben, beispielsweise das Cmdlet "Set-AzureRmVMSqlServerExtension".

### Beispiel 2: Erstellen einer automatischen Sicherungskonfiguration mithilfe des Speicher Kontexts
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureRmVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

Der erste Befehl erstellt einen Speicherkontext und speichert ihn dann in der $StorageContext-Variablen.
Weitere Informationen finden Sie unter New-AzureStorageContext.

Mit dem zweiten Befehl wird ein Automatisches Backup-Konfigurationsobjekt erstellt, indem der Speicherkontext in $StorageContext angegeben wird.
Die automatische Sicherung ist aktiviert, und automatische Sicherungen werden 10 Tage lang aufbewahrt.

### Beispiel 3: Erstellen einer automatischen Sicherungskonfiguration mithilfe des Speicher Kontexts mit Verschlüsselung und Kennwort
```
PS C:\> $StorageContext = New-AzureRmVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

Mit diesem Befehl wird ein Automatisches Backup-Konfigurationsobjekt erstellt und gespeichert.
Der Befehl gibt den in einem vorherigen Beispiel erstellten Speicherkontext an.
Der Befehl ermöglicht die Verschlüsselung mit einem Kennwort.
Das Kennwort wurde zuvor als sichere Zeichenfolge in der $CertificatePassword Variablen gespeichert.
Verwenden Sie zum Erstellen einer sicheren Zeichenfolge das ConvertTo-SecureString-Cmdlet.

## Parameter

### -BackupScheduleType
Sicherungszeitplan, manuell oder automatisiert

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

### -BackupSystemDbs
Sicherungssystem Datenbanken

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

### -CertificatePassword
Gibt ein Kennwort zum Verschlüsseln des Zertifikats an, mit dem SQL Server-verschlüsselte Sicherungen ausgeführt werden.

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -Enable
Gibt an, dass die automatische Sicherung für den virtuellen SQL Server-Computer aktiviert ist.
Wenn Sie diesen Parameter angeben, legt automatisiertes Backup einen Sicherungszeitplan für alle aktuellen und neuen Datenbanken fest.
Damit werden die Einstellungen für verwaltete Sicherungen so aktualisiert, dass Sie diesem Zeitplan folgen.

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

### -EnableEncryption
Gibt an, dass dieses Cmdlet die Verschlüsselung aktiviert.

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

### -FullBackupFrequency
Vollständige SQL Server-Backup-Häufigkeit, täglich oder wöchentlich

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

### -FullBackupStartHour
Stunde des Tages (0-23), wenn die vollständige Sicherung von SQL Server gestartet werden soll

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

### -FullBackupWindowInHours
Vollständiges SQL Server-Sicherungsfenster in Stunden

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

### -LogBackupFrequencyInMinutes
SQL Server-Protokoll Sicherungshäufigkeit, einmal alle 1-60 Minuten

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

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe des virtuellen Computers an.

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

### -RetentionPeriodInDays
Gibt die Anzahl der Tage an, für die eine Sicherung aufbewahrt werden soll.

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

### -Storagecontext
Gibt das Speicherkonto an, das zum Speichern von Sicherungen verwendet wird.
Verwenden Sie das New-AzureStorageContext-Cmdlet, um ein **AzureStorageContext** -Objekt zu erhalten.
Der Standardwert ist das Speicherkonto, das dem virtuellen SQL Server-Computer zugeordnet ist.

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

### -StorageKey
Gibt den Speicherschlüssel des BLOB-speicherkontos an.

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

### -StorageUri
Gibt den Uniform Resource Identifier (URI) des BLOB-speicherkontos an.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. Compute. AutoBackupSettings

## Notizen

## Verwandte Links



[Satz-AzureRmVMSqlServerExtension](./Set-AzureRMVMSqlServerExtension.md)


