---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E3D405D-69FB-42C2-8A5B-BDBD27B63088
online version: ''
schema: 2.0.0
ms.openlocfilehash: 503c2e0a076be3f31b6435a30dc658af9b45835a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006373"
---
# Remove-AzureCertificate

## Synopsis
Entfernt ein Zertifikat aus einem Azure-Dienst.

## Syntax

```
Remove-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureCertificate** entfernt ein Zertifikat aus einem Azure-Dienst.

## Beispiele

### Beispiel 1: Entfernen eines Zertifikats aus einem Dienst
```
PS C:\> Remove-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

Dieser Befehl entfernt das Certificate-Objekt, das den angegebenen Fingerabdruck hat, aus dem clouddienst.

### Beispiel 2: Entfernen aller Zertifikate aus einem Dienst
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" | Remove-AzureCertificate
```

Dieser Befehl ruft alle Zertifikate des Diensts mit dem Namen ContosoService mit dem Cmdlet **Get-AzureCertificate** ab.
Der Befehl übergibt jedes Zertifikat mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Dieses Cmdlet entfernt jedes Zertifikat aus dem clouddienst.

### Beispiel 3: Entfernen aller Zertifikate aus einem Dienst, die einen bestimmten Fingerabdruckalgorithmus verwenden
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" -ThumbprintAlgorithm "sha1" | Remove-AzureCertificate
```

Dieser Befehl ruft alle Zertifikate des Diensts mit dem Namen ContosoService ab, die den SHA1-Fingerabdruckalgorithmus verwenden.
Der Befehl übergibt jedes Zertifikat an das aktuelle Cmdlet, wodurch jedes Zertifikat entfernt wird.

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
Gibt den Namen des Azure-Diensts an, aus dem dieses Cmdlet ein Zertifikat entfernt.

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

### -Fingerabdruck
Gibt den Fingerabdruck des Zertifikats an, das vom Cmdlet entfernt wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ThumbprintAlgorithm
Gibt den Algorithmus an, der zum Erstellen des Zertifikat Fingerabdrucks verwendet wird.

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

[Add-AzureCertificate](./Add-AzureCertificate.md)

[Get-AzureCertificate](./Get-AzureCertificate.md)

[Neu – AzureCertificateSetting](./New-AzureCertificateSetting.md)


