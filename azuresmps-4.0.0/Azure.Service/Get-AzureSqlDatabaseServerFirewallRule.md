---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: BE00A25D-3ECE-4B27-9D79-78128CFEBDB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 100202df1871610aff3af1fe90bb7d603c141d62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005778"
---
# Get-AzureSqlDatabaseServerFirewallRule

## Synopsis
Ruft Firewallregeln für Azure SQL-Daten Bank Server ab.

## Syntax

```
Get-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureSqlDatabaseServerFirewallRule** " ruft Firewallregeln für eine Instanz des Azure SQL-Datenbankservers ab.
Wenn Sie eine Firewallregel mit dem Namen angeben, gibt dieses Cmdlet Informationen zu dieser Firewallregel zurück.
Andernfalls gibt das Cmdlet Informationen zu allen Firewallregeln auf dem angegebenen Azure SQL-Datenbankserver zurück.

## Beispiele

### Beispiel 1: Abrufen aller Firewallregeln auf einem Server
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y"
```

Dieser Befehl ruft alle Firewallregeln auf dem Azure SQL-Datenbankserver mit dem Namen lpqd0zbr8y ab.

### Beispiel 2: Abrufen einer Firewallregel mithilfe des Namens
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24"
```

Dieser Befehl ruft die Firewallregel mit dem Namen FirewallRule24 auf dem Server mit dem Namen lpqd0zbr8y.

## Parameter

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RuleName
Gibt den Namen der Firewall-Regel an, die dieses Cmdlet erhält.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Servername
Gibt den Namen eines Servers an.
Dieses Cmdlet ruft Firewallregeln vom Server ab, den dieser Parameter angibt.
Geben Sie den Servernamen und nicht den vollqualifizierten DNS-Namen an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerFirewallRuleContext

## Ausgaben

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext\>

## Notizen

## Verwandte Links

[Azure SQL-Datenbank](https://azure.microsoft.com/en-us/services/sql-database/)

[Listen Firewall-Regeln](https://msdn.microsoft.com/en-us/library/azure/dn505715.aspx)

[Vorgänge für Azure SQL-Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Neu – AzureSqlDatabaseServerFirewallRule](./New-AzureSqlDatabaseServerFirewallRule.md)

[Remove-AzureSqlDatabaseServerFirewallRule](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[Satz-AzureSqlDatabaseServerFirewallRule](./Set-AzureSqlDatabaseServerFirewallRule.md)


