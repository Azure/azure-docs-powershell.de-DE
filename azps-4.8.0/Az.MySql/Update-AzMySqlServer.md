---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: e23cc8b942033805d8ed8cd122b19e6a59bf457c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009181"
---
# Update-AzMySqlServer

## Synopsis
Aktualisiert einen vorhandenen Server.
Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Server Definition vorhanden sind.
Verwenden Sie stattdessen Update-AzMySqlConfiguration, wenn Sie Update Serverparameter wie wait_timeout oder net_retry_count verwenden möchten.

## Syntax

### UpdateExpanded (Standard)
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-ReplicationRole <String>] [-Sku <String>] [-SkuCapacity <Int32>]
 [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Beschreibung
Aktualisiert einen vorhandenen Server.
Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Server Definition vorhanden sind.
Verwenden Sie stattdessen Update-AzMySqlConfiguration, wenn Sie Update Serverparameter wie wait_timeout oder net_retry_count verwenden möchten.

## Beispiele

### Beispiel 1: Aktualisieren von MySQL Server nach Ressourcengruppe und Servername
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

Dieses Cmdlet aktualisiert MySQL Server nach Ressourcengruppe und Servername.

### Beispiel 2: Aktualisieren von MySQL Server nach Identität.
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

Dieses Cmdlet aktualisiert MySQL Server nach Identität.

## Parameter

### -AdministratorLoginPassword
Das Kennwort des Administrator Anmeldenamens.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -BackupRetentionDay
Aufbewahrungstage für Backups für den Server.
Die Anzahl der Tage liegt zwischen 7 und 35.

```yaml
Type: System.Int32
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
Parameter Identity.
Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
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
Parameter Sets: UpdateExpanded
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

### -ReplicationRole
Die Replikations Rolle des Servers.

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

### -ResourceGroupName
Der Name der Ressourcengruppe, die die Ressource enthält.
Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
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

### -SkuCapacity
Die Skalierungskapazität, die die Compute-Einheiten des Servers repräsentiert.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuFamily
Die Hardwarefamilie.

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

### -SkuTier
Die Stufe der jeweiligen SKU, z.b. Basic.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslEnforcement
Aktivieren der SSL-Erzwingung oder nicht beim Herstellen einer Verbindung mit dem Server.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAutogrow
Aktivieren der automatischen Vergrößerung von Speicher.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageInMb
Maximaler Speicherplatz, der für einen Server zulässig ist.

```yaml
Type: System.Int32
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
Parameter Sets: UpdateExpanded
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

### Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. IMySqlIdentity

## Ausgaben

### Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. Api20171201. IServer

## Notizen

Aliase

komplexe Parameter Eigenschaften

Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften. Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.


Inputobject <IMySqlIdentity> : Identity-Parameter
  - `[ConfigurationName <String>]`: Der Name der Serverkonfiguration.
  - `[DatabaseName <String>]`: Der Name der Datenbank.
  - `[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.
  - `[Id <String>]`: Ressourcen Identitäts Pfad
  - `[LocationName <String>]`: Der Name des Standorts.
  - `[ResourceGroupName <String>]`: Der Name der Ressourcengruppe. Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.
  - `[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.
  - `[ServerName <String>]`: Der Name des Servers.
  - `[SubscriptionId <String>]`: Die ID des zielabonnements.
  - `[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.

## Verwandte Links

