---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: dfbb993e0753ab536fa1daf54024facf8fed1624
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003652"
---
# Add-AzVMSshPublicKey

## Synopsis
Fügt die öffentlichen Schlüssel für SSH für einen virtuellen Computer hinzu.

## Syntax

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Add-AzVMSshPublicKey** fügt die öffentlichen Schlüssel hinzu, die Sie zum Herstellen einer Verbindung mit einem virtuellen Linux-Computer über Secure Shell (SSH) verwenden können.

## Beispiele

### Beispiel 1: Hinzufügen eines öffentlichen Schlüssels zu einem virtuellen Computer
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 mit dem Cmdlet **Get-AzVM** ab.
Der Befehl speichert den virtuellen Computer in der $VirtualMachine-Variablen.
Mit dem zweiten Befehl wird der öffentliche Schlüssel an der Position auf VirtualMachine07 hinzugefügt, die vom path-Parameter angegeben wird.

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

### -KeyData
Gibt eine Basis 64-Codierung eines öffentlichen Schlüssels an.
Sie können eine Verbindung mit einem virtuellen Linux-Computer herstellen, indem Sie SSH verwenden oder den Schlüssel verwenden, den dieser Parameter angibt.

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

### -Path
Gibt den vollständigen Pfad einer Datei auf dem virtuellen Computer an, in dem dieses Cmdlet den öffentlichen SSH-Schlüssel speichert.
Wenn die Datei bereits vorhanden ist, hängt dieses Cmdlet den Schlüssel an die Datei an.

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

### -VM
Gibt das Objekt des virtuellen Computers an, das von diesem Cmdlet geändert wird.
Verwenden Sie das Cmdlet [Get-AzVM](./Get-AzVM.md) , um ein Objekt eines virtuellen Computers zu erhalten.
Sie können das Cmdlet [New-AzVMConfig](./New-AzVMConfig.md) verwenden, um ein Objekt eines virtuellen Computers zu erstellen.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

## Notizen

## Verwandte Links

[Get-AzVM](./Get-AzVM.md)

[Neu – AzVMConfig](./New-AzVMConfig.md)
