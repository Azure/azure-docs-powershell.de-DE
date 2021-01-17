---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 1b5f447e95e137ba9199ba596029f2088a977c91
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459696"
---
# Set-AzRecoveryServicesAsrReplicationProtectedItem

## SYNOPSIS
Legt Wiederherstellungseigenschaften wie Zielnetzwerk und Größe virtueller Computer für das angegebene replikationsgeschützte Element fest.

## SYNTAX

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryProximityPlacementGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-UseManagedDisk <String>]
 [-DiskIdToDiskEncryptionSetMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoAzureVMName <String>]
 [-ASRVMNicConfiguration <ASRVMNicConfig[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Set-AzRecoveryServicesAsrReplicationProtectedItem"** legt die Wiederherstellungseigenschaften für ein replikationsgeschütztes Element fest.

## BEISPIELE

### Beispiel 1
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

Startet den Vorgang zum Aktualisieren der einstellungen für replikationsgeschützte Elemente mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.

### Beispiel 2
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

Startet den Vorgang der Aktualisierung der Einstellungen für die replikationsgeschützte Netzwerkschnittstellenkarte (NIC Reduction) unter Verwendung der angegebenen Parameter und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.

### Beispiel 3
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

Startet den Vorgang der Aktualisierung der primären NIC (für die für wiederhergestellte vm )-Einstellungen verwendete replikationsgeschützte Element mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.

### Beispiel 4
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

Startet den Vorgang der Aktualisierung der replikationsgeschützten Element-NIC-Einstellungen (zur Verwendung für wiederhergestellte vm )-Einstellungen mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.

### Beispiel 5
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

Startet den Vorgang zum Aktualisieren des durch die Replikation geschützten Elements, das "noc tp enable accelerated networking on recovery VM(for Azure to Azure Disaster Recovery)" aktiviert ist.
Übergeben Sie "-EnableAccepharmaNetworkingOnRecovery" nicht, um beschleunigtes Netzwerk zu deaktivieren.

### Beispiel 6
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

Starten Sie den Aktualisierungsvorgang für das angegebene verschlüsselte replikationsgeschützte Element, um die angegebenen Verschlüsselungsdetails für Failover-VM zu verwenden.

### Beispiel 7
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -RecoveryProximityPlacementGroupId $ppg
```

Starten Sie den Aktualisierungsvorgang für das angegebene replikationsgeschützte Element, um die bereitgestellte Näherungsplatzierungsgruppe für Failover-VM zu verwenden.


## PARAMETERS

### -ASRVMNicConfiguration
Gibt die Details der Test failover- und failover-NIC-Konfiguration an.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureToAzureUpdateReplicationConfiguration
Gibt die Datenträgerkonfiguration an, die für verwaltete Datenträger-VM (Azure zu Azure DR scenrio) udpated werden soll.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
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

### -DiskEncryptionSecretUrl
Gibt die geheime Festplattenverschlüsselungs-URL mit version(Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.

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

### -DiskEncryptionVaultId
Gibt die Schlüsseltresor-ID (Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.

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

### -DiskIdToDiskEncryptionSetMap
Das Wörterbuch der Datenträgerressourcen-ID zum Datenträgerverschlüsselungssatz ARM ID.

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAcce 2010NetworkingOnRecovery
Gibt die angegebene NIC auf der Wiederherstellungs-VM an, nachdem failoverbeschleunigtes Netzwerk verwendet wurde.

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

### -InputObject
Das Eingabeobjekt für das Cmdlet: Das asR-replikationsgeschützte Elementobjekt, das dem zu aktualisierende replikationsgeschützten Element entspricht.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyEncryptionKeyUrl
Gibt die URL-Version des Datenträgerverschlüsselungsschlüssels (Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.

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

### -KeyEncryptionVaultId
Gibt die Schlüssel-ID des Datenträgerverschlüsselungsschlüssels (Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.


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
Geben Sie die Lizenztypauswahl an, die für virtuelle Windows Server-Computer verwendet werden soll. Wenn Sie berechtigt sind, den Azure Hybrid Use Benefit (HUB) für Migrationen zu verwenden, und angeben möchten, dass die Hubeinstellung verwendet wird, während ein Fehler bei diesem geschützten Element vor sich geht, legen Sie den Lizenztyp auf "WindowsServer" fest.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen des virtuellen Wiederherstellungscomputers an, der bei einem Failover erstellt wird.

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

### -NicSelectionType
Gibt die Eigenschaften der Netzwerkschnittstellenkarte (NIC) an, die von einem Benutzer oder standardmäßig festgelegt werden.
Sie können "NotSelected" angeben, um zu den Standardwerten zurück zu wechseln.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryNic
Gibt die NIC an, die nach dem Failover als primäre NIC für recvcovery VM verwendet wird.

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

### -RecoveryAvailabilitySet
Verfügbarkeitssatz für replikationsgeschütztes Element nach dem Failover.

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

### -RecoveryBootDiagStorageAccountId
Gibt das Speicherkonto für die Startdiagnose für die Wiederherstellung der Azure VM an.

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

### -RecoveryCloudServiceId
Die Ressourcen-ID des Wiederherstellungs-Clouddiensts für den Failover dieses virtuellen Computers.

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

### -RecoveryLBBackendAddressPoolId
Gibt die Ziel-Back-End-Adresspools an, die der Wiederherstellungs-NIC zugeordnet werden sollen.

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

### -RecoveryNetworkId
Gibt die ID des virtuellen Azure-Netzwerks an, für das ein Fehler beim geschützten Element ausgeführt werden soll.

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

### -RecoveryNetworkSecurityGroupId
Gibt die ID der Netzwerksicherheitsgruppe an, die der Wiederherstellungs-NIC zugeordnet werden soll.

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

### -RecoveryNicStaticIPAddress
Gibt die statische IP-Adresse an, die der primären NIC für die Wiederherstellung zugewiesen werden soll.

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

### -RecoveryNicSubnetName
Gibt den Namen des Subnetzes im virtuellen Wiederherstellungsnetzwerk von Azure an, mit dem diese NIC des geschützten Elements bei einem Failover verbunden werden soll.

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

### -RecoveryProximityPlacementGroupId
Gibt die Ressourcen-ID der Näherungsplatzierungsgruppe für die Wiederherstellung an, zu der der virtuelle Computer über einen Failover führen soll.

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

### -RecoveryPublicIPAddressId
Gibt die ID der öffentlichen IP-Adressressource an, die der Wiederherstellungs-NIC zugeordnet werden soll.

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

### -RecoveryResourceGroupId
Die ID der Azure-Ressourcengruppe in der Wiederherstellungsregion, in der das geschützte Element bei einem Failover wiederhergestellt wird.

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

### -Size
Gibt die Größe des virtuellen Wiederherstellungscomputers an.
Der Wert sollte aus der Reihe von Größen kommen, die von virtuellen Computern von Azure unterstützt werden.

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

### -TfoAzureVMName
Gibt den Namen der Test failover VM an.

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

### -UpdateNic
Gibt die NIC des virtuellen Computers an, für den dieses Cmdlet die Eigenschaft des Wiederherstellungsnetzwerks auf udpated setzt.

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

### -UseManagedDisk
Gibt an, ob der im Failover erstellte virtuelle Azure-Computer verwaltete Datenträger verwenden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

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

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem

## AUSGABEN

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzRecoveryServicesAsrReplicationProtectedItem](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[New-AzRecoveryServicesAsrReplicationProtectedItem](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[Remove-AzRecoveryServicesAsrReplicationProtectedItem](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
