---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C9470E5-21D2-4AF5-9F11-F66F94B133C0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23f4511f8e0439c1581cc388843a37266092f4d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006660"
---
# Remove-AzureVMImage

## Synopsis
Entfernt ein Betriebssystemabbild aus dem Image-Repository.

## Syntax

```
Remove-AzureVMImage [-ImageName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureVMImage** entfernt ein Betriebssystemabbild aus dem Image-Repository.
Standardmäßig wird mit diesem Cmdlet nicht das zugeordnete physische Abbild-BLOB aus dem Speicherkonto gelöscht.
Verwenden Sie den **DeleteVHD** -Parameter, um die zugeordnete virtuelle Festplatte (VHD) zu löschen.

## Beispiele

### Beispiel 1: Entfernen eines Bilds aus dem Bild-Repository
```
PS C:\> Remove-AzureVMImage -ImageName "Image001"
```

Dieser Befehl entfernt das Bild mit dem Namen Image001 aus dem Bild-Repository.

### Beispiel 2: Entfernen eines Bilds aus dem Bild-Repository und auch der VHD
```
PS C:\> Remove-AzureVMImage -ImageName " Image001" -DeleteVHD
```

Mit diesem Befehl wird das Bild mit dem Namen Image001 aus dem Bild-Repository entfernt und auch das physische VHD-Abbild aus dem Speicherkonto gelöscht.

### Beispiel 3: Einrichten eines Abonnement Kontexts und Entfernen aller Bilder
```
PS C:\> $SubsId = &amp;lt;MySubscriptionID&amp;gt;
PS C:\> $Cert = Get-AzureCertificate cert:\LocalMachine\MY\&amp;lt;CertificateThumbprint&amp;gt;
PS C:\> Get-AzureVMImage `
| Where-Object {$_.Label -match "Beta" }`
| Foreach-Object {Remove-AzureVMImage -ImageName $_.name }
```

Mit diesem Befehl wird der Abonnement Kontext festgelegt und dann alle Bilder aus dem Image-Repository entfernt, dessen Beschriftung den Namen Beta enthält.

## Parameter

### -DeleteVHD
Gibt an, dass dieses Cmdlet den physikalischen VHD-Abbild-BLOB aus dem Speicherkonto löscht.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bildname
Gibt das Bild des Betriebssystems oder des virtuellen Computers an, das aus dem Image-Repository entfernt werden soll.

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

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Save-AzureVMImage](./Save-AzureVMImage.md)

[Update-AzureVMImage](./Update-AzureVMImage.md)


