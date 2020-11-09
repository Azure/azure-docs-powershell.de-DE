---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 4b262b219c479cc2c56311c54d41eb05e2eb866d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296398"
---
# Update-AzVmss

## Synopsis
Aktualisiert den Zustand eines VMSS.

## Syntax

### Defaultparameter (Standard)
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-ImageReferenceId <String>] [-ImageReferenceOffer <String>]
 [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>]
 [-ImageUri <String>] [-LicenseType <String>] [-ManagedDiskStorageAccountType <String>]
 [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>] [-MaxUnhealthyInstancePercent <Int32>]
 [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-OsDiskCaching <CachingTypes>]
 [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>] [-PauseTimeBetweenBatches <String>]
 [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>] [-PlanPublisher <String>]
 [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>]
 [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>] [-SkuCapacity <Int32>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-IdentityId <String[]>] -IdentityType <ResourceIdentityType>
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Update-AzVmss** aktualisiert den Zustand eines virtuellen Computer-Skalierungs Satzes (VMSS) auf den Zustand eines lokalen VMSS-Objekts.

## Beispiele

### Beispiel 1: Aktualisieren Sie den Zustand eines VMSS auf den Zustand eines lokalen VMSS-Objekts.
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

Dieser Befehl aktualisiert den Zustand des VMSS mit dem Namen VMSS001, der zur Ressourcengruppe mit dem Namen Group001 gehört, in den Zustand eines lokalen VMSS-Objekts $LocalVMSS.

## Parameter

### -AsJob
Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.

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

### -AutomaticOSUpgrade
Legt fest, ob Betriebssystem-Upgrades automatisch auf Skalierungs Satz Instanzen angewendet werden sollen, wenn eine neuere Version des Bilds verfügbar ist.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutomaticRepairGracePeriod
Die Zeitdauer, für die automatische Reparaturen aufgrund einer Zustandsänderung auf VM angehalten werden. Die Kulanzzeit beginnt, nachdem die Zustandsänderung abgeschlossen wurde. Auf diese Weise können vorzeitige oder unbeabsichtigte Reparaturen vermieden werden. Die Zeitdauer sollte im ISO 8601-Format angegeben werden. Die zulässige Mindestfrist beträgt 30 Minuten (PT30M), was auch der Standardwert ist. Die maximal zulässige Kulanzzeit beträgt 90 Minuten (PT90M).

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

### -BootDiagnosticsEnabled
Gibt an, ob die Start Diagnose für den Skalierungs Satz der virtuellen Maschine aktiviert werden soll.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootDiagnosticsStorageUri
Der URI des speicherkontos, das für die Platzierung der Konsolenausgabe und des Screenshots verwendet werden soll.

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

### -CustomData
Gibt eine codierte Base-64-Zeichenfolge mit benutzerdefinierten Daten an.
Dies wird in einem binären Array dekodiert, das als Datei auf dem virtuellen Computer gespeichert ist.
Die maximale Länge des binären Arrays beträgt 65535 Bytes. <br>
Informationen zum Verwenden von Cloud-init für Ihre VM finden Sie unter [Verwenden von Cloud-init zum Anpassen einer Linux-VM während der Erstellung](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableAutoRollback
Deaktivieren des automatischen Rollbacks für die Richtlinie für das automatische OS-Upgrade

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisablePasswordAuthentication
Gibt an, dass dieses Cmdlet die Kennwortauthentifizierung für Linux-Betriebssystem deaktiviert.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutomaticRepair
Aktivieren oder deaktivieren Sie automatische Reparaturen auf dem Skalierungs Satz der virtuellen Maschine.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutomaticUpdate
Gibt an, ob die Windows-virtuellen Computer im VMSS für automatische Updates aktiviert sind.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionAtHost
Dieser Parameter kann vom Benutzer in der Anforderung verwendet werden, um die Host Verschlüsselung für den Skalierungs Satz der virtuellen Maschine zu aktivieren oder zu deaktivieren. 

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identitäts Kennung
Gibt die Liste der Benutzeridentitäten an, die dem Skalierungs Satz der virtuellen Maschine zugeordnet sind.
Die Benutzer Identitäts Bezüge sind arm-Ressourcen-IDs in der Form: '/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/Identities/{identityName} '

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityType
Gibt den Typ der Identität an, die für den Skalierungs Satz der virtuellen Maschine verwendet wird.
Der Typ "SystemAssignedUserAssigned" umfasst sowohl eine implizit erstellte Identität als auch eine Gruppe von Benutzer zugewiesenen Identitäten.
Der Typ "None" entfernt alle Identitäten aus dem Skalierungs Satz der virtuellen Maschine.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- SystemAssigned
- UserAssigned
- SystemAssignedUserAssigned
- Keine

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Imagereference-Nr
Gibt die Bildreferenz-ID an.

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

### -ImageReferenceOffer
Gibt den Typ des VMImage (Virtual Machine Image)-Angebots an.
Verwenden Sie das Get-AzVMImageOffer-Cmdlet, um ein Bildangebot zu erhalten.

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

### -ImageReferencePublisher
Gibt den Namen des Herausgebers eines VMImage an.
Verwenden Sie zum Abrufen eines Verlegers das Get-AzVMImagePublisher-Cmdlet.

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

### -ImageReferenceSku
Gibt die VMImage-SKU an.
Verwenden Sie zum Abrufen von SKUs das Get-AzVMImageSku-Cmdlet.

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

### -ImageReferenceVersion
Gibt die Version von VMImage an.
Wenn Sie die neueste Version verwenden möchten, geben Sie einen Wert von Latest anstelle einer bestimmten Version an.

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

### -ImageUri
Gibt den BLOB-URI für das Benutzerbild an.
VMSS erstellt einen Betriebssystemdatenträger im gleichen Container des Benutzerbilds.

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

### -LicenseType
Geben Sie den Lizenztyp an, der für die Einführung Ihres eigenen Lizenz Szenarios steht.

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

### -ManagedDiskStorageAccountType
Gibt den Speicher Kontotyp für verwalteten Datenträger an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- StandardLRS
- PremiumLRS

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

### -MaxBatchInstancePercent
Der maximale Prozentsatz der virtuellen Computer Instanzen, die vom parallelen Upgrade in einem Batch gleichzeitig aktualisiert werden.
Da dies ein Maximum ist, können ungesunde Instanzen in früheren oder zukünftigen Batches dazu führen, dass der Prozentsatz der Instanzen in einem Batch verringert wird, um eine höhere Zuverlässigkeit zu gewährleisten.
Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.

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

### -MaxPrice
Gibt den Höchstpreis an, den Sie für eine VM-VMSS mit niedriger Priorität bezahlen möchten. Dieser Preis ist in US-Dollar angegeben. Dieser Preis wird mit dem aktuellen Preis für niedrige Priorität für die VM-Größe verglichen. Außerdem werden die Preise zum Zeitpunkt der Erstellung/Aktualisierung von VM-VMSS mit niedriger Priorität verglichen, und der Vorgang ist nur erfolgreich, wenn der maxprice größer als der aktuelle Preis für niedrige Priorität ist. Die maxprice wird auch zum Entfernen einer VM-VMSS mit niedriger Priorität verwendet, wenn der aktuelle Preis für niedrige Priorität über die maxprice nach der Erstellung von VM/VMSS hinausgeht. Mögliche Werte sind: beliebiger Dezimalwert größer als 0 (null). Beispiel: 0,01538.  -1 gibt an, dass die VM-VMSS mit niedriger Priorität aus Preisgründen nicht vertrieben werden sollte. Außerdem ist der standardmäßige Höchstpreis-1, wenn er nicht von Ihnen bereitgestellt wird.

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxUnhealthyInstancePercent
Der maximale Prozentsatz der gesamten virtuellen Computer Instanzen im Skalierungs Satz, die gleichzeitig fehlerhaft sein können, entweder als Ergebnis eines Upgrades oder durch die Integritätsprüfung des virtuellen Computers in einem ungesunden Zustand, bevor das parallele Upgrade abgebrochen wird.
Diese Einschränkung wird vor dem Starten eines Batches überprüft.
Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.

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

### -MaxUnhealthyUpgradedInstancePercent
Der maximale Prozentsatz der aktualisierten virtuellen Computer Instanzen, die sich in einem fehlerhaften Zustand befinden.
Diese Überprüfung erfolgt, nachdem jeder Batch aktualisiert wurde.
Wenn dieser Prozentsatz jemals überschritten wird, wird das Rolling-Update abgebrochen.
Wenn der Wert nicht angegeben ist, wird er auf 20 festgelegt.

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

### -OsDiskCaching
Gibt den Zwischenspeichermodus des Betriebssystemdatenträgers an. Die zulässigen Werte für diesen Parameter lauten wie folgt:
- Keine
- ReadOnly
- ReadWrite der Standardwert ist ReadWrite.
Wenn Sie den Wert für die Zwischenspeicherung ändern, startet das Cmdlet den virtuellen Computer neu.
Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OsDiskWriteAccelerator
Gibt an, ob WriteAccelerator auf dem Betriebssystemdatenträger aktiviert oder deaktiviert werden soll.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Überversorgung
Gibt an, ob das Cmdlet die VMSS überzeichnet.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PauseTimeBetweenBatches
Die Wartezeit zwischen dem Abschließen des Updates für alle virtuellen Computer in einem Batch und dem Starten des nächsten Batches.
Die Zeitdauer sollte im ISO 8601-Format angegeben werden.
Der Standardwert ist 0 Sekunden (PT0S).

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

### -Planname
Gibt den Plan Namen an.

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

### -PlanProduct
Gibt das Plan Produkt an.

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

### -PlanPromotionCode
Gibt den Plan Promotionscode an.

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

### -PlanPublisher
Gibt den Plan Herausgeber an.

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

### -ProvisionVMAgent
Gibt an, ob der Virtual Machine-Agent auf den virtuellen Windows-Computern im VMSS bereitgestellt werden soll.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProximityPlacementGroupId
Die Ressourcen-ID der für diesen Skalierungs Satz zu verwendenden Näherungs Platzierungs Gruppe.

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
Gibt den Namen der Ressourcengruppe an, zu der der VMSS gehört.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScaleInPolicy
Die Regeln, die beim Skalieren in einem Skalierungs Satz einer virtuellen Maschine befolgt werden müssen.  Mögliche Werte sind: "Standard", "OldestVM" und "NewestVM".  "Standard" Wenn der Skalierungs Satz einer virtuellen Maschine skaliert wird, wird der Skalierungs Satz zunächst zonenübergreifend ausbalanciert, wenn es sich um einen Zonal-Skalierungs Satz handelt.  In diesem Fall werden die fehlerdomänen so weit wie möglich ausgeglichen.  Innerhalb jeder fehlerdomäne sind die für die Entfernung ausgewählten virtuellen Computer die neuesten, die nicht vor dem Skalieren geschützt sind.  "OldestVM" Wenn ein Skalierungs Satz für einen virtuellen Computer skaliert wird, werden die ältesten virtuellen Computer, die nicht vor dem Skalieren geschützt sind, zum Entfernen ausgewählt.  Bei Skalen Sätzen für virtuelle Maschinen in Zonal wird der Skalierungs Satz zunächst zonenübergreifend ausgeglichen.  Innerhalb jeder Zone werden die ältesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.  "NewestVM" Wenn ein Skalierungs Satz für virtuelle Maschinen skaliert wird, werden die neuesten virtuellen Computer, die nicht vor dem Skalieren geschützt sind, zum Entfernen ausgewählt.  Bei Skalen Sätzen für virtuelle Maschinen in Zonal wird der Skalierungs Satz zunächst zonenübergreifend ausgeglichen.  In jeder Zone werden die neuesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SinglePlacementGroup
Gibt die Gruppe für einzelne Placements an.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipExtensionsOnOverprovisionedVMs
Gibt an, dass die Erweiterungen nicht auf den zusätzlichen überlegten VMS ausgeführt werden.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuCapacity
Gibt die Anzahl der Instanzen im VMSS an.

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

### -SkuName
Gibt die Größe aller Instanzen von VMSS an.

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
Gibt die VMSS-Ebene an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- Standard
- Grundlegende

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

### -Tag
Schlüssel-Wert-Paare in Form einer Hashtabelle Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}

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

### -TerminateScheduledEventNotBeforeTimeoutInMinutes
Konfigurierbare Zeitdauer (in Minuten) ein gelöschter virtueller Computer muss möglicherweise das Terminate scheduled-Ereignis genehmigen, bevor das Ereignis automatisch genehmigt wird (Timeout).

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TerminateScheduledEvents
Gibt an, ob das terminierte terminierte Ereignis aktiviert oder deaktiviert ist.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeZone
Gibt die Zeitzone für Windows-Betriebssysteme an. z.b. \" Pacific Normalzeit \" . <br>
Mögliche Werte können [TimeZoneInfo.ID](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) -Wert aus Zeitzonen sein, die von [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)zurückgegeben werden.

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

### -UltraSSDEnabled
Das Flag, mit dem eine Funktion für einen oder mehrere verwaltete Datenlaufwerke mit UltraSSD_LRS Speicher Kontotyp auf dem Skalierungs Satz der virtuellen Maschine aktiviert oder deaktiviert wird.
Verwaltete Datenträger mit Speicher Kontotyp UltraSSD_LRS können nur dann einem VMSS hinzugefügt werden, wenn diese Eigenschaft aktiviert ist.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UpgradePolicyMode
Hat den Modus für ein Upgrade auf virtuelle Maschinen im Skalierungs Satz angegeben.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- Automatisch
- Manuell
- Rollout

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VhdContainer
Gibt die Container-URLs an, die zum Speichern von Betriebssystemdatenträgern für VMSS verwendet werden.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Gibt ein lokales VMSS-Objekt an.
Verwenden Sie das Get-AzVmss-Cmdlet, um ein VMSS-Objekt zu erhalten.
Dieses Objekt für einen virtuellen Computer enthält den aktualisierten Zustand für die VMSS.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VMScaleSetName
Gibt den Namen des von diesem Cmdlet erstellten VMSS an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

### Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet

### System. Boolean

## Ausgaben

### Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet

## Notizen

## Verwandte Links

[Get-AzVmss](./Get-AzVmss.md)

[Neu – AzVmss](./New-AzVmss.md)

[Remove-AzVmss](./Remove-AzVmss.md)

[Neustart-AzVmss](./Restart-AzVmss.md)

[Satz-AzVmss](./Set-AzVmss.md)

[Anfang-AzVmss](./Start-AzVmss.md)

[Stopp-AzVmss](./Stop-AzVmss.md)


