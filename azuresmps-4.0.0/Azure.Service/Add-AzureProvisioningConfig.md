---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0B3EF123-8424-4CCA-95E8-01301B70CBDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84db81f51a4f8d0da605917f99e14c1721cd89d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006588"
---
# Add-AzureProvisioningConfig

## Synopsis
Fügt die Bereitstellungskonfiguration für einen virtuellen Azure-Computer hinzu.

## Syntax

### Windows (Standard)
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>] [-Windows]
 [-AdminUsername <String>] [-Password <String>] [-ResetPasswordOnFirstLogon] [-DisableAutomaticUpdates]
 [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>] [-EnableWinRMHttp]
 [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>]
 [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### Linux
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-Linux] [-LinuxUser <String>]
 [-DisableSSH] [-NoSSHEndpoint] [-NoSSHPassword] [-SSHPublicKeys <SSHPublicKeyList>]
 [-SSHKeyPairs <SSHKeyPairList>] [-CustomDataFile <String>] [-Password <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Windows Domain
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>]
 -AdminUsername <String> [-WindowsDomain] [-Password <String>] [-ResetPasswordOnFirstLogon]
 [-DisableAutomaticUpdates] [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>]
 -JoinDomain <String> -Domain <String> -DomainUserName <String> -DomainPassword <String>
 [-MachineObjectOU <String>] [-EnableWinRMHttp] [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>]
 [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das **Add-AzureProvisioningConfig-** Cmdlet fügt einer Azure Virtual Machine-Konfiguration Bereitstellungs Konfigurationsinformationen hinzu.
Sie können das Configuration-Objekt zum Erstellen eines virtuellen Computers verwenden.

Dieses Cmdlet unterstützt verschiedene Bereitstellungskonfigurationen, einschließlich eigenständiger Windows-Server, Windows-Server, die einer Active Directory-Domäne beigetreten sind, und Linux-basierten Servern.

Wenn Sie einen Active Directory-Domänen beigetretenen Server erstellen möchten, geben Sie den vollqualifizierten Domänennamen der Active Directory-Domäne und die Domänenanmeldeinformationen eines Benutzers an, der die Berechtigung hat, dem virtuellen Computer mit der Domäne beizutreten.

## Beispiele

### Beispiel 1: Erstellen eines eigenständigen virtuellen Computers
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService"
```

Mit diesem Befehl wird ein Virtual Machine-Konfigurationsobjekt mithilfe des Cmdlets **New-AzureVMConfig** erstellt.
Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet fügt die Bereitstellungskonfiguration für einen virtuellen Computer hinzu, auf dem das Windows-Betriebssystem ausgeführt wird.
Die Konfiguration umfasst den Benutzernamen und das Kennwort des Administrators.
Der Befehl übergibt die Konfiguration an das Cmdlet **New-AzureVM** , das den virtuellen Computer erstellt.

### Beispiel 2: Erstellen einer Domäne, die einem virtuellen Computer beigetreten ist
```
PS C:\> New-AzureVMConfig -Name "DomainVM" -InstanceSize Small -ImageName "Image09" | Add-AzureProvisioningConfig -WindowsDomain -Password "password" -AdminUsername "AdminMain" -ResetPasswordOnFirstLogon -JoinDomain "contoso.com" -Domain "contoso" -DomainUserName "DomainAdminUser" -DomainPassword "DomainPassword" -MachineObjectOU 'OU=AzureVMs,DC=contoso,DC=com' | New-AzureVM -ServiceName "ContosoService"
```

Mit diesem Befehl wird ein Konfigurationsobjekt für einen virtuellen Computer erstellt und an das aktuelle Cmdlet weitergeleitet.
Das aktuelle Cmdlet fügt eine Bereitstellungskonfiguration für einen virtuellen Computer hinzu, der mit der Contoso-Domäne verbunden werden soll.
Der Befehl enthält den Benutzernamen und das Kennwort, die erforderlich sind, um den virtuellen Computer zur Domäne hinzufügen zu können.
Bei der Konfiguration muss der Benutzer das Benutzerkennwort bei der ersten Anmeldung ändern.
Der Befehl erstellt den virtuellen Computer basierend auf dem Bereitstellungsobjekt.

### Beispiel 3: Erstellen eines Linux-basierten virtuellen Computers
```
PS C:\> New-AzureVMConfig -Name "LinuxVM" -InstanceSize Small -ImageName "LinuxImage03" | Add-AzureProvisioningConfig -Linux -LinuxUser "LinuxRoot" -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

Mit diesem Befehl wird ein Konfigurationsobjekt für einen virtuellen Computer erstellt und an das aktuelle Cmdlet weitergeleitet.
Das aktuelle Cmdlet fügt die Bereitstellungskonfiguration für einen virtuellen Computer hinzu, auf dem das Linux-Betriebssystem ausgeführt wird.
Die Konfiguration umfasst den Stammbenutzer Namen und das Kennwort.
Der Befehl erstellt den virtuellen Computer basierend auf dem Bereitstellungsobjekt.

### Beispiel 4: Erstellen eines virtuellen Computers, der Zertifikate für WinRM enthält
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image11" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Der erste Befehl ruft Zertifikate aus einem Zertifikatspeicher ab und speichert Sie dann in der $certs-Arrayvariablen.

Der zweite Befehl erstellt ein Konfigurationsobjekt für einen virtuellen Computer und übergibt es an das aktuelle Cmdlet.
Das aktuelle Cmdlet fügt eine Bereitstellungskonfiguration mit Zertifikaten für WinRM hinzu.
Der Befehl erstellt den virtuellen Computer basierend auf dem Bereitstellungsobjekt.

### Beispiel 5: Erstellen eines virtuellen Computers, auf dem WinRM über HTTP aktiviert ist
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image14" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -EnableWinRMHttp | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Mit diesem Befehl wird ein Konfigurationsobjekt für einen virtuellen Computer erstellt und an das aktuelle Cmdlet weitergeleitet.
Das aktuelle Cmdlet fügt die Bereitstellungskonfiguration hinzu, bei der WinRM über HTTP aktiviert ist.
Der Befehl erstellt den virtuellen Computer basierend auf dem Bereitstellungsobjekt.

### Beispiel 6: Erstellen eines virtuellen Computers, auf dem WinRM über HTTPS deaktiviert ist
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -DisableWinRMHttps | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Mit diesem Befehl wird ein Konfigurationsobjekt für einen virtuellen Computer erstellt und an das aktuelle Cmdlet weitergeleitet.
Das aktuelle Cmdlet fügt die Bereitstellungskonfiguration hinzu, die WinRM über HTTPS deaktiviert.
Der Befehl erstellt den virtuellen Computer basierend auf dem Bereitstellungsobjekt.

### Beispiel 7: Erstellen einer virtuellen Maschine ohne Schlüsselexport
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -X509Certificates $certs[0], $certs[1] -NoExportPrivateKey | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Der erste Befehl ruft Zertifikate aus einem Zertifikatspeicher ab und speichert Sie dann in der $certs-Arrayvariablen.

Der zweite Befehl erstellt ein Konfigurationsobjekt für einen virtuellen Computer und übergibt es an das aktuelle Cmdlet.
Das aktuelle Cmdlet fügt die Bereitstellungskonfiguration für einen virtuellen Computer hinzu, der Zertifikate enthält, und exportiert keine privaten Schlüssel.
Der Befehl erstellt den virtuellen Computer basierend auf dem Bereitstellungsobjekt.

## Parameter

### -Nation aus AdminUsername
Gibt den Benutzernamen des Administrator Kontos an, das von dieser Konfiguration auf dem virtuellen Computer erstellt wird.

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

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zertifikate
Gibt eine Reihe von Zertifikaten an, die von dieser Konfiguration auf dem virtuellen Computer installiert werden.

```yaml
Type: CertificateSettingList
Parameter Sets: Windows, WindowsDomain
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

Wenn es sich bei dem Gastbetriebssystem um das Windows-Betriebssystem handelt, speichert diese Konfiguration diese Daten als Binärdatei mit dem Namen%SystemDrive%\AzureData\CustomData.bin.

Wenn es sich bei dem Gastbetriebssystem um Linux handelt, übergibt diese Konfiguration die Daten mithilfe der ovf-env.xml-Datei.
Die Konfiguration kopiert diese Datei in das/var/lib/waagent-Verzeichnis.
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

### -DisableAutomaticUpdates
Gibt an, dass diese Konfiguration automatische Updates deaktiviert.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableGuestAgent
Gibt an, dass diese Konfiguration den Gast-Agent "Infrastructure as a Service (IaaS)" deaktiviert.

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

### -DisableSSH
Gibt an, dass diese Konfiguration SSH deaktiviert.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWinRMHttps
Gibt an, dass diese Konfiguration die Windows-Remote Verwaltung (WinRM) auf HTTPS deaktiviert.
Standardmäßig ist WinRM über HTTPS aktiviert.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Domäne
Gibt den Namen der Domäne des Kontos an, das über die Berechtigung zum Hinzufügen des Computers zu einer Domäne verfügt.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainPassword
Gibt das Kennwort des Benutzerkontos an, das über die Berechtigung zum Hinzufügen des Computers zu einer Domäne verfügt.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Domain User Name
Gibt den Namen des Benutzerkontos an, das über die Berechtigung zum Hinzufügen des Computers zu einer Domäne verfügt.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWinRMHttp
Gibt an, dass diese Konfiguration WinRM über HTTP aktiviert.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
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

### -JoinDomain
Gibt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) der Domäne an, der Sie beitreten möchten.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Linux
Gibt an, dass diese Konfiguration eine Linux-Konfiguration erstellt.

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
Gibt den Benutzernamen des Linux-Administratorkontos an, das von dieser Konfiguration auf dem virtuellen Computer erstellt wird.

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

### -MachineObjectOU
Gibt den vollqualifizierten Namen der Organisationseinheit an, in der die Konfiguration das Computerkonto erstellt.

```yaml
Type: String
Parameter Sets: WindowsDomain
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
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoRDPEndpoint
Gibt an, dass diese Konfiguration einen virtuellen Computer ohne einen Remote Desktop Endpunkt erstellt.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoSSHEndpoint
Gibt an, dass diese Konfiguration einen virtuellen Computer ohne einen SSH-Endpunkt erstellt.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoSSHPassword
Gibt an, dass diese Konfiguration einen virtuellen Computer ohne ein SSH-Kennwort erstellt.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWinRMEndpoint
Gibt an, dass diese Konfiguration keinen WinRM-Endpunkt für den virtuellen Computer hinzufügt.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
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

### -ResetPasswordOnFirstLogon
Gibt an, dass der Benutzer das Kennwort bei der ersten Anmeldung vom virtuellen Computer ändern muss.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
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

### -TimeZone
Gibt die Zeitzone für den virtuellen Computer an, beispielsweise Pacific Standard Time oder Kanada Central Normalzeit.

```yaml
Type: String
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Gibt ein Objekt eines virtuellen Computers an.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Windows
Gibt an, dass diese Konfiguration einen eigenständigen virtuellen Computer erstellt, auf dem das Windows-Betriebssystem ausgeführt wird.

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

### -Windows Domain
Gibt an, dass diese Konfiguration Windows Server erstellt, der einer Active Directory-Domäne beigetreten ist.

```yaml
Type: SwitchParameter
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WinRMCertificate
Gibt ein Zertifikat an, das diese Konfiguration einem WinRM-Endpunkt zuordnet.

```yaml
Type: X509Certificate2
Parameter Sets: Windows, WindowsDomain
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
Parameter Sets: Windows, WindowsDomain
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

[Neu – AzureVM](./New-AzureVM.md)

[Neu – AzureVMConfig](./New-AzureVMConfig.md)


