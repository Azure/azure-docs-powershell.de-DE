---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8F881112-3603-4EE7-88A4-ED45040A60AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: ecc71708c0dff8e359813bb01db0f09f2c91a0cb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006017"
---
# Set-AzureVMAccessExtension

## Synopsis
Legt die VMAccess-Erweiterung für einen virtuellen Computer fest.

## Syntax

### EnableAccessExtension (Standard)
```
Set-AzureVMAccessExtension [[-UserName] <String>] [[-Password] <String>] [[-ReferenceName] <String>]
 [[-Version] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### DisableAccessExtension
```
Set-AzureVMAccessExtension [-Disable] [[-ReferenceName] <String>] [[-Version] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### UninstallAccessExtension
```
Set-AzureVMAccessExtension [-Uninstall] [[-ReferenceName] <String>] [[-Version] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureVMAccessExtension** " fügt die VMAccess-Erweiterung des virtuellen Computers zu einem virtuellen Computer hinzu. VMAccess Extension kann verwendet werden, um ein temporäres Kennwort festzulegen, das nach der Anmeldung am Computer sofort geändert werden sollte.

## Beispiele

### Beispiel 1: Festlegung der auf einen angegebenen virtuellen Computer angewendeten VMAccess-Erweiterung
```
PS C:\> Set-AzureVMAccessExtension -VM $VM -UserName $User -Password $PWD;
```

Mit diesem Befehl wird die auf den angegebenen virtuellen Computer angewendete VMAccess-Erweiterung so festgelegt, wie Sie in der Variablen $VM gespeichert ist.

## Parameter

### -Deaktivieren Sie
Gibt an, dass das Cmdlet den Erweiterungszustand auf Disable festlegt.

```yaml
Type: SwitchParameter
Parameter Sets: DisableAccessExtension
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceUpdate
Gibt an, dass dieses Cmdlet eine Konfiguration erneut auf eine Erweiterung anwendet, wenn die Konfiguration nicht aktualisiert wurde.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
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

### -Kennwort
Gibt das Kennwort für das Zurücksetzen der Anmeldeinformationen für den virtuellen Computer an.

```yaml
Type: String
Parameter Sets: EnableAccessExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Gibt den Verweisnamen der Access-Erweiterung an.

Hierbei handelt es sich um eine benutzerdefinierte Zeichenfolge, die verwendet wird, um auf eine Erweiterung zu verweisen.
Sie wird angegeben, wenn die Erweiterung zum ersten Mal dem virtuellen Computer hinzugefügt wird.
Bei nachfolgenden Updates sollten Sie beim Aktualisieren der Erweiterung den zuvor verwendeten Verweisnamen angeben.
Der *Verweisname* , der einer Erweiterung zugewiesen ist, wird mit dem Cmdlet **Get-AzureVM** zurückgegeben.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Deinstallieren
Gibt an, ob dieses Cmdlet die Access-Erweiterung deinstalliert.

```yaml
Type: SwitchParameter
Parameter Sets: UninstallAccessExtension
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserName
Gibt den Benutzernamen an, den dieses Cmdlet verwendet, um die Anmeldeinformationen des virtuellen Computers zurückzusetzen.

```yaml
Type: String
Parameter Sets: EnableAccessExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Gibt die Version der Erweiterung an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureVMAccessExtension](./Get-AzureVMAccessExtension.md)

[Remove-AzureVMAccessExtension](./Remove-AzureVMAccessExtension.md)


