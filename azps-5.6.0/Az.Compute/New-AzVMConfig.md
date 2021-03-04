---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 71aa555528ff1cdb5748c1a4ac62481ddd17c17c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938872"
---
# New-AzVMConfig

## SYNOPSIS
Erstellt ein konfigurierbares Objekt für einen virtuellen Computer.

## SYNTAX

### DefaultParameterSet (Standard)
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet New-AzVMConfig** erstellt ein konfigurierbares Objekt für einen lokalen virtuellen Computer für Azure.
Andere Cmdlets können zum Konfigurieren eines Virtuellen Computerobjekts verwendet werden, z. B. Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface und Set-AzVMOSDisk.

## BEISPIELE

### Beispiel 1: Erstellen eines Virtuellen Computerobjekts
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

Der erste Befehl ruft den Verfügbarkeitssatz "AvailabilitySet03" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.
Mit dem zweiten Befehl wird ein Objekt eines virtuellen Computers erstellt und dann in der $VirtualMachine gespeichert.
Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.
Der virtuelle Computer gehört zu dem Verfügbarkeitssatz, der auf der $AvailabilitySet.

## PARAMETER

### -AvailabilitySetId
Gibt die ID eines Verfügbarkeitssets an.
Um ein Verfügbarkeitssatzobjekt zu erhalten, verwenden Sie das Get-AzAvailabilitySet Cmdlet.
Das Verfügbarkeitssatzobjekt enthält eine ID-Eigenschaft. <br>
Virtuelle Computer, die im gleichen Verfügbarkeitssatz angegeben sind, werden verschiedenen Knoten zugeordnet, um die Verfügbarkeit zu maximieren. <br>
Weitere Informationen zu Verfügbarkeitssätzen finden Sie unter [Verwalten der Verfügbarkeit virtueller Computer.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json) <br>
Weitere Informationen zur geplanten Wartung von Azure finden Sie unter [Geplante Wartung für virtuelle Computer in Azure.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json) <br>
Derzeit kann eine VM nur zur Verfügbarkeit hinzugefügt werden, die zur Erstellungszeit festgelegt wurde. Der Verfügbarkeitssatz, dem der virtuelle Computer hinzugefügt wird, sollte sich unter derselben Ressourcengruppe wie die Verfügbarkeitssatzressource befindet. Eine vorhandene VM kann einem Verfügbarkeitssatz nicht hinzugefügt werden. <br>
Diese Eigenschaft kann nicht zusammen mit einem Verweis auf "non-null properties.virtualMachineScaleSet" vorhanden sein.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -EnableUltraSSD
Ermöglicht eine Funktion, über eine oder mehrere verwaltete Datenträger mit UltraSSD_LRS Speicherkontotyp auf der VM zu verfügen.
Verwaltete Datenträger mit Speicherkontotyp UltraSSD_LRS einem virtuellen Computer nur hinzugefügt werden, wenn diese Eigenschaft aktiviert ist.


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
Die Räumungsrichtlinie für den virtuellen Azure Spot-Computer.  Unterstützte Werte sind "Deallocate" und "Delete".

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

### -HostId
Die Id des Hosts

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
Gibt die Liste der Benutzeridentitäten an, die dem Skalierungssatz für virtuelle Computer zugeordnet sind.
Die Benutzeridentitätsverweise werden ARM Ressourcen-ID im Formular "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" angezeigt.

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
Die Identität des virtuellen Computers, sofern konfiguriert.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseType
Gibt einen Lizenztyp an, der angibt, dass das Bild oder der Datenträger für den virtuellen Computer lokal lizenziert wurde.
Mögliche Werte für Windows Server sind:
- Windows_Client
- Windows_Server Mögliche Werte für Das Betriebssystem Linux Server sind: 
- RHEL_BYOS (für RREL) 
- SLES_BYOS (für SUSE) 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPreis
Gibt den Höchstpreis an, den Sie für eine VM/VMSS mit niedriger Priorität zahlen möchten. Dieser Preis ist in US-Dollar angegeben. Dieser Preis wird mit dem aktuellen Preis mit niedriger Priorität für die Größe des virtuellen Computers verglichen. Außerdem werden die Preise zum Zeitpunkt der Erstellung/Aktualisierung von VM/VMSS mit niedriger Priorität verglichen, und der Vorgang ist nur erfolgreich, wenn der maxPreis größer als der aktuelle Preis mit niedriger Priorität ist. Der maxPrice wird auch zum Räumung einer VM/VMSS mit niedriger Priorität verwendet, wenn der aktuelle Preis mit niedriger Priorität nach der Erstellung von VM/VMSS über den maxPreis hinausgeht. Mögliche Werte sind: jeder Dezimalwert größer als Null. Beispiel: 0,01538.  -1 gibt an, dass die VM/VMSS mit niedriger Priorität aus Preisgründen nicht entfernt werden sollte. Außerdem ist der standardmäßige Höchstpreis -1, wenn er nicht von Ihnen bereitgestellt wird.

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

### -EncryptionAtHost
Die EncryptionAtHost-Eigenschaft kann vom Benutzer in der Anforderung verwendet werden, um die Hostverschlüsselung für den Skalierungssatz des virtuellen Computers oder virtuellen Computers zu aktivieren oder zu deaktivieren. Dadurch wird die Verschlüsselung für alle Datenträger aktiviert, einschließlich des Ressourcen-/Temp-Datenträgers beim Host selbst. Standard: Die Verschlüsselung beim Host wird deaktiviert, es sei denn, diese Eigenschaft ist für die Ressource auf true festgelegt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priorität
Die Priorität für den virtuellen Computer.  Nur unterstützte Werte sind "Normal", "Spot" und "Niedrig".
"Regular" ist für einen normalen virtuellen Computer.
"Spot" ist für virtuelle Spotcomputer.
"Low" ist auch für virtuelle Spotcomputer, wird aber durch "Spot" ersetzt. Verwenden Sie "Spot" statt "Niedrig".

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
Die Ressourcen-ID der Näherungsgruppe, die für diesen virtuellen Computer verwendet werden soll.

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

### -Tags
Die Tags, die der Ressource angefügt sind.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Gibt einen Namen für den virtuellen Computer an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSize
Gibt die Größe für den virtuellen Computer an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmssId
Die ID des Skalierungssets für virtuelle Computer

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

### -Zone
Gibt die Liste der Verfügbarkeitszonen für den virtuellen Computer an. Die zulässigen Werte hängen von den Funktionen der Region ab. Zulässige Werte sind normalerweise 1,2,3.

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

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

### System.String[]

### System.Collections.Hashtable

### System.Management.Automation.SwitchParameter

## AUSGABEN

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## NOTIZEN

## VERWANDTE LINKS

[Update-AzVM](./Update-AzVM.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)

[Set-AzVMSourceImage](./Set-AzVMSourceImage.md)

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)


