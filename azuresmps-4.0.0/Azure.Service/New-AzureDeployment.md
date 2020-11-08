---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2BDB255A-EFB3-4580-BE95-187008DB208C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21195f6d3ed938844717789f8a0df16f49fbd85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006135"
---
# New-AzureDeployment

## Synopsis
Erstellt eine Bereitstellung aus einem Dienst.

## Syntax

```
New-AzureDeployment [-ServiceName] <String> [-Package] <String> [-Configuration] <String> [-Slot] <String>
 [[-Label] <String>] [[-Name] <String>] [-DoNotStart] [-TreatWarningsAsError]
 [-ExtensionConfiguration <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureDeployment** erstellt eine Azure-Bereitstellung von einem Dienst, der Webrollen und worker-Rollen umfasst.
Dieses Cmdlet erstellt eine Bereitstellung auf der Grundlage einer Paketdatei (cspkg) und einer Dienstkonfigurationsdatei (. cscfg).
Geben Sie einen Namen an, der innerhalb der Bereitstellungsumgebung eindeutig ist.

Verwenden Sie das Cmdlet **New-AzureVM** , um eine Bereitstellung basierend auf Azure Virtual Machines zu erstellen.

## Beispiele

### Beispiel 1: Erstellen einer Bereitstellung
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Label "ContosoDeployment"
```

Dieser Befehl erstellt eine Produktionsbereitstellung auf der Grundlage eines Pakets mit dem Namen "ContosoPackage. cspkg" und einer Konfiguration mit dem Namen ContosoConfiguration. cscfg.
Der Befehl gibt eine Bezeichnung für die Bereitstellung an.
Es wird kein Name angegeben.
Mit diesem Cmdlet wird eine GUID als Name erstellt.

### Beispiel 2: Erstellen einer Bereitstellung auf der Grundlage einer Erweiterungskonfiguration
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

Dieser Befehl erstellt eine Produktionsbereitstellung auf der Grundlage eines Pakets und einer Konfiguration.
Der Befehl gibt eine Erweiterungskonfiguration mit dem Namen "ContosoExtensionConfig. cscfg" an.
Dieses Cmdlet erstellt GUIDs als Namen und Beschriftung.

## Parameter

### -Konfiguration
Gibt den vollständigen Pfad einer Dienst Konfigurationsdatei an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DoNotStart
Gibt an, dass dieses Cmdlet die Bereitstellung nicht startet.

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

### -ExtensionConfiguration
Gibt ein Array von Erweiterungs Konfigurationsobjekten an.

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Label
Gibt einen Etikettennamen für die Bereitstellung an.
Wenn Sie keine Beschriftung angeben, verwendet dieses Cmdlet eine GUID.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt einen Bereitstellungsnamen an.
Wenn Sie keinen Namen angeben, verwendet dieses Cmdlet eine GUID.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Paket
Gibt den Pfad oder URI einer cspkg-Datei im Speicher innerhalb desselben Abonnements oder Projekts an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

### -ServiceName
Gibt den Namen des Azure-Diensts für die Bereitstellung an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
Gibt die Umgebung an, in der dieses Cmdlet die Bereitstellung erstellt.
Gültige Werte sind: Staging und Production.
Der Standardwert ist Production.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TreatWarningsAsError
Gibt an, dass Warnmeldungen Fehler sind.
Wenn Sie diesen Parameter angeben, führt eine Warnmeldung dazu, dass die Bereitstellung fehlschlägt.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureDeployment](./Get-AzureDeployment.md)

[Get-AzureDeploymentEvent](./Get-AzureDeploymentEvent.md)

[Verschieben-AzureDeployment](./Move-AzureDeployment.md)

[Neu – AzureVM](./New-AzureVM.md)

[Remove-AzureDeployment](./Remove-AzureDeployment.md)

[Satz-AzureDeployment](./Set-AzureDeployment.md)


