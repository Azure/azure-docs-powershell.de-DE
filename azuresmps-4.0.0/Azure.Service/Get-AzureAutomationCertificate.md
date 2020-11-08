---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FED10AA9-DD3A-4034-B78E-F9E55290B353
online version: ''
schema: 2.0.0
ms.openlocfilehash: 272969751988d3747788c2a214e8eb7ed509f232
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005869"
---
# Get-AzureAutomationCertificate

## Synopsis

Ruft ein Azure-Automatisierungs Zertifikat ab.

## Syntax

### Seitensaller (Standard)
```
Get-AzureAutomationCertificate -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByCertificateName
```
Get-AzureAutomationCertificate -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

Das Cmdlet " **Get-AzureAutomationCertificate** " ruft mindestens ein Microsoft Azure-Automatisierungs Zertifikat ab.
Standardmäßig werden alle Zertifikate zurückgegeben.
Um ein bestimmtes Zertifikat abzurufen, geben Sie dessen Namen an.

## Beispiele

### Beispiel 1: Abrufen aller Zertifikate
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17"
```

Dieser Befehl ruft alle Zertifikate im Azure Automation-Konto mit dem Namen Contoso17 ab.

### Beispiel 2: Abrufen eines Zertifikats
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyUserCertificate"
```

Dieser Befehl ruft das Zertifikat mit dem Namen MyUserCertificate ab.

## Parameter

### -AutomationAccountName
Gibt den Namen des Automatisierungs Kontos mit dem Zertifikat an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen eines Zertifikats an, das abgerufen werden soll.

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: 

Required: True
Position: Named
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. CertificateInfo

## Notizen

## Verwandte Links

[Neu – AzureAutomationCertificate](./New-AzureAutomationCertificate.md)

[Remove-AzureAutomationCertificate](./Remove-AzureAutomationCertificate.md)

[Satz-AzureAutomationCertificate](./Set-AzureAutomationCertificate.md)


