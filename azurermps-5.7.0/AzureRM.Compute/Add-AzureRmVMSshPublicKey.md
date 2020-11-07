---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
ms.openlocfilehash: b4cbc3ba7dd90d2810c4833fe1b74c13541fcb7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662593"
---
# Add-AzureRmVMSshPublicKey

## Synopsis
Fügt die öffentlichen Schlüssel für SSH für einen virtuellen Computer hinzu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Add-AzureRmVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Add-AzureRmVMSshPublicKey** fügt die öffentlichen Schlüssel hinzu, die Sie zum Herstellen einer Verbindung mit einem virtuellen Computer über Secure Shell (SSH) verwenden können.

## Beispiele

### Beispiel 1: Hinzufügen eines öffentlichen Schlüssels zu einem virtuellen Computer
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzureRmVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 mit dem Cmdlet **Get-AzureRmVM** ab.
Der Befehl speichert den virtuellen Computer in der $VirtualMachine-Variablen.

Mit dem zweiten Befehl wird der öffentliche Schlüssel an der Position auf VirtualMachine07 hinzugefügt, die vom path-Parameter angegeben wird.

## Parameter

### -KeyData
Gibt eine Basis 64-Codierung eines öffentlichen Schlüssels an.
Sie können mithilfe von ssh eine Verbindung mit einem virtuellen Computer herstellen oder mithilfe des Schlüssels, den dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Gibt den vollständigen Pfad einer Datei auf dem virtuellen Computer an, in dem dieses Cmdlet den öffentlichen SSH-Schlüssel speichert.
Wenn die Datei bereits vorhanden ist, hängt dieses Cmdlet den Schlüssel an die Datei an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Gibt das Objekt des virtuellen Computers an, das von diesem Cmdlet geändert wird.
Verwenden Sie das Cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) , um ein Objekt eines virtuellen Computers zu erhalten.
Sie können das Cmdlet [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) verwenden, um ein Objekt eines virtuellen Computers zu erstellen.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Neu – AzureRmVMConfig](./New-AzureRmVMConfig.md)
