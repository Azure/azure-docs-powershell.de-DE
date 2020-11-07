---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaserecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: 49ea5796e8f2b03fe67a6c40ab42dc7f1c2481e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825875"
---
# Set-AzSqlDatabaseRecommendedActionState

## Synopsis
Aktualisiert den Zustand einer Azure SQL-Datenbank Empfohlene Aktion.

## Syntax

```
Set-AzSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzSqlDatabaseRecommendedActionState** " aktualisiert den Zustand einer Azure SQL-Datenbank-empfohlenen Aktion.
Dadurch kann eine empfohlene Aktion auf Grundlage des neuen Zustands angewendet, zurückgesetzt oder verworfen werden.

## Beispiele

### Beispiel 1: Anwenden eines empfohlenen Aktionszustands auf "Ausstehend"
```
PS C:\>Set-AzSqlDatabaseRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
DatabaseName               : WIRunner

ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.0361551_6C7AE8CC9C87E7FD5893], [indexType, 
                             NONCLUSTERED], [schema, [test_schema]], [table, [test_table_0.0361551]]...} 
ErrorDetails               : Microsoft.Azure.Management.Sql.Models.RecommendedActionErrorInfo
EstimatedImpact            : {ActionDuration, SpaceChange}
ExecuteActionDuration      : PT1M
ExecuteActionInitiatedBy   : User
ExecuteActionInitiatedTime : 4/21/2016 3:24:47 PM
ExecuteActionStartTime     : 4/21/2016 3:24:47 PM
ImplementationDetails      : Microsoft.Azure.Management.Sql.Models.RecommendedActionImplementationInfo
IsArchivedAction           : False
IsExecutableAction         : True
IsRevertableAction         : True
LastRefresh                : 4/21/2016 3:24:47 PM
LinkedObjects              : {}
ObservedImpact             : {CpuUtilization, LogicalReads, LogicalWrites, QueriesWithImprovedPerformance...} 
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 2
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

Dieser Befehl aktualisiert den Zustand der empfohlenen Aktion mit dem Namen IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893, die zu der Datenbank mit dem Namen WIRunner to Pending gehört.

## Parameter

### -Advisorname
Gibt den Namen des Beraters an, zu dem diese empfohlene Aktion gehört.

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

### -DatabaseName
Gibt den Namen der Datenbank an, für die dieses Cmdlet den empfohlenen Aktionszustand festlegt.

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -RecommendedActionName
Gibt den Namen der empfohlenen Aktion an, für die der Zustand aktualisiert wird.

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

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe des Servers an, der diese Datenbank enthält.

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

### -Servername
Gibt den Namen des Servers an, in dem sich die Datenbank befindet.

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

### -Bundesland
Gibt den neuen Wert an, mit dem dieses Cmdlet den empfohlenen Aktionszustand aktualisiert.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- Active
- Ausstehend
- PendingRevert
- RevertCancelled
- Ignoriert
- Gelöst

```yaml
Type: Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Pending, PendingRevert, RevertCancelled, Ignored, Resolved

Required: True
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

### Microsoft. Azure. Commands. SQL. recommended. Cmdlet. RecommendedActionState

## Ausgaben

### Microsoft. Azure. Commands. SQL. recommendive. Model. AzureSqlDatabaseRecommendedActionModel

## Notizen
* Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, SQL, Datenbank, MSSQL, Ratgeber, empfohlenes

## Verwandte Links

[Get-AzSqlServerAdvisor](./Get-AzSqlServerAdvisor.md)

[Get-AzSqlElasticPoolAdvisor](./Get-AzSqlElasticPoolAdvisor.md)

[Get-AzSqlServerRecommendedAction](./Get-AzSqlServerRecommendedAction.md)

[Get-AzSqlElasticPoolRecommendedAction](./Get-AzSqlElasticPoolRecommendedAction.md)

[Satz-AzSqlElasticPoolRecommendedActionState](./Set-AzSqlElasticPoolRecommendedActionState.md)

[Satz-AzSqlElasticPoolAdvisorAutoExecuteStatus](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[Satz-AzSqlElasticPoolRecommendedActionState](./Set-AzSqlElasticPoolRecommendedActionState.md)

[Satz-AzSqlServerRecommendedActionState](./Set-AzSqlServerRecommendedActionState.md)

[Satz-AzSqlElasticPoolAdvisorAutoExecuteStatus](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[Satz-AzSqlServerAdvisorAutoExecuteStatus](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[SQL-Datenbank-Dokumentation](https://docs.microsoft.com/azure/sql-database/)
