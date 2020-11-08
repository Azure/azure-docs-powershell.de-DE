---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
ms.openlocfilehash: ab2e820ec0e1c943cfeb5f8b3d83babece38ed95
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173687"
---
# Get-AzMySqlConnectionString

## Synopsis
Rufen Sie die Verbindungszeichenfolge entsprechend dem Client Verbindungsanbieter ab.

## Syntax

### Abrufen (Standard)
```
Get-AzMySqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzMySqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## Beschreibung
Rufen Sie die Verbindungszeichenfolge entsprechend dem Client Verbindungsanbieter ab.

## Beispiele

### Beispiel 1: Abrufen der MySQL Server-Verbindungszeichenfolge nach Ressourcengruppe und Servername
```powershell
PS C:\> Get-AzMySqlConnectionString -Client ADO.NET -Name mysql-test -ResourceGroupName PowershellMySqlTest

Server=mysql-test.mysql.database.azure.com; Port=3306; Database={your_database}; Uid=mysql_test@mysql-test; Pwd={your_password};
```

Dieses Cmdlet ruft die MySQL Server-Verbindungszeichenfolge nach Ressourcengruppe und Servername ab.

### Beispiel 2: Abrufen der Verbindungszeichenfolge von MySQL Server nach Identität
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test@mysql-test", {your_password}, {your_database}, 3306);
```

Dieses Cmdlet ruft die MySQL Server-Verbindungszeichenfolge nach Identität ab.

## Parameter

### -Client
Client Verbindungsanbieter.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Das Quellserver Objekt, aus dem Replikat erstellt werden soll.
Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Der Name des Servers.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe, die die Ressource enthält, Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Abonnement-Nr
Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. Api20171201. IServer

## Ausgaben

### System. String

## Notizen

Aliase

komplexe Parameter Eigenschaften

Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften. Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.


Inputobject <IServer> : das Quellserver Objekt, aus dem Replikat erstellt werden soll.
  - `Location <String>`: Der Speicherort, in dem sich die Ressource befindet.
  - `[Tag <ITrackedResourceTags>]`: Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.
    - `[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.
  - `[AdministratorLogin <String>]`: Der Anmeldename des Administrators auf einem Server. Kann nur angegeben werden, wenn der Server erstellt wird (und für die Erstellung erforderlich ist).
  - `[EarliestRestoreDate <DateTime?>]`: Frühester Erstellungszeitpunkt des Wiederherstellungspunkts (ISO8601-Format)
  - `[FullyQualifiedDomainName <String>]`: Der vollqualifizierte Domänenname eines Servers.
  - `[IdentityType <IdentityType?>]`: Der Identity-Typ. Legen Sie diesen Wert auf "SystemAssigned", um automatisch einen Azure Active Directory-Prinzipal für die Ressource zu erstellen und zuzuweisen.
  - `[InfrastructureEncryption <InfrastructureEncryption?>]`: Status, der zeigt, ob die Server-Infrastruktur Verschlüsselung aktiviert ist.
  - `[MasterServerId <String>]`: Die Masterserver-ID eines Replikatservers.
  - `[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Erzwingen Sie eine minimale TLS-Version für den Server.
  - `[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Ob öffentlicher Netzwerkzugriff für diesen Server zulässig ist oder nicht. Der Wert ist optional, muss aber bei der Übergabe "aktiviert" oder "deaktiviert" sein.
  - `[ReplicaCapacity <Int32?>]`: Die maximale Anzahl von Replikaten, die ein Masterserver aufweisen kann.
  - `[ReplicationRole <String>]`: Die Replikations Rolle des Servers.
  - `[SkuCapacity <Int32?>]`: Die Skalierungskapazität, die die Compute-Einheiten des Servers repräsentiert.
  - `[SkuFamily <String>]`: Die Hardwarefamilie.
  - `[SkuName <String>]`: Der Name der SKU, in der Regel Tier + Familie + Kerne, beispielsweise B_Gen4_1, GP_Gen5_8.
  - `[SkuSize <String>]`: Der Größencode, der von der Ressource entsprechend interpretiert wird.
  - `[SkuTier <SkuTier?>]`: Die Stufe der jeweiligen SKU, z.b. Basic.
  - `[SslEnforcement <SslEnforcementEnum?>]`: Aktivieren der SSL-Erzwingung oder nicht, wenn eine Verbindung mit dem Server hergestellt wird.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: Backup-Aufbewahrungstage für den Server.
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivieren Sie Geo-redundante oder nicht für Server-Backups.
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivieren der automatischen Vergrößerung von Speicher.
  - `[StorageProfileStorageMb <Int32?>]`: Maximaler Speicherplatz, der für einen Server zulässig ist.
  - `[UserVisibleState <ServerState?>]`: Ein Zustand eines Servers, der für den Benutzer sichtbar ist.
  - `[Version <ServerVersion?>]`: Server Version.

## Verwandte Links

