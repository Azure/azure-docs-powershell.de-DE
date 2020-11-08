---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5BEE9430-D6BF-49F1-A23D-32784C6C818E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 98b9abe6bcb9998067fe978a5f99f5d8b64cd26d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006537"
---
# Get-AzurePublicIP

## Synopsis
Ruft die öffentlichen IP-Informationen für einen virtuellen Azure-Computer ab.

## Syntax

```
Get-AzurePublicIP [[-PublicIPName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzurePublicIP** " Ruft die öffentlichen IP-Informationen für einen virtuellen Azure-Computer ab.
Um die IP-Adresse der öffentlichen IP-Adresse abzurufen, verwenden Sie das Cmdlet **Get-AzureVM** .

## Beispiele

### Beispiel 1: Abrufen der öffentlichen IP-Konfiguration
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Get-AzurePublicIP
```

Dieser Befehl ruft den virtuellen Computer mit dem Namen FTPInstance im Dienst FTPInAzure mit dem Cmdlet **Get-AzureVM** ab.
Der Befehl übergibt diesen virtuellen Computer mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet ruft die öffentliche IP-Konfiguration vom virtuellen Computer ab.

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

### -PublicIPName
Gibt den öffentlichen IP-Namen an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Gibt den virtuellen Computer an, für den dieses Cmdlet die öffentliche IP-Konfiguration erhält.

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

### Microsoft. WindowsAzure. Commands. Servicemanagement. AssignPublicIPCollection

## Notizen

## Verwandte Links

[Get-AzureVM](./Get-AzureVM.md)

[Remove-AzurePublicIP](./Remove-AzurePublicIP.md)

[Satz-AzurePublicIP](./Set-AzurePublicIP.md)


