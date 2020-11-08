---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 268D3E91-AB0F-451F-93B2-9226985910B9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41648470b76d889c1ee9d47e4200f843e9f11522
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006055"
---
# Set-AzureVMPuppetExtension

## Synopsis
Legt die Marionetten Erweiterung für einen virtuellen Computer fest.

## Syntax

```
Set-AzureVMPuppetExtension [-PuppetMasterServer] <String> [[-Version] <String>] [-Disable]
 [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzureVMPuppetExtension** " legt die Marionetten Erweiterung für einen virtuellen Computer fest.

## Beispiele

### Beispiel 1: Einrichten der Marionetten Erweiterung für einen virtuellen Computer
```
PS C:\> Set-AzureVMPuppetExtension -VM $VM
```

In diesem Beispiel wird die Marionetten Erweiterung für den angegebenen virtuellen Computer so festgelegt, wie er in der Variablen $VM gespeichert ist.

## Parameter

### -Deaktivieren Sie
Gibt an, dass dieses Cmdlet den Erweiterungszustand deaktiviert.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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

### -PuppetMasterServer
Gibt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Marionetten Masterservers an.

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

### -ReferenceName
Gibt den Verweisnamen der Erweiterung an.

Hierbei handelt es sich um eine benutzerdefinierte Zeichenfolge, die verwendet wird, um auf eine Erweiterung zu verweisen.
Sie wird angegeben, wenn die Erweiterung zum ersten Mal dem virtuellen Computer hinzugefügt wird.
Für nachfolgende Updates müssen Sie den zuvor verwendeten Verweisnamen angeben, wenn Sie die Erweiterung aktualisieren.
Der Verweisname, der einer Erweiterung zugewiesen ist, wird mit dem Cmdlet **Get-AzureVM** zurückgegeben.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Gibt die Erweiterungsversion an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
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

[Get-AzureVM](./Get-AzureVM.md)


