---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A6D5C40-2532-4FD1-A74F-16725CAD8EDD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29d049dbdce93102411a875cfaef8e5fb9c719b6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006601"
---
# Add-AzureCertificate

## Synopsis
Lädt ein Zertifikat in einen Azure Cloud-Dienst hoch.

## Syntax

```
Add-AzureCertificate [-ServiceName] <String> [-CertToDeploy] <Object> [-Password <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Add-AzureCertificate** lädt ein Zertifikat für einen Azure-Dienst hoch.

## Beispiele

### Beispiel 1: Hochladen eines Zertifikats und eines Kennworts
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy ContosoCertificate.pfx -Password "password"
```

Mit diesem Befehl wird die Zertifikatdatei ContosoCertificate. pfx in einen clouddienst hochgeladen.
Der Befehl gibt das Kennwort für das Zertifikat an.

### Beispiel 2: Hochladen einer Zertifikatsdatei
```
PS C:\> Add-AzureCertificate -serviceName "MyService" -CertToDeploy ContosoCertificate.cer
```

Mit diesem Befehl wird die Zertifikatdatei ContosoCertificate. CER in einen clouddienst hochgeladen.
Der Befehl gibt das Kennwort für das Zertifikat an.

### Beispiel 3: Hochladen eines Certificate-Objekts
```
PS C:\> $Certificate = Get-Item cert:\PATTIFULLER\MY\1D6E34B526723E06C235BE8E5457784BF12C9F39
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy $Certificate
```

Der erste Befehl ruft mithilfe des Windows PowerShell Core **Get-Item-** Cmdlets ein Zertifikat aus dem My Store eines Benutzers ab.
Der Befehl speichert das Zertifikat in der $Certificate-Variablen.

Mit dem zweiten Befehl wird das Zertifikat in $Certificate in einen clouddienst hochgeladen.

## Parameter

### -CertToDeploy
Gibt das Zertifikat an, das bereitgestellt werden soll.
Sie können den vollständigen Pfad einer Zertifikatsdatei angeben, beispielsweise eine Datei mit einem *. cer oder *.
PFX-Dateinamenerweiterung oder ein X. 509-Zertifikatobjekt.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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
Gibt das Zertifikat Kennwort an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

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
Gibt den Namen des Azure-Diensts an, dem dieses Cmdlet ein Zertifikat hinzufügt.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### ManagementOperationContext

## Notizen

## Verwandte Links

[Get-AzureCertificate](./Get-AzureCertificate.md)

[Neu – AzureCertificateSetting](./New-AzureCertificateSetting.md)

[Remove-AzureCertificate](./Remove-AzureCertificate.md)


