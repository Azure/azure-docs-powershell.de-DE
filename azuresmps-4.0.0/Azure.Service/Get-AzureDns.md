---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 184FB33A-C866-4AF0-BA31-8ADCFC6EE8E2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15ce5d8511383ad93e288b97381416d7864c3f80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005852"
---
# Get-AzureDns

## Synopsis
Ruft die DNS-Einstellungen für eine Azure-Bereitstellung ab.

## Syntax

```
Get-AzureDns [-DnsSettings <DnsSettings>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureDns** " Ruft die DNS-Einstellungen für eine Azure-Bereitstellung ab.
Das Cmdlet gibt den Anzeigenamen und die IP-Adresse des DNS-Servers in einem DNS-Einstellungsobjekt zurück.

## Beispiele

### Beispiel 1: Abrufen von DNS-Einstellungen
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Production" | Get-AzureDNS
```

Dieser Befehl verwendet das Cmdlet " **Get-AzureDeployment** ", um die Produktionsbereitstellung des Diensts mit dem Namen ContosoService zu erhalten.
Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet ruft die DNS-Einstellungen ab.

## Parameter

### -DnsSettings
Gibt ein **DnsSettings** -Objekt an.

```yaml
Type: DnsSettings
Parameter Sets: (All)
Aliases: InputObject

Required: False
Position: Named
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Add-AzureDns](./Add-AzureDns.md)

[Get-AzureDeployment](./Get-AzureDeployment.md)

[Neu – AzureDns](./New-AzureDns.md)

[Remove-AzureDns](./Remove-AzureDns.md)

[Satz-AzureDns](./Set-AzureDns.md)


