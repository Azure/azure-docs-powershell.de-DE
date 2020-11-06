---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D3BA6534-CAAC-41E2-8442-0606B712E2B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: a7cf769b1150ef7e209bd02234674bb26927f9a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498170"
---
# Remove-AzureRmSqlDatabaseAuditing

## Synopsis
Entfernt die Überwachung einer Datenbank.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Remove-AzureRmSqlDatabaseAuditing [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureRmSqlDatabaseAuditing** entfernt die Überwachung einer Azure SQL-Datenbank.
Um dieses Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Datenbank zu identifizieren.
Nachdem Sie dieses Cmdlet ausgeführt haben, wird die Überwachung der Datenbank nicht durchgeführt.
Wenn der Befehl erfolgreich ausgeführt wird und Sie den *passthru* -Parameter verwendet haben, gibt das Cmdlet zusätzlich zu den Datenbankbezeichnern ein Objekt zurück, das die aktuelle Überwachungsrichtlinie beschreibt.
Zu den Datenbankbezeichnern gehören die **ResourceGroupName** , **Servername** und **DatabaseName** , sind aber nicht darauf limitiert.
Wenn Sie die Überwachung einer Azure SQL-Datenbank entfernen, wird die Bedrohungserkennung ebenfalls entfernt.
Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.

## Beispiele

### Beispiel 1: Entfernen der Überwachung einer Azure SQL-Datenbank
```
PS C:\>Remove-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

Dieser Befehl entfernt die Überwachung der Datenbank mit dem Namen database01.
Diese Datenbank befindet sich auf Server01, die der Ressourcengruppe mit dem Namen ResourceGroup01 zugewiesen ist.

## Parameter

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -PassThru
Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten. Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.

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

### -Servername
Gibt den Namen des Servers an, der die Datenbank enthält.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. SQL. Auditing. Model. AuditingPolicyModel

## Notizen

## Verwandte Links

[Get-AzureRmSqlDatabaseAuditingPolicy](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[Satz-AzureRmSqlDatabaseAuditingPolicy](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[SQL-Datenbank-Dokumentation](https://docs.microsoft.com/azure/sql-database/)


