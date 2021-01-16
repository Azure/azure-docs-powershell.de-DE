---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
ms.openlocfilehash: e3c0d7e8d3b3d9fe42bc97c40ad54424b7bfd0da
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293375"
---
# New-AzPostgreSqlReplica

## SYNOPSIS
Erstellt eine neue Replikatdatei aus einer vorhandenen Datenbank.

## SYNTAX

```
New-AzPostgreSqlReplica -ReplicaName <String> -ResourceGroupName <String> -Master <IServer>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## BESCHREIBUNG
Erstellt eine neue Replikatdatei aus einer vorhandenen Datenbank.

## BEISPIELE

### Beispiel 1: Erstellen einer neuen PostgreSql-Serverreplikate
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | New-AzPostgreSqlReplica -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

Dieses Cmdlet erstellt eine neue PostgreSql-Serverreplikate.

### Beispiel 2: Erstellen einer neuen PostgreSql-Serverreplikate
```powershell
PS C:\> $pgDb = Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 
PS C:\> New-AzPostgreSqlReplica -Master $pgDb -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

Dieses Cmdlet erstellt eine neue PostgreSql-Serverreplikate.

## PARAMETERS

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
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -Location
Der Speicherort, an dem sich die Ressource befindet.

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

### -Master
Das Quellserverobjekt, aus dem eine Replikat erstellt werden soll.
Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu #A0 und zum Erstellen einer Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NoWait
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

### -ReplicaName
Der Name des Servers.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicaServerName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe, die die Ressource enthält. Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.

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

### -SKU
Der Name der SKU , normalerweise Stufen + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.

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

### -SubscriptionId
Die Abonnement-ID, die ein Azure-Abonnement identifiziert.

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

### -Confirm
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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

### -Waswenn
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer

## AUSGABEN

### Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer

## HINWEISE

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften. Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.


MASTER: <IServer> Das Quellserverobjekt, aus dem eine Replikaterstellung erstellt werden soll.
  - `Location <String>`: Der Speicherort, an dem sich die Ressource befindet.
  - `[Tag <ITrackedResourceTags>]`: Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.
    - `[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.
  - `[AdministratorLogin <String>]`: Der Anmeldename eines Administrators für einen Server. Kann nur angegeben werden, wenn der Server erstellt wird (und für die Erstellung erforderlich ist).
  - `[EarliestRestoreDate <DateTime?>]`: Früheste Erstellungszeit des Wiederherstellungspunkts (ISO8601-Format)
  - `[FullyQualifiedDomainName <String>]`: Der vollqualifizierte Domänenname eines Servers.
  - `[IdentityType <IdentityType?>]`: Der Identitätstyp. Legen Sie diesen Wert auf "SystemAssigned" ein, um automatisch einen Azure Active Directory-Prinzipal für die Ressource zu erstellen und zuzuweisen.
  - `[InfrastructureEncryption <InfrastructureEncryption?>]`: Status, der zeigt, ob die Serverinfrastrukturverschlüsselung aktiviert ist.
  - `[MasterServerId <String>]`: Die Masterserver-ID eines Replikatservers.
  - `[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Erzwingen Sie eine minimale Version von Tls für den Server.
  - `[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Gibt an, ob der Zugriff auf öffentliche Netzwerke für diesen Server zulässig ist. Der Wert ist optional, muss aber bei übergebenem Wert "Enabled" oder "Disabled" sein.
  - `[ReplicaCapacity <Int32?>]`: Die maximale Anzahl von Replikaten, die ein Masterserver haben kann.
  - `[ReplicationRole <String>]`: Die Replikationsrolle des Servers.
  - `[SkuCapacity <Int32?>]`: Die Skalierungs-/Outkapazität, die die Recheneinheiten des Servers darstellt.
  - `[SkuFamily <String>]`: Die Hardwarefamilie.
  - `[SkuName <String>]`: Der Name der SKU, in der Regel Stufe + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.
  - `[SkuSize <String>]`: Der Größencode, der von der Ressource entsprechend interpretiert werden soll.
  - `[SkuTier <SkuTier?>]`: Die Ebene einer bestimmten SKU, z. B. "Standard".
  - `[SslEnforcement <SslEnforcementEnum?>]`: Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: Sicherungsaufbewahrungstage für den Server.
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivieren Sie georedundant oder nicht für die Serversicherung.
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivieren Sie "Speicher automatisch anwachsen".
  - `[StorageProfileStorageMb <Int32?>]`: Maximal zulässiger Speicherplatz für einen Server.
  - `[UserVisibleState <ServerState?>]`: Der Zustand eines Servers, der für den Benutzer sichtbar ist.
  - `[Version <ServerVersion?>]`: Serverversion.

## LINKS ZU VERWANDTEN THEMEN

