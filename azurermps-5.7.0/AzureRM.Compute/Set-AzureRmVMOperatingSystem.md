---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
ms.openlocfilehash: 01f9d007d54e7e96ac28e81b5081dc696d3af406
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497702"
---
# Set-AzureRmVMOperatingSystem

## Synopsis
Legt die Betriebssystemeigenschaften für einen virtuellen Computer fest.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Windows (Standard)
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [<CommonParameters>]
```

### WindowsWinRmHttps
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [<CommonParameters>]
```

### Linux
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzureRmVMOperatingSystem** " legt die Betriebssystemeigenschaften für einen virtuellen Computer fest.
Sie können Anmeldeinformationen, Computername und Typ des Betriebssystems angeben.

## Beispiele

### Beispiel 1: Einrichten von Betriebssystemeigenschaften für eine neue virtuelle Maschine
```
PS C:\> $SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $ComputerName = "ContosoVM122"
PS C:\> $WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
PS C:\> $TimeZone = "Pacific Standard Time"
PS C:\> $CustomData = "echo 'Hello World'"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone
```

Der erste Befehl wandelt ein Kennwort in eine sichere Zeichenfolge um und speichert es dann in der $SecurePassword-Variablen.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help ConvertTo-SecureString` .

Mit dem zweiten Befehl werden die Anmeldeinformationen für den Benutzer FullerP und das in $SecurePassword gespeicherte Kennwort erstellt, und die Anmeldeinformationen werden dann in der $Credential Variablen gespeichert.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help New-Object` .

Der dritte Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.

Der vierte Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.
Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.
Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.

In den nächsten vier Befehlen werden Variablenwerte zugewiesen, die Sie im folgenden Befehl verwenden können.
Da Sie diese Zeichenfolgen direkt im Befehl " **Satz-AzureRmVMOperatingSystem** " angeben können, wird dieser Ansatz nur zur Lesbarkeit verwendet.
Sie können jedoch einen solchen Ansatz in Skripten verwenden.

Mit dem letzten Befehl werden die Betriebssystemeigenschaften für den virtuellen Computer festgelegt, der in $VirtualMachine gespeichert ist.
Der Befehl verwendet die in $Credential gespeicherten Anmeldeinformationen.
Der Befehl verwendet für einige Parameter in vorherigen Befehlen zugewiesene Variablen.

## Parameter

### -Computername
Gibt den Namen des Computers an.

```yaml
Type: String
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
Type: PSCredential
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
Die maximale Länge des binären Arrays beträgt 65535 Bytes.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisablePasswordAuthentication
Gibt an, dass dieses Cmdlet die Kennwortauthentifizierung deaktiviert.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableAutoUpdate
Gibt an, dass dieses Cmdlet die automatische Aktualisierung aktiviert.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
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
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProvisionVMAgent
Gibt an, dass für die Einstellungen der Virtual Machine-Agent auf dem virtuellen Computer installiert werden muss.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeZone
Gibt die Zeitzone für den virtuellen Computer an.

```yaml
Type: String
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Gibt das Objekt des lokalen virtuellen Computers an, auf dem Betriebssystemeigenschaften festgelegt werden sollen.
Verwenden Sie das Get-AzureRmVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.
Erstellen Sie ein Objekt für einen virtuellen Computer mithilfe des New-AzureRmVMConfig-Cmdlets.

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

### -Windows
Gibt an, dass der Typ des Betriebssystems Windows ist.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
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
Type: Uri
Parameter Sets: WindowsWinRmHttps
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
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
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
Type: SwitchParameter
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
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


