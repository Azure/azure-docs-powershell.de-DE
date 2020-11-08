---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C263CCAD-E51F-420E-9AD4-4FAC09C99CB1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3c10a7694034fe4400ed415891e74f7089ce8558
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006318"
---
# Remove-AzureServiceRemoteDesktopExtension

## Synopsis
Entfernt die auf alle Rollen oder benannten Rollen angewendete Cloud-Dienst-Remote Desktop Erweiterung in einem angegebenen Bereitstellungs Steckplatz.

## Syntax

### RemoveByRoles (Standard)
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### RemoveAllRoles
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>]
 [-UninstallConfiguration] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureServiceRemoteDesktopExtension** entfernt die Remote Desktop Erweiterung des Cloud-Diensts, die für alle Rollen oder benannten Rollen in einem bestimmten Bereitstellungs Steckplatz angewendet wurde.

## Beispiele

### Beispiel 1: Entfernen der Remote Desktop Erweiterung
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc
```

Mit diesem Befehl wird die Remote Desktop Erweiterung entfernt.

### Beispiel 2: Entfernen der Remote Desktop Erweiterung von einer angegebenen Rolle
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc -Role "WebRole1"
```

Mit diesem Befehl wird die Remote Desktop Erweiterung von einer angegebenen Rolle entfernt.

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

### -Role
Gibt ein optionales Array von Rollen an, für die die Remote Desktopkonfiguration angegeben werden soll.
Wenn nicht angegeben, wird die Remote Desktopkonfiguration als Standardkonfiguration für alle Rollen verwendet.

```yaml
Type: String[]
Parameter Sets: RemoveByRoles
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Gibt den Azure-Dienstnamen der Bereitstellung an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
Gibt die Umgebung der Bereitstellung an, die geändert werden soll.
Unterstützte Werte sind "Production" oder "Staging".

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UninstallConfiguration
Gibt an, dass dieses Cmdlet alle RDP-Konfigurationen aus dem clouddienst deinstalliert.

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 2
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

[Satz-AzureServiceRemoteDesktopExtension](./Set-AzureServiceRemoteDesktopExtension.md)


