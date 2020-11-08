---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7F51F534-6C64-4983-A08F-4732A39C2E7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c62f3d29b4cd2c87fd5606ca013eb03958fb62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006270"
---
# Set-AzureDeployment

## Synopsis
Ändert den Status, die Konfigurationseinstellungen oder den Aktualisierungsmodus einer Bereitstellung.

## Syntax

### Upgrade
```
Set-AzureDeployment [-Upgrade] [-ServiceName] <String> [-Package] <String> [-Configuration] <String>
 [-Slot] <String> [[-Mode] <String>] [[-Label] <String>] [[-RoleName] <String>] [-Force]
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Config
```
Set-AzureDeployment [-Config] [-ServiceName] <String> [-Configuration] <String> [-Slot] <String>
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Status
```
Set-AzureDeployment [-Status] [-ServiceName] <String> [-Slot] <String> [-NewStatus] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **festlegen-AzureDeployment** " werden der Status, die Konfigurationseinstellungen oder der Upgrademodus einer Azure-Bereitstellung geändert.
Sie können den Status der Bereitstellung entweder auf "ausgeführt" oder "angehalten" ändern.
Sie können die cscfg-Datei für die Bereitstellung ändern.
Sie können den Aktualisierungsmodus und Konfigurationsdateien aktualisieren.
Verwenden Sie das Cmdlet " **Satz-AzureWalkUpgradeDomain** ", um ein Upgrade zu initiieren.

## Beispiele

### Beispiel 1: Ändern des Status einer Bereitstellung
```
PS C:\> Set-AzureDeployment -Status -ServiceName "ContosoService" -Slot "Production" -NewStatus "Running"
```

Dieser Befehl legt den Status der Bereitstellung für den Dienst mit dem Namen ContosoService in der Produktionsumgebung auf Running fest.

### Beispiel 2: Zuweisen einer anderen Konfigurationsdatei zu einer Bereitstellung
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Slot "Staging" -Configuration "C:\Temp\MyServiceConfig.Cloud.csfg"
```

Dieser Befehl weist in der Stagingumgebung eine andere Konfigurationsdatei für die Bereitstellung des Diensts mit dem Namen "ContosoService" zu.

### Beispiel 3: Einrichten des Upgrademodus auf "automatisch"
```
PS C:\> Set-AzureDeployment -Upgrade -ServiceName "ContosoService" -Mode Auto -Package "C:\packages\ContosoApp.cspkg" -Configuration "C:\Config\ContosoServiceConfig.Cloud.csfg"
```

Mit diesem Befehl wird der Aktualisierungsmodus auf Auto festgelegt, und es wird ein Upgrade-Paket und eine neue Konfigurationsdatei angegeben.

### Beispiel 4: Installieren der Erweiterungskonfiguration in einem Dienst
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Mode "Automatic" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Slot "Production" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

Mit diesem Befehl wird die Erweiterungskonfiguration im angegebenen cloudbasierten Dienst installiert und auf Rollen angewendet.

## Parameter

### -Config
Gibt an, dass dieses Cmdlet die Konfiguration der Bereitstellung ändert.

```yaml
Type: SwitchParameter
Parameter Sets: Config
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Konfiguration
Gibt den vollständigen Pfad einer cscfg-Konfigurationsdatei an.
Sie können eine Konfigurationsdatei für eine Upgrade-oder Konfigurationsänderung angeben.

```yaml
Type: String
Parameter Sets: Upgrade, Config
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtensionConfiguration
Gibt ein Array von Erweiterungs Konfigurationsobjekten an.

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: Upgrade, Config
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Gibt an, dass das Cmdlet ein erzwungenes Upgrade ausführt.

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 8
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

### -Label
Gibt eine Bezeichnung für die aktualisierte Bereitstellung an.

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Modus
Gibt den Aktualisierungsmodus an.
Gültige Werte sind: 

- Auto 
- Manuell 
- Gleichzeitiges

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Statusanzeige
Gibt den Zielstatus für die Bereitstellung an.
Gültige Werte sind: wird ausgeführt und angehalten.

```yaml
Type: String
Parameter Sets: Status
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Paket
Gibt den vollständigen Pfad einer Upgrade-Paketdatei an.

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 2
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

### -RoleName
Gibt den Namen der Rolle an, die aktualisiert werden soll.

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceName
Gibt den Namen des Azure-Diensts der Bereitstellung an.

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

### -Slot
Gibt die Umgebung der Bereitstellung an, die geändert werden soll.
Gültige Werte sind: Production und Staging.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Status
Gibt an, dass mit diesem Cmdlet der Status der Bereitstellung geändert wird.

```yaml
Type: SwitchParameter
Parameter Sets: Status
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Upgrade
Gibt an, dass dieses Cmdlet die Bereitstellung aktualisiert.

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 0
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

[Neu – AzureDeployment](./New-AzureDeployment.md)

[Remove-AzureDeployment](./Remove-AzureDeployment.md)

[Satz-AzureWalkUpgradeDomain](./Set-AzureWalkUpgradeDomain.md)


