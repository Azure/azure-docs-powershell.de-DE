---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0f43956dfa29dac2d7c6ca1869716400b8adad35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501373"
---
# Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy

## Synopsis
Ruft eine Datenbank-langfristige Aufbewahrungsrichtlinie ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-Current] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** " Ruft die langfristige Aufbewahrungsrichtlinie ab, die für diese Datenbank registriert ist.
Bei der Richtlinie handelt es sich um eine Azure-Sicherungs Ressource, die zum Definieren von Sicherungsspeicher Richtlinien verwendet wird.

## Beispiele

### Beispiel 1: Abrufen der aktuellen Version der langfristigen Aufbewahrungsrichtlinie
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -Current


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

Dieser Befehl ruft die aktuelle Version der langfristigen Aufbewahrungsrichtlinie für database01 ab.

### Beispiel 2: Abrufen der älteren Version der langfristigen Aufbewahrungsrichtlinie
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        :
MonthlyRetention                       :
YearlyRetention                        :
WeekOfYear                             :
State                                  : Enabled
RecoveryServicesBackupPolicyResourceId : /subscriptions/4f2b42fc-4fc3-fd41-8ab8-5a382d8b30df/resourceGroups/resourcegroup01/providers/MicrosoftRecoveryServices/vaults/vault01/backupPolicies/policy01
Location                               : Southeast Asia
```

Dieser Befehl ruft die Legacy Version der langfristigen Aufbewahrungsrichtlinie für database01

## Parameter

### -Current
Wenn Sie nicht bereitgestellt wird, gibt der Befehl die Legacy Informationen zur langfristigen Aufbewahrungsrichtlinie zurück.
Andernfalls gibt der Befehl die aktuelle Version der langfristigen Aufbewahrungsrichtlinie zurück.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
Der Name der zu verwendenden Azure SQL-Datenbank.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -ResourceGroupName
Der Name der Ressourcengruppe.

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

### -Servername
Der Name des Azure SQL Server, in dem sich die Datenbank befindet.

```yaml
Type: String
Parameter Sets: (All)
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
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.
Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel

## Notizen

## Verwandte Links

[Get-AzureRmSqlDatabaseLongTermRetentionBackup](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[Remove-AzureRmSqlDatabaseLongTermRetentionBackup](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[Satz-AzureRmSqlDatabaseBackupLongTermRetentionPolicy](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[SQL-Datenbank-Dokumentation](https://docs.microsoft.com/azure/sql-database/)
