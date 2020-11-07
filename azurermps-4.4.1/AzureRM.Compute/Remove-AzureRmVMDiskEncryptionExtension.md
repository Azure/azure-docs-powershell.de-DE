---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiskEncryptionExtension.md
ms.openlocfilehash: 3fc1424fe2cde9b2137ca6925a8788fa5c8a8139
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662276"
---
# Remove-AzureRmVMDiskEncryptionExtension

## Synopsis
Entfernt die Datenträger Verschlüsselungs Erweiterung von einem virtuellen Computer.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Remove-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureRmVMDiskEncryptionExtension** entfernt die Datenträger Verschlüsselungs Erweiterung von einem virtuellen Computer.
Wenn kein Erweiterungsname angegeben wird, entfernt dieses Cmdlet die Erweiterung mit dem Standardnamen AzureDiskEncryption für virtuelle Computer, die das Windows-Betriebssystem oder AzureDiskEncryptionForLinux für Linux-basierte virtuelle Maschinen ausführen.
Dieses Cmdlet deaktiviert die Verschlüsselung auf dem virtuellen Computer nicht.
Sie entfernt die Erweiterung und die zugehörige Erweiterungskonfiguration vom virtuellen Computer.

## Beispiele

### Beispiel 1: Entfernen Sie die Datenträger Verschlüsselungs Erweiterung von einem virtuellen Computer.
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

Dieser Befehl entfernt die Erweiterung mit dem Standardnamen AzureDiskEncryption für einen virtuellen Computer, auf dem das Windows-Betriebssystem oder AzureDiskEncryptionForLinux für Linux basierter virtueller Computer mit dem Namen MyTestVM ausgeführt wird.

### Beispiel 2: Entfernen einer bestimmten Datenträger Verschlüsselungs Erweiterung von einem virtuellen Computer
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

Dieser Befehl entfernt die Verschlüsselungs Erweiterung mit dem Namen MyDiskEncryptionExtension vom virtuellen Computer mit dem Namen MyTestVM.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Mit dem Set-AzureRmVMDiskEncryptionExtension-Cmdlet wird dieser Name auf AzureDiskEncryption für virtuelle Computer festgelegt, auf denen das Windows-Betriebssystem und AzureDiskEncryptionForLinux für Linux-virtuelle Computer ausgeführt werden.
Geben Sie diesen Parameter nur an, wenn Sie den Standardnamen im Cmdlet " **Satz-AzureRmVMDiskEncryptionExtension** " geändert oder einen anderen Ressourcennamen in einer Ressourcen-Manager-Vorlage verwendet haben.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureRmVMDiskEncryptionStatus](./Get-AzureRmVMDiskEncryptionStatus.md)

[Satz-AzureRmVMDiskEncryptionExtension](./Set-AzureRmVMDiskEncryptionExtension.md)


