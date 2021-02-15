---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: e17b495147c308d20d6d5b950914d26ce56a5706
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166585"
---
# Add-AzVMSshPublicKey

## SYNOPSIS
Fügt die öffentlichen Schlüssel für SSH für einen virtuellen Computer hinzu, wenn nur die VM erstellt wird.

## SYNTAX

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Add-AzVMSshPublicKey"** fügt die öffentlichen Schlüssel hinzu, die Sie verwenden können, um über SSH (Secure Shell) eine Verbindung mit einem virtuellen Linux-Computer herzustellen. Dies kann nach der Erstellung von VM nicht verwendet werden. Wenn Sie versuchen, dies nach der Erstellung der VM ohne Update-AzVM zu verwenden, tritt kein Fehler auf. Wenn Sie den Befehl mit Update-AzVM verwenden, tritt ein Fehler auf.

## BEISPIELE

### Beispiel 1: Hinzufügen eines öffentlichen Schlüssels zu einem virtuellen Computer
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

Der erste Befehl ruft den virtuellen Computer "VirtualMachine07" mithilfe des **Get-AzVM-Cmdlets** ab.
Der Befehl speichert den virtuellen Computer in der $VirtualMachine Variable.
Der zweite Befehl fügt den öffentlichen Schlüssel dem vom Parameter "Path" angegebenen Speicherort in VirtualMachine07 hinzu.

## PARAMETERS

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

### -KeyData
Gibt die Basis-64-Codierung eines öffentlichen Schlüssels an.
Sie können eine Verbindung mit einem virtuellen Linux-Computer herstellen, indem Sie SSH oder den Schlüssel verwenden, den dieser Parameter angibt.

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
Gibt den vollständigen Pfad einer Datei auf dem virtuellen Computer an, auf dem dieses Cmdlet den öffentlichen SSH-Schlüssel speichert.
Wenn die Datei bereits vorhanden ist, fügt dieses Cmdlet den Schlüssel an die Datei an.

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
Verwenden Sie das [Get-AzVM-Cmdlet,](./Get-AzVM.md) um ein Objekt des virtuellen Computers zu erhalten.
Sie können das [Cmdlet "New-AzVMConfig"](./New-AzVMConfig.md) verwenden, um ein Objekt für einen virtuellen Computer zu erstellen.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)
