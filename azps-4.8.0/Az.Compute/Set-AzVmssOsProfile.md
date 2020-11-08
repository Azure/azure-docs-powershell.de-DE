---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 71bd8ca26755118a4bb9c075ae89bad765922f3d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010212"
---
# Set-AzVmssOsProfile

## Synopsis
Legt die Profileigenschaften des VMSS-Betriebssystems fest.

## Syntax

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Set-AzVmssOsProfile** werden die Eigenschaften des virtuellen Computers für das Betriebssystem festgelegt.

## Beispiele

### Beispiel 1: Einrichten der Profileigenschaften des Betriebssystems für ein VMSS
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

Mit diesem Befehl werden die Profileigenschaften des Betriebssystems für die virtuellen Computer festgelegt, die zum VMSS mit dem Namen ContosoVMSS gehören.
Der Befehl legt das Präfix für den Computernamen für alle Instanzen des virtuellen Computers im VMSS fest, um den Benutzernamen und das Kennwort des Administrators zu testen und bereitzustellen.

## Parameter

### -AdditionalUnattendContent
Gibt ein unbeaufsichtigtes Inhaltsobjekt an.
Sie können die Add-AzVMAdditionalUnattendContent verwenden, um das Objekt zu erstellen.

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
Gibt das Administratorkennwort an, das für alle Instanzen des virtuellen Computers in der VMSS verwendet werden soll.

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

### -Nation aus AdminUsername
Gibt den Namen des Administratorkontos an, das für alle Instanzen des virtuellen Computers in VMSS verwendet werden soll. <br>
**Nur Windows-Einschränkungen:** Kann nicht beendet werden \" .\" <br>
Nicht **zulässige Werte:** \" Administrator, Administrator \" \" \" , \" Benutzer \" , \" Benutzer1 \" , \" Test \" , \" User2 \" , \" test1 \" , \" user3 \" , \" Admin1 \" , \" 1 \" , \" 123 \" , \" a \" , \" ACTUser \" , \" adm \" , \" admin2 \" , \" ASPNET \" , \" Backup \" , \" Console \" , \" David \" , \" Guest \" , \" John \" , \" Owner \" , \" root \" , \" Server \" , \" SQL \" , \" Support \" , \" Support_388945a0 \" , \" sys \" , \" test2 \" , \" test3 \" , \" benutzer4 \" , \" user5 \" . <br>
**Minimale Länge (Linux):** 1 Zeichen <br>
**Max-length (Linux):** 64 Zeichen <br>
**Max-length (Windows):** 20 Zeichen  <br>
<li> Informationen zum root-Zugriff auf die Linux-VM finden Sie unter [Verwenden von root-Privilegien auf virtuellen Linux-Computern in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).<br>
<li> Eine Liste der integrierten Systembenutzer unter Linux, die nicht in diesem Feld verwendet werden sollten, finden Sie unter [Auswählen von Benutzernamen für Linux auf Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).

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
Gibt das Präfix für den Computernamen für alle Instanzen des virtuellen Computers im VMSS an.
Computer Namen müssen 1 bis 15 Zeichen lang sein.

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
Gibt eine codierte Base-64-Zeichenfolge mit benutzerdefinierten Daten an.
Dies wird in einem binären Array dekodiert, das als Datei auf dem virtuellen Computer gespeichert ist.
Die maximale Länge des binären Arrays beträgt 65535 Bytes. <br>
Informationen zum Verwenden von Cloud-init für Ihre VM finden Sie unter [Verwenden von Cloud-init zum Anpassen einer Linux-VM während der Erstellung](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).

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
Gibt die Windows-Remote Verwaltung (WinRM)-Listener an.
Dies ermöglicht die Remote-Windows PowerShell.
Sie können das Add-AzVmssWinRMListener-Cmdlet verwenden, um den Listener zu erstellen.

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
Gibt das Secure Shell (SSH)-Objekt für öffentliche Schlüssel an.
Sie können das Add-AzVMSshPublicKey-Cmdlet verwenden, um das Objekt zu erstellen.

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
Gibt das Secrets-Objekt an, das die Zertifikat Verweise enthält, die auf dem virtuellen Computer platziert werden sollen.
Sie können das Add-AzVmssSecret-Cmdlet verwenden, um das Secrets-Objekt zu erstellen.

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
Gibt die Zeitzone des virtuellen Computers an. z.b. \" Pacific Normalzeit \" . <br>
Mögliche Werte können [TimeZoneInfo.ID](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) -Wert aus Zeitzonen sein, die von [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)zurückgegeben werden.

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
Sie können das New-AzVmssConfig-Cmdlet verwenden, um das Objekt zu erstellen.

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
Gibt an, ob der Virtual Machine-Agent auf den virtuellen Computern im VMSS bereitgestellt werden soll.

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
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet

### System. String

### System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

### Microsoft. Azure. Management. Compute. Models. AdditionalUnattendContent []

### Microsoft. Azure. Management. Compute. Models. WinRMListener []

### Microsoft. Azure. Management. Compute. Models. SshPublicKey []

### Microsoft. Azure. Management. Compute. Models. VaultSecretGroup []

## Ausgaben

### Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet

## Notizen

## Verwandte Links

[Add-AzVMAdditionalUnattendContent](./Add-AzVMAdditionalUnattendContent.md)

[Add-AzVmssWinRMListener](./Add-AzVmssWinRMListener.md)

[Add-AzVMSshPublicKey](./Add-AzVMSshPublicKey.md)

[Add-AzVmssSecret](./Add-AzVmssSecret.md)

[Neu – AzVmssConfig](./New-AzVmssConfig.md)


