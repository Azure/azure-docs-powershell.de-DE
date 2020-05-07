---
title: Grundlegende Änderungen für Microsoft Azure PowerShell 6.0.0
description: Dieser Migrationsleitfaden enthält eine Liste mit grundlegenden Änderungen, die in Version 6 an Azure PowerShell vorgenommen wurden.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 1fbd24996da2fbc7d4e95c2a63f828aea6cb3145
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534923"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a>Grundlegende Änderungen für Microsoft Azure PowerShell 6.0.0

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Dieses Dokument informiert über grundlegende Änderungen und fungiert als Migrationsleitfaden für Kunden mit Microsoft Azure PowerShell-Cmdlets. In den einzelnen Abschnitten werden jeweils der Grund für die grundlegende Änderung und der Migrationspfad des geringsten Widerstands beschrieben. Ausführlichen Kontext finden Sie unter der Pull-Anforderung für die jeweilige Änderung.

## <a name="table-of-contents"></a>Inhaltsverzeichnis

- [Allgemeine grundlegende Änderungen](#general-breaking-changes)
    - [Festlegung der erforderlichen PowerShell-Mindestversion auf 5.0](#minimum-powershell-version-required-bumped-to-50)
    - [Standardmäßige Aktivierung der automatischen Kontextspeicherung](#context-autosave-enabled-by-default)
    - [Entfernung des Tags-Alias](#removal-of-tags-alias)
- [Grundlegende Änderungen an AzureRM.Compute-Cmdlets](#breaking-changes-to-azurermcompute-cmdlets)
- [Grundlegende Änderungen an AzureRM.DataLakeStore-Cmdlets](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [Grundlegende Änderungen an AzureRM.Dns-Cmdlets](#breaking-changes-to-azurermdns-cmdlets)
- [Grundlegende Änderungen an AzureRM.Insights-Cmdlets](#breaking-changes-to-azurerminsights-cmdlets)
- [Grundlegende Änderungen an AzureRM.KeyVault-Cmdlets](#breaking-changes-to-azurermkeyvault-cmdlets)
- [Grundlegende Änderungen an AzureRM.Network-Cmdlets](#breaking-changes-to-azurermnetwork-cmdlets)
- [Grundlegende Änderungen an AzureRM.RedisCache-Cmdlets](#breaking-changes-to-azurermrediscache-cmdlets)
- [Grundlegende Änderungen an AzureRM.Resources-Cmdlets](#breaking-changes-to-azurermresources-cmdlets)
- [Grundlegende Änderungen an AzureRM.Storage-Cmdlets](#breaking-changes-to-azurermstorage-cmdlets)
- [Entfernte Module](#removed-modules)
    - [`AzureRM.ServerManagement`](#azurermservermanagement)
    - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a>Allgemeine grundlegende Änderungen

### <a name="minimum-powershell-version-required-bumped-to-50"></a>Festlegung der erforderlichen PowerShell-Mindestversion auf 5.0

Bisher war _mindestens_ Version 3.0 von PowerShell erforderlich, um Cmdlets ausführen zu können. Diese Anforderung wurde auf Version 5.0 von PowerShell erhöht. Informationen zur Durchführung eines Upgrades auf PowerShell 5.0 finden Sie in [dieser Tabelle](https://docs.microsoft.com/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).

### <a name="context-autosave-enabled-by-default"></a>Standardmäßige Aktivierung der automatischen Kontextspeicherung

Bei der automatischen Kontextspeicherung geht es um die Speicherung von Azure-Anmeldeinformationen, die für neue und unterschiedliche PowerShell-Sitzungen verwendet werden können. Weitere Informationen zur automatischen Kontextspeicherung finden Sie in [diesem Dokument](https://docs.microsoft.com/powershell/azure/context-persistence).

Bisher war die automatische Kontextspeicherung standardmäßig deaktiviert. Die Azure-Authentifizierungsinformationen eines Benutzers wurden zwischen Sitzungen erst gespeichert, wenn er das `Enable-AzureRmContextAutosave`-Cmdlet ausgeführt hat, um die Kontextbeibehaltung zu aktivieren. Ab jetzt ist die automatische Kontextspeicherung standardmäßig aktiviert. Dies bedeutet, dass für Benutzer _ohne gespeicherte Einstellungen für die automatische Kontextspeicherung_ der Kontext bei der nächsten Anmeldung gespeichert wird. Benutzer können sich gegen die Nutzung dieser Funktionalität entscheiden, indem sie das `Disable-AzureRmContextAutosave`-Cmdlet verwenden.

_Hinweis_: Benutzer, die die automatische Kontextspeicherung bisher deaktiviert bzw. aktiviert hatten, und vorhandene Kontexte sind von dieser Änderung nicht betroffen.

### <a name="removal-of-tags-alias"></a>Entfernung des Tags-Alias

Der `Tags`-Alias für den Parameter `Tag` wurde für viele Cmdlets entfernt. Hier ist eine Liste mit den Modulen (und den dazugehörigen Cmdlets) angegeben, die hiervon betroffen sind:

#### `AzureRM.ApiManagement`

- `New-AzureRmApiManagement`
- `New-AzureRmApiManagementProperty`
- `Set-AzureRmApiManagementProperty`

#### `AzureRM.Automation`
- `Set-AzureRmAutomationRunbook`

#### `AzureRM.Cdn`
- `New-AzureRmCdnEndpoint`
- `New-AzureRmCdnProfile`

#### `AzureRM.Compute`
- `New-AzureRmVM`
- `Update-AzureRmVM`

#### `AzureRM.DataFactories`
- `New-AzureRmDataFactories`

#### `AzureRM.DataLakeAnalytics`
- `New-AzureRmDataLakeAnalyticsAccount`

#### `AzureRM.DataLakeStore`
- `New-AzureRmDataLakeStoreAccount`
- `Set-AzureRmDataLakeStoreAccount`

#### `AzureRM.MachineLearning`
- `Update-AzureRmMlCommitmentPlan`

#### `AzureRM.Media`
- `Set-AzureRmMediaService`

#### `AzureRM.OperationalInsights`
- `New-AzureRmOperationalInsightsSavedSearch`
- `New-AzureRmOperationalInsightsWorkspace`
- `Set-AzureRmOperationalInsightsSavedSearch`
- `Set-AzureRmOperationalInsightsWorkspace`

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a>Grundlegende Änderungen an AzureRM.Compute-Cmdlets

**Verschiedenes**
- Die in den Typen `PSDisk` und `PSSnapshot` geschachtelte SKU-Name-Eigenschaft wurde von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.

```powershell-interactive
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- Die in den Typen `PSVirtualMachine`, `PSVirtualMachineScaleSet` und `PSImage` geschachtelte Speicherkontotyp-Eigenschaft wurde von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.

```powershell-interactive
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

**Add-AzureRmImageDataDisk**
- Die zulässigen Werte für den Parameter `StorageAccountType` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.

**Add-AzureRmVMDataDisk**
- Die zulässigen Werte für den Parameter `StorageAccountType` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.

**Add-AzureRmVmssDataDisk**
- Die zulässigen Werte für den Parameter `StorageAccountType` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.

**New-AzureRmAvailabilitySet**
- Der Parameter `Managed` wurde entfernt und durch `Sku` ersetzt.

```powershell-interactive
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

**New-AzureRmDiskConfig**
- Die zulässigen Werte für den Parameter `SkuName` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.

**New-AzureRmDiskUpdateConfig**
- Die zulässigen Werte für den Parameter `SkuName` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.

**New-AzureRmSnapshotConfig**
- Die zulässigen Werte für den Parameter `SkuName` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.

**New-AzureRmSnapshotUpdateConfig**
- Die zulässigen Werte für den Parameter `SkuName` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.

**Set-AzureRmImageOsDisk**
- Die zulässigen Werte für den Parameter `StorageAccountType` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.

**Set-AzureRmVMAEMExtension**
- Der Parameter `DisableWAD` wurde entfernt.
    -  Die Microsoft Azure-Diagnose ist standardmäßig deaktiviert.

**Set-AzureRmVMDataDisk**
- Die zulässigen Werte für den Parameter `StorageAccountType` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.

**Set-AzureRmVMOSDisk**
- Die zulässigen Werte für den Parameter `StorageAccountType` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.

**Set-AzureRmVmssStorageProfile**
- Die zulässigen Werte für den Parameter `ManagedDisk` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.

**Update-AzureRmVmss**
- Die zulässigen Werte für den Parameter `ManagedDiskStorageAccountType` wurden von `StandardLRS` und `PremiumLRS` in `Standard_LRS` bzw. `Premium_LRS` geändert.

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a>Grundlegende Änderungen an AzureRM.DataLakeStore-Cmdlets

**Export-AzureRmDataLakeStoreItem**
- Die Parameter `PerFileThreadCount` und `ConcurrentFileCount` wurden entfernt. Verwenden Sie ab jetzt den Parameter `Concurrency`.

```powershell-interactive
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

**Import-AzureRmDataLakeStoreItem**
- Die Parameter `PerFileThreadCount` und `ConcurrentFileCount` wurden entfernt. Verwenden Sie ab jetzt den Parameter `Concurrency`.

```powershell-interactive
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

**Remove-AzureRmDataLakeStoreItem**
- Der Parameter `Clean` wurde entfernt.

```powershell-interactive
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a>Grundlegende Änderungen an AzureRM.Dns-Cmdlets

**New-AzureRmDnsRecordSet**
- Der Parameter `Force` wurde entfernt.

**Remove-AzureRmDnsRecordSet**
- Der Parameter `Force` wurde entfernt.

**Remove-AzureRmDnsZone**
- Der Parameter `Force` wurde entfernt.

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a>Grundlegende Änderungen an AzureRM.Insights-Cmdlets

**Add-AzureRmAutoscaleSetting**
- Die Parameteraliase `AutoscaleProfiles` und `Notifications` wurden entfernt.

**Add-AzureRmLogProfile**
- Die Parameteraliase `Categories` und `Locations` wurden entfernt.

**Add-AzureRmMetricAlertRule**
- Der Parameteralias `Actions` wurde entfernt.

**Add-AzureRmWebtestAlertRule**
- Der Parameteralias `Actions` wurde entfernt.

**Get-AzureRmLog**
- Die Parameteraliase `MaxRecords` und `MaxEvents` wurden entfernt.

**Get-AzureRmMetricDefinition**
- Der Parameteralias `MetricNames` wurde entfernt.

**New-AzureRmAlertRuleEmail**
- Die Parameteraliase `CustomEmails` und `SendToServiceOwners` wurden entfernt.

**New-AzureRmAlertRuleWebhook**
- Der Parameteralias `Properties` wurde entfernt.

**New-AzureRmAutoscaleNotification**
- Die Parameteraliase `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` und `Webhooks` wurden entfernt.

**New-AzureRmAutoscaleProfile**
- Die Parameteraliase `Rules`, `ScheduleDays`, `ScheduleHours` und `ScheduleMinutes` wurden entfernt.

**New-AzureRmAutoscaleWebhook**
- Der Parameteralias `Properties` wurde entfernt.

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a>Grundlegende Änderungen an AzureRM.KeyVault-Cmdlets

**Add-AzureKeyVaultCertificate**
- Der Parameter `CertificatePolicy` ist jetzt obligatorisch.

**Set-AzureKeyVaultManagedStorageSasDefinition**
- Das Cmdlet akzeptiert keine einzelnen Parameter mehr, aus denen das Zugriffstoken besteht. Stattdessen ersetzt das Cmdlet explizite Tokenparameter, z.B. `Service` oder `Permissions`, durch den generischen Parameter `TemplateUri`, der einem an anderer Stelle definierten Beispielzugriffstoken entspricht (meist über Storage PowerShell-Cmdlets oder per manueller Zusammenstellung gemäß Storage-Dokumentation). Das Cmdlet behält den Parameter `ValidityPeriod` bei.

Weitere Informationen zum Verfassen von SAS-Token für Azure Storage finden Sie auf den entsprechenden Seiten in der Dokumentation:
- [Constructing a Service SAS (Erstellen einer Dienstebenen-SAS)](https://docs.microsoft.com/rest/api/storageservices/Constructing-a-Service-SAS)
- [Constructing an Account SAS (Erstellen einer Kontoebenen-SAS)](https://docs.microsoft.com/rest/api/storageservices/constructing-an-account-sas)

```powershell-interactive
# Old
$sas = Set-AzureKeyVaultManagedStorageSasDefinition -VaultName myVault -Name myKey -Service Blob -Permissions 'rcw' -ValidityPeriod 180d

# New
$sctx=New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
$start=[System.DateTime]::Now.AddDays(-1)
$end=[System.DateTime]::Now.AddMonths(1)
$at=New-AzureStorageAccountSasToken -Service blob -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
$sas=Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
```

**Set-AzureKeyVaultCertificateIssuer**
- Der Parameter `IssuerProvider` ist jetzt obligatorisch.

**Undo-AzureKeyVaultCertificateRemoval**
- Die Ausgabe dieses Cmdlets wurde von `CertificateBundle` in `PSKeyVaultCertificate` geändert.

**Undo-AzureRmKeyVaultRemoval**
- `ResourceGroupName` wurde aus dem `InputObject`-Parametersatz entfernt und wird stattdessen über die `ResourceId`-Eigenschaft des Parameters `InputObject` abgerufen.

**Set-AzureRmKeyVaultAccessPolicy**
- Die Berechtigung `all` wurde aus `PermissionsToKeys`, `PermissionsToSecrets` und `PermissionsToCertificates` entfernt.

**Allgemein**
- Die `ValueFromPipelineByPropertyName`-Eigenschaft wurde aus allen Cmdlets entfernt, für die das Piping per `InputObject` aktiviert war.  Hiervon sind die folgenden Cmdlets betroffen:
    - `Add-AzureKeyVaultCertificate`
    - `Add-AzureKeyVaultCertificateContact`
    - `Add-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultSecret`
    - `Get-AzureKeyVaultCertficate`
    - `Get-AzureKeyVaultCertificateContact`
    - `Get-AzureKeyVaultCertificateIssuer`
    - `Get-AzureKeyVaultCertificateOperation`
    - `Get-AzureKeyVaultCertificatePolicy`
    - `Get-AzureKeyVaultKey`
    - `Get-AzureKeyVaultManagedStorageAccount`
    - `Get-AzureKeyVaultManagedStorageSasDefinition`
    - `Get-AzureKeyVaultSecret`
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureRmKeyVaultAccessPolicy`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateContact`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Restore-AzureKeyVaultKey`
    - `Restore-AzureKeyVaultSecret`
    - `Set-AzureRmKeyVaultAccessPolicy`
    - `Set-AzureKeyVaultCertificateAttribute`
    - `Set-AzureKeyVaultCertificateIssuer`
    - `Set-AzureKeyVaultCertificatePolicy`
    - `Set-AzureKeyVaultKeyAttribute`
    - `Set-AzureKeyVaultManagedStorageSasDefinition`
    - `Set-AzureKeyVaultSecret`
    - `Set-AzureKeyVaultSecretAttribute`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Undo-AzureKeyVaultCertificateRemoval`
    - `Undo-AzureKeyVaultKeyRemoval`
    - `Undo-AzureRmKeyVaultRemoval`
    - `Undo-AzureKeyVaultSecretRemoval`
    - `Update-AzureKeyVaultManagedStorageAccount`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- `ConfirmImpact`-Ebenen wurden aus allen Cmdlets entfernt.  Hiervon sind die folgenden Cmdlets betroffen:
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- Das `IKeyVaultDataServiceClient`-Element wurde aktualisiert, damit für alle Zertifikatvorgänge PSTypes anstelle von SDK-Typen zurückgegeben werden. Dies schließt Folgendes ein:
    - `SetCertificateContacts`
    - `GetCertificateContacts`
    - `GetCertificate`
    - `GetDeletedCertificate`
    - `MergeCertificate`
    - `ImportCertificate`
    - `DeleteCertificate`
    - `RecoverCertificate`
    - `EnrollCertificate`
    - `UpdateCertificate`
    - `GetCertificateOperation`
    - `DeleteCertificateOperation`
    - `CancelCertificateOperation`
    - `GetCertificatePolicy`
    - `UpdateCertificatePolicy`
    - `GetCertificateIssuer`
    - `SetCertificateIssuer`
    - `DeleteCertificateIssuer`

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a>Grundlegende Änderungen an AzureRM.Network-Cmdlets


**Add-AzureRmApplicationGatewayBackendHttpSettings**
- Der Parameter `ProbeEnabled` wurde entfernt.

**Add-AzureRmVirtualNetworkPeering**
- Der Parameteralias `AlloowGatewayTransit` wurde entfernt.

**New-AzureRmApplicationGatewayBackendHttpSettings**
- Der Parameter `ProbeEnabled` wurde entfernt.

**Set-AzureRmApplicationGatewayBackendHttpSettings**
- Der Parameter `ProbeEnabled` wurde entfernt.

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a>Grundlegende Änderungen an AzureRM.RedisCache-Cmdlets

**New-AzureRmRedisCache**
- Die Parameter `Subnet` und `VirtualNetwork` wurden entfernt und durch `SubnetId` ersetzt.
- Der Parameter `RedisVersion` wurde entfernt.
- Der Parameter `MaxMemoryPolicy` wurde entfernt und durch `RedisConfiguration` ersetzt.

```powershell-interactive
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

**Set-AzureRmRedisCache**
- Der Parameter `MaxMemoryPolicy` wurde entfernt und durch `RedisConfiguration` ersetzt.

```powershell-interactive
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a>Grundlegende Änderungen an AzureRM.Resources-Cmdlets

**Find-AzureRmResource**
- Dieses Cmdlet wurde entfernt, und die Funktionalität wurde in `Get-AzureRmResource` verschoben.

```powershell-interactive
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

**Find-AzureRmResourceGroup**
- Dieses Cmdlet wurde entfernt, und die Funktionalität wurde in `Get-AzureRmResourceGroup` verschoben.

```powershell-interactive
# Old
Find-AzureRmResourceGroup
Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Find-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }

# New
Get-AzureRmResourceGroup
Get-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Get-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }
```

**Get-AzureRmRoleDefinition**
- Der Parameter `AtScopeAndBelow` wurde entfernt.

```powershell-interactive

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a>Grundlegende Änderungen an AzureRM.Storage-Cmdlets

**New-AzureRmStorageAccount**
- Der Parameter `EnableEncryptionService` wurde entfernt.

**Set-AzureRmStorageAccount**
- Die Parameter `EnableEncryptionService` und `DisableEncryptionService` wurden entfernt.

## <a name="removed-modules"></a>Entfernte Module

### `AzureRM.ServerManagement`

Da der Serververwaltungstools-Dienst [letztes Jahr eingestellt](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/) wurde, wurde das entsprechende Modul `AzureRM.ServerManagement` für SMT aus `AzureRM` entfernt und wird nicht mehr ausgeliefert.

### `AzureRM.SiteRecovery`

Das Modul `AzureRM.SiteRecovery` wird von `AzureRM.RecoveryServices.SiteRecovery` abgelöst. Hierbei handelt es sich um eine funktionale Obermenge des Moduls `AzureRM.SiteRecovery` mit einem neuen Satz gleichwertiger Cmdlets. Die vollständige Liste mit der Zuordnung alter und neuer Cmdlets finden Sie hier:

| Veraltetes Cmdlet                                        | Gleichwertiges Cmdlet                                                | Aliase                                  |
|----------------------------------------------------------|------------------------------------------------------------------|------------------------------------------|
| `Edit-AzureRmSiteRecoveryRecoveryPlan`                   | `Edit-AzureRmRecoveryServicesAsrRecoveryPlan`                    | `Edit-ASRRecoveryPlan`                   |
| `Get-AzureRmSiteRecoveryFabric`                          | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryJob`                             | `Get-AzureRmRecoveryServicesAsrJob`                              | `Get-ASRJob`                             |
| `Get-AzureRmSiteRecoveryNetwork`                         | `Get-AzureRmRecoveryServicesAsrNetwork`                          | `Get-ASRNetwork`                         |
| `Get-AzureRmSiteRecoveryNetworkMapping`                  | `Get-AzureRmRecoveryServicesAsrNetworkMapping`                   | `Get-ASRNetworkMapping`                  |
| `Get-AzureRmSiteRecoveryPolicy`                          | `Get-AzureRmRecoveryServicesAsrPolicy`                           | `Get-ASRPolicy`                          |
| `Get-AzureRmSiteRecoveryProtectableItem`                 | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryProtectionContainer`             | `Get-AzureRmRecoveryServicesAsrProtectionContainer`              | `Get-ASRProtectionContainer`             |
| `Get-AzureRmSiteRecoveryProtectionContainerMapping`      | `Get-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `Get-ASRProtectionContainerMapping`      |
| `Get-AzureRmSiteRecoveryProtectionEntity`                | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryRecoveryPlan`                    | `Get-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `Get-ASRRecoveryPlan`                    |
| `Get-AzureRmSiteRecoveryRecoveryPoint`                   | `Get-AzureRmRecoveryServicesAsrRecoveryPoint`                    | `Get-ASRRecoveryPoint`                   |
| `Get-AzureRmSiteRecoveryReplicationProtectedItem`        | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Get-AzureRmSiteRecoveryServer`                          | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoveryServicesProvider`                | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoverySite`                            | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryStorageClassification`           | `Get-AzureRmRecoveryServicesAsrStorageClassification`            | `Get-ASRStorageClassification`           |
| `Get-AzureRmSiteRecoveryStorageClassificationMapping`    | `Get-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `Get-ASRStorageClassificationMapping`    |
| `Get-AzureRmSiteRecoveryVault`                           | `Get-AzureRmRecoveryServicesVault`                               |                                          |
| `Get-AzureRmSiteRecoveryVaultSettings`                   | `Get-AzureRmRecoveryServicesAsrVaultContext`                     |                                          |
| `Get-AzureRmSiteRecoveryVaultSettingsFile`               | `Get-AzureRmRecoveryServicesVaultSettingsFile`                   |                                          |
| `Get-AzureRmSiteRecoveryVM`                              | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Import-AzureRmSiteRecoveryVaultSettingsFile`            | `Import-AzureRmRecoveryServicesAsrVaultSettingsFile`             |                                          |
| `New-AzureRmSiteRecoveryFabric`                          | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryNetworkMapping`                  | `New-AzureRmRecoveryServicesAsrNetworkMapping`                   | `New-ASRNetworkMapping`                  |
| `New-AzureRmSiteRecoveryPolicy`                          | `New-AzureRmRecoveryServicesAsrPolicy`                           | `New-ASRPolicy`                          |
| `New-AzureRmSiteRecoveryProtectionContainerMapping`      | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `New-AzureRmSiteRecoveryRecoveryPlan`                    | `New-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `New-ASRRecoveryPlan`                    |
| `New-AzureRmSiteRecoveryReplicationProtectedItem`        | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `New-AzureRmSiteRecoverySite`                            | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryStorageClassificationMapping`    | `New-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `New-ASRStorageClassificationMapping`    |
| `New-AzureRmSiteRecoveryVault`                           | `New-AzureRmRecoveryServicesVault`                               |                                          |
| `Remove-AzureRmSiteRecoveryFabric`                       | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryNetworkMapping`               | `Remove-AzureRmRecoveryServicesAsrNetworkMapping`                | `Remove-ASRNetworkMapping`               |
| `Remove-AzureRmSiteRecoveryPolicy`                       | `Remove-AzureRmRecoveryServicesAsrPolicy`                        | `Remove-ASRPolicy`                       |
| `Remove-AzureRmSiteRecoveryProtectionContainerMapping`   | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Remove-AzureRmSiteRecoveryRecoveryPlan`                 | `Remove-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Remove-ASRRecoveryPlan`                 |
| `Remove-AzureRmSiteRecoveryReplicationProtectedItem`     | `Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem`      | `Remove-ASRReplicationProtectedItem`     |
| `Remove-AzureRmSiteRecoveryServer`                       | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              |                                          |
| `Remove-AzureRmSiteRecoveryServicesProvider`             | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              | `Remove-ASRServicesProvider`             |
| `Remove-AzureRmSiteRecoverySite`                         | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryStorageClassificationMapping` | `Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping`  | `Remove-ASRStorageClassificationMapping` |
| `Remove-AzureRmSiteRecoveryVault`                        | `Remove-AzureRmRecoveryServicesVault`                            |                                          |
| `Restart-AzureRmSiteRecoveryJob`                         | `Restart-AzureRmRecoveryServicesAsrJob`                          | `Restart-ASRJob`                         |
| `Resume-AzureRmSiteRecoveryJob`                          | `Resume-AzureRmRecoveryServicesAsrJob`                           | `Resume-ASRJob`                          |
| `Set-AzureRmSiteRecoveryProtectionEntity`                | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryReplicationProtectedItem`        | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryVaultSettings`                   | `Set-AzureRmRecoveryServicesAsrVaultContext`                     | `Set-ASRVaultContext`                    |
| `Set-AzureRmSiteRecoveryVM`                              | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Start-AzureRmSiteRecoveryApplyRecoveryPoint`            | `Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint`             | `Start-ASRApplyRecoveryPoint`            |
| `Start-AzureRmSiteRecoveryCommitFailoverJob`             | `Start-AzureRmRecoveryServicesAsrCommitFailoverJob`              | `Start-ASRCommitFailoverJob`             |
| `Start-AzureRmSiteRecoveryPlannedFailoverJob`            | `Start-AzureRmRecoveryServicesAsrPlannedFailoverJob`             | `Start-ASRPlannedFailoverJob`            |
| `Start-AzureRmSiteRecoveryPolicyAssociationJob`          | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `Start-AzureRmSiteRecoveryPolicyDissociationJob`         | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Start-AzureRmSiteRecoveryTestFailoverJob`               | `Start-AzureRmRecoveryServicesAsrTestFailoverJob`                | `Start-ASRTestFailoverJob`               |
| `Start-AzureRmSiteRecoveryUnplannedFailoverJob`          | `Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob`           | `Start-ASRUnplannedFailoverJob`          |
| `Stop-AzureRmSiteRecoveryJob`                            | `Stop-AzureRmRecoveryServicesAsrJob`                             | `Stop-ASRJob`                            |
| `Update-AzureRmSiteRecoveryPolicy`                       | `Update-AzureRmRecoveryServicesAsrPolicy`                        | `Update-ASRPolicy`                       |
| `Update-AzureRmSiteRecoveryProtectionDirection`          | `Update-AzureRmRecoveryServicesAsrProtectionDirection`           | `Update-ASRProtectionDirection`          |
| `Update-AzureRmSiteRecoveryRecoveryPlan`                 | `Update-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Update-ASRRecoveryPlan`                 |
| `Update-AzureRmSiteRecoveryServer`                       | `Update-AzureRmRecoveryServicesAsrServicesProvider`              | `Update-ASRServicesProvider`             |
| `Update-AzureRmSiteRecoveryServicesProvider`             | `Update-AzureRmRecoveryServicesAsrvCenter`                       | `Update-ASRvCenter`                      |
