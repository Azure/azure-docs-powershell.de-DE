---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 4c9e66d751b5465f4112b7cb6d971022e43fa023
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008607"
---
# Remove-AzVMDiskEncryptionExtension

## Synopsis
Entfernt die Datenträger Verschlüsselungs Erweiterung von einem virtuellen Computer.

## Syntax

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzVMDiskEncryptionExtension** entfernt die Datenträger Verschlüsselungs Erweiterung und die zugehörige Erweiterungskonfiguration von einem virtuellen Computer. Wenn kein Erweiterungsname angegeben wird, entfernt dieses Cmdlet die Erweiterung mit dem Standardnamen AzureDiskEncryption für virtuelle Computer, die das Windows-Betriebssystem oder AzureDiskEncryptionForLinux für Linux-basierte virtuelle Maschinen ausführen. 

Bei diesem Cmdlet tritt ein Fehler auf, wenn die Verschlüsselung auf dem virtuellen Computer nicht zuerst deaktiviert wurde.  Wenn Sie die Verschlüsselung auf einem virtuellen Computer deaktivieren möchten, verwenden Sie [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md). 

## Beispiele

### Beispiel 1: Entfernen Sie die Datenträger Verschlüsselungs Erweiterung von einem virtuellen Computer.
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

Dieser Befehl entfernt die Erweiterung mit dem Standardnamen AzureDiskEncryption für einen virtuellen Computer, auf dem das Windows-Betriebssystem oder AzureDiskEncryptionForLinux für Linux basierter virtueller Computer mit dem Namen MyTestVM ausgeführt wird.

### Beispiel 2: Entfernen einer bestimmten Datenträger Verschlüsselungs Erweiterung von einem virtuellen Computer
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

Dieser Befehl entfernt die Verschlüsselungs Erweiterung mit dem Namen MyDiskEncryptionExtension vom virtuellen Computer mit dem Namen MyTestVM.

## Parameter

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

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

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

### -Name
Gibt den Namen der Azure Resource Manager-Ressource an, die die Erweiterung darstellt.
Mit dem Set-AzVMDiskEncryptionExtension-Cmdlet wird dieser Name auf AzureDiskEncryption für virtuelle Computer festgelegt, auf denen das Windows-Betriebssystem und AzureDiskEncryptionForLinux für Linux-virtuelle Computer ausgeführt werden.
Geben Sie diesen Parameter nur an, wenn Sie den Standardnamen im Cmdlet " **Satz-AzVMDiskEncryptionExtension** " geändert oder einen anderen Ressourcennamen in einer Ressourcen-Manager-Vorlage verwendet haben.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nowait
Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück. Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.

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
Gibt den Namen der Ressourcengruppe für den virtuellen Computer an.

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

### -VMName
Gibt den Namen der virtuellen Maschine an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

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

## Ausgaben

### Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse

## Notizen

## Verwandte Links

[Get-AzVMDiskEncryptionStatus](./Get-AzVMDiskEncryptionStatus.md)

[Satz-AzVMDiskEncryptionExtension](./Set-AzVMDiskEncryptionExtension.md)


