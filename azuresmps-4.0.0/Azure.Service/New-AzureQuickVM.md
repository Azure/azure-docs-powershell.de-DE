---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F94584BC-EC02-412D-B089-B98A6FF8F505
online version: ''
schema: 2.0.0
ms.openlocfilehash: a5b7758a7316fa6c34ffe6b5225cd252f39c5d7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006115"
---
# New-AzureQuickVM

## Synopsis
Konfiguriert und erstellt einen virtuellen Azure-Computer.

## Syntax

### Windows (Standard)
```
New-AzureQuickVM [-Windows] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-AdminUsername <String>]
 [-Certificates <CertificateSettingList>] [-WaitForBoot] [-DisableWinRMHttps] [-EnableWinRMHttp]
 [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey]
 [-NoWinRMEndpoint] [-VNetName <String>] [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>]
 [-HostCaching <String>] [-AvailabilitySetName <String>] [-InstanceSize <String>] [-MediaLocation <String>]
 [-DisableGuestAgent] [-CustomDataFile <String>] [-ReservedIPName <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Linux
```
New-AzureQuickVM [-Linux] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-LinuxUser <String>] [-WaitForBoot]
 [-SSHPublicKeys <SSHPublicKeyList>] [-SSHKeyPairs <SSHKeyPairList>] [-VNetName <String>]
 [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>] [-HostCaching <String>] [-AvailabilitySetName <String>]
 [-InstanceSize <String>] [-MediaLocation <String>] [-DisableGuestAgent] [-CustomDataFile <String>]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureQuickVM** konfiguriert und erstellt einen virtuellen Azure-Computer.
Dieses Cmdlet kann einen virtuellen Computer in einem vorhandenen Azure-Dienst bereitstellen.
Dieses Cmdlet kann alternativ einen Azure-Dienst erstellen, der den neuen virtuellen Computer hostet.

## Beispiele

### Beispiel 1: Erstellen eines virtuellen Computers
```
PS C:\> New-AzureQuickVM -Windows -ServiceName "ContosoService17" -Name "VirutalMachine01" -ImageName "Image07" -Password "password" -AdminUsername "AdminMain" -WaitForBoot
```

Dieser Befehl erstellt einen virtuellen Computer, auf dem das Windows-Betriebssystem in einem vorhandenen Dienst ausgeführt wird.
Das Cmdlet basiert auf dem angegebenen Bild auf dem virtuellen Computer.
Der Befehl gibt den *WaitForBoot* -Parameter an.
Daher wartet das Cmdlet auf den Start des virtuellen Computers.

### Beispiel 2: Erstellen eines virtuellen Computers mit Zertifikaten
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
PS C:\> New-AzureQuickVM -Windows -ServiceName "MySvc1" -name "MyWinVM1" -ImageName "Image07" -Password "password" -AdminUserName "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] -WaitForBoot
```

Der erste Befehl ruft Zertifikate aus einem Store ab und speichert Sie in der $certs-Variablen.

Der zweite Befehl erstellt einen virtuellen Computer, der das Windows-Betriebssystem in einem vorhandenen Dienst aus einem Bild ausführt.
Standardmäßig ist WinRM HTTPS-Listener auf dem virtuellen Computer aktiviert.
Der Befehl gibt den *WaitForBoot* -Parameter an.
Daher wartet das Cmdlet auf den Start des virtuellen Computers.
Der Befehl lädt ein WinRM-Zertifikat und-X509Certificates in den gehosteten Dienst hoch.

### Beispiel 3: Erstellen eines virtuellen Computers, auf dem das Linux-Betriebssystem ausgeführt wird
```
PS C:\> New-AzureQuickVM -Linux -ServiceName "ContosoServiceLinux01" -Name "LinuxVirtualMachine01" -ImageName "LinuxImage01" -LinuxUser "RootMain" -Password "password" -Location "Central US"
```

Dieser Befehl erstellt einen virtuellen Computer, auf dem das Linux-Betriebssystem aus einem Bild ausgeführt wird.
Dieser Befehl erstellt einen Dienst zum Hosten des neuen virtuellen Computers.
Der Befehl gibt einen Speicherort für den Dienst an.

### Beispiel 4: Erstellen eines virtuellen Computers und Erstellen eines Diensts zum Hosten des neuen virtuellen Computers
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService03" -Name " VirtualMachine25" -ImageName $images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name
```

Der erste Befehl ruft Speicherorte mit dem Cmdlet **Get-AzureLocation** ab und speichert Sie dann in der $Locations-Arrayvariablen.

Der zweite Befehl ruft verfügbare Bilder mit dem Cmdlet **Get-AzureVMImage** ab und speichert Sie dann in der $Images-Arrayvariablen.

Der endgültige Befehl erstellt einen umfangreichen virtuellen Computer mit dem Namen VirtualMachine25.
Auf dem virtuellen Computer wird das Betriebssystem Windows ausgeführt.
Sie basiert auf einem der Bilder in $Images.
Der Befehl erstellt einen Dienst mit dem Namen ContosoService03 für den neuen virtuellen Computer.
Der Dienst befindet sich an einem Speicherort in $Locations.

### Beispiel 5: Erstellen eines virtuellen Computers mit einem reservierten IP-Namen
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService04" -Name "VirtualMachine27" -ImageName $Images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name -ReservedIPName $ipName
```

Der erste Befehl ruft Speicherorte ab und speichert Sie dann in der $Locations-Arrayvariablen.

Der zweite Befehl ruft verfügbare Bilder ab und speichert Sie dann in der $Images-Arrayvariablen.

Der endgültige Befehl erstellt einen virtuellen Computer mit dem Namen VirtualMachine27, der auf einem der Bilder in $Images basiert.
Der Befehl erstellt einen Dienst an einem Speicherort in $Locations.
Der virtuelle Computer verfügt über einen reservierten IP-Namen, der zuvor in der $ipName-Variablen gespeichert wurde.

## Parameter

### -Nation aus AdminUsername
Gibt den Benutzernamen des Administrator Kontos an, das dieses Cmdlet auf dem virtuellen Computer erstellt.

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Affinitygroup
Gibt die affinitätsgruppe für den virtuellen Computer an.
Geben Sie diesen Parameter oder den *Location* -Parameter nur an, wenn mit diesem Cmdlet ein Azure-Dienst für den virtuellen Computer erstellt wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AvailabilitySetName
Gibt den Namen des Verfügbarkeits Satzes an, in dem dieses Cmdlet den virtuellen Computer erstellt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zertifikate
Gibt eine Liste der Zertifikate an, die dieses Cmdlet zum Erstellen des Diensts verwendet.

```yaml
Type: CertificateSettingList
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomDataFile
Gibt eine Datendatei für den virtuellen Computer an.
Dieses Cmdlet codiert den Inhalt der Datei als Base64.
Die Datei muss weniger als 64 KB lang sein.

Wenn es sich bei dem Gastbetriebssystem um das Windows-Betriebssystem handelt, speichert dieses Cmdlet diese Daten als Binärdatei mit dem Namen%SystemDrive%\AzureData\CustomData.bin.

Wenn es sich bei dem Gastbetriebssystem um Linux handelt, übergibt dieses Cmdlet die Daten mithilfe der ovf-env.xml-Datei.
Bei der Installation wird die Datei in das/var/lib/waagent-Verzeichnis kopiert.
Der Agent speichert auch die Base64-codierten Daten in/var/lib/waagent/CustomData.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableGuestAgent
Gibt an, dass dieses Cmdlet den Guest-Agent "Infrastructure as a Service (IaaS)" deaktiviert.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWinRMHttps
Gibt an, dass dieses Cmdlet die Windows-Remote Verwaltung (WinRM) auf HTTPS deaktiviert.
Standardmäßig ist WinRM über HTTPS aktiviert.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DnsSettings
Gibt ein Array von DNS-Server Objekten an, die die DNS-Einstellungen für die neue Bereitstellung definieren.
Verwenden Sie zum Erstellen eines **DnsServer** -Objekts das Cmdlet **New-AzureDns** .

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWinRMHttp
Gibt an, dass das Cmdlet WinRM über HTTP aktiviert.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching
Gibt den Host Zwischenspeicherungsmodus für den Datenträger des Betriebssystems an.
Gültige Werte sind: 

- ReadOnly
- ReadWrite

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bildname
Gibt den Namen der Datenträgerabbildung an, die dieses Cmdlet zum Erstellen des Betriebssystemdatenträgers verwendet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Information
Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.

Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Weiterhin
- Ignorieren
- Erkundigen
- SilentlyContinue
- Beenden
- Anhalten

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Gibt eine Informations Variable an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Instanzen
Gibt die Größe der Instanz an.
Gültige Werte sind: 

- ExtraSmall
- Kleine
- Mittel
- Große
- Extra Large
- A5
- A6
- A7
- A8
- A9
- Basic_A0
- Basic_A1
- Basic_A2
- Basic_A3
- Basic_A4
- Standard_D1
- Standard_D2
- Standard_D3
- Standard_D4
- Standard_D11
- Standard_D12
- Standard_D13
- Standard_D14

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
Gibt an, dass mit diesem Cmdlet ein Linux-basierter virtueller Computer erstellt wird.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LinuxUser
Gibt den Benutzernamen des Linux-Administratorkontos an, das dieses Cmdlet auf dem virtuellen Computer erstellt.

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Standort
Gibt das Azure Datacenter an, das den virtuellen Computer hostet.
Wenn Sie diesen Parameter angeben, erstellt das Cmdlet einen Azure-Dienst an der angegebenen Position.
Geben Sie diesen Parameter oder den *affinitygroup* -Parameter nur an, wenn mit diesem Cmdlet ein Azure-Dienst für den virtuellen Computer erstellt wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaLocation
Gibt den Azure-Speicherort an, an dem mit diesem Cmdlet die virtuellen Computer Datenträger erstellt werden.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen des virtuellen Computers an, der vom Cmdlet erstellt wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoExportPrivateKey
Gibt an, dass diese Konfiguration den privaten Schlüssel nicht hochlädt.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWinRMEndpoint
Gibt an, dass dieses Cmdlet keinen WinRM-Endpunkt für den virtuellen Computer hinzufügt.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kennwort
Gibt das Kennwort für das Administratorkonto an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -ReservedIPName
Gibt den reservierten IP-Namen an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReverseDnsFqdn
Gibt den vollqualifizierten Domänennamen für die Reverse-DNS-Suche an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Gibt den Namen eines neuen oder vorhandenen Azure-Diensts an, dem dieses Cmdlet den neuen virtuellen Computer hinzufügt.

Wenn Sie einen neuen Dienst angeben, wird er von diesen Cmdlets erstellt.
Wenn Sie einen neuen Dienst erstellen möchten, müssen Sie den Parameter *Location* oder *affinitygroup* angeben.

Wenn Sie einen vorhandenen Dienst angeben, geben Sie *Location* oder *affinitygroup* nicht an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHKeyPairs
Gibt SSH-Schlüsselpaare an.

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHPublicKeys
Gibt die öffentlichen SSH-Schlüssel an.

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetNames
Gibt ein Array von Namen des Subnets für den virtuellen Computer an.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VNetName
Gibt den Namen eines virtuellen Netzwerks für den virtuellen Computer an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForBoot
Gibt an, dass dieses Cmdlet auf den virtuellen Computer wartet, um den Zustand ReadyRole zu erreichen.
Wenn der virtuelle Computer einen der folgenden Zustände erreicht, schlägt das Cmdlet fehl: FailedStartingVM, ProvisioningFailed oder ProvisioningTimeout.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Windows
Gibt an, dass dieses Cmdlet einen virtuellen Windows-Computer erstellt.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WinRMCertificate
Gibt ein Zertifikat an, das dieses Cmdlet einem WinRM-Endpunkt zuordnet.

```yaml
Type: X509Certificate2
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -X509Certificates
Gibt ein Array von X509-Zertifikaten an, die für einen gehosteten Dienst bereitgestellt werden.

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureLocation](./Get-AzureLocation.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Neu – AzureDns](./New-AzureDns.md)


