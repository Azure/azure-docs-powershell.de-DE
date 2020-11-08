---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6A280C0B-5F55-4575-9B11-596F497C4305
online version: ''
schema: 2.0.0
ms.openlocfilehash: 71e49425724926848ee69b24f5dfca70df664913
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006332"
---
# Remove-AzureServiceADDomainExtension

## Synopsis
Entfernt die für alle Rollen oder benannten Rollen in einem bestimmten Bereitstellungs Steckplatz angewendete Active Directory-Domänenerweiterung für Cloud-Dienst.

## Syntax

### RemoveByRoles (Standard)
```
Remove-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### RemoveAllRoles
```
Remove-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureServiceADDomainExtension** entfernt die Active Directory (AD)-Domänenerweiterung des Cloud-Diensts, die für alle Rollen oder benannten Rollen in einem bestimmten Bereitstellungs Steckplatz angewendet wurde.

## Beispiele

### Beispiel 1: Entfernen einer AD-Domänenerweiterung
```
PS C:\> Remove-AzureServiceADDomainExtension -ServiceName $Svc
```

Mit diesem Befehl wird die von der $SVC-Variable angegebene Erweiterung entfernt.

### Beispiel 2: Entfernen einer AD-Domänenerweiterung für eine angegebene Rolle
```
PS C:\> Remove-AzureServiceADDomainExtension -ServiceName $Svc -Role "WebRole1"
```

Mit diesem Befehl wird die Diensterweiterung für die angegebene Rolle entfernt.

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
Wenn Sie nicht angegeben wird, wird die AD-Domänenkonfiguration als Standardkonfiguration für alle Rollen verwendet.

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
Gibt den Namen eines Azure-Diensts an.

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
Gültige Werte sind: Production oder Staging.

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
Gibt an, dass dieses Cmdlet alle AD-Domänenkonfigurationen aus dem clouddienst deinstalliert.

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

[Get-AzureServiceADDomainExtension](./Get-AzureServiceADDomainExtension.md)

[Satz-AzureServiceADDomainExtension](./Set-AzureServiceADDomainExtension.md)


