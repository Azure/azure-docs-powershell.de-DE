---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: c22e1a09f20eca32cb21056ae45334f0d55ce14b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177699"
---
# Set-AzVMOperatingSystem

## Synopsis
Legt die Betriebssystemeigenschaften für einen virtuellen Computer fest.

## Syntax

### Windows (Standard)
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### WindowsWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDisableVMAgent
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### WindowsDisableVMAgentWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Linux
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzVMOperatingSystem** " legt die Betriebssystemeigenschaften für einen virtuellen Computer fest.
Sie können Anmeldeinformationen, Computername und Typ des Betriebssystems angeben.

## Beispiele

### Beispiel 1: Einrichten von Betriebssystemeigenschaften für eine neue virtuelle Maschine
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

Der erste Befehl wandelt ein Kennwort in eine sichere Zeichenfolge um und speichert es dann in der $SecurePassword-Variablen.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help ConvertTo-SecureString` .
Mit dem zweiten Befehl werden die Anmeldeinformationen für den Benutzer FullerP und das in $SecurePassword gespeicherte Kennwort erstellt, und die Anmeldeinformationen werden dann in der $Credential Variablen gespeichert.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help New-Object` .
Der dritte Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailabilitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.
Der vierte Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.
Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.
Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.
In den nächsten vier Befehlen werden Variablenwerte zugewiesen, die Sie im folgenden Befehl verwenden können.
Da Sie diese Zeichenfolgen direkt im Befehl " **Satz-AzVMOperatingSystem** " angeben können, wird dieser Ansatz nur zur Lesbarkeit verwendet.
Sie können jedoch einen solchen Ansatz in Skripten verwenden.
Mit dem letzten Befehl werden die Betriebssystemeigenschaften für den virtuellen Computer festgelegt, der in $VirtualMachine gespeichert ist.
Der Befehl verwendet die in $Credential gespeicherten Anmeldeinformationen.
Der Befehl verwendet für einige Parameter in vorherigen Befehlen zugewiesene Variablen.

## Parameter

### -Computername
Gibt den Namen des Computers an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Anmeldeinformationen
Gibt den Benutzernamen und das Kennwort für den virtuellen Computer als **PSCredential** -Objekt an.
Verwenden Sie zum Abrufen von Anmeldeinformationen das Get-Credential-Cmdlet.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomData
Gibt eine codierte Base-64-Zeichenfolge mit benutzerdefinierten Daten an.
Dies wird in einem binären Array dekodiert, das als Datei auf dem virtuellen Computer gespeichert ist.
Die maximale Länge des binären Arrays beträgt 65535 Bytes.<br>
**Hinweis: übergeben Sie keine Geheimnisse oder Kennwörter in der CustomData-Eigenschaft.**<br>
Diese Eigenschaft kann nicht aktualisiert werden, nachdem die VM erstellt wurde. <br>
CustomData wird an den virtuellen Computer übergeben, der als Datei gespeichert werden soll, weitere Informationen finden Sie unter [benutzerdefinierte Daten auf Azure VMS](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/) <br>
Informationen zum Verwenden von Cloud-init für Ihre Linux-VM finden Sie unter [Verwenden von Cloud-init zum Anpassen einer Linux-VM während der Erstellung](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init) .

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

### -DisablePasswordAuthentication
Gibt an, dass dieses Cmdlet die Kennwortauthentifizierung deaktiviert.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisableVMAgent
Bereitstellen des VM-Agents deaktivieren.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutoUpdate
Gibt an, dass dieses Cmdlet die automatische Aktualisierung aktiviert.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
Gibt an, dass der Typ des Betriebssystems Linux ist.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PatchMode
Gibt den Modus des in-Guest-Patches für IaaS Virtual Machine an.<br><br>
Mögliche Werte:<br>
**Manuell** : Sie steuern die Anwendung von Patches auf einem virtuellen Computer. Dazu können Sie Patches manuell innerhalb des VM anwenden. In diesem Modus sind automatische Updates deaktiviert; die Eigenschaft WindowsConfiguration. enableAutomaticUpdates muss "falsch" sein.<br>
**AutomaticByOS** – die virtuelle Maschine wird automatisch vom Betriebssystem aktualisiert. Die Eigenschaft WindowsConfiguration. enableAutomaticUpdates muss true sein. <br >
**AutomaticByPlatform** – die virtuelle Maschine wird automatisch vom Betriebssystem aktualisiert. Die Eigenschaften provisionVMAgent und WindowsConfiguration. enableAutomaticUpdates müssen wahr sein.

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProvisionVMAgent
Gibt an, dass für die Einstellungen der Virtual Machine-Agent auf dem virtuellen Computer installiert werden muss.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeZone
Gibt die Zeitzone des virtuellen Computers an. z.b. \" Pacific Normalzeit \" . <br>
Mögliche Werte können [TimeZoneInfo.ID](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) -Wert aus Zeitzonen sein, die von [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)zurückgegeben werden.

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Gibt das Objekt des lokalen virtuellen Computers an, auf dem Betriebssystemeigenschaften festgelegt werden sollen.
Verwenden Sie das Get-AzVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.
Erstellen Sie ein Objekt für einen virtuellen Computer mithilfe des New-AzVMConfig-Cmdlets.

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

### -Windows
Gibt an, dass der Typ des Betriebssystems Windows ist.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMCertificateUrl
Gibt den URI eines WinRM-Zertifikats an.
Dieser muss in einem schlüsseltresor gespeichert werden.

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMHttp
Gibt an, dass dieses Betriebssystem http WinRM verwendet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMHttps
Gibt an, dass dieses Betriebssystem HTTPS WinRM verwendet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

### System. Management. Automation. Switchparameter

### System. String

### System. Management. Automation. PSCredential

### System. Uri

## Ausgaben

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

## Notizen

## Verwandte Links

[Get-AzVM](./Get-AzVM.md)

[Neu – AzVMConfig](./New-AzVMConfig.md)


