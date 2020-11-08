---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: cdcd4788e3eefdce858cb88c0bf1885353f8a673
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006176"
---
# New-AzureSqlDatabaseServerContext

## Synopsis
Erstellt einen Server Verbindungskontext.

## Syntax

### ByServerNameWithSqlAuth (Standard)
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByManageUrlWithSqlAuth
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerNameWithCertAuth
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByFullyQualifiedServerNameWithSqlAuth
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByFullyQualifiedServerNameWithCertAuth
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureSqlDatabaseServerContext** erstellt einen Azure SQL-Datenbankserver-Verbindungskontext.
Verwenden Sie die SQL Server-Authentifizierung, um einen Verbindungskontext zu einem SQL-Datenbankserver mithilfe der angegebenen Anmeldeinformationen zu erstellen.
Sie können den SQL-Datenbankserver über den Namen, den vollqualifizierten Namen oder die URL angeben.
Verwenden Sie zum Abrufen von Anmeldeinformationen das Get-Credential-Cmdlet, in dem Sie aufgefordert werden, den Benutzernamen und das Kennwort anzugeben.

Verwenden Sie das Cmdlet **New-AzureSqlDatabaseServerContext** mit zertifikatbasierter Authentifizierung, um einen Verbindungskontext zum angegebenen SQL-Datenbankserver mithilfe der angegebenen Azure-Abonnementdaten zu erstellen.
Sie können den SQL-Datenbankserver nach Name oder nach dem vollqualifizierten Namen angeben.
Sie können die Abonnementdaten als Parameter angeben, oder Sie können aus dem aktuellen Azure-Abonnement abgerufen werden.
Verwenden Sie das Cmdlet Select-AzureSubscription https://msdn.microsoft.com/library/windowsazure/jj152833.aspx , um das aktuelle Azure-Abonnement auszuwählen.

## Beispiele

### Beispiel 1: Erstellen eines Kontexts mithilfe der SQL Server-Authentifizierung
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

In diesem Beispiel wird die SQL Server-Authentifizierung verwendet.

Der erste Befehl fordert Sie zur Eingabe von Anmeldeinformationen für den Server Administrator auf und speichert die Anmeldeinformationen in der $Credential Variablen.

Der zweite Befehl stellt mithilfe von $Credential eine Verbindung mit dem SQL-Datenbankservernamens lpqd0zbr8y her.

Der endgültige Befehl erstellt eine Datenbank mit dem Namen Database17 auf dem Server, die Teil des Kontexts in $context ist.

### Beispiel 2: Erstellen eines Kontexts mithilfe der zertifikatbasierten Authentifizierung
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

In diesem Beispiel wird die zertifikatbasierte Authentifizierung verwendet.

Die ersten beiden Befehle weisen den $SubscriptionId-und $Thumbprint Variablenwerte zu.

Der dritte Befehl ruft das vom Fingerabdruck angegebene Zertifikat in $Thumbprint ab und speichert es in $Certificate.

Der vierte Befehl legt fest, dass das Abonnement Subscription07 sein soll, und der fünfte Befehl wählt dieses Abonnement aus.

Der endgültige Befehl erstellt einen Kontext im aktuellen Abonnement für den Server mit dem Namen lpqd0zbr8y.

## Parameter

### – Anmeldeinformationen
Gibt ein Anmeldeinformationsobjekt an, das Ihnen die SQL Server-Authentifizierung für den Zugriff auf den Server bietet.

```yaml
Type: PSCredential
Parameter Sets: ByServerNameWithSqlAuth, ByManageUrlWithSqlAuth, ByFullyQualifiedServerNameWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullyQualifiedServerName
Gibt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) für den Azure SQL-Datenbankserver an.
Beispiel: Server02.Database.Windows.net.

```yaml
Type: String
Parameter Sets: ByFullyQualifiedServerNameWithSqlAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManageUrl
Gibt die URL an, die dieses Cmdlet für den Zugriff auf das Azure SQL DatabaseManagement-Portal für den Server verwendet.

```yaml
Type: Uri
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: True
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

### -Servername
Gibt den Namen des Datenbankservers an.

```yaml
Type: String
Parameter Sets: ByServerNameWithSqlAuth, ByServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Abonnementname
Gibt den Namen des Azure-Abonnements an, das von diesem Cmdlet zum Erstellen des Verbindungskontexts verwendet wird.
Wenn Sie keinen Wert für diesen Parameter angeben, verwendet das Cmdlet das aktuelle Abonnement.
Führen Sie das Select-AzureSubscription-Cmdlet aus, um das aktuelle Abonnement zu ändern.

```yaml
Type: String
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UseSubscription
Gibt an, dass dieses Cmdlet Azure-Abonnement zum Erstellen des Verbindungskontexts verwendet.

```yaml
Type: SwitchParameter
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. IServerDataServiceContext

## Notizen
* Wenn Sie sich authentifizieren, ohne eine Domäne anzugeben, und wenn Sie Windows PowerShell 2,0 verwenden, gibt das Get-Credential-Cmdlet einen umgekehrten Schrägstrich () zurück, \\ der dem Benutzernamen vorangestellt wurde, beispielsweise \User. Windows PowerShell 3,0 fügt den umgekehrten Schrägstrich nicht hinzu. Dieser umgekehrte Schrägstrich wird vom *Credential* -Parameter des **New-AzureSqlDatabaseServerContext-** Cmdlets nicht erkannt. Verwenden Sie die folgenden Befehle, um Sie zu entfernen:

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## Verwandte Links

[Azure SQL-Datenbank-Cmdlets](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[Neu – AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Satz-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


