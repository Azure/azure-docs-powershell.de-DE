---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95298AFC-B492-4EA6-AFC2-E862D3086AF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84b1256d7d911d22a4f1344bdf841943ce87ee7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006322"
---
# Remove-AzureServiceDiagnosticsExtension

## Synopsis
Entfernt die Erweiterung für die Cloud-Dienst Diagnose, die für alle Rollen oder benannten Rollen in einem bestimmten Bereitstellungs Steckplatz angewendet wurde.

## Syntax

### RemoveByRoles (Standard)
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### RemoveAllRoles
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureServiceDiagnosticsExtension** entfernt die auf alle Rollen oder benannten Rollen angewendete Cloud Service Diagnostics-Erweiterung in einem bestimmten Bereitstellungs Steckplatz.

## Beispiele

### Beispiel 1: Entfernen der Diagnose Erweiterung für einen Dienst
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc
```

Mit diesem Befehl wird die Diagnose Erweiterung für eine angegebene Rolle entfernt.

### Beispiel 2: Entfernen der Diagnose Erweiterung für einen Dienst in einer angegebenen Rolle
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc -Role "WebRole01"
```

Mit diesem Befehl wird die Diagnose Erweiterung für eine angegebene Rolle entfernt.

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
Gibt ein optionales Array von Rollen an, für das die Remote Desktopkonfiguration angegeben werden soll.
Wenn Sie diesen Parameter nicht angeben, wird die Remote Desktopkonfiguration als Standardkonfiguration für alle Rollen verwendet.

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
Gültige Werte sind Production oder Staging.

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
Gibt an, dass dieses Cmdlet alle RDP-Konfigurationen vom clouddienst deinstalliert.

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

[Get-AzureServiceDiagnosticsExtension](./Get-AzureServiceDiagnosticsExtension.md)

[Satz-AzureServiceDiagnosticsExtension](./Set-AzureServiceDiagnosticsExtension.md)


