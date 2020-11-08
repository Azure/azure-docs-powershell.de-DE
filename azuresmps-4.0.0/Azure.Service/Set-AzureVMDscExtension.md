---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 649D0A6C-77CE-4E49-AFF8-DF70ABE9FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bb63ff2ffecc3cab8c7d227d10afdd8374dde2a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007557"
---
# Set-AzureVMDscExtension

## Synopsis
Konfiguriert die DSC-Erweiterung auf einem virtuellen Computer.

## Syntax

```
Set-AzureVMDscExtension [-ReferenceName <String>] [-ConfigurationArgument <Hashtable>]
 [-ConfigurationDataPath <String>] [-ConfigurationArchive] <String> [-ConfigurationName <String>]
 [-ContainerName <String>] [-Force] [-StorageContext <AzureStorageContext>] [-Version <String>]
 [-StorageEndpointSuffix <String>] [-WmfVersion <String>] [-DataCollection <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **festlegen-AzureVMDscExtension** " konfiguriert die Erweiterung der gewünschten Zustands Konfiguration (DSC) auf einem virtuellen Computer.

## Beispiele

### Beispiel 1: Konfigurieren der DSC-Erweiterung auf einem virtuellen Computer
```
PS C:\> Set-AzureVMDscExtension -VM $VM -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Path = 'C:\MyDirectory' }
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Contoso.Compute.BGInfo}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd6
OperationStatus             : OK
```

Mit diesem Befehl wird die DSC-Erweiterung auf einem virtuellen Computer konfiguriert.

Das MyConfiguration.ps1.zip-Paket muss zuvor mit dem Befehl **Publish-AzureVMDscConfiguration** in den Azure-Speicher hochgeladen worden sein und enthält das MyConfiguration.ps1-Skript und die Module, von denen es abhängig ist.

Das myconfiguration-Argument gibt die spezifische DSC-Konfiguration innerhalb des Skripts an, die ausgeführt werden soll.
Der Parameter- *ConfigurationArgument* gibt eine Hashtable mit den Argumenten an, die an die Konfigurationsfunktion übergeben werden.

### Beispiel 2: Konfigurieren der DSC-Erweiterung auf einem virtuellen Computer mithilfe eines Pfads zu den Konfigurationsdaten
```
PS C:\> $VM | Set-AzureVMDscExtension -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Credential = Get-Credential } -ConfigurationDataPath MyConfigurationData.psd1
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Microsoft.Compute.BGInfo, Microsoft.Powershell.DSC}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd7
OperationStatus             : OK
```

Dieser Befehl konfiguriert die DSC-Erweiterung auf einem virtuellen Computer mithilfe eines Pfads zu den Konfigurationsdaten.

## Parameter

### -ConfigurationArchive
Gibt den Namen des Konfigurationspakets (ZIP-Datei) an, das zuvor von Publish-AzureVMDscConfiguration hochgeladen wurde.
Dieser Parameter muss nur den Namen der Datei ohne Pfad angeben.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationArgument
Gibt eine Hashtable an, die die Argumente für die Konfigurationsfunktion angibt.
Die Schlüssel entsprechen den Parameternamen und den Werten für die Parameterwerte.

Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Primitive Typen
- Zeichenfolge
- Matrix
- PSCredential

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationDataPath
Gibt den Pfad einer psd1-Datei an, die die Daten für die Konfigurationsfunktion angibt.
Diese Datei muss eine Hashtable enthalten, wie unter Trennen von Konfigurations-und Umgebungsdaten beschrieben https://msdn.microsoft.com/en-us/PowerShell/DSC/configData .

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

### -ConfigurationName
Gibt den Namen des Konfigurationsskripts oder Moduls an, das von der DSC-Erweiterung aufgerufen wird.

Der Wert dieses Parameters muss der Name einer der Konfigurationsfunktionen sein, die in den Skripts oder Modulen enthalten sind, die in *ConfigurationArchive* verpackt sind.

Dieses Cmdlet ist standardmäßig mit dem Namen der Datei versehen, die vom *ConfigurationArchive* -Parameter angegeben wird, wenn Sie diesen Parameter ohne Erweiterung auslassen.
Wenn *ConfigurationArchive* beispielsweise "SalesWebSite.ps1.zip" ist, lautet der Standardwert für *ConfigurationName* "SalesWebSite".

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

### -Containername
Gibt den Namen des Azure-Speichercontainers an, in dem sich der *ConfigurationArchive* befindet.

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

### -DataCollection
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

### -Force
Gibt an, dass mit diesem Cmdlet vorhandene BLOBs überschrieben werden.

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

### -ReferenceName
Gibt eine benutzerdefinierte Zeichenfolge an, die verwendet werden kann, um auf eine Erweiterung zu verweisen.
Dieser Parameter wird angegeben, wenn die Erweiterung zum ersten Mal dem virtuellen Computer hinzugefügt wird.
Bei nachfolgenden Updates sollten Sie den zuvor verwendeten Verweisnamen angeben, während Sie die Erweiterung aktualisieren.
Der *Verweisname* , der einer Erweiterung zugewiesen ist, wird mit dem Cmdlet **Get-AzureVM** zurückgegeben.

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

### -Storagecontext
Gibt den Azure-Speicherkontext an, in dem die Sicherheitseinstellungen für den Zugriff auf das Konfigurationsskript bereitgestellt werden.
Dieser Kontext bietet Lesezugriff auf den Container, der durch den *Containername* -Parameter angegeben wird.

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEndpointSuffix
Gibt das DNS-Endpunkt Suffix für alle Speicherdienste an, beispielsweise "Core.contoso.net".

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

### -Version
Gibt die spezifische Version der zu verwendenden DSC-Erweiterung an.
Der Standardwert ist auf "1. *" festgelegt, wenn dieser Parameter nicht angegeben ist.

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

### -VM
Gibt das Objekt des beständigen virtuellen Computers an.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WmfVersion
Gibt die Version des Windows Management Framework (WMF) an, die auf dem virtuellen Computer installiert werden soll.
Die DSC-Erweiterung hängt von den DSC-Funktionen ab, die nur in den WMF-Updates zur Verfügung stehen.
Dieser Parameter gibt an, welche Version des Updates auf dem virtuellen Computer installiert werden soll.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- 4,0.
Installiert WMF 4,0, es sei denn, eine neuere Version ist bereits installiert.
- 5,0.
Installiert die neueste Version von WMF 5,0.
- neueste.
Installiert die aktuelle WMF, derzeit WMF 5,0.

Der Standardwert ist aktuell.

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

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureVMDscExtension](./Get-AzureVMDscExtension.md)

[Remove-AzureVMDscExtension](./Remove-AzureVMDscExtension.md)

[Remove-AzureVMDscExtension](./Remove-AzureVMDscExtension.md)

[Get-AzureVM](./Get-AzureVM.md)

[Publish-AzureVMDscConfiguration](./Publish-AzureVMDscConfiguration.md)


