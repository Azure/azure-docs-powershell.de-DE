---
title: Alle Änderungen von AzureRM zum Azure PowerShell Az-Modul 1.0.0
description: Dieser Migrationsleitfaden enthält eine Liste mit grundlegenden Änderungen, die in Az-Version 1 an Azure PowerShell vorgenommen wurden.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: ae2539a09b93fb482ed3f8a363c7a0a66e02a412
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "92001918"
---
# <a name="breaking-changes-for-az-100"></a>Grundlegende Änderungen für Az 1.0.0

Dieses Dokument enthält ausführliche Informationen zu den Änderungen zwischen AzureRM 6.x und dem neuen Az-Modul, Version 1.x und höher. Das Inhaltsverzeichnis führt Sie durch einen vollständigen Migrationspfad, einschließlich modulspezifischer Änderungen, die sich auf Ihre Skripte auswirken können.

Allgemeine Hinweise zu den ersten Schritten bei einer Migration von AzureRM zum Az-Modul finden Sie unter [Starten der Migration von AzureRM zu Az](migrate-from-azurerm-to-az.md).

> [!IMPORTANT]
> Es gab auch zwischen den Versionen Az 1.0.0 und Az 2.0.0 wichtige Änderungen. Nachdem Sie diesem Leitfaden zum Aktualisieren von AzureRM auf Az gefolgt sind, lesen Sie die Anleitung [Az 2.0.0 Breaking Changes](migrate-az-2.0.0.md), um zu ermitteln, ob Sie zusätzliche Änderungen vornehmen müssen.

## <a name="table-of-contents"></a>Inhaltsverzeichnis

- [Allgemeine grundlegende Änderungen](#general-breaking-changes)
  - [Änderungen von Cmdlet-Nomen](#cmdlet-noun-prefix-changes)
  - [Änderungen von Modulnamen](#module-name-changes)
  - [Entfernte Module](#removed-modules)
  - [Windows PowerShell 5.1 und .NET 4.7.2](#windows-powershell-51-and-net-472)
  - [Vorübergehende Entfernung der Benutzeranmeldung per PSCredential](#temporary-removal-of-user-login-using-pscredential)
  - [Anmeldung per Standardgerätecode anstelle einer Webbrowser-Eingabeaufforderung](#default-device-code-login-instead-of-web-browser-prompt)
- [Grundlegende Änderungen am Modul](#module-breaking-changes)
  - [Az.ApiManagement (bisher AzureRM.ApiManagement)](#azapimanagement-previously-azurermapimanagement)
  - [Az.Billing (bisher AzureRM.Billing, AzureRM.Consumption und AzureRM.UsageAggregates)](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [Az.CognitiveServices (bisher AzureRM.CognitiveServices)](#azcognitiveservices-previously-azurermcognitiveservices)
  - [Az.Compute (bisher AzureRM.Compute)](#azcompute-previously-azurermcompute)
  - [Az.DataFactory (bisher AzureRM.DataFactories und AzureRM.DataFactoryV2)](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [Az.DataLakeAnalytics (bisher AzureRM.DataLakeAnalytics)](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [Az.DataLakeStore (bisher AzureRM.DataLakeStore)](#azdatalakestore-previously-azurermdatalakestore)
  - [Az.KeyVault (bisher AzureRM.KeyVault)](#azkeyvault-previously-azurermkeyvault)
  - [Az.Media (bisher AzureRM.Media)](#azmedia-previously-azurermmedia)
  - [Az.Monitor (bisher AzureRM.Insights)](#azmonitor-previously-azurerminsights)
  - [Az.Network (bisher AzureRM.Network)](#aznetwork-previously-azurermnetwork)
  - [Az.OperationalInsights (bisher AzureRM.OperationalInsights)](#azoperationalinsights-previously-azurermoperationalinsights)
  - [Az.RecoveryServices (bisher AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup und AzureRM.RecoveryServices.SiteRecovery)](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [Az.Resources (bisher AzureRM.Resources)](#azresources-previously-azurermresources)
  - [Az.ServiceFabric (bisher AzureRM.ServiceFabric)](#azservicefabric-previously-azurermservicefabric)
  - [Az.Sql (bisher AzureRM.Sql)](#azsql-previously-azurermsql)
  - [Az.Storage (bisher Azure.Storage und AzureRM.Storage)](#azstorage-previously-azurestorage-and-azurermstorage)
  - [Az.Websites (bisher AzureRM.Websites)](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a>Allgemeine grundlegende Änderungen

In diesem Abschnitt werden die allgemeinen grundlegenden Änderungen beschrieben, die Teil des neuen Entwurfs des Az-Moduls sind.

### <a name="cmdlet-noun-prefix-changes"></a>Änderungen von Cmdlet-Nomen

Im AzureRM-Modul verwenden Cmdlets entweder `AzureRM` oder `Azure` als Nomenpräfix.  Az vereinfacht und normalisiert Cmdlet-Namen, sodass alle Cmdlets „Az“ als Nomenpräfix verwenden. Beispiel:

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

Geändert in:

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

Um die Umstellung auf diese neuen Cmdlet-Namen zu vereinfachen, werden mit Az die beiden neuen Cmdlets [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) und [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias) eingeführt.  `Enable-AzureRmAlias` erstellt Aliase für die älteren Cmdlet-Namen in AzureRM, die den neueren Az-Cmdlet-Namen zugeordnet sind. Indem Sie das Argument `-Scope` mit `Enable-AzureRmAlias` verwenden, können Sie auswählen, wo Aliase aktiviert werden.

Ein Beispiel hierfür ist das folgende Skript in AzureRM:

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Es kann mit `Enable-AzureRmAlias` mit minimalen Änderungen ausgeführt werden:

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Durch das Ausführen von `Enable-AzureRmAlias -Scope CurrentUser` werden die Aliase für alle von Ihnen geöffneten PowerShell-Sitzungen aktiviert. Nach der Ausführung dieses Cmdlets sind für ein Skript dieser Art keinerlei Änderungen erforderlich:

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Ausführliche Informationen zur Nutzung der Alias-Cmdlets finden Sie in der [Enable-AzureRmAlias-Referenz](/powershell/module/az.accounts/enable-azurermalias).

Wenn Sie bereit sind, Aliase zu deaktivieren, entfernt `Disable-AzureRmAlias` die erstellten Aliase. Ausführliche Informationen finden Sie in der [Disable-AzureRmAlias-Referenz](/powershell/module/az.accounts/disable-azurermalias).

> [!IMPORTANT]
> Wenn Sie Aliase deaktivieren, stellen Sie sicher, dass sie für _alle_ Bereiche deaktiviert sind, in denen Aliase aktiviert waren.

### <a name="module-name-changes"></a>Änderungen von Modulnamen

Die Modulnamen wurden von `AzureRM.*` in `Az.*` geändert, mit Ausnahme der folgenden Module:

| AzureRM-Modul | Az-Modul |
|----------------|-----------|
| Azure.Storage | Az.Storage |
| Azure.AnalysisServices | Az.AnalysisServices |
| AzureRM.Profile | Az.Accounts |
| AzureRM.Insights | Az.Monitor |
| AzureRM.DataFactories | Az.DataFactory |
| AzureRM.DataFactoryV2 | Az.DataFactory |
| AzureRM.RecoveryServices.Backup | Az.RecoveryServices |
| AzureRM.RecoveryServices.SiteRecovery | Az.RecoveryServices |
| AzureRM.Tags | Az.Resources |
| AzureRM.MachineLearningCompute | Az.MachineLearning |
| AzureRM.UsageAggregates | Az.Billing |
| AzureRM.Consumption | Az.Billing |

Die Änderungen der Modulnamen bedeuten, dass alle Skripts, die `#Requires` oder `Import-Module` zum Laden von bestimmten Modulen nutzen, auf die Verwendung des neuen Moduls umgestellt werden müssen. Für Module, bei denen sich das Cmdlet-Suffix nicht geändert hat, bedeutet dies, dass sich das Suffix, das den Operationsbereich angibt, _nicht_ geändert hat, obwohl der Modulname geändert wurde.

#### <a name="migrating-requires-and-import-module-statements"></a>Migrieren von #Requires- und Import-Module-Anweisungen

Skripts, für die `#Requires` oder `Import-Module` zum Deklarieren einer Abhängigkeit von AzureRM-Modulen verwendet wird, müssen aktualisiert werden, damit die neuen Modulnamen genutzt werden. Beispiel:

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

Änderung erforderlich in:

```azurepowershell-interactive
#Requires -Module Az.Compute
```

Für `Import-Module`:

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

Änderung erforderlich in:

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a>Migrieren von vollqualifizierten Cmdlet-Aufrufen

Bei Verwendung von Skripts, für die Cmdlet-Aufrufe mit Modulqualifikation verwendet werden, z. B.:

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

Diese müssen geändert werden, damit die neuen Modul- und Cmdlet-Namen verwendet werden:

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a>Migrieren von Modulmanifestabhängigkeiten

Für Module, die Abhängigkeiten von AzureRM-Modulen anhand einer Modulmanifestdatei (.psd1) ausdrücken, müssen die Modulnamen jeweils im Abschnitt `RequiredModules` aktualisiert werden:

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

Änderung erforderlich in:

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a>Entfernte Module

Folgende Module wurden entfernt:

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

Die Tools für diese Dienste werden nicht mehr aktiv unterstützt.  Kunden wird die zeitnahe Umstellung auf alternative Dienste empfohlen.

### <a name="windows-powershell-51-and-net-472"></a>Windows PowerShell 5.1 und .NET 4.7.2

Für die Verwendung von Az mit PowerShell 5.1 für Windows ist die Installation von .NET Framework 4.7.2 erforderlich. Die Verwendung von PowerShell Core 6.x oder höher erfordert kein .NET Framework.

### <a name="temporary-removal-of-user-login-using-pscredential"></a>Vorübergehende Entfernung der Benutzeranmeldung per PSCredential

Aufgrund von Änderungen am Authentifizierungsablauf für .NET Standard entfernen wir die Benutzeranmeldung per PSCredential vorübergehend. Diese Funktion wird mit dem PowerShell 5.1-Release für Windows vom 15.01.2019 wieder eingeführt. Eine ausführliche Beschreibung finden Sie unter [diesem GitHub-Problem](https://github.com/Azure/azure-powershell/issues/7430).

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a>Anmeldung per Standardgerätecode anstelle einer Webbrowser-Eingabeaufforderung

Aufgrund von Änderungen am Authentifizierungsablauf für .NET Standard nutzen wir die Geräteanmeldung während der interaktiven Anmeldung als Standardanmeldungsablauf. Die Anmeldung per Webbrowser wird im PowerShell 5.1-Release für Windows vom 15.01.2019 wieder als Standard eingeführt. Benutzer können dann die Geräteanmeldung mit einem Switch-Parameter wählen.

## <a name="module-breaking-changes"></a>Grundlegende Änderungen am Modul

In diesem Abschnitt werden bestimmte wichtige Änderungen für einzelne Module und Cmdlets beschrieben.

### <a name="azapimanagement-previously-azurermapimanagement"></a>Az.ApiManagement (bisher AzureRM.ApiManagement)

- Folgende Cmdlets wurden entfernt:
  - New-AzureRmApiManagementHostnameConfiguration
  - Set-AzureRmApiManagementHostnames
  - Update-AzureRmApiManagementDeployment
  - Import-AzureRmApiManagementHostnameCertificate
  - Verwenden Sie stattdessen das Cmdlet **Set-AzApiManagement**, um diese Eigenschaften festzulegen.
- Die folgenden Eigenschaften wurden entfernt:
  - Die Eigenschaften `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` und `ScmHostnameConfiguration` vom Typ `PsApiManagementHostnameConfiguration` wurden aus `PsApiManagementContext` entfernt. Verwenden Sie stattdessen `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` und `ScmCustomHostnameConfiguration` vom Typ `PsApiManagementCustomHostNameConfiguration`.
  - Die `StaticIPs`-Eigenschaft wurde aus PsApiManagementContext entfernt. Die Eigenschaft wurde in `PublicIPAddresses` und `PrivateIPAddresses` unterteilt.
  - Die erforderliche `Location`-Eigenschaft wurde aus dem Cmdlet New-AzureApiManagementVirtualNetwork entfernt.

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a>Az.Billing (bisher AzureRM.Billing, AzureRM.Consumption und AzureRM.UsageAggregates)

- Der Parameter `InvoiceName` wurde aus dem Cmdlet `Get-AzConsumptionUsageDetail` entfernt.  Für Skripts müssen andere Identitätsparameter für die Rechnung genutzt werden.

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a>Az.CognitiveServices (bisher AzureRM.CognitiveServices)

- Der Parametersatz `GetSkusWithAccountParamSetName` wurde aus dem Cmdlet `Get-AzCognitiveServicesAccountSkus` entfernt.  Sie müssen SKUs nach Kontotyp und Standort abrufen, anstatt ResourceGroupName und den Kontonamen zu verwenden.

### <a name="azcompute-previously-azurermcompute"></a>Az.Compute (bisher AzureRM.Compute)

- `IdentityIds` wurden aus der `Identity`-Eigenschaft in den Objekten `PSVirtualMachine` und `PSVirtualMachineScaleSet` entfernt. In Skripts sollte der Wert dieses Felds nicht mehr verwendet werden, um Verarbeitungsentscheidungen zu treffen.
- Der Typ der `InstanceView`-Eigenschaft des `PSVirtualMachineScaleSetVM`-Objekts wurde von `VirtualMachineInstanceView` in `VirtualMachineScaleSetVMInstanceView` geändert.
- Die Eigenschaften `AutoOSUpgradePolicy` und `AutomaticOSUpgrade` wurden aus der `UpgradePolicy`-Eigenschaft entfernt.
- Der Typ der `Sku`-Eigenschaft im `PSSnapshotUpdate`-Objekt wurde von `DiskSku` in `SnapshotSku` geändert.
- `VmScaleSetVMParameterSet` wurde aus dem Cmdlet `Add-AzVMDataDisk` entfernt. Sie können einer ScaleSet-VM nicht mehr einzeln einen Datenträger hinzufügen.

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a>Az.DataFactory (bisher AzureRM.DataFactories und AzureRM.DataFactoryV2)

- Der Parameter `GatewayName` ist im Cmdlet `New-AzDataFactoryEncryptValue` jetzt obligatorisch.
- Das Cmdlet `New-AzDataFactoryGatewayKey` wurde entfernt.
- Der Parameter `LinkedServiceName` wurde aus dem Cmdlet `Get-AzDataFactoryV2ActivityRun` entfernt. In Skripts sollte der Wert dieses Felds nicht mehr verwendet werden, um Verarbeitungsentscheidungen zu treffen.

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a>Az.DataLakeAnalytics (bisher AzureRM.DataLakeAnalytics)

- Veraltete Cmdlets wurden entfernt: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret` und `Set-AzDataLakeAnalyticsCatalogSecret`.

### <a name="azdatalakestore-previously-azurermdatalakestore"></a>Az.DataLakeStore (bisher AzureRM.DataLakeStore)

- Für die folgenden Cmdlets wurde der Typ des Parameters `Encoding` von `FileSystemCmdletProviderEncoding` in `System.Text.Encoding` geändert. Bei dieser Änderung wurden die Codierungswerte `String` und `Oem` entfernt. Alle anderen bisherigen Codierungswerte bleiben erhalten.
  - New-AzureRmDataLakeStoreItem
  - Add-AzureRmDataLakeStoreItemContent
  - Get-AzureRmDataLakeStoreItemContent
- Der veraltete Eigenschaftenalias `Tags` wurde aus den Cmdlets `New-AzDataLakeStoreAccount` und `Set-AzDataLakeStoreAccount` entfernt.

  Skripts mit Verwendung von:
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  Änderung erforderlich in:
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- Die veralteten Eigenschaften `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier` und `FirewallAllowAzureIps` wurden aus dem `PSDataLakeStoreAccountBasic`-Objekt entfernt.  Alle Skripts, für die das von `Get-AzDataLakeStoreAccount` zurückgegebene `PSDatalakeStoreAccount`-Objekt verwendet wird, sollten nicht auf diese Eigenschaften verweisen.

### <a name="azkeyvault-previously-azurermkeyvault"></a>Az.KeyVault (bisher AzureRM.KeyVault)

- Die `PurgeDisabled`-Eigenschaft wurde aus den Objekten `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` und `PSKeyVaultSecretAttributes` entfernt. In Skripts sollte nicht mehr auf die ```PurgeDisabled```-Eigenschaft verwiesen werden, um Verarbeitungsentscheidungen zu treffen.

### <a name="azmedia-previously-azurermmedia"></a>Az.Media (bisher AzureRM.Media)

- Der veraltete Eigenschaftenalias `Tags` wurde aus dem Cmdlet `New-AzMediaService` entfernt. Skripts mit Verwendung von:
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  Änderung erforderlich in:
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a>Az.Monitor (bisher AzureRM.Insights)

- Die Plural-Parameternamen `Categories` und `Timegrains` wurden in Singular-Parameternamen aus dem Cmdlet `Set-AzDiagnosticSetting` geändert. Skripts mit Verwendung von:
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  Änderung erforderlich in:
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a>Az.Network (bisher AzureRM.Network)

- Der veraltete Parameter `ResourceId` wurde aus dem Cmdlet `Get-AzServiceEndpointPolicyDefinition` entfernt.
- Die verwaltete `EnableVmProtection`-Eigenschaft wurde aus dem `PSVirtualNetwork`-Objekt entfernt.
- Das veraltete Cmdlet `Set-AzVirtualNetworkGatewayVpnClientConfig` wurde entfernt.

Für Skripts sollten basierend auf den Werten dieser Felder keine Verarbeitungsentscheidungen mehr getroffen werden.

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a>Az.OperationalInsights (bisher AzureRM.OperationalInsights)

- Der Standardparametersatz für `Get-AzOperationalInsightsDataSource` wurde entfernt, und `ByWorkspaceNameByKind` ist zum Standardparametersatz geworden.

  Skripts mit Auflistung von Datenquellen mit:
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  Änderung mit Angabe der Art erforderlich:
  ```azurepowershell-interactive
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a>Az.RecoveryServices (bisher AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup und AzureRM.RecoveryServices.SiteRecovery)

- Der Parameter `Encryption` wurde aus dem Cmdlet `New/Set-AzRecoveryServicesAsrPolicy` entfernt.
- Der Parameter `TargetStorageAccountName` ist für Wiederherstellungen von verwalteten Datenträgern im Cmdlet `Restore-AzRecoveryServicesBackupItem` jetzt obligatorisch.
- Die Parameter `StorageAccountName` und `StorageAccountResourceGroupName` im Cmdlet `Restore-AzRecoveryServicesBackupItem` wurden entfernt.
- Der Parameter `Name` im Cmdlet `Get-AzRecoveryServicesBackupContainer` wurde entfernt.

### <a name="azresources-previously-azurermresources"></a>Az.Resources (bisher AzureRM.Resources)

- Der Parameter `Sku` wurde aus dem Cmdlet `New/Set-AzPolicyAssignment` entfernt.
- Der Parameter `Password` wurde aus den Cmdlets `New-AzADServicePrincipal` und `New-AzADSpCredential` entfernt. Die Kennwörter werden automatisch generiert. Bei Verwendung von Skripts mit Bereitstellung des Kennworts:

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  Änderung erforderlich, damit das Kennwort aus der Ausgabe verwendet wird:

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a>Az.ServiceFabric (bisher AzureRM.ServiceFabric)

- Die folgenden Cmdlet-Rückgabetypen wurden geändert:
  - Die `ServiceTypeHealthPolicies`-Eigenschaft vom Typ `ApplicationHealthPolicy` wurde entfernt.
  - Die `ApplicationHealthPolicies`-Eigenschaft vom Typ `ClusterUpgradeDeltaHealthPolicy` wurde entfernt.
  - Die `OverrideUserUpgradePolicy`-Eigenschaft vom Typ `ClusterUpgradePolicy` wurde entfernt.
  - Diese Änderungen wirken sich auf die folgenden Cmdlets aus:
    - Add-AzServiceFabricClientCertificate
    - Add-AzServiceFabricClusterCertificate
    - Add-AzServiceFabricNode
    - Add-AzServiceFabricNodeType
    - Get-AzServiceFabricCluster
    - Remove-AzServiceFabricClientCertificate
    - Remove-AzServiceFabricClusterCertificate
    - Remove-AzServiceFabricNode
    - Remove-AzServiceFabricNodeType
    - Remove-AzServiceFabricSetting
    - Set-AzServiceFabricSetting
    - Set-AzServiceFabricUpgradeType
    - Update-AzServiceFabricDurability
    - Update-AzServiceFabricReliability

### <a name="azsql-previously-azurermsql"></a>Az.Sql (bisher AzureRM.Sql)

- Die Parameter `State` und `ResourceId` wurden aus dem Cmdlet `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` entfernt.
- Veraltete Cmdlets wurden entfernt: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing` und `Remove-AzSqlServerAuditing`.
- Der veraltete Parameter `Current` wurde aus dem Cmdlet `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` entfernt.
- Der veraltete Parameter `DatabaseName` wurde aus dem Cmdlet `Get-AzSqlServerServiceObjective` entfernt.
- Der veraltete Parameter `PrivilegedLogin` wurde aus dem Cmdlet `Set-AzSqlDatabaseDataMaskingPolicy` entfernt.

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a>Az.Storage (bisher Azure.Storage und AzureRM.Storage)

- Der Standardparametersatz wurde in `OAuthParameterSet` geändert, um die Erstellung eines OAuth-Speicherkontexts nur mit dem Speicherkontonamen zu unterstützen.
  - Beispiel: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`
- Der Parameter `Location` ist im Cmdlet `Get-AzStorageUsage` jetzt obligatorisch.
- Für die Methoden der Storage-API wird jetzt anstelle von synchronen API-Aufrufen das aufgabenbasierte asynchrone Muster (Task-based Asynchronous Pattern, TAP) verwendet. Die folgenden Beispiele veranschaulichen die neuen asynchronen Befehle:

#### <a name="blob-snapshot"></a>Momentaufnahme eines Blobs erstellen

AzureRM:

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

Az:

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a>Momentaufnahme freigeben

AzureRM:

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

Az:

```azurepowershell-interactive
$Share = Get-AzStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a>Vorläufig gelöschten Blob wiederherstellen

AzureRM:

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

Az:

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a>Blobtarif festlegen

AzureRM:

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

Az:

```azurepowershell-interactive
$blockBlob = Get-AzStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a>Az.Websites (bisher AzureRM.Websites)

- Die veralteten Eigenschaften wurden aus den Objekten `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` und `PSSite` entfernt.
