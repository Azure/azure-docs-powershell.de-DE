---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F41E3B17-A33C-4FBF-B532-2E86F1AAE2B8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4bc3e4245e3d223d95c3ec5d793a53d5d3bfbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006465"
---
# Import-AzureStorSimpleLegacyApplianceConfig

## Synopsis
Importiert eine Konfigurationsdatei.

## Syntax

```
Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath <String> -TargetDeviceName <String>
 -ConfigDecryptionKey <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **Import-AzureStorSimpleLegacyApplianceConfig** " wird die Konfigurationsdatei aus der Legacy Appliance importiert.
Diese Datei enthält Informationen zu Volumen Containern, Sicherungsrichtlinien und Speicherkonto Anmeldeinformationen für den Azure StorSimple-Dienst.
Dieses Cmdlet gibt die Konfigurationsmetadaten der Legacy Appliance zurück.

## Beispiele

### Beispiel 1: Importieren einer Konfigurationsdatei
```
PS C:\>Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath "C:\MigrationData\LegacyStorSimpleConfig.sse" -TargetDeviceName "8100-123456789" -ConfigDecryptionKey "fWs793hHVhR90NKdDYTeNq"
LegacyConfigId      : e2d5c9b1-b528-4c21-b8ae-533feefc8a41
ImportedOn          : 4/8/2015 7:23:04 PM
ConfigFile          : D:\configs\StorSimpleConfig_27_Mar_15_12_19.xml.sse
TargetApplianceName : Arunkm-N4
Details             : Available Cloud Configuration(s) for migration : 
                          Cloud Configuration(s) 1    : TC8Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 2    : fulle_cc4
                          Cloud Configuration(s) 3    : fulle_cc2
                          Cloud Configuration(s) 4    : fulle_cc3
                          Cloud Configuration(s) 5    : TC9Cloud[Stingray18-FP3] 
                          Cloud Configuration(s) 6    : fulle_cc1
                          Cloud Configuration(s) 7    : Container-New[Stingray19-FP6] 
                          Cloud Configuration(s) 8    : TC6Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 9    : TC7Cloud[Stingray18-FP3] 

Result              : Successfully imported config from the legacy appliance! 
Save the legacy config id and cloud configuration(s) for future reference.
```

Mit diesem Befehl wird die Konfigurationsdatei im angegebenen Pfad importiert.
Der Befehl enthält den Schlüssel zum Entschlüsseln der Datei.

## Parameter

### -ConfigDecryptionKey
Gibt den Entschlüsselungsschlüssel für die Konfiguration der Legacy-Appliance an.

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

### -ConfigFilePath
Gibt den absoluten Pfad der abzurufenden Konfigurationsdatei an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: FilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Gibt ein Azure-Profil an.

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

### -TargetDeviceName
Gibt den Namen des Zielgeräts an, wie es im Portal angezeigt wird.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### LegacyApplianceConfiguration
Dieses Cmdlet gibt die Details der Konfiguration zurück.
Das **LegacyApplianceConfiguration** -Objekt enthält die folgenden Informationen: Konfigurations-ID, Volumen Containernamen, Zugriffssteuerungseinträge, Sicherungsrichtlinien, Bandbreiteneinstellungen, Volumen Container, Anmeldeinformationen für das Speicherkonto und Volumes.

## Notizen

## Verwandte Links

[Importieren-AzureStorSimpleLegacyVolumeContainer](./Import-AzureStorSimpleLegacyVolumeContainer.md)


