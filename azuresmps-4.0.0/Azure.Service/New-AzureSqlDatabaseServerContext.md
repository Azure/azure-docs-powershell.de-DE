---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5312556cb49d02ea901b4cb2526a36f7237f66d1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404172"
---
# New-AzureSqlDatabaseServerContext

## SYNOPSIS
Erstellt einen Serververbindungskontext.

## SYNTAX

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

## BESCHREIBUNG
Das **Cmdlet "New-AzureSqlDatabaseServerContext"** erstellt einen Azure SQL Datenbankserververbindungskontext.
Verwenden SQL Server A0 zum Erstellen eines Verbindungskontexts mit SQL Datenbankserver mit den angegebenen Anmeldeinformationen.
Sie können den SQL Datenbankserver nach Name, vollqualifizierten Namen oder URL angeben.
Zum Abrufen von Anmeldeinformationen verwenden Sie das Get-Credential-Cmdlet, in dem Sie aufgefordert werden, den Benutzernamen und das Kennwort anzugeben.

Verwenden Sie **das Cmdlet "New-AzureSqlDatabaseServerContext"** mit zertifikatbasierter Authentifizierung, um einen Verbindungskontext mit dem angegebenen SQL-Datenbankserver mithilfe der angegebenen Azure-Abonnementdaten zu erstellen.
Sie können SQL Datenbankserver nach Name oder nach dem vollqualifizierten Namen angeben.
Sie können die Abonnementdaten als Parameter angeben oder sie aus dem aktuellen Abonnement von Azure abrufen.
Verwenden Sie das Cmdlet "Select-AzureSubscription", https://msdn.microsoft.com/library/windowsazure/jj152833.aspx um das aktuelle Azure-Abonnement auszuwählen.

## BEISPIELE

### Beispiel 1: Erstellen eines Kontexts mithilfe SQL Server Authentifizierung
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

In diesem Beispiel wird die SQL Server verwendet.

Der erste Befehl fordert Sie zur Eingabe von Serveradministratoranmeldeinformationen auf und speichert die Anmeldeinformationen in der $Credential Variable.

Der zweite Befehl stellt mithilfe von "lpqd0zbr8y" eine Verbindung mit dem SQL Datenbankserver $Credential.

Mit dem letzten Befehl wird eine Datenbank mit dem Namen "Database17" auf dem Server erstellt, die Teil des Kontexts in $Context.

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

Die ersten beiden Befehle weisen den Variablen $SubscriptionId $Thumbprint zu.

Der dritte Befehl ruft das Zertifikat ab, das durch den Fingerabdruck in der $Thumbprint identifiziert wurde, und speichert es in $Certificate.

Der vierte Befehl legt das Abonnement auf "Subscription07" fest, und mit dem fünften Befehl wird dieses Abonnement ausgewählt.

Der letzte Befehl erstellt einen Kontext im aktuellen Abonnement für den Server namens lpqd0zbr8y.

## PARAMETERS

### -Credential
Gibt ein Anmeldeinformationsobjekt an, das SQL Server für den Zugriff auf den Server bietet.

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
Gibt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) für den Azure SQL Datenbankserver an.
Beispiel: Server02.database.windows.net.

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
Gibt die URL an, die dieses Cmdlet für den Zugriff auf das Azure SQL DatabaseManagement Portal für den Server verwendet.

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

### -Profile
Gibt das Azure-Profil an, aus dem dieses Cmdlet liest.
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

### -ServerName
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

### -SubscriptionName
Gibt den Namen des Azure-Abonnements an, das von diesem Cmdlet zum Erstellen des Verbindungskontexts verwendet wird.
Wenn Sie keinen Wert für diesen Parameter angeben, verwendet das Cmdlet das aktuelle Abonnement.
Führen Sie Select-AzureSubscription cmdlet aus, um das aktuelle Abonnement zu ändern.

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
Gibt an, dass dieses Cmdlet das Abonnement von Azure zum Erstellen des Verbindungskontexts verwendet.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

## AUSGABEN

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext

## HINWEISE
* Wenn Sie sich authentifizieren, ohne eine Domäne anzugeben, und wenn Sie Windows PowerShell 2.0 verwenden, gibt das Cmdlet Get-Credential einen umgekehrten Schrägstrich () zurück, der dem Benutzernamen vorankommt, z. B. \\ "\user". Windows PowerShell 3.0 wird kein umgekehrter Schrägstrich hinzugefügt. Dieser umgekehrte Schrägstrich wird vom Parameter *"Credential"* des **Cmdlets "New-AzureSqlDatabaseServerContext"** nicht erkannt. Verwenden Sie zum Entfernen Befehle wie die folgenden:

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## LINKS ZU VERWANDTEN THEMEN



[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[New-AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


