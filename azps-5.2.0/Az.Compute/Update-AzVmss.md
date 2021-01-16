---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 4b262b219c479cc2c56311c54d41eb05e2eb866d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300968"
---
# Update-AzVmss

## SYNOPSIS
Aktualisiert den Zustand eines VMSS.

## SYNTAX

### Standardparameter (Standard)
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

## BESCHREIBUNG
Das **Cmdlet "Update-AzVmss"** aktualisiert den Zustand eines Virtual Machine Scale Set (VMSS) auf den Zustand eines lokalen VMSS-Objekts.

## BEISPIELE

### Beispiel 1: Aktualisieren des Zustands eines VMSS auf den Zustand eines lokalen VMSS-Objekts.
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

Mit diesem Befehl wird der Zustand der VMSS namens VMSS001 aktualisiert, die der Ressourcengruppe "Group001" zum Zustand eines lokalen VMSS-Objekts ($LocalVMSS.

## PARAMETERS

### -AsJob
Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.

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
Legt fest, ob Betriebssystemupgrade automatisch auf Skalierungssatzinstanzen fortlaufend angewendet werden sollen, wenn eine neuere Version des Bilds verfügbar wird.

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
Die Zeit, für die automatische Reparaturen aufgrund einer Zustandsänderung auf der VM angehalten werden. Die Nachfrist beginnt nach Abschluss der Zustandsänderung. Dadurch können vorzeitig oder versehentliche Reparaturen vermieden werden. Die Zeitdauer sollte im ISO 8601-Format angegeben werden. Die zulässige Nachfrist beträgt 30 Minuten (PT30M), was auch der Standardwert ist. Die maximal zulässige Nachfrist beträgt 90 Minuten (PT90M).

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
Ob die Startdiagnose für den Skalierungssatz des virtuellen Computers aktiviert werden soll.

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
URI des Speicherkontos, das zum Platzieren der Konsolenausgabe und des Screenshots verwendet wird.

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
Gibt eine base-64-codierte Zeichenfolge mit benutzerdefinierten Daten an.
Dies wird in ein Binärarray decodiert, das als Datei auf dem virtuellen Computer gespeichert wird.
Die maximale Länge des Binärarrays beträgt 65535 Bytes. <br>
Informationen zur Verwendung von cloud-init für Ihre VM finden Sie unter "Verwenden von [cloud-init zum Anpassen einer Linux-VM während der Erstellung".](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)

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
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
Deaktivieren des automatischen Rollbacks für die Upgraderichtlinie für das automatische Betriebssystem

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
Gibt an, dass dieses Cmdlet die Kennwortauthentifizierung für Linux OS deaktiviert.

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
Aktivieren oder deaktivieren Sie automatische Reparaturen für den Skalierungssatz des virtuellen Computers.

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
Gibt an, ob die virtuellen Computer von Windows in VMSS für automatische Updates aktiviert sind.

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
Dieser Parameter kann vom Benutzer in der Anforderung verwendet werden, um die Hostverschlüsselung für den Skalierungssatz des virtuellen Computers zu aktivieren oder zu deaktivieren. 

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

### -IdentityId
Gibt die Liste der Benutzeridentitäten an, die dem Skalierungssatz für den virtuellen Computer zugeordnet sind.
Die Benutzeridentitätsverweise werden ARM Ressourcen-ID im Format '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}' angegeben.

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
Gibt den Identitätstyp an, der für den Skalierungssatz des virtuellen Computers verwendet wird.
Der Typ "SystemAssignedUserAssigned" enthält sowohl eine implizit erstellte Identität als auch eine Gruppe von vom Benutzer zugewiesenen Identitäten.
Mit dem Typ "None" werden alle Identitäten aus dem Skalierungssatz des virtuellen Computers entfernt.
Die zulässigen Werte für diesen Parameter sind:
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

### -ImageReferenceId
Gibt die Bildverweis-ID an.

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
Gibt den Typ des Virtual Machine Image (VMImage)-Angebots an.
Um ein Bildangebot zu erhalten, verwenden Sie das Get-AzVMImageOffer Cmdlet.

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
Gibt den Namen eines Herausgebers eines VMImage an.
Verwenden Sie zum Abrufen eines Herausgebers das Get-AzVMImagePublisher Cmdlet.

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
Verwenden Sie zum Abrufen von SKUs das Get-AzVMImageSku Cmdlet.

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
Wenn Sie die neueste Version verwenden möchten, geben Sie den Wert "Neueste Version" anstelle einer bestimmten Version an.

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
VMSS erstellt einen Betriebssystemdatenträger im gleichen Container des Benutzerabbilds.

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
Geben Sie den Lizenztyp an, mit dem Sie Ihr eigenes Lizenzszenario erstellen können.

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
Gibt den Speicherkontotyp für verwalteten Datenträger an.
Die zulässigen Werte für diesen Parameter sind:
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
Der maximale Prozentwert der gesamten Instanzen virtueller Computer, die gleichzeitig durch das rollende Upgrade in einem Batch aktualisiert werden.
Da dies eine maximale Anzahl fehlerhafter Instanzen in vorherigen oder zukünftigen Batches ist, kann dies dazu führen, dass der Prozentsatz der Instanzen in einem Batch abgenommen wird, um eine höhere Zuverlässigkeit zu gewährleisten.
Wenn der Wert nicht angegeben wird, wird er auf 20 festgelegt.

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
Gibt den Maximalpreis an, den Sie für eine VM/VMSS mit niedriger Priorität bezahlen möchten. Dieser Preis wird in US-Dollar angegeben. Dieser Preis wird mit dem aktuellen Preis mit niedriger Priorität für die Größe der VM verglichen. Außerdem werden die Preise zum Zeitpunkt der Erstellung/Aktualisierung von VM/VMSS mit niedriger Priorität verglichen, und der Vorgang ist nur erfolgreich, wenn der "maxPrice" größer als der aktuelle Preis mit niedriger Priorität ist. Der "maxPrice" wird auch zum Entfernung einer VM/VMSS mit niedriger Priorität verwendet, wenn der aktuelle Preis mit niedriger Priorität nach der Erstellung von VM/VMSS über den maxPrice hinausgeht. Mögliche Werte sind: beliebige Dezimalwerte größer als Null. Beispiel: 0,01538.  -1 gibt an, dass die VM/VMSS mit niedriger Priorität aus Preisgründen nicht entfernt werden sollte. Außerdem beträgt der standardmäßige Maximalpreis -1, wenn er nicht von Ihnen bereitgestellt wird.

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
Der maximale Prozentsatz der gesamten Instanzen des virtuellen Computers in dem Skalierungssatz, der gleichzeitig fehlerhaft sein kann, entweder als Ergebnis des Upgrades oder durch Die Integritätsprüfungen des virtuellen Computers in einem fehlerhaften Zustand vor dem Abbruch des Rollups.
Diese Einschränkung wird vor dem Starten eines Batches überprüft.
Wenn der Wert nicht angegeben wird, wird er auf 20 festgelegt.

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
Der maximale Prozentsatz der aktualisierten Instanzen virtueller Computer, für die ein fehlerhafter Zustand gefunden werden kann.
Diese Überprüfung wird ausgeführt, nachdem für jeden Batch ein Upgrade ausgeführt wurde.
Wenn dieser Prozentsatz jemals überschritten wird, wird das rollierte Update abgebrochen.
Wenn der Wert nicht angegeben wird, wird er auf 20 festgelegt.

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
Gibt den Cachemodus des Betriebssystemdatenträgers an. Die zulässigen Werte für diesen Parameter sind:
- Keine
- ReadOnly
- ReadWrite Der Standardwert ist "ReadWrite".
Wenn Sie den Zwischenspeicherungswert ändern, wird der virtuelle Computer vom Cmdlet neu gestartet.
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

### -Overprovision
Gibt an, ob das Cmdlet die VMSS übergibt.

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

### -PlanName
Gibt den Plannamen an.

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
Gibt das Planprodukt an.

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
Gibt den Promotionscode für den Plan an.

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
Gibt den Planherausgeber an.

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
Gibt an, ob der Agent für virtuelle Computer auf den virtuellen Computern von Windows auf der VMSS bereitgestellt werden soll.

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
Die Ressourcen-ID der Näherungsplatzierungsgruppe, die für diesen Skalierungssatz verwendet werden soll.

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
Gibt den Namen der Ressourcengruppe an, der die VMSS angehört.

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
Die Regeln, die beim Skalieren in einem Skalierungssatz für einen virtuellen Computer zu beachten sind.  Mögliche Werte sind: "Default", "OldestVM" und "NewestVM".  "Standard", wenn ein Skalierungssatz für einen virtuellen Computer skaliert wird, wird der Skalierungssatz zuerst zonenübergreifend ausgeglichen, wenn es sich um einen standardmäßigen Skalierungssatz handelt.  Anschließend wird sie so weit wie möglich über Fehlerdomänen hinweg ausgeglichen.  Innerhalb jeder Fault Domain sind die zum Entfernen ausgewählten virtuellen Computer die neuesten, die nicht vor scale-in geschützt sind.  "OldestVM", wenn ein Skalierungssatz für einen virtuellen Computer skaliert wird, werden die ältesten virtuellen Computer, die nicht vor "scale-in" geschützt sind, zum Entfernen ausgewählt.  Bei tiernalen Skalierungssätzen virtueller Computer wird der Skalierungssatz zuerst zonenübergreifend ausgeglichen.  Innerhalb jeder Zone werden die ältesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.  "NewestVM", wenn ein Skalierungssatz für einen virtuellen Computer skaliert wird, werden die neuesten virtuellen Computer, die nicht vor scale-in geschützt sind, zum Entfernen ausgewählt.  Bei tiernalen Skalierungssätzen virtueller Computer wird der Skalierungssatz zuerst zonenübergreifend ausgeglichen.  In jeder Zone werden die neuesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.

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
Gibt die einzelne Platzierungsgruppe an.

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
Gibt an, dass die Erweiterungen nicht für die zusätzlichen überprovisionierten VMs ausgeführt werden.

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

### -Sku1
Gibt die Anzahl der Instanzen in der VMSS an.

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
Gibt die Stufe von VMSS an.
Die zulässigen Werte für diesen Parameter sind:
- Standard
- Standard

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
Schlüssel-Wert-Paare in Form einer Hashtabelle. Beispiel: @{key0="value0";key1=$null;key2="value2"}

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
Eine konfigurierbare Dauer (in Minuten) für einen gelöschten virtuellen Computer muss potenziell das Ereignis "Terminiertes Ereignis beenden" genehmigen, bevor das Ereignis automatisch genehmigt (Timed out) wird.

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
Gibt an, ob das Ereignis "Termingerecht beenden" aktiviert oder deaktiviert ist.

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
Gibt die Zeitzone für das Windows-Betriebssystem an. z. B. \" Pacific Standard \" Time. <br>
Mögliche Werte können als [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) zeitzonen verwendet werden, die von ["TimeZoneInfo.GetSystemTimeZones" zurückgegeben werden.](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)

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
Das Kennzeichen, mit dem eine Funktion aktiviert oder deaktiviert wird, um eine oder mehrere verwaltete Datenträger mit UltraSSD_LRS Speicherkontotyp auf dem Skalierungssatz des virtuellen Computers zu verwenden.
Verwaltete Datenträger mit speicherkontotyp UltraSSD_LRS können einem VMSS nur hinzugefügt werden, wenn diese Eigenschaft aktiviert ist.

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
Der Modus für ein Upgrade auf virtuelle Computer wurde im Skalierungssatz angegeben.
Die zulässigen Werte für diesen Parameter sind:
- Automatisch
- Manuell
- Rollen

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
Gibt die Container-URLs an, die zum Speichern von Betriebssystemdatenträgern für die VMSS verwendet werden.

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
Verwenden Sie zum Abrufen eines VMSS-Objekts das Get-AzVmss-Cmdlet.
Dieses Objekt des virtuellen Computers enthält den aktualisierten Zustand für die VMSS.

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
Gibt den Namen der VMSS an, die von diesem Cmdlet erstellt wird.

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

### -Confirm
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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

### -Waswenn
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

### System.Boolean

## AUSGABEN

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzVmss](./Get-AzVmss.md)

[New-AzVmss](./New-AzVmss.md)

[Remove-AzVmss](./Remove-AzVmss.md)

[Restart-AzVmss](./Restart-AzVmss.md)

[Set-AzVmss](./Set-AzVmss.md)

[Start-AzVmss](./Start-AzVmss.md)

[Stop-AzVmss](./Stop-AzVmss.md)


