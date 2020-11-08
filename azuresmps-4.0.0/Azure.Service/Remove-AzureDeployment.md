---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D6D54096-670D-43E4-93EB-24C8FBA199A4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2db1d7a6bc87c694cf06ea1fef0a886c61734a75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006371"
---
# Remove-AzureDeployment

## Synopsis
Löscht eine Bereitstellungeines Cloud-Diensts.

## Syntax

```
Remove-AzureDeployment [-ServiceName] <String> [-Slot] <String> [-DeleteVHD] [-Force]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureDeployment** löscht eine Bereitstellungeines Azure Cloud-Diensts.
Wenn Sie eine Bereitstellung löschen möchten, müssen Sie Sie zuerst anhalten.

## Beispiele

### Beispiel 1: Entfernen einer Bereitstellung
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService"
```

Dieser Befehl entfernt die Bereitstellung des Azure-Diensts mit dem Namen ContosoService.
Da dieser Befehl keinen Steckplatz angibt, wird der Dienst aus der Produktionsumgebung entfernt.

### Beispiel 2: Entfernen einer Bereitstellung und virtueller Festplatten
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService" -DeleteVHD
```

Mit diesem Befehl wird die Bereitstellung des Diensts mit dem Namen ContosoService aus der Produktionsumgebung entfernt.
Der Befehl entfernt auch die zugrunde liegenden virtuellen Festplatten.

## Parameter

### -DeleteVHD
Gibt an, dass dieses Cmdlet die Bereitstellung und die virtuellen Festplatten (VHD) aus dem BLOB-Speicher entfernt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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

### -ServiceName
Gibt den Namen des Diensts an, für den das Cmdlet eine Bereitstellung löscht.

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
Gibt die Bereitstellungsumgebung an, aus der dieses Cmdlet die Bereitstellung löscht.
Gültige Werte sind: Staging und Production.
Der Standardwert ist Production.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### ManagementOperationContext

## Notizen

## Verwandte Links

[Get-AzureDeployment](./Get-AzureDeployment.md)

[Get-AzureDeploymentEvent](./Get-AzureDeploymentEvent.md)

[Verschieben-AzureDeployment](./Move-AzureDeployment.md)

[Neu – AzureDeployment](./New-AzureDeployment.md)

[Satz-AzureDeployment](./Set-AzureDeployment.md)


