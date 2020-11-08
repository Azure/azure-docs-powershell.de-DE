---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B935B615-1200-4A83-95AF-4F17785793B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a331f3e0ff2797b84c241e64872e3af0841cb106
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006450"
---
# Move-AzureDeployment

## Synopsis
Tauscht Bereitstellungen zwischen Produktion und Staging aus.

## Syntax

```
Move-AzureDeployment [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Move-AzureDeployment** tauscht die virtuellen IP-Adressen von Bereitstellungen in Produktions-und Staging-Umgebungen aus.
Mit diesem Cmdlet wird eine Bereitstellung, die derzeit in der Stagingumgebung ausgeführt wird, in die Produktionsumgebung und eine Bereitstellung, die in der Produktionsumgebung ausgeführt wird, in der Stagingumgebung ausgetauscht.
Wenn in der Stagingumgebung eine Bereitstellung vorhanden ist und keine Bereitstellung in der Produktionsumgebung erfolgt, verschiebt das Cmdlet die Bereitstellung in die Produktionsumgebung.
Wenn eine Bereitstellung in der Produktionsumgebung und keine Bereitstellung in der Stagingumgebung vorhanden ist, schlägt das Cmdlet fehl.

## Beispiele

### Beispiel 1: Austauschen von Bereitstellungen für einen Dienst
```
PS C:\> Move-AzureDeployment -ServiceName "ContosoService"
```

Dieser Befehl tauscht die Bereitstellungen des Diensts mit dem Namen ContosoService zwischen den Produktions-und Staging-Umgebungen aus.

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
Gibt den Namen des Diensts an, für den das Cmdlet Produktions-und Staging-Bereitstellungen vertauscht.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### ManagementOperationContext

## Notizen

## Verwandte Links

[Get-AzureDeployment](./Get-AzureDeployment.md)

[Get-AzureDeploymentEvent](./Get-AzureDeploymentEvent.md)

[Neu – AzureDeployment](./New-AzureDeployment.md)

[Remove-AzureDeployment](./Remove-AzureDeployment.md)

[Satz-AzureDeployment](./Set-AzureDeployment.md)


