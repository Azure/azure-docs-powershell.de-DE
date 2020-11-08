---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A723D12D-DCF5-4F0C-AAC2-8BADFBAC3328
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0383e451d8346d4b6465390cc78850b270f6ac3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006175"
---
# New-AzureSqlDatabaseServerFirewallRule

## Synopsis
Erstellt eine Firewall-Regel in Azure SQL-Daten Bank Server.

## Syntax

### IpRange (Standard)
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AllowAllAzureServices
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-AllowAllAzureServices]
 [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureSqlDatabaseServerFirewallRule** erstellt eine Firewallregel in der angegebenen Instanz des Azure SQL-Datenbankservers im aktuellen Abonnement.

Verwenden Sie die *StartIpAddress* -und *EndIpAddress* -Parameter, um einen Bereich von IP-Adressen anzugeben, die von dieser Regel zum Herstellen einer Verbindung mit dem Azure SQL-Datenbankserver zulässig sind.

Geben Sie den *AllowAllAzureServices* -Parameter an, um eine Regel zu erstellen, die Azure-Verbindungen mit dem Server ermöglicht.
Die Regel hat die Anfangs-und Endwerte der IP-Adressen von 0.0.0.0.
Wenn Sie keinen Firewallregel-Regelnamen angeben, weist dieses Cmdlet den Standardnamen AllowAllAzureServices zu.

## Beispiele

### Beispiel 1: Erstellen einer Firewall-Regel
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.1 -EndIpAddress 10.1.1.2
```

Mit diesem Befehl wird ein Firewallregel-FirewallRule24 auf dem Azure SQL-Datenbankserver mit dem Namen lpqd0zbr8y erstellt.
Der Befehl gibt einen IP-Adressbereich an.

### Beispiel 2: Erstellen einer Regel, die alle Azure-Dienste zulässt
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices -RuleName "AzureConnections"
```

Dieser Befehl erstellt eine Firewallregel mit dem Namen AzureConnections auf dem Server mit dem Namen lpqd0zbr8y, der Azure-Verbindungen zulässt.

### Beispiel 3: Erstellen einer Regel, mit der alle Azure-Dienste, die den Standardnamen verwenden, eine Regel erstellen, die alle Azure-Dienste zulässt, die den Standardnamen verwenden
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices
```

Mit diesem Befehl wird eine Firewallregel auf dem angegebenen Server mit dem Namen "lpqd0zbr8y" erstellt, die Azure-Verbindungen zulässt.
Der Befehl weist den standardmäßigen Regelnamen AllowAllAzureServices.

## Parameter

### -AllowAllAzureServices
Gibt an, dass diese Firewall-Regel alle Azure-IP-Adressen für den Zugriff auf den Server aktiviert.

```yaml
Type: SwitchParameter
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndIpAddress
Gibt den Endwert des IP-Adressbereichs für diese Regel an.

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
Gibt den Namen der neuen Firewallregel an.

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Servername
Gibt den Namen eines Servers an.
Mit diesem Cmdlet wird eine Firewallregel auf dem Server erstellt, die von diesem Cmdlet angegeben wird.
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

### -StartIpAddress
Gibt den Startwert des IP-Adressbereichs für die Firewallregel an.

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

## Ausgaben

### Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerFirewallRuleContext

## Notizen

## Verwandte Links

[Azure SQL-Datenbank](https://azure.microsoft.com/en-us/services/sql-database/)

[Firewall-Regel erstellen](https://msdn.microsoft.com/en-us/library/azure/dn505712.aspx)

[Vorgänge für Azure SQL-Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabaseServerFirewallRule](./Get-AzureSqlDatabaseServerFirewallRule.md)

[Remove-AzureSqlDatabaseServerFirewallRule](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[Satz-AzureSqlDatabaseServerFirewallRule](./Set-AzureSqlDatabaseServerFirewallRule.md)


