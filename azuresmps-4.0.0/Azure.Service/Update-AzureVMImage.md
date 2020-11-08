---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5544F2E2-27EF-4079-8E13-6B85DF2018A2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a71ad8b25a17c1c2933cdcf305ba0b53f67bf0f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006789"
---
# Update-AzureVMImage

## Synopsis
Aktualisiert die Beschriftung eines Betriebssystemabbilds im Bild-Repository.

## Syntax

```
Update-AzureVMImage [-ImageName] <String> [-Label] <String> [[-Eula] <String>] [[-Description] <String>]
 [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>]
 [[-DiskConfig] <VirtualMachineImageDiskConfigSet>] [[-Language] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-DontShowInGui] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Update-AzureVMImage** aktualisiert die Beschriftung eines Betriebssystemabbilds im Bild-Repository.
Sie gibt ein Image-Objekt mit Informationen über das aktualisierte Bild zurück.

## Beispiele

### Beispiel 1: Aktualisieren eines Bilds durch Ändern der Bildbeschriftung
```
PS C:\> Update-AzureVMImage -ImageName "Windows-Server-2008-SP2" -Label "DoNotUse"
```

Dieser Befehl aktualisiert das Bild mit dem Namen Windows-Server-2008-SP2 durch Ändern der Bildbeschriftung in DoNotUse.

### Beispiel 2: Abrufen aller Betriebssysteme nach Beschriftung und Aktualisieren der Bezeichnung
```
PS C:\> Get-AzureVMImage | Where-Object {$_.Label -eq "DoNotUse" } | Update-AzureVMImage -Label "Updated"
```

Dieser Befehl ruft alle Betriebssystem Bilder mit der Bezeichnung "DoNotUse" ab und ändert die Beschriftung in "aktualisiert".

## Parameter

### -Beschreibung
Gibt die Beschreibung des Betriebssystemabbilds an.

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

### -DiskConfig
Gibt den Betriebssystemdatenträger und die Datenträgerkonfiguration für das Bild des virtuellen Computers an, das mit den Cmdlets **New-AzureVMImageDiskConfigSet** , **AzureVMImageOSDiskConfig** und **festgelegt** wurde.

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DontShowInGui
Gibt an, dass dieses Cmdlet das Bild nicht in der GUI anzeigt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EULA
Gibt den Endbenutzer-Lizenzvertrag an.
Wir empfehlen, dass es sich bei dem Wert um eine URL handelt.

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

### -IconName
Gibt den Standardsymbolnamen für das Betriebssystem oder das Bild des virtuellen Computers an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: IconUri

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Imagefamily
Gibt einen Wert an, der zum Gruppieren von Bildern des Betriebssystem-oder virtuellen Computers verwendet werden kann.

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

### -Bildname
Gibt den Namen des Bilds an, das im Bild-Repository aktualisiert werden soll.

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
Gibt die neue Beschriftung des Bilds an.

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

### – Sprache
Gibt die Sprache für das Betriebssystem auf dem virtuellen Computer oder dem Betriebssystemabbild an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PrivacyUri
Gibt den URI an, der auf ein Dokument verweist, das die Datenschutzrichtlinie enthält, die sich auf das Betriebssystemabbild bezieht.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
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

### -PublishedDate
Gibt das Datum an, an dem das Betriebssystemabbild dem Image-Repository hinzugefügt wurde.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecommendedVMSize
Gibt die Größe des virtuellen Computers an.

Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Mittel
- Große
- Extra Large
- A5
- A6
- A7

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SmallIconName
Gibt den kleinen Symbolnamen für das Betriebssystem oder das Bild des virtuellen Computers an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SmallIconUri

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### OSImageContext

## Notizen

## Verwandte Links

[Add-AzureVMImage](./Add-AzureVMImage.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Remove-AzureVMImage](./Remove-AzureVMImage.md)

[Save-AzureVMImage](./Save-AzureVMImage.md)

[Neu – AzureVMImageDiskConfigSet](./New-AzureVMImageDiskConfigSet.md)

[Satz-AzureVMImageOSDiskConfig](./Set-AzureVMImageOSDiskConfig.md)

[Satz-AzureVMImageDataDiskConfig](./Set-AzureVMImageDataDiskConfig.md)


