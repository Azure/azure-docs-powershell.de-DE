---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2171943B-D1AC-45FD-99FD-DD0C14AFC60C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38990d3084cf5f494dc811ec6fe458003b8313c9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006561"
---
# Get-AzureDeployment

## Synopsis
Ruft Details einer Bereitstellung ab.

## Syntax

```
Get-AzureDeployment [-ServiceName] <String> [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureDeployment** " ruft Details einer Azure-Bereitstellung ab.
Geben Sie den Namen des Azure-Diensts und den Steckplatz der Bereitstellung an.

## Beispiele

### Beispiel 1: Abrufen von Details für eine Produktionsbereitstellung
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService"
```

Dieser Befehl gibt die Details der Bereitstellung für den Dienst mit dem Namen ContosoService zurück.
Mit diesem Befehl wird kein Steckplatz angegeben.
Daher verwendet der Befehl den Standardwert von Production.

### Beispiel 2: Abrufen von Details für eine Staging-Bereitstellung
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Staging"
```

Dieser Befehl gibt die Details der Staging-Bereitstellung von ContosoService zurück.

## Parameter

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

### -ServiceName
Gibt den Namen des Diensts an.

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
Gibt die Umgebung der Bereitstellung an.
Gültige Werte sind: Staging oder Production.
Der Standardwert ist Production.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
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

[Get-AzureDeploymentEvent](./Get-AzureDeploymentEvent.md)

[Verschieben-AzureDeployment](./Move-AzureDeployment.md)

[Neu – AzureDeployment](./New-AzureDeployment.md)

[Remove-AzureDeployment](./Remove-AzureDeployment.md)

[Satz-AzureDeployment](./Set-AzureDeployment.md)


