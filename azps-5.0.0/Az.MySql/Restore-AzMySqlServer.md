---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/restore-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
ms.openlocfilehash: 49ae121273b42d3718d1a334edcaa72fa2c57583
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176783"
---
# Restore-AzMySqlServer

## Synopsis
Wiederherstellen eines Servers aus einer vorhandenen Sicherung

## Syntax

### Georestore (Standard)
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### PointInTimeRestore
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## Beschreibung
Wiederherstellen eines Servers aus einer vorhandenen Sicherung

## Beispiele

### Beispiel 1: Wiederherstellen des MySQL-Servers mithilfe der georeplica-Wiederherstellung
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test-replica | Restore-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -UseGeoRestore 

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

Dieses Cmdlet stellt den MySQL-Server mithilfe der georeplikat-Wiederherstellung wieder her.

### Beispiel 2: Wiederherstellen des MySQL-Servers mithilfe der PointInTime-Wiederherstellung
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Restore-AzMySqlServer -Name mysql-test-restore -ResourceGroupName PowershellMySqlTest -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-restore eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

Diese Cmdlets stellen den MySQL-Server mithilfe der PointInTime-Wiederherstellung wieder her.

## Parameter

### -AsJob
Führen Sie den Befehl als Auftrag aus.

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
Das Quellserver Objekt, von dem wiederhergestellt werden soll.
Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Standort
Der Speicherort, in dem sich die Ressource befindet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name des Servers.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nowait
Führen Sie den Befehl asynchron aus.

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
Der Name der Ressourcengruppe, die die Ressource enthält, Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.

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

### -RestorePointInTime
Der Speicherort, in dem sich die Ressource befindet.

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKU
Der Name der SKU, in der Regel Tier + Familie + Kerne, beispielsweise B_Gen4_1, GP_Gen5_8.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Abonnement-Nr
Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseGeoRestore
Verwenden des Geo-Modus zum Wiederherstellen

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UsePointInTimeRestore
Verwenden des PointInTime-Modus zum Wiederherstellen

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeRestore
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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. Api20171201. IServer

## Ausgaben

### Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. Api20171201. IServer

## Notizen

Aliase

komplexe Parameter Eigenschaften

Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften. Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.


Inputobject <IServer> : das Quellserver Objekt, von dem wiederhergestellt werden soll.
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

