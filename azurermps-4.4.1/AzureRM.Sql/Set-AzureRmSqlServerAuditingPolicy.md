---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4FCC7D8B-A46E-4E5B-8BE2-F62B3D3E715D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: daec1290dfa70166e532265da98bdb507b1318e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499117"
---
# Set-AzureRmSqlServerAuditingPolicy

## Synopsis
Ändert die Überwachungsrichtlinie eines SQL-Datenbankservers.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmSqlServerAuditingPolicy [-AuditType <AuditType>] [-AuditActionGroup <AuditActionGroups[]>]
 [-PassThru] [-EventType <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-TableIdentifier <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureRmSqlServerAuditingPolicy** " ändert die Überwachungsrichtlinie eines Azure SQL-Datenbankservers.
Geben Sie die Parameter *ResourceGroupName* und *Servername* an, um den Server zu identifizieren, den *StorageAccountName* -Parameter, um das Speicherkonto für die Überwachungsprotokolle anzugeben, und den *StorageKeyType* -Parameter, um die zu verwendenden Speicherschlüssel zu definieren.

Sie können auch die Aufbewahrung für die Überwachungsprotokolltabelle definieren, indem Sie den Wert der *RetentionInDays* -und Table *Identifier* -Parameter festlegen, um den Zeitraum und den Startwert für die Namen der Überwachungsprotokoll Tabellen zu definieren.
Geben Sie den *eventType* -Parameter an, um die zu überwachenden Ereignistypen zu definieren.
Nachdem Sie dieses Cmdlet ausgeführt haben, ist die Überwachung der Datenbanken, die die Richtlinie dieses Servers verwenden, aktiviert.
Wenn das Cmdlet erfolgreich ausgeführt wird und Sie den *passthru* -Parameter angeben, gibt das Cmdlet ein Objekt zurück, das die aktuelle Überwachungsrichtlinie beschreibt, und die Server-IDs.
Server-IDs sind **ResourceGroupName** und Server **Name**.

## Beispiele

### Beispiel 1: Festlegen der Überwachungsrichtlinie einer Azure SQL Server-Tabellen Überwachung verwenden
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Table -StorageAccountName "Storage22"
```

Mit diesem Befehl wird die Überwachungsrichtlinie des Servers mit dem Namen Server01 für die Verwendung eines speicherkontos mit dem Namen Storage22 festgelegt.

### Beispiel 2: Festlegen des Speicherkonto Schlüssels einer vorhandenen Überwachungsrichtlinie eines Azure SQL Server
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountKey Secondary
```

Mit diesem Befehl wird die Überwachungsrichtlinie des Servers mit dem Namen Server01 so festgelegt, dass der sekundäre Schlüssel verwendet wird.
Der Befehl ändert den Namen des speicherkontos nicht.

### Beispiel 3: Festlegen der Überwachungsrichtlinie eines Azure SQL Server für die Verwendung eines bestimmten Ereignistyps
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventType Login_Failure
```

### Beispiel 4: Festlegen der Überwachungsrichtlinie einer Datenbank für die Verwendung der BLOB-Überwachung
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -RetentionInDays 8
```

Mit diesem Befehl wird die Überwachungsrichtlinie des Servers mit dem Namen Server01 für die Verwendung des Login_Failure-Ereignistyps festgelegt.
Mit diesem Befehl werden keine anderen Einstellungen geändert.

## Parameter

### -AuditActionGroup
Geben Sie mindestens eine Überwachungs Aktionsgruppe an. Dieser Parameter gilt nur für die BLOB-Überwachung.

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
Geben Sie den Überwachungstyp an. Überwachungsprotokolle können in den Tabellenspeicher oder BLOB-Speicher geschrieben werden. Die BLOB-Überwachung bietet eine höhere Leistung und unterstützt die Überwachung auf Objektebene.

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

### -EventType
Gibt die zu überwachenden Ereignistypen an.
Dieser Parameter gilt nur für die Tabellen Überwachung.

Sie können mehrere Ereignistypen angeben.
Sie können alle angeben, um alle Ereignistypen oder None zu überwachen, um anzugeben, dass keine Ereignisse überwacht werden.
Wenn Sie alle oder keine gleichzeitig angeben, schlägt der Befehl fehl.

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
Gibt den Namen der Ressourcengruppe an, die die Datenbank enthält.

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
Dies ist die Standardeinstellung.
Wenn Sie einen Wert angeben, der größer als 0 (null) ist, müssen Sie auch einen Wert für den *TableIdentifer* -Parameter angeben.

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
Gibt den Namen des Servers an, der die Datenbank enthält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Gibt den Namen des speicherkontos für die Überwachung der Datenbank an.
Platzhalterzeichen sind nicht zulässig.
Wenn Sie diesen Parameter nicht angeben, verwendet das Cmdlet das Speicherkonto, das zuvor als Teil der Überwachungsrichtlinie der Datenbank definiert wurde.
Wenn dies das erste Mal ist, dass eine Datenbank-Überwachungsrichtlinie definiert ist und Sie diesen Parameter nicht angeben, schlägt der Befehl fehl.

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

### Microsoft. Azure. Commands. SQL. Security. Model. ServerAuditingPolicyModel

## Notizen

## Verwandte Links

[Get-AzureRmSqlServerAuditingPolicy](./Get-AzureRmSqlServerAuditingPolicy.md)

[Verwenden von-AzureRmSqlServerAuditingPolicy](./Use-AzureRmSqlServerAuditingPolicy.md)

[SQL-Datenbank-Dokumentation](https://docs.microsoft.com/azure/sql-database/)


