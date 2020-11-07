---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
ms.openlocfilehash: cf9bea67027e7a2c5e3928755f6d88b1dc124489
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826083"
---
# Get-AzSqlServerAuditing

## Synopsis
**Wichtig: Dieses Cmdlet ist veraltet, wenn Sie von [Get-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveraudit) ersetzt werden.**

Ruft die Überwachungseinstellungen eines Azure SQL Server ab.

## Syntax

### DefaultParameterSet (Standard)
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### EventHubSet
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### LogAnalyticsSet
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BlobStorageByParentResourceSet
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### EventHubByParentResourceSet
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### LogAnalyticsByParentResourceSet
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzSqlServerAuditing** " Ruft die Überwachungseinstellungen eines Azure SQL Server ab.
Geben Sie die Parameter *ResourceGroupName* und Server *Name* an, um den Server zu identifizieren.
Das Ziel der Überwachungsprotokolle wird bestimmt, indem Sie einen der folgenden Switch-Parameter angeben: BlobStorage, LogAnalytics oder EventHub (wenn keine angegeben ist, ist der Standardwert BlobStorage).

## Beispiele

### Beispiel 1: Abrufen der BLOB-Speicher Überwachungseinstellungen eines Azure SQL Server
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### Beispiel 2: Abrufen der Speicher Überwachungseinstellungen für BLOB-Speicher eines Azure SQL Server
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -BlobStorage
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### Beispiel 3: Abrufen, durch Pipeline, die Speicher Überwachungseinstellungen für BLOB-Speicher eines Azure SQL Server
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerAuditing -BlobStorage
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### Beispiel 4: Abrufen der Ereignis-Hub-Überwachungseinstellungen eines Azure SQL Server
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -EventHub
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
PredicateExpression                 : statement <> 'select 1'
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
```

### Beispiel 5: Abrufen, durch Pipeline, die Ereignis-Hub-Überwachungseinstellungen eines Azure SQL Server
```
PS C:\>$server = Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
PS C:\>$server | Get-AzSqlServerAuditing -EventHub
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
PredicateExpression                 : statement <> 'select 1'
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
```

### Beispiel 6: Abrufen der Überwachungseinstellungen für die Protokollanalyse eines Azure SQL Server
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -LogAnalytics
AuditActionGroup    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName   : resourcegroup01
ServerName          : server01
AuditState          : Enabled
PredicateExpression : statement <> 'select 1'
WorkspaceResourceId : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## Parameter

### -BlobStorage
Gibt an, dass das Überwachungsprotokoll Ziel BLOB-Speicher ist

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -EventHub
Gibt an, dass das Überwachungsprotokoll Zielereignis-Hub ist

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Inputobject
Das Serverobjekt, dessen Überwachungsrichtlinie verwaltet werden soll.

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: BlobStorageByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LogAnalytics
Gibt an, dass die Überwachungsprotokolle Zielprotokoll Analyse sind.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Servername
SQL Server-Name.

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
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

### System. Management. Automation. Switchparameter

## Ausgaben

### Microsoft. Azure. Commands. SQL. Auditing. Model. ServerBlobAuditingSettingsModel

## Notizen

## Verwandte Links
