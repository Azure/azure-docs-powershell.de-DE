---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
ms.openlocfilehash: d6d4480f2a4be2fa10a6e6ea8b69da1de9c61f39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929936"
---
# Update-AzPostgreSqlServer

## SYNOPSIS
Aktualisiert einen vorhandenen Server.
Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Serverdefinition vorhanden sind.
Verwenden Update-AzPostSqlConfiguration sie stattdessen, wenn Sie Serverparameter aktualisieren möchten, z. B. wait_timeout oder net_retry_count.

## SYNTAX

### UpdateExpanded (Standard)
```
Update-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## BESCHREIBUNG
Aktualisiert einen vorhandenen Server.
Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Serverdefinition vorhanden sind.
Verwenden Update-AzPostSqlConfiguration sie stattdessen, wenn Sie Serverparameter aktualisieren möchten, z. B. wait_timeout oder net_retry_count.

## BEISPIELE

### Beispiel 1: Aktualisieren des PostgreSql-Servers nach Ressourcengruppe und Servername
```powershell
PS C:\> Update-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SslEnforcement Disabled

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

Dieses Cmdlet aktualisiert den PostgreSql-Server nach Ressourcengruppe und Servername.

### Beispiel 2: Aktualisieren des PostgreSql-Servers nach Identität.
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Update-AzPostgreSqlServer -BackupRetentionDay 23

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

Dieses Cmdlet aktualisiert den PostgreSql-Server nach Identität.

## PARAMETER

### -AdministratorLoginPassword
Das Kennwort der Administratoranmeldung.

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
Sicherungsaufbewahrungstage für den Server.
Die Tagesanzahl liegt zwischen 7 und 35.

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

### -InputObject
Identitätsparameter.
Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MinimalTlsVersion
Legen Sie die minimale TLS-Version für Verbindungen mit dem Server bei aktiviertem SSL ein.
Standardmäßig sind TLSEnforcementDisabled.accepted-Werte: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.MinimalTlsVersionEnum
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
Parameter Sets: UpdateExpanded
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -ReplicationRole
Die Replikationsrolle des Servers.

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

### -Sku
Der Name der Sku ist in der Regel Ebene + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.

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
Die skalierungs-/out-Kapazität, die die Recheneinheiten des Servers darstellt.

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
Die Ebene der bestimmten SKU, z. B. Basic.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslEnforcement
Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAutogrow
Aktivieren Sie "Automatisches Wachstum" für "Speicher".

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.StorageAutogrow
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

### -SubscriptionId
Die Abonnement-ID, die ein Azure-Abonnement identifiziert.

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

### -WhatIf
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity

## AUSGABEN

### Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer

## NOTIZEN

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält. Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.


INPUTOBJECT <IPostgreSqlIdentity> : Identitätsparameter.
  - `[ConfigurationName <String>]`: Der Name der Serverkonfiguration.
  - `[DatabaseName <String>]`: Der Name der Datenbank.
  - `[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.
  - `[Id <String>]`: Ressourcenidentitätspfad
  - `[LocationName <String>]`: Der Name des Speicherorts.
  - `[ResourceGroupName <String>]`: Der Name der Ressourcengruppe. Der Name ist groß- und kleinschreibungsunabhängiger.
  - `[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.
  - `[ServerName <String>]`: Der Name des Servers.
  - `[SubscriptionId <String>]`: Die ID des Zielabonnements.
  - `[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.

## VERWANDTE LINKS

