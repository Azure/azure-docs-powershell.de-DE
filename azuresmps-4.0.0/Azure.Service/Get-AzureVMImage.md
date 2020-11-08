---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E712421A-FA69-46E7-A0DE-F2734D767F2D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8355e0a1d36a6c1dc5b2ca8172cde5bf94480bbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006738"
---
# Get-AzureVMImage

## Synopsis
Ruft die Eigenschaften für eine oder eine Liste von Betriebssystemen oder ein Bild eines virtuellen Computers im Bild-Repository ab.

## Syntax

```
Get-AzureVMImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureVMImage** " Ruft Eigenschaften für eine oder eine Liste von Betriebssystemen oder ein Bild eines virtuellen Computers im Bild-Repository ab.
Das Cmdlet gibt Informationen zu allen Bildern im Repository oder zu einem bestimmten Bild zurück, wenn sein Bildname angegeben wird.

## Beispiele

### Beispiel 1: Abrufen eines bestimmten Image-Objekts aus dem aktuellen Bild-Repository.
```
PS C:\> Get-AzureVMImage -ImageName Image001
```

Dieser Befehl ruft das Image-Objekt mit dem Namen Image001 aus dem aktuellen Bild-Repository ab.

### Beispiel 2: Abrufen aller Bilder aus dem aktuellen Bild-Repository
```
PS C:\> Get-AzureVMImage
```

Dieser Befehl ruft alle Bilder aus dem aktuellen Bild-Repository ab.

### Beispiel 3: Einrichten des Abonnement Kontexts und Abrufen aller Bilder
```
PS C:\> $SubsId = <MySubscriptionID>
C:\PS>$Cert = Get-AzureCertificate cert:\LocalMachine\MY\<CertificateThumbprint>
C:\PS>$MyOSImages = Get-AzureVMImage
```

Mit diesem Befehl wird der Abonnement Kontext festgelegt und dann alle Bilder aus dem Bild-Repository abgerufen.

## Parameter

### -Bildname
Gibt den Namen des Betriebssystem-oder virtuellen Computer Bilds im Bild-Repository an.
Wenn Sie diesen Parameter nicht angeben, werden alle Bilder zurückgegeben.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Add-AzureVMImage](./Add-AzureVMImage.md)

[Remove-AzureVMImage](./Remove-AzureVMImage.md)

[Save-AzureVMImage](./Save-AzureVMImage.md)

[Update-AzureVMImage](./Update-AzureVMImage.md)


