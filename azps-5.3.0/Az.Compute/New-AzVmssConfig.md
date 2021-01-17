---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 4fdfd5c5da9cc803cacdd2aca90b7f66771988fd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458180"
---
# New-AzVmssConfig

## SYNOPSIS
Erstellt ein VMSS-Konfigurationsobjekt.

## SYNTAX

### DefaultParameterSet (Standard)
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] [-EncryptionAtHost]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzVmssConfig"** erstellt ein konfigurierbares lokales Virtual Manager Scale Set (VMSS)-Objekt. Weitere Cmdlets sind zum Konfigurieren des VMSS-Objekts erforderlich. Diese Cmdlets sind:
- Set-AzVmssOsProfile
- Set-AzVmssStorageProfile
- Add-AzVmssNetworkInterfaceConfiguration
- Add-AzVmssExtension

## BEISPIELE

### Beispiel 1: Erstellen eines VMSS-Konfigurationsobjekts
```powershell
PS C:\> $VMSS = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

In diesem Beispiel wird ein VMSS-Konfigurationsobjekt erstellt. Der erste Befehl verwendet das **Cmdlet "New-AzVmssConfig",** um ein VMSS-Konfigurationsobjekt zu erstellen, und speichert das Ergebnis in der Variablen namens $VMSS. Der zweite Befehl verwendet das **Cmdlet "New-AzVmss",** um ein VMSS zu erstellen, das das im ersten Befehl erstellte VMSS-Konfigurationsobjekt verwendet.

### Beispiel 2

Erstellt ein VMSS-Konfigurationsobjekt. (automatisch generiert)

```powershell <!-- Aladdin Generated Example --> 
New-AzVmssConfig -Location <String> -Overprovision $false -SkuCapacity 2 -SkuName 'Standard_A0' -Tag 'Sql' -UpgradePolicyMode Automatic
```

## PARAMETERS

### -AutomaticRepairGracePeriod
Die Zeit, für die automatische Reparaturen aufgrund einer Zustandsänderung auf vm angehalten werden. Die Nachfrist beginnt nach Abschluss der Zustandsänderung. Dadurch können vorzeitig oder versehentliche Reparaturen vermieden werden. Die Zeitdauer sollte im ISO 8601-Format angegeben werden. Die zulässige Nachfrist beträgt 30 Minuten (PT30M), was auch der Standardwert ist. Die maximal zulässige Nachfrist beträgt 90 Minuten (PT90M).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoOSUpgrade
Legt fest, ob Betriebssystemupgrade automatisch auf Skalierungssatzinstanzen fortlaufend angewendet werden sollen, wenn eine neuere Version des Bilds verfügbar wird.

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

### -BootDiagnostic
Gibt das Profil der Startdiagnose für den Skalierungssatz des virtuellen Computers an.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.BootDiagnostics
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -EnableAutomaticRepair
Ermöglicht automatische Reparaturen für den Skalierungssatz des virtuellen Computers.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableUltraSSD
Ermöglicht es einer Funktion, eine oder mehrere verwaltete Datenträger mit UltraSSD_LRS Speicherkontotyp auf dem Skalierungssatz des virtuellen Computers zu verwenden.
Verwaltete Datenträger mit speicherkontotyp UltraSSD_LRS können einem VMSS nur hinzugefügt werden, wenn diese Eigenschaft aktiviert ist.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EncryptionAtHost
Dieser Parameter aktiviert die Verschlüsselung für alle Datenträger, einschließlich des Ressourcen-/Temp-Datenträgers beim Host selbst. Standard: Die Verschlüsselung beim Host wird deaktiviert, es sei denn, diese Eigenschaft ist für die Ressource auf "true" festgelegt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EvictionPolicy
Gibt die Entfernungsrichtlinie für die virtuellen Computer im Skalierungssatz an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Erweiterung
Gibt das Erweiterungsinformationsobjekt für die VMSS an. Sie können das **Cmdlet "Add-AzVmssExtension"** verwenden, um dieses Objekt hinzuzufügen.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HealthProbeId
Gibt die ID einer Lastenausgleichssonde an, mit der die Integrität einer Instanz im Skalierungssatz des virtuellen Computers ermittelt wird.
HealthProbeId liegt in Form von '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}' vor.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
Gibt den Azure-Speicherort an, an dem der VMSS erstellt wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxPrice
Gibt den maximal zulässigen Preis für eine Spot VM/VMSS an. Dieser Preis wird in US-Dollar angegeben. Dieser Preis wird mit dem aktuellen Spotpreis für die Größe der VM verglichen. Außerdem werden die Preise zum Zeitpunkt der Erstellung/Aktualisierung von Spot VM/VMSS verglichen, und der Vorgang ist nur erfolgreich, wenn der max.Preis höher als der aktuelle Spotpreis ist. Der maxPrice wird auch zum Entfernung einer Spot VM/VMSS verwendet, wenn der aktuelle Spotpreis nach der Erstellung von VM/VMSS über den maxPrice hinausgeht. Mögliche Werte sind: beliebige Dezimalwerte größer als Null. Beispiel: 0,01538.  -1 gibt an, dass die Spot VM/VMSS aus Preisgründen nicht entfernt werden sollte. Außerdem beträgt der standardmäßige maximaler Preis -1, wenn er nicht von Ihnen bereitgestellt wird.

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkInterfaceConfiguration
Gibt das Netzwerkprofilobjekt an, das die Netzwerkeigenschaften für die VMSS-Konfiguration enthält.
Sie können das **Cmdlet "Add-AzVmssNetworkInterfaceConfiguration"** verwenden, um dieses Objekt hinzuzufügen.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsProfile
Gibt das Betriebssystemprofilobjekt an, das die Betriebssystemeigenschaften für die KONFIGURATION der VMSS enthält.
Sie können dieses Objekt mithilfe des **Cmdlets "Set-AzVmssOsProfile"** festlegen.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overprovision
Gibt an, ob das Cmdlet die VMSS übergibt.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PlatformFaultDomainCount
Anzahl der Fehlerdomänen für jede Platzierungsgruppe.

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

### -Priority
Die Priorität für die virtuellen "anderen" im Skalierungssatz.  Nur unterstützte Werte sind "Regular", "Spot" und "Low".
"Regular" ist für normale virtuelle Computer.
"Spot" ist für virtuelle Spotcomputer.
"Low" ist auch für virtuelle Spotcomputer, wird aber durch "Spot" ersetzt. Verwenden Sie "Spot" anstelle von "Niedrig".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RollingUpgradePolicy
Gibt die Rollupgraderichtlinie an.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScaleInPolicy
Die Regeln, die beim Skalieren in einem Skalierungssatz für einen virtuellen Computer zu beachten sind.  Mögliche Werte: "Default", "OldestVM" und "NewestVM".  Wenn ein Skalierungssatz für einen virtuellen Computer skaliert wird, wird der Skalierungssatz zuerst zonenübergreifend ausgeglichen, wenn es sich um einen standardmäßigen Skalierungssatz handelt.  Anschließend wird sie so weit wie möglich über Fehlerdomänen hinweg ausgeglichen.  Innerhalb jeder Fault Domain sind die zum Entfernen ausgewählten virtuellen Computer die neuesten Computer, die nicht vor "scale-in" geschützt sind.  "OldestVM", wenn ein Skalierungssatz für einen virtuellen Computer skaliert wird, werden die ältesten virtuellen Computer, die nicht vor "scale-in" geschützt sind, zum Entfernen ausgewählt.  Bei tiernalen Skalierungssätzen virtueller Computer wird der Skalierungssatz zuerst zonenübergreifend ausgeglichen.  Innerhalb jeder Zone werden die ältesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.  "NewestVM", wenn ein Skalierungssatz für einen virtuellen Computer skaliert wird, werden die neuesten virtuellen Computer, die nicht vor scale-in geschützt sind, zum Entfernen ausgewählt.  Bei tiernalen Skalierungssätzen virtueller Computer wird der Skalierungssatz zuerst zonenübergreifend ausgeglichen.  In jeder Zone werden die neuesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SinglePlacementGroup
Gibt die einzelne Platzierungsgruppe an.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipExtensionsOnOverprovisionedVMs
Gibt an, dass die Erweiterungen nicht für die zusätzlichen überprovisionierten VMs ausgeführt werden.

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

### -Sku1
Gibt die Anzahl der Instanzen in der VMSS an.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuName
Gibt die Größe aller Instanzen von VMSS an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuTier
Gibt die Stufe von VMSS an. Die zulässigen Werte für diesen Parameter sind:
- Standard
- Standard

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageProfile
Gibt das Speicherprofilobjekt an, das die Datenträgereigenschaften für die KONFIGURATION der VMSS enthält.
Sie können dieses Objekt mithilfe des **Cmdlets "Set-AzVmssStorageProfile"** festlegen.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Schlüssel-Wert-Paare in Form einer Hashtabelle. Beispiel: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Aktivieren der Ereignisse "Termin planmäßig beenden"

```yaml
Type: System.Management.Automation.SwitchParameter
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

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.UpgradeMode]
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Gibt die Zonenliste für den Skalierungssatz des virtuellen Computers an.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ZoneBalance
Ob sie für den Fall, dass es zu einem Zonenausfall kommt, ausschließlich eine X-Zone-übergreifende Virtual Machine-Verteilung erzwingen soll.

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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

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

### System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.String

### System.Collections.Hashtable

### System.Int32

### System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

### Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile

### Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile

### Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]

### Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]

### System.String[]

### Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy

### System.Management.Automation.SwitchParameter

### Microsoft.Azure.Management.Compute.Models.BootDiagnostics

### System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## AUSGABEN

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Set-AzVmssOsProfile](./Set-AzVmssOsProfile.md)

[Set-AzVmssStorageProfile](./Set-AzVmssStorageProfile.md)

[Add-AzVmssNetworkInterfaceConfiguration](./Add-AzVmssNetworkInterfaceConfiguration.md)

[Add-AzVmssExtension](./Add-AzVmssExtension.md)

[New-AzVmss](./New-AzVmss.md)
