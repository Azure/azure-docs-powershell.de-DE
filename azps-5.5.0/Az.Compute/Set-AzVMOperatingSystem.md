---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: c22e1a09f20eca32cb21056ae45334f0d55ce14b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171096"
---
# Set-AzVMOperatingSystem

## SYNOPSIS
Legt die Betriebssystemeigenschaften für einen virtuellen Computer fest.

## SYNTAX

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

## BESCHREIBUNG
Das **Cmdlet "Set-AzVMOperatingSystem"** legt die Betriebssystemeigenschaften für einen virtuellen Computer fest.
Sie können Anmeldeinformationen, den Computernamen und den Betriebssystemtyp angeben.

## BEISPIELE

### Beispiel 1: Festlegen von Betriebssystemeigenschaften für neue virtuelle Computer
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

Der erste Befehl konvertiert ein Kennwort in eine sichere Zeichenfolge und speichert es dann in $SecurePassword Variable.
Weitere Informationen erhalten Sie, wenn Sie " `Get-Help ConvertTo-SecureString` eingeben" aus.
Der zweite Befehl erstellt eine Anmeldeinformationen für den Benutzer "FullerP" und das in $SecurePassword gespeicherte Kennwort und speichert die Anmeldeinformationen dann in der $Credential Variable.
Weitere Informationen erhalten Sie, wenn Sie " `Get-Help New-Object` eingeben" aus.
Der dritte Befehl ruft den Verfügbarkeitssatz namens "AvailabilitySet03" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $AvailabilitySet Variable.
Der vierte Befehl erstellt ein Objekt des virtuellen Computers und speichert es dann in der $VirtualMachine Variable.
Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.
Der virtuelle Computer gehört zu dem Verfügbarkeitssatz, der auf der $AvailabilitySet.
Die nächsten vier Befehle weisen Variablen Werte zu, die im folgenden Befehl verwendet werden.
Da Sie diese Zeichenfolgen direkt im Befehl **"Set-AzVMOperatingSystem"** angeben können, wird dieser Ansatz nur zur Lesbarkeit verwendet.
Sie können jedoch einen ansatz wie diesen in Skripts verwenden.
Der letzte Befehl legt die Betriebssystemeigenschaften für den virtuellen Computer fest, der in $VirtualMachine.
Der Befehl verwendet die in der Datei gespeicherten $Credential.
Der Befehl verwendet für einige Parameter Variablen, die in den vorherigen Befehlen zugewiesen wurden.

## PARAMETERS

### -ComputerName
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

### -Credential
Gibt den Benutzernamen und das Kennwort für den virtuellen Computer als ein **"PSCredential"-Objekt** an.
Verwenden Sie zum Abrufen der Anmeldeinformationen das Get-Credential Cmdlet.
Weitere Informationen erhalten Sie, wenn Sie " `Get-Help Get-Credential` eingeben" aus.

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
Gibt eine base-64-codierte Zeichenfolge mit benutzerdefinierten Daten an.
Dies wird in ein Binärarray decodiert, das als Datei auf dem virtuellen Computer gespeichert wird.
Die maximale Länge des Binärarrays beträgt 65535 Bytes.<br>
**Hinweis: Übergeben Sie keine geheimen Daten oder Kennwörter in der Eigenschaft "customData".**<br>
Diese Eigenschaft kann nach dem Erstellen der VM nicht mehr aktualisiert werden. <br>
customData wird an die VM übergeben, die als Datei gespeichert wird. Weitere Informationen finden Sie unter "Benutzerdefinierte [Daten in Azure-VMs".](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/) <br>
Informationen zur Verwendung von cloud-init für Ihre Linux VM finden Sie unter "Verwenden von [cloud-init](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init) zum Anpassen einer Linux VM während der Erstellung"

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
Deaktivieren Sie Provision VM Agent.

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
Gibt den Modus des In-Guest-Patchings auf dem virtuellen Computer IaaS an.<br><br>
Mögliche Werte sind:<br>
**Manuell** – Sie steuern die Anwendung von Patches auf einen virtuellen Computer. Dazu werden Patches manuell innerhalb der VM angewendet. In diesem Modus sind automatische Updates deaktiviert. die Eigenschaft "WindowsConfiguration.enableAutomaticUpdates" muss "false" sein.<br>
**AutomaticByOS** – Der virtuelle Computer wird vom Betriebssystem automatisch aktualisiert. Die Eigenschaft "WindowsConfiguration.enableAutomaticUpdates" muss "true" sein. <br >
**AutomaticByPlatform** – Der virtuelle Computer wird vom Betriebssystem automatisch aktualisiert. Die Eigenschaften "provisionVMAgent" und "WindowsConfiguration.enableAutomaticUpdates" müssen "true" sein.

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
Gibt an, dass für die Einstellungen die Installation des Agent für den virtuellen Computer auf dem virtuellen Computer erforderlich ist.

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
Gibt die Zeitzone des virtuellen Computers an. z. B. \" Pacific Standard \" Time. <br>
Mögliche Werte können als [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) zeitzonen verwendet werden, die von ["TimeZoneInfo.GetSystemTimeZones" zurückgegeben werden.](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)

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
Gibt das Objekt des lokalen virtuellen Computers an, für das Betriebssystemeigenschaften festgelegt werden.
Verwenden Sie zum Abrufen eines Objekts für einen virtuellen Computer das Get-AzVM Cmdlet.
Erstellen Sie ein Objekt für einen virtuellen Computer mithilfe des New-AzVMConfig Cmdlets.

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
Dies muss in einem Schlüsseltresor gespeichert sein.

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
Gibt an, dass dieses Betriebssystem HTTP WinRM verwendet.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.Management.Automation.SwitchParameter

### System.String

### System.Management.Automation.PSCredential

### System.URI

## AUSGABEN

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)


