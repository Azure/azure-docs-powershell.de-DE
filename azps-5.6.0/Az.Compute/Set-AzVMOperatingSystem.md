---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 75eb0ef60443cdbf2dfe3fa53202d3c8141d4888
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938272"
---
# Set-AzVMOperatingSystem

## SYNOPSIS
Legt die Betriebssystemeigenschaften für einen virtuellen Computer fest.

## SYNTAX

### Windows (Standard)
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDisableVMAgent
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDisableVMAgentWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Linux
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-PatchMode <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Set-AzVMOperatingSystem** legt Betriebssystemeigenschaften für einen virtuellen Computer fest.
Sie können Anmeldeinformationen, Computername und Betriebssystemtyp angeben.

## BEISPIELE

### Beispiel 1: Festlegen von Betriebssystemeigenschaften für einen neuen virtuellen Computer
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

Mit dem ersten Befehl wird ein Kennwort in eine sichere Zeichenfolge konvertiert und dann in der $SecurePassword gespeichert.
Weitere Informationen finden Sie unter `Get-Help ConvertTo-SecureString` .
Der zweite Befehl erstellt eine Anmeldeinformationen für den Benutzer FullerP und das kennwort, das in $SecurePassword gespeichert ist, und speichert dann die Anmeldeinformationen in der $Credential Variablen.
Weitere Informationen finden Sie unter `Get-Help New-Object` .
Der dritte Befehl ruft den Verfügbarkeitssatz "AvailabilitySet03" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.
Mit dem vierten Befehl wird ein Objekt eines virtuellen Computers erstellt und dann in der $VirtualMachine gespeichert.
Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.
Der virtuelle Computer gehört zu dem Verfügbarkeitssatz, der auf der $AvailabilitySet.
Die nächsten vier Befehle weisen Variablen Werte zu, die im folgenden Befehl verwendet werden.
Da Sie diese Zeichenfolgen direkt im **Befehl Set-AzVMOperatingSystem** angeben können, wird dieser Ansatz nur zur Lesbarkeit verwendet.
Sie können jedoch einen ansatz wie diesen in Skripts verwenden.
Der letzte Befehl legt die Betriebssystemeigenschaften für den virtuellen Computer fest, der auf der $VirtualMachine.
Der Befehl verwendet die in der Datei $Credential.
Der Befehl verwendet Variablen, die in früheren Befehlen für einige Parameter zugewiesen wurden.

### Beispiel 2: Festlegen von Betriebssystemeigenschaften für einen neuen virtuellen Computer mit aktivierter hot patching
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform" -EnableHotPatching
```

Mit dem ersten Befehl wird ein Kennwort in eine sichere Zeichenfolge konvertiert und dann in der $SecurePassword gespeichert.
Weitere Informationen finden Sie unter `Get-Help ConvertTo-SecureString` .
Der zweite Befehl erstellt eine Anmeldeinformationen für den Benutzer FullerP und das kennwort, das in $SecurePassword gespeichert ist, und speichert dann die Anmeldeinformationen in der $Credential Variablen.
Weitere Informationen finden Sie unter `Get-Help New-Object` .
Der dritte Befehl ruft den Verfügbarkeitssatz "AvailabilitySet03" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.
Mit dem vierten Befehl wird ein Objekt eines virtuellen Computers erstellt und dann in der $VirtualMachine gespeichert.
Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.
Der virtuelle Computer gehört zu dem Verfügbarkeitssatz, der auf der $AvailabilitySet.
Die nächsten vier Befehle weisen Variablen Werte zu, die im folgenden Befehl verwendet werden.
Da Sie diese Zeichenfolgen direkt im **Befehl Set-AzVMOperatingSystem** angeben können, wird dieser Ansatz nur zur Lesbarkeit verwendet.
Sie können jedoch einen ansatz wie diesen in Skripts verwenden.
Der letzte Befehl legt die Betriebssystemeigenschaften für den virtuellen Computer fest, der auf der $VirtualMachine.
Der Befehl verwendet die in der Datei $Credential.
Der Befehl verwendet Variablen, die in früheren Befehlen für einige Parameter zugewiesen wurden.
Der Befehl aktiviert hotpatching auf dem virtuellen Computer.

### Beispiel 3: Festlegen von Betriebssystemeigenschaften für einen neuen virtuellen Linux-Computer
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -PatchMode "AutomaticByPlatform"
```

Mit dem ersten Befehl wird ein Kennwort in eine sichere Zeichenfolge konvertiert und dann in der $SecurePassword gespeichert.
Weitere Informationen finden Sie unter `Get-Help ConvertTo-SecureString` .
Der zweite Befehl erstellt eine Anmeldeinformationen für den Benutzer FullerP und das kennwort, das in $SecurePassword gespeichert ist, und speichert dann die Anmeldeinformationen in der $Credential Variablen.
Weitere Informationen finden Sie unter `Get-Help New-Object` .
Der dritte Befehl ruft den Verfügbarkeitssatz "AvailabilitySet03" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.
Mit dem vierten Befehl wird ein Objekt eines virtuellen Computers erstellt und dann in der $VirtualMachine gespeichert.
Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.
Der virtuelle Computer gehört zu dem Verfügbarkeitssatz, der auf der $AvailabilitySet.
Die nächsten beiden Befehle weisen Variablen Werte zu, die im folgenden Befehl verwendet werden.
Der letzte Befehl legt die Betriebssystemeigenschaften für den virtuellen Computer fest, der auf der $VirtualMachine.
Der Befehl verwendet die in der Datei $Credential.
Der Befehl verwendet Variablen, die in früheren Befehlen für einige Parameter zugewiesen wurden.
Der Befehl legt den Patchmoduswert auf dem virtuellen Computer auf "AutomaticByPlatform" fest.

## PARAMETER

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

### -Anmeldeinformationen
Gibt den Benutzernamen und das Kennwort für den virtuellen Computer als **PSCredential-Objekt** an.
Verwenden Sie das cmdlet Get-Credential, um eine Anmeldeinformationen zu erhalten.
Weitere Informationen finden Sie unter `Get-Help Get-Credential` .

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
Gibt eine Zeichenfolge an, die an den virtuellen Computer übergeben werden soll. Weitere Informationen finden Sie unter [Benutzerdefinierte Daten auf Azure VMs](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data).
**Hinweis: Es wird nicht empfohlen, vertrauliche Informationen in benutzerdefinierten Daten zu speichern.**


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
Deaktivieren Sie den Bereitstellungs-VM-Agent.

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

### -EnableHotpatching
Ermöglicht Kunden das Patchen ihrer Azure VMs, ohne dass ein Neustart erforderlich ist. Für enableHotpatching muss der Wert "provisionVMAgent" auf "true" und "patchMode" auf "AutomaticByPlatform" festgelegt sein.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
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
Gibt den Modus des In-Guest-Patchings auf den virtuellen IaaS-Computer an.<br><br>
Mögliche Werte sind:<br>
**Manuell** – Sie steuern die Anwendung von Patches auf einen virtuellen Computer. Dazu müssen Sie Patches manuell innerhalb der VM anwenden. In diesem Modus werden automatische Updates deaktiviert. die -Eigenschaft WindowsConfiguration.enableAutomaticUpdates muss false sein.<br>
**AutomaticByOS** – Der virtuelle Computer wird automatisch vom Betriebssystem aktualisiert. Die -Eigenschaft WindowsConfiguration.enableAutomaticUpdates muss true sein. <br >
**AutomaticByPlatform** – Der virtuelle Computer wird automatisch vom Betriebssystem aktualisiert. Die Eigenschaften provisionVMAgent und WindowsConfiguration.enableAutomaticUpdates müssen true sein.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProvisionVMAgent
Gibt an, dass für die Einstellungen die Installation des virtuellen Computer-Agents auf dem virtuellen Computer erforderlich ist.

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
Gibt die Zeitzone des virtuellen Computers an. z. B. \" Pacific Standard Time \" . <br>
Mögliche Werte können [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) aus Zeitzonen angezeigt werden, die von [TimeZoneInfo.GetSystemTimeZones zurückgegeben werden.](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)

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
Zum Abrufen eines Virtuellen Computerobjekts verwenden Sie das Get-AzVM Cmdlet.
Erstellen Sie ein Virtuelles Computerobjekt mithilfe des New-AzVMConfig-Cmdlets.

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
Dies muss in einem Schlüsseltresor gespeichert werden.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.Management.Automation.SwitchParameter

### System.String

### System.Management.Automation.PSCredential

### System.Uri

## AUSGABEN

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## NOTIZEN

## VERWANDTE LINKS

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)


