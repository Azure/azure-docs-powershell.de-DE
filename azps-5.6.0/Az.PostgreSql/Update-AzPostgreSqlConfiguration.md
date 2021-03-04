---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
ms.openlocfilehash: c0af624683e3d12cc1b12c057caa419c5633d45f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919379"
---
# Update-AzPostgreSqlConfiguration

## SYNOPSIS
Aktualisiert eine Konfiguration eines Servers.
Verwenden Update-AzPostgreSqlServer sie stattdessen, wenn Sie AdministratorLoginPassword, Sku usw. aktualisieren möchten.

## SYNTAX

### UpdateExpanded (Standard)
```
Update-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## BESCHREIBUNG
Aktualisiert eine Konfiguration eines Servers.
Verwenden Update-AzPostgreSqlServer sie stattdessen, wenn Sie AdministratorLoginPassword, Sku usw. aktualisieren möchten.

## BEISPIELE

### Beispiel 1: Aktualisieren der PostgreSql-Konfiguration nach Name
```powershell
PS C:\> Update-AzPostgreSqlConfiguration -Name intervalstyle -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -Value SQL_STANDARD

Name          Value
----          -----
intervalstyle SQL_STANDARD
```

Dieses Cmdlet aktualisiert die PostgreSql-Konfiguration nach Name.

### Beispiel 2: Aktualisieren der PostgreSql-Konfiguration nach Identität.
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/configurations/deadlock_timeout"
PS C:\> Update-AzPostgreSqlConfiguration -InputObject $ID -Value 2000

Name             Value
----             -----
deadlock_timeout 2000
```

Diese Cmdlets aktualisieren die PostgreSql-Konfiguration nach Identität.

## PARAMETER

### -AsJob
Ausführen des Befehls als Auftrag

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

### -InputObject
Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.

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

### -Name
Der Name der Serverkonfiguration.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Asynchrones Ausführen des Befehls

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
Der Name der Ressourcengruppe.
Der Name ist groß- und kleinschreibungsunabhängiger.

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

### -Servername
Der Name des Servers.

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

### -Source
Quelle der Konfiguration.

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
Die ID des Zielabonnements.

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

### -Wert
Wert der Konfiguration.

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

### Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration

## NOTIZEN

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält. Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.


INPUTOBJECT <IPostgreSqlIdentity> : Identitätsparameter
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

