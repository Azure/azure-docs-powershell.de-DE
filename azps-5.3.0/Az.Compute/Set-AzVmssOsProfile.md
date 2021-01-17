---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 71bd8ca26755118a4bb9c075ae89bad765922f3d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470829"
---
# Set-AzVmssOsProfile

## SYNOPSIS
Legt die Profileigenschaften des Betriebssystems VMSS fest.

## SYNTAX

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Set-AzVmssOsProfile"** legt die Profileigenschaften des Betriebssystems "Virtual Machine Scale Set" fest.

## BEISPIELE

### Beispiel 1: Festlegen der Betriebssystemprofileigenschaften für eine VMSS
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

Mit diesem Befehl werden die Profileigenschaften des Betriebssystems für die virtuellen Computer festgelegt, die zu den VMSS mit dem Namen ContosoVMSS gehören.
Der Befehl legt das Computernamenpräfix für alle Instanzen des virtuellen Computers in VMSS auf "Test" fest und stellt den Benutzernamen und das Kennwort des Administrators zur Verfügung.

## PARAMETERS

### -AdditionalUnattendContent
Gibt ein unbeaufsichtigtes Inhaltsobjekt an.
Sie können die Add-AzVMAdditionalUnattendContent zum Erstellen des Objekts verwenden.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminPassword
Gibt das Administratorkennwort an, das für alle Instanzen des virtuellen Computers in vmSS verwendet werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminUsername
Gibt den Administratorkontonamen an, der für alle Instanzen des virtuellen Computers in vmSS verwendet werden soll. <br>
**Einschränkung nur für Windows:** Kann nicht enden mit \" .\" <br>
**Unzulässige Werte:** \" \"Administrator, \" \" \" \" Administrator, Benutzer, \" \" \" Benutzer1, \" Test, \" \" Benutzer2, \" \" Test1, \" \" Benutzer3, \" \" Administrator1, \" \" 1, \" 123 \" , a , \" \" \" Actuser, \" \" \" Adm, \" \" \" Admin2, \" Aspnet, \" \" Sicherung, \" \" Konsole, \" \" David, \" \" Gast, \" \" John, \" \" Besitzer, \" \" Stamm, \" \" Server, \" \" SQL, \" \" Support, \" support_388945a0 , sys \" , \" \" \" \" Test2, \" \" Test3, \" \" Benutzer4, \" \" Benutzer5. <br>
**Mindestlänge (Linux):** 1 Zeichen <br>
**Maximale Länge (Linux):** 64 Zeichen <br>
**Maximale Länge (Windows):** 20 Zeichen  <br>
<li> Informationen zum Stammzugriff auf die Linux VM finden Sie unter "Verwenden von Stammberechtigungen [auf virtuellen Linux-Computern in Azure".](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)<br>
<li> Eine Liste der integrierten Systembenutzer unter Linux, die in diesem Feld nicht verwendet werden sollten, finden Sie unter Auswählen von Benutzernamen für [Linux auf Azure.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)

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

### -ComputerNamePrefix
Gibt das Computernamenpräfix für alle Instanzen virtueller Computer in der VMSS an.
Computernamen müssen 1 bis 15 Zeichen lang sein.

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
Position: 4
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

### -LinuxConfigurationDisablePasswordAuthentication
Gibt an, dass dieses Cmdlet die Kennwortauthentifizierung deaktiviert.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Listener
Gibt die Windows Remote Management (WinRM)-Listener an.
Dies ermöglicht Remote-Windows PowerShell.
Sie können das cmdlet Add-AzVmssWinRMListener zum Erstellen des Listeners verwenden.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.WinRMListener[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicKey
Gibt das öffentliche Schlüsselobjekt der Secure Shell (SSH) an.
Sie können das cmdlet Add-AzVMSshPublicKey zum Erstellen des Objekts verwenden.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.SshPublicKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Secret
Gibt das geheime Objekt an, das die Zertifikatverweise enthält, die auf dem virtuellen Computer platzieren werden.
Sie können das cmdlet Add-AzVmssSecret zum Erstellen des geheimen Objekts verwenden.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeZone
Gibt die Zeitzone des virtuellen Computers an. z. B. \" Pacific Standard \" Time. <br>
Mögliche Werte können als [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) zeitzonen verwendet werden, die von ["TimeZoneInfo.GetSystemTimeZones" zurückgegeben werden.](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Gibt das "VMSS"-Objekt an.
Sie können das New-AzVmssConfig zum Erstellen des Objekts verwenden.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WindowsConfigurationEnableAutomaticUpdate
Gibt an, ob die virtuellen Computer in VMSS für automatische Updates aktiviert sind.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WindowsConfigurationProvisionVMAgent
Gibt an, ob der Agent für virtuelle Computer auf den virtuellen Computern auf der VMSS bereitgestellt werden soll.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
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

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

### System.String

### System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]

### Microsoft.Azure.Management.Compute.Models.WinRMListener[]

### Microsoft.Azure.Management.Compute.Models.SshPublicKey[]

### Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]

## AUSGABEN

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Add-AzVMAdditionalUnattendContent](./Add-AzVMAdditionalUnattendContent.md)

[Add-AzVmssWinRMListener](./Add-AzVmssWinRMListener.md)

[Add-AzVMSshPublicKey](./Add-AzVMSshPublicKey.md)

[Add-AzVmssSecret](./Add-AzVmssSecret.md)

[New-AzVmssConfig](./New-AzVmssConfig.md)


