---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/restore-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlFlexibleServer.md
ms.openlocfilehash: 299897ecd1eb4062a3f7ec8e61b8dffc19696066
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934840"
---
# Restore-AzMySqlFlexibleServer

## SYNOPSIS
Wiederherstellen eines Servers aus einer vorhandenen Sicherung

## SYNTAX

```
Restore-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> -InputObject <IServerAutoGenerated>
 -RestorePointInTime <DateTime> [-SubscriptionId <String>] [-Zone <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## BESCHREIBUNG
Wiederherstellen eines Servers aus einer vorhandenen Sicherung

## BEISPIELE

### Beispiel 1: Wiederherstellen des MySql-Servers mithilfe der PointInTime-Wiederherstellung
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Restore-AzMySqlFlexibleServer -Name mysql-test-restore -ResourceGroupName PowershellMySqlTest -RestorePointInTime $restorePointInTime 

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier       
----               -------- ------------------ ------- ----------------------- -------   -------       
mysql-test-restore eastus   mysql_test         5.7     10240                   Standard_D2ds_v4 GeneralPurpose
```

Diese Cmdlets wiederherstellen den MySql-Server mithilfe von PointInTime Restore.

## PARAMETER

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

### -InputObject
Das Quellserverobjekt, von dem wiederherstellen werden soll.
Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated
Parameter Sets: (All)
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
Parameter Sets: (All)
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

### -RestorePointInTime
Der Speicherort, an dem sich die Ressource befindet.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
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

### -Zone
Verfügbarkeitszone, in der die Ressource bereitgestellt werden soll.

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

### Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated

## AUSGABEN

### Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated

## NOTIZEN

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält. Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.


INPUTOBJECT <IServerAutoGenerated> : Das Quellserverobjekt, von dem wiederherstellen werden soll.
  - `Location <String>`: Der Geospeicherort, an dem sich die Ressource befindet
  - `[Tag <ITrackedResourceTags>]`: Ressourcentags.
    - `[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.
  - `[AdministratorLogin <String>]`: Der Anmeldename eines Servers des Administrators. Kann nur angegeben werden, wenn der Server erstellt wird (und für die Erstellung erforderlich ist).
  - `[AdministratorLoginPassword <SecureString>]`: Das Kennwort der Administratoranmeldung (erforderlich für die Servererstellung).
  - `[AvailabilityZone <String>]`: Verfügbarkeit Zone-Informationen des Servers.
  - `[CreateMode <CreateMode?>]`: Der Modus zum Erstellen eines neuen MySQL-Servers.
  - `[DelegatedSubnetArgumentSubnetArmResourceId <String>]`: Delegierte Ressourcen-ID des Subnetzarms.
  - `[HaEnabled <HaEnabledEnum?>]`: Aktivieren Sie HA oder nicht für einen Server.
  - `[IdentityType <ResourceIdentityType?>]`: Der Identitätstyp.
  - `[InfrastructureEncryption <InfrastructureEncryptionEnum?>]`: Status, der zeigt, ob der Server die Infrastrukturverschlüsselung aktiviert hat.
  - `[MaintenanceWindowCustomWindow <String>]`: gibt an, ob benutzerdefiniertes Fenster aktiviert oder deaktiviert ist
  - `[MaintenanceWindowDayOfWeek <Int32?>]`: Wochentag für Wartungsfenster
  - `[MaintenanceWindowStartHour <Int32?>]`: Startzeit für Wartungsfenster
  - `[MaintenanceWindowStartMinute <Int32?>]`: Startminute für Wartungsfenster
  - `[PropertiesTag <IServerPropertiesTags>]`: Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.
    - `[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.
  - `[ReplicationRole <String>]`: Die Replikationsrolle.
  - `[RestorePointInTime <DateTime?>]`: Wiederherstellen der Punkterstellungszeit (ISO8601-Format) mit Angabe der Wiederherstellungszeit.
  - `[SkuName <String>]`: Der Name der Sku, z. B. Standard_D32s_v3.
  - `[SkuTier <SkuTier?>]`: Die Ebene der jeweiligen SKU, z. B. GeneralPurpose.
  - `[SourceServerId <String>]`: Die MySQL-Server-Id der Quelle.
  - `[SslEnforcement <SslEnforcementEnum?>]`: Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: Sicherungsaufbewahrungstage für den Server.
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivieren Sie "Automatisches Wachstum" für Speicher.
  - `[StorageProfileStorageIop <Int32?>]`: Speicher-IOPS für einen Server.
  - `[StorageProfileStorageMb <Int32?>]`: Maximaler Speicherplatz, der für einen Server zulässig ist.
  - `[Version <ServerVersion?>]`: Serverversion.

## VERWANDTE LINKS

