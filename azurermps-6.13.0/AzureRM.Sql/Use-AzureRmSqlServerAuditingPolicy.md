---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 381F5B34-983C-4733-B384-35D6579B79A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/use-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: a0dc151c86caf41131649f7e4e37ee60c6f19b01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498165"
---
# Use-AzureRmSqlServerAuditingPolicy

## Synopsis
Gibt an, dass eine Datenbank die Überwachungsrichtlinie Ihres Hostservers verwendet.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Use-AzureRmSqlServerAuditingPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **use-AzureRmSqlServerAuditingPolicy** gibt an, dass eine Datenbank die Überwachungsrichtlinie Ihres Hostservers verwendet.
Geben Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* an, um die Datenbank zu identifizieren.
Wenn für den Datenbankserver keine Überwachungsrichtlinie definiert ist, schlägt dieses Cmdlet fehl.
Wenn der Host die Überwachung auf Serverebene verwendet, wird die Bedrohungserkennung entfernt.

## Beispiele

### Beispiel 1: Konfigurieren einer Datenbank für die Verwendung der Überwachungsrichtlinie Ihres Servers
```
PS C:\>Use-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server02" -DatabaseName "Database01"
```

Dieser Befehl gibt an, dass die Datenbank mit dem Namen database01 in Server02 die Überwachungsrichtlinie des Servers verwendet.

## Parameter

### -DatabaseName
Gibt den Namen der Datenbank an, in der die Überwachungsrichtlinie verwendet wird.

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
Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.

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
Gibt den Namen des Servers an, der die Datenbank hostet, die die Überwachungsrichtlinie verwendet.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. SQL. Auditing. Model. AuditingPolicyModel

## Notizen

## Verwandte Links

[Get-AzureRmSqlDatabaseAuditingPolicy](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[Get-AzureRmSqlServerAuditingPolicy](./Get-AzureRmSqlServerAuditingPolicy.md)

[Satz-AzureRmSqlDatabaseAuditingPolicy](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[Satz-AzureRmSqlServerAuditingPolicy](./Set-AzureRmSqlServerAuditingPolicy.md)

[SQL-Datenbank-Dokumentation](https://docs.microsoft.com/azure/sql-database/)


