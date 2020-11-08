---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA7BD103-5C91-4E3B-9E46-2CAEDA5BA615
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5643756cfad93399664298378e97264dedc2f
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007604"
---
# New-WAPackVM

## Synopsis
Erstellt einen virtuellen Computer.

## Syntax

### CreateVMFromTemplate (Standard)
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>]
 [-ProductKey <String>] [-Windows] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### CreateLinuxVMFromTemplate
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>] [-Linux]
 [-AdministratorSSHKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### CreateVMFromOSDisk
```
New-WAPackVM -Name <String> [-VNet <VMNetwork>] -OSDisk <VirtualHardDisk> -VMSizeProfile <HardwareProfile>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Diese Themen sind veraltet und werden in Zukunft entfernt.
In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .

Das Cmdlet **New-WAPackVM** erstellt einen virtuellen Computer.

## Beispiele

### Beispiel 1: Erstellen eines virtuellen Computers für das Windows-Betriebssystem mithilfe einer Vorlage
```
PS C:\> $Credentials = Get-Credential PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate04"PS C:\> New-WAPackVM -Name "ContosoV023" -Template $Template -VMCredential $Credentials -Windows
```

Der erste Befehl erstellt ein **PSCredential** -Objekt und speichert es dann in der $Credentials-Variablen.
Das Cmdlet fordert Sie zur Eingabe eines Kontos und eines Kennworts auf.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .

Der zweite Befehl ruft die Vorlage für den virtuellen Computer mit dem Namen ContosoTemplate04 mit dem Cmdlet **Get-WAPackVMTemplate** ab und speichert Sie dann in der $Template-Variablen.

Der endgültige Befehl erstellt einen virtuellen Computer mit dem Namen ContosoV023, basierend auf der Vorlage, die in der $Template-Variablen gespeichert ist.
Der Befehl gibt den *Windows* -Parameter an, und daher muss auf dem virtuellen Computer eine Version des Windows-Betriebssystems ausgeführt werden.

### Beispiel 2: Erstellen eines virtuellen Computers für das Linux-Betriebssystem mithilfe einer Vorlage
```
PS C:\> $Credentials = Get-Credential
PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate19"
PS C:\> New-WAPackVM -Linux -Name "ContosoV028" -Template $Template -VMCredential $Credentials
```

Der erste Befehl erstellt ein **PSCredential** -Objekt und speichert es dann in der $Credentials-Variablen.

Der zweite Befehl ruft die Vorlage für den virtuellen Computer mit dem Namen ContosoTemplate19 mit dem Cmdlet **Get-WAPackVMTemplate** ab und speichert Sie dann in der $Template-Variablen.

Der endgültige Befehl erstellt einen virtuellen Computer mit dem Namen ContosoV028, basierend auf der Vorlage, die in der $Template-Variablen gespeichert ist.
Der Befehl gibt den *Linux* -Parameter an, und daher muss auf dem virtuellen Computer eine Version des Linux-Betriebssystems ausgeführt werden.

### Beispiel 3: Erstellen eines virtuellen Computers aus einem Betriebssystemdatenträger und einem Größen Profil
```
PS C:\> $OSDisk = Get-WAPackVMOSDisk -Name "ContosoDiskOS"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> New-WAPackVM -Name "ContosoV073" -OSDisk $OSDisk -VMSizeProfile $SizeProfile
```

Der erste Befehl ruft mit dem Cmdlet **Get-WAPackVMOSDisk** einen Betriebssystemdatenträger mit dem Namen ContosoDiskOS ab und speichert ihn dann in der $OSDisk Variablen.

Der zweite Befehl ruft das size-Profil mit dem Namen MediumSizeVM mit dem Cmdlet **Get-WAPackVMSizeProfile** ab und speichert es dann in der $SizeProfile-Variablen.

Der endgültige Befehl erstellt einen virtuellen Computer mit dem Namen ContosoV073 aus dem in $OSDisk gespeicherten Betriebssystemdatenträger und dem in $SizeProfile gespeicherten Größen Profil.

## Parameter

### -AdministratorSSHKey
Gibt den Secure Shell (SSH)-Schlüssel für das Administrator Konto an.

```yaml
Type: String
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
Gibt an, dass das Cmdlet einen virtuellen Computer zum Ausführen des Linux-Betriebssystems erstellt.

```yaml
Type: SwitchParameter
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt einen Namen für den virtuellen Computer an.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OSDisk
Gibt einen Betriebssystemdatenträger als **VirtualHardDisk** -Objekt an.
Um einen Betriebssystemdatenträger zu erhalten, verwenden Sie das Cmdlet **Get-WAPackVMOSDisk** .

```yaml
Type: VirtualHardDisk
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProductKey
Gibt einen Product Key an.
Der Product Key ist eine 25-stellige Nummer, die die Produktlizenz kennzeichnet.
Verwenden Sie einen Product Key für ein Betriebssystem, das Sie auf einem virtuellen Computer oder einem Host installieren möchten.

```yaml
Type: String
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vorlage
Gibt eine Vorlage an.
Das Cmdlet erstellt einen virtuellen Computer basierend auf der von Ihnen angegebenen Vorlage.
Verwenden Sie zum Abrufen eines Vorlagenobjekts das Get-WAPackVMTemplate-Cmdlet.

```yaml
Type: VMTemplate
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMCredential
Gibt die Anmeldeinformationen für das lokale Administrator Konto an.
Verwenden Sie das Cmdlet **Get-Credential** , um ein **PSCredential** -Objekt zu erhalten.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .

```yaml
Type: PSCredential
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSizeProfile
Gibt ein Größen Profil für einen virtuellen Computer als **Hardwareprofile** -Objekt an.
Um ein Größen Profil zu erhalten, verwenden Sie das Cmdlet **Get-WAPackVMSizeProfile** .

```yaml
Type: HardwareProfile
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VNet
Gibt ein virtuelles Netzwerk an.
Das Cmdlet verbindet den virtuellen Computer mit dem von Ihnen angegebenen virtuellen Netzwerk.
Um ein virtuelles Netzwerk zu erhalten, verwenden Sie das Cmdlet **Get-WAPackVNet** .

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Windows
Gibt an, dass das Cmdlet einen virtuellen Computer zum Ausführen des Windows-Betriebssystems erstellt.

```yaml
Type: SwitchParameter
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-WAPackVM](./Get-WAPackVM.md)

[Remove-WAPackVM](./Remove-WAPackVM.md)

[Neustart-WAPackVM](./Restart-WAPackVM.md)

[Lebenslauf-WAPackVM](./Resume-WAPackVM.md)

[Satz-WAPackVM](./Set-WAPackVM.md)

[Anfang-WAPackVM](./Start-WAPackVM.md)

[Stopp-WAPackVM](./Stop-WAPackVM.md)

[Suspend-WAPackVM](./Suspend-WAPackVM.md)

[Get-WAPackVMSizeProfile](./Get-WAPackVMSizeProfile.md)

[Get-WAPackVMTemplate](./Get-WAPackVMTemplate.md)

[Get-WAPackVMOSDisk](./Get-WAPackVMOSDisk.md)


