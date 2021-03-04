---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e7a86b191687f72cb538fb017a904890e4958d50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920600"
---
# Update-AzVM

## SYNOPSIS
Aktualisiert den Zustand eines virtuellen Azure-Computers.

## SYNTAX

### ResourceGroupNameParameterSetName (Standard)
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### IdParameterSetName
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Update-AzVM-Cmdlet** aktualisiert den Zustand eines virtuellen Azure-Computers auf den Zustand eines virtuellen Computerobjekts.

## BEISPIELE

### Beispiel 1: Aktualisieren eines virtuellen Computers
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

Mit diesem Befehl wird der virtuelle Computer $VirtualMachine In ResourceGroup11 aktualisiert.
Der Befehl aktualisiert ihn mithilfe des in der Variablen $VirtualMachine virtuellen Computerobjekts.
Zum Abrufen eines Virtuellen Computerobjekts verwenden Sie **das Get-AzVM-Cmdlet.**

## PARAMETER

### -AsJob
Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -EncryptionAtHost
Die EncryptionAtHost-Eigenschaft kann vom Benutzer in der Anforderung verwendet werden, um die Hostverschlüsselung für den Skalierungssatz des virtuellen Computers oder virtuellen Computers zu aktivieren oder zu deaktivieren. Dadurch wird die Verschlüsselung für alle Datenträger aktiviert, einschließlich des Ressourcen-/Temp-Datenträgers beim Host selbst. 

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

### -ID
Gibt die Ressourcen-ID des virtuellen Computers an.

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdentityId
Gibt die Liste der Benutzeridentitäten an, die dem virtuellen Computer zugeordnet sind.
Die Benutzeridentitätsverweise werden ARM Ressourcen-IDs im Formular "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" angezeigt.

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
Der Für den virtuellen Computer verwendete Identitätstyp. Gültige Werte sind SystemAssigned, UserAssigned, SystemAssignedUserAssigned und None.

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

### -NoWait
Startet den Vorgang und gibt sofort zurück, bevor der Vorgang abgeschlossen ist. Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.

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

### -ProximityPlacementGroupId
Die Ressourcen-ID der Näherungsgruppe, die für diesen virtuellen Computer verwendet werden soll.

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
Gibt den Namen der Ressourcengruppe des virtuellen Computers an.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Gibt an, dass die Ressourcen und Ressourcengruppen mit einer Reihe von Namen-Wert-Paaren markiert werden können.
Durch das Hinzufügen von Tags zu Ressourcen können Sie Ressourcen über Ressourcengruppen hinweg gruppieren und eigene Ansichten erstellen.
Jede Ressource oder Ressourcengruppe kann maximal 15 Tags haben.

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

### -UltraSSDEnabled
Das -Kennzeichen, mit dem eine Funktion aktiviert oder deaktiviert wird, um eine oder mehrere verwaltete Datenträger mit UltraSSD_LRS Speicherkontotyp auf der VM zu verwenden.
Verwaltete Datenträger mit Speicherkontotyp UltraSSD_LRS einem virtuellen Computer nur hinzugefügt werden, wenn diese Eigenschaft aktiviert ist.

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

### -VM
Gibt ein Objekt des lokalen virtuellen Computers an.
Zum Abrufen eines Virtuellen Computerobjekts verwenden Sie das Get-AzVM Cmdlet.
Dieses Objekt des virtuellen Computers enthält den aktualisierten Zustand für den virtuellen Computer.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```


### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.Boolean

## AUSGABEN

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## NOTIZEN

## VERWANDTE LINKS

[Get-AzVM](./Get-AzVM.md)

[New-AzVM](./New-AzVM.md)

[Remove-AzVM](./Remove-AzVM.md)

[Neustart-AzVM](./Restart-AzVM.md)

[Start-AzVM](./Start-AzVM.md)

[Stopp-AzVM](./Stop-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)


