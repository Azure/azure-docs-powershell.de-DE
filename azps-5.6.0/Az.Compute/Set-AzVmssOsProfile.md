---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 046812a0339a0dd33df140f29e00ec8b882c91cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922059"
---
# Set-AzVmssOsProfile

## SYNOPSIS
Legt die Profileigenschaften des VMSS-Betriebssystems fest.

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
Das **Cmdlet Set-AzVmssOsProfile** legt die Profileigenschaften des Betriebssystems für die Skalierungssatz für virtuelle Computer fest.

## BEISPIELE

### Beispiel 1: Festlegen der Eigenschaften des Betriebssystemprofils für einen VMSS
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

Mit diesem Befehl werden die Profileigenschaften des Betriebssystems für die virtuellen Computer festgelegt, die zum VMSS mit dem Namen ContosoVMSS gehören.
Der Befehl legt das Computernamenpräfix für alle Instanzen virtueller Computer im VMSS auf Testen fest und stellt den Benutzernamen und das Kennwort des Administrators zur Verfügung.

## PARAMETER

### -AdditionalUnattendContent
Gibt ein unbeaufsichtigtes Inhaltsobjekt an.
Sie können die Add-AzVMAdditionalUnattendContent verwenden, um das -Objekt zu erstellen.

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
Gibt das Administratorkennwort an, das für alle Instanzen des virtuellen Computers im VMSS verwendet werden soll.

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
Gibt den Administratorkontonamen an, der für alle Instanzen des virtuellen Computers im VMSS verwendet werden soll. <br>
**Einschränkung nur für Windows:** Kann nicht in \" enden.\" <br>
**Unzulässige Werte:** \" Administrator , Administrator , Benutzer , Benutzer1 , Test \" \" , \" \" \" \" \" \" \" \" Benutzer2 , \" \" Test1 , \" \" Benutzer3 , \" \" Admin1 , \" \" 1 , \" \" 123 \" , a , \" \" \" actuser \" , \" adm , \" \" admin2 , \" \" aspnet , backup \" , console , david , guest , john \" , owner , root \" , server , \" sql , \" support \" , \" \" support_388945a0 \" , sys \" \" \" \" \" \" , \" \" \" \" \" \" \" \" \" \" \" test2 , \" \" test3 , \" \" user4 , \" \" user5 \" . <br>
**Mindestlänge (Linux):** 1 Zeichen <br>
**Max. Länge (Linux):** 64 Zeichen <br>
**Max. Länge (Windows):** 20 Zeichen  <br>
<li> Informationen zum Stammzugriff auf die Linux-VM finden Sie unter Verwenden von Stammberechtigungen auf [virtuellen Linux-Computern in Azure.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)<br>
<li> Eine Liste der integrierten Systembenutzer unter Linux, die in diesem Feld nicht verwendet werden sollten, finden Sie unter Auswählen von Benutzernamen für [Linux in Azure.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)

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
Gibt das Computernamenpräfix für alle Instanzen des virtuellen Computers im VMSS an.
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
Informationen zur Verwendung von cloud-init für Ihre VM finden Sie unter Verwenden von cloud-init zum Anpassen [einer Linux-VM während der Erstellung.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)

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
Dies ermöglicht remote Windows PowerShell.
Sie können das cmdlet Add-AzVmssWinRMListener verwenden, um den Listener zu erstellen.

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
Gibt das Öffentliche Schlüsselobjekt (Secure Shell, SSH) an.
Sie können das cmdlet Add-AzVMSshPublicKey verwenden, um das -Objekt zu erstellen.

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
Gibt das Secrets-Objekt an, das die Zertifikatverweise enthält, die auf dem virtuellen Computer zu platzieren sind.
Sie können das Add-AzVmssSecret verwenden, um das Secrets-Objekt zu erstellen.

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
Gibt die Zeitzone des virtuellen Computers an. z. B. \" Pacific Standard Time \" . <br>
Mögliche Werte können [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) aus Zeitzonen angezeigt werden, die von [TimeZoneInfo.GetSystemTimeZones zurückgegeben werden.](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)

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
Gibt das VMSS-Objekt an.
Sie können das cmdlet New-AzVmssConfig verwenden, um das -Objekt zu erstellen.

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
Gibt an, ob die virtuellen Computer im VMSS für automatische Updates aktiviert sind.

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
Gibt an, ob der Virtuelle Computer-Agent auf den virtuellen Computern im VMSS bereitgestellt werden soll.

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

### -Bestätigen
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

### -WhatIf
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

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

## NOTIZEN

## VERWANDTE LINKS

[Add-AzVMAdditionalUnattendContent](./Add-AzVMAdditionalUnattendContent.md)

[Add-AzVmssWinRMListener](./Add-AzVmssWinRMListener.md)

[Add-AzVMSshPublicKey](./Add-AzVMSshPublicKey.md)

[Add-AzVmssSecret](./Add-AzVmssSecret.md)

[New-AzVmssConfig](./New-AzVmssConfig.md)


