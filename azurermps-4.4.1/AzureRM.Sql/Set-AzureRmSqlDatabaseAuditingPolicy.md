---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: 99fb9bf57f056a869310de2fe27d00a72ce5d8c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478849"
---
# Set-AzureRmSqlDatabaseAuditingPolicy

## Synopsis
Legt die Überwachungsrichtlinie für eine Datenbank fest.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmSqlDatabaseAuditingPolicy [-AuditType <AuditType>] [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-EventType <String[]>]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-TableIdentifier <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureRmSqlDatabaseAuditingPolicy** " ändert die Überwachungsrichtlinie einer Azure SQL-Datenbank.
Um das Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Datenbank zu identifizieren.
Geben Sie den *StorageAccountName* -Parameter an, um das Speicherkonto für die Überwachungsprotokolle und den *StorageKeyType* -Parameter anzugeben, um die Speicherschlüssel zu definieren.

Sie können auch die Aufbewahrung für die Überwachungsprotokolltabelle definieren, indem Sie den Wert der *RetentionInDays* -und Table *Identifier* -Parameter festlegen, um den Zeitraum und den Startwert für die Namen der Überwachungsprotokoll Tabellen zu definieren.
Geben Sie den *eventType* -Parameter an, um die zu überwachenden Ereignistypen zu definieren.

Nachdem das Cmdlet erfolgreich ausgeführt wurde, ist die Überwachung der Datenbank aktiviert.
Wenn die Datenbank die Richtlinie Ihres Servers für die Überwachung verwendet hat, bevor Sie dieses Cmdlet ausgeführt haben, beendet die Überwachung die Verwendung dieser Richtlinie.
Wenn das Cmdlet erfolgreich ist und Sie den *passthru* -Parameter verwenden, gibt es zusätzlich zu den Datenbankbezeichnern ein Objekt zurück, das die aktuelle Überwachungsrichtlinie beschreibt.
Zu den Datenbankbezeichnern gehören **ResourceGroupName** , **Servername** und **DatabaseName** , sind aber nicht darauf limitiert.

Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.

## Beispiele

### Beispiel 1: Festlegen der Überwachungsrichtlinie einer Datenbank für die Verwendung der Tabellen Überwachung
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Table -StorageAccountName "Storage31"
```

Mit diesem Befehl wird die Überwachungsrichtlinie der Datenbank mit dem Namen Database01 auf Server01 festgelegt, um das Speicherkonto mit dem Namen Storage31 zu verwenden.

### Beispiel 2: Festlegen des Speicherkonto Schlüssels einer vorhandenen Überwachungsrichtlinie einer Datenbank
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -StorageAccountKey Secondary
```

Mit diesem Befehl wird die Überwachungsrichtlinie der Datenbank mit dem Namen Database01 auf Server01 festgelegt, damit derselbe Speicherkonto Name verwendet wird, aber jetzt der sekundäre Schlüssel verwendet wird.

### Beispiel 3: Festlegen der Überwachungsrichtlinie einer Datenbank für die Verwendung eines bestimmten Ereignistyps
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventType Login_Failure
```

### Beispiel 4: Festlegen der Überwachungsrichtlinie einer Datenbank für die Verwendung der BLOB-Überwachung
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -AuditAction "UPDATE ON database::[Database01] BY [public]"  -RetentionInDays 8
```

Dieser Befehl legt die Überwachungsrichtlinie der Datenbank mit dem Namen Database01 auf Server01 fest.
Die Richtlinie protokolliert den Login_Failure-Ereignistyp.
Der Befehl ändert keine Speichereinstellungen.

## Parameter

### -Auditing
Geben Sie mindestens eine Überwachungsaktion an.
Dieser Parameter gilt nur für die BLOB-Überwachung.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AuditActionGroup
Geben Sie mindestens eine Überwachungs Aktionsgruppe an.
Dieser Parameter gilt nur für die BLOB-Überwachung.

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases: 
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Audittype
```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType
Parameter Sets: (All)
Aliases: 
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatabaseName
Gibt den Namen der Datenbank an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventType
Gibt die zu überwachenden Ereignistypen an.
Dieser Parameter gilt nur für die Tabellen Überwachung.

Sie können mehrere Ereignistypen angeben.
Sie können alle angeben, um alle Ereignistypen oder None zu überwachen, um anzugeben, dass keine Ereignisse überwacht werden.
Wenn Sie alle oder keine gleichzeitig angeben, wird das Cmdlet nicht ausgeführt.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.
Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.

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

### -RetentionInDays
Gibt die Anzahl der Aufbewahrungstage für die Überwachungsprotokolltabelle an.
Der Wert 0 (null) bedeutet, dass die Tabelle nicht beibehalten wird.
Der Standardwert ist 0 (null).
Wenn Sie einen Wert angeben, der größer als 0 (null) ist, müssen Sie einen Wert für den *TableIdentifer* -Parameter angeben.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Servername
Gibt den Namen des Servers an, der die Datenbank hostet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Gibt den Namen des speicherkontos für die Überwachung der Datenbank an.
Platzhalterzeichen sind nicht zulässig.
Dieser Parameter ist nicht erforderlich.
Wenn Sie diesen Parameter nicht angeben, verwendet das Cmdlet das Speicherkonto, das zuvor als Teil der Überwachungsrichtlinie der Datenbank definiert wurde.
Wenn Sie zum ersten Mal eine Datenbank-Überwachungsrichtlinie definieren und diesen Parameter nicht angeben, schlägt das Cmdlet fehl.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKeyType
Gibt an, welche der Speicherzugriffs Tasten verwendet werden soll.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Primär
- Sekundär

Der Standardwert ist Primary.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tabellenidentifier
Gibt den Namen der Überwachungsprotokolltabelle an.
Geben Sie diesen Wert an, wenn Sie für den *RetentionInDays* -Parameter einen Wert größer als 0 angeben.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. Azure. Commands. SQL. Security. Model. DatabaseAuditingPolicyModel

## Notizen

## Verwandte Links

[Get-AzureRmSqlDatabaseAuditingPolicy](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[Remove-AzureRmSqlDatabaseAuditing](./Remove-AzureRmSqlDatabaseAuditing.md)

[SQL-Datenbank-Dokumentation](https://docs.microsoft.com/azure/sql-database/)


