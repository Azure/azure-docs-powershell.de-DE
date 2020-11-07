---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
ms.openlocfilehash: 8601be969ce08c86a723af51e82be89125367d4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825720"
---
# Set-AzSqlServerAudit

## Synopsis
Ändert die Überwachungseinstellungen eines Azure SQL Server.

## Syntax

### ServerParameterSet (Standard)
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServerObjectParameterSet
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzSqlServerAudit** " ändert die Überwachungseinstellungen eines Azure SQL Server.
Um das Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* und Server *Name* , um den Server zu identifizieren.
Wenn der BLOB-Speicher ein Ziel für Überwachungsprotokolle ist, geben Sie den *StorageAccountResourceId* -Parameter an, um das Speicherkonto für die Überwachungsprotokolle und den *StorageKeyType* -Parameter zum Definieren der Speicherschlüssel zu ermitteln. Sie können auch die Aufbewahrung für die Überwachungsprotokolle definieren, indem Sie den Wert des *RetentionInDays* -Parameters festlegen, um den Zeitraum für die Überwachungsprotokolle zu definieren.

## Beispiele

### Beispiel 1: Aktivieren der BLOB-Speicher Überwachungsrichtlinie eines Azure SQL Server
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### Beispiel 2: Deaktivieren der BLOB-Speicher Überwachungsrichtlinie eines Azure SQL Server
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### Beispiel 3,1: Aktivieren der BLOB-Speicher Überwachungsrichtlinie eines Azure SQL Server mit erweiterter Filterung mithilfe eines T-SQL-Prädikats
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -PredicateExpression "statement <> 'select 1'"
```

### Beispiel 3,2: Entfernen der erweiterten Filtereinstellung aus der Überwachungsrichtlinie eines Azure SQL Server
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -PredicateExpression ""
```

### Beispiel 4: Aktivieren der Ereignis-Hub-Überwachungsrichtlinie eines Azure SQL Server
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### Beispiel 5: Deaktivieren der Ereignis-Hub-Überwachungsrichtlinie eines Azure SQL Server
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### Beispiel 6: Aktivieren der Überwachungsrichtlinie für die Protokollanalyse eines Azure SQL Server
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### Beispiel 7: Deaktivieren der Überwachungsrichtlinie für die Protokollanalyse eines Azure SQL Server
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### Beispiel 8: Deaktivieren Sie die Protokollanalyse-Überwachungsrichtlinie eines Azure SQL Server durch Pipeline.
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAudit -LogAnalyticsTargetState Disabled
```

### Beispiel 9: Deaktivieren Sie das Senden von Überwachungseinträgen eines Azure SQL Server an den BLOB-Speicher, und aktivieren Sie das Senden an die Protokollanalyse.
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### Beispiel 10: Aktivieren des Sendens von Überwachungsdatensätzen eines Azure SQL Server an BLOB-Speicher, Ereignis-Hub und Protokollanalyse.
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## Parameter

### -AsJob
Ausführen eines Cmdlets im Hintergrund

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

### -AuditActionGroup
Die empfohlene Gruppe der zu verwendenden Aktionsgruppen ist die folgende Kombination, die alle Abfragen und gespeicherten Prozeduren überprüft, die für die Datenbank ausgeführt werden, sowie erfolgreiche und fehlgeschlagene Anmeldungen:  
  
"BATCH_COMPLETED_GROUP",  
"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",  
"FAILED_DATABASE_AUTHENTICATION_GROUP"  
Diese obige Kombination ist auch die standardmäßig konfigurierte Gruppe. Diese Gruppen decken alle SQL-Anweisungen und gespeicherten Prozeduren ab, die für die Datenbank ausgeführt werden, und sollten nicht in Verbindung mit anderen Gruppen verwendet werden, da dies zu doppelten Überwachungsprotokollen führt.
Weitere Informationen finden Sie unter https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlobStorageTargetState
Gibt an, ob der BLOB-Speicher ein Ziel für Überwachungsdatensätze ist.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -EventHubAuthorizationRuleResourceId
Die Ressourcen-ID für die Ereignis-Hub-Autorisierungsregel

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

### -EventHubName
Der Name des Ereignis Hubs. Wenn beim Bereitstellen von EventHubAuthorizationRuleResourceId keine angegeben wird, wird der Standardereignis-Hub ausgewählt.

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

### -EventHubTargetState
Gibt an, ob der Ereignis-Hub ein Ziel für Überwachungsdatensätze ist.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LogAnalyticsTargetState
Gibt an, ob die Protokollanalyse ein Ziel für Überwachungsdatensätze ist.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Gibt an, ob die Überwachungsrichtlinie am Ende der Cmdlet-Ausführung ausgegeben werden soll.

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

### -Prädikat
Das T-SQL-Prädikat (WHERE-Klausel), das zum Filtern von Überwachungsprotokollen verwendet wird.

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

### -ResourceGroupName
Der Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetentionInDays
Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Servername
SQL Server-Name.

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerObject
Das Serverobjekt, dessen Überwachungsrichtlinie verwaltet werden soll.

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StorageAccountResourceId
Die Ressourcen-ID des speicherkontos

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

### -StorageKeyType
Gibt an, welche der Speicherzugriffs Tasten verwendet werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceResourceId
Die Arbeitsbereichs-ID (Ressourcen-ID eines Protokollanalyse Arbeitsbereichs) für einen Protokollanalyse Arbeitsbereich, an den Sie Überwachungsprotokolle senden möchten. Beispiel:/Subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/Insights-Integration/Providers/Microsoft.OperationalInsights/Workspaces/viruela2

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

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

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

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

### Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel

### Microsoft. Azure. Commands. SQL. Auditing. Model. AuditActionGroups []

### System. GUID

### System. Nullable ' 1 [[System. UInt32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

### Microsoft. Azure. Commands. SQL. Auditing. Model. ServerAuditModel

## Ausgaben

### System. Boolean

## Notizen

## Verwandte Links
