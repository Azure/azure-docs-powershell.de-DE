---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383DD041-78DC-4170-9529-1FD6F13BC178
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29cbf01629ef772fc41436f3916a2077c1535329
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006312"
---
# Remove-AzureSqlDatabaseServerFirewallRule

## Synopsis
Entfernt eine Firewall-Regel von einem Azure SQL-Datenbankserver.

## Syntax

```
Remove-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Remove-AzureSqlDatabaseServerFirewallRule** " entfernt eine Firewall-Regel aus einer Instanz des Azure SQL-Datenbankservers im aktuellen Abonnement.

## Beispiele

### Beispiel 1: Entfernen einer Regel
```
PS C:\>Remove-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24"
```

Dieser Befehl entfernt die Firewallregel mit dem Namen FirewallRule24 aus dem Azure SQL-Datenbankserver mit dem Namen lpqd0zbr8y.

## Parameter

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
Gibt den Namen der Firewall-Regel an, die vom Cmdlet entfernt wird.

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

### -Servername
Gibt den Namen eines Servers an.
Dieses Cmdlet entfernt eine Firewallregel vom Server, die dieser Parameter angibt.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerFirewallRuleContext

## Ausgaben

## Notizen

## Verwandte Links

[Azure SQL-Datenbank](https://azure.microsoft.com/en-us/services/sql-database/)

[Firewall-Regel löschen](https://msdn.microsoft.com/en-us/library/azure/dn505706.aspx)

[Vorgänge für Azure SQL-Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabaseServerFirewallRule](./Get-AzureSqlDatabaseServerFirewallRule.md)

[Neu – AzureSqlDatabaseServerFirewallRule](./New-AzureSqlDatabaseServerFirewallRule.md)

[Satz-AzureSqlDatabaseServerFirewallRule](./Set-AzureSqlDatabaseServerFirewallRule.md)


