---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9EA98944-1923-4573-991E-3B9CA21004BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f16b51dc8abf5c6243b4b489789d65029acc3c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006354"
---
# Remove-AzurePublicIP

## Synopsis
Entfernt die öffentliche IP-Konfiguration von einem Azure Virtual Machine.

## Syntax

```
Remove-AzurePublicIP [[-PublicIPName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzurePublicIP** entfernt die öffentliche IP-Konfiguration von einem Azure Virtual Machine.

## Beispiele

### Beispiel 1: Entfernen der öffentlichen IP-Konfiguration
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Remove-AzurePublicIP | Update-AzureVM
```

Dieser Befehl ruft den virtuellen Computer mit dem Namen FTPInstance im Dienst FTPInAzure mit dem Cmdlet **Get-AzureVM** ab.
Der Befehl übergibt diesen virtuellen Computer mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet entfernt die öffentliche IP-Konfiguration vom virtuellen Computer.
Der Befehl übergibt den virtuellen Computer an das Cmdlet **Update-AzureVM** , das Ihre Änderungen implementiert.

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
Gibt den virtuellen Computer an, von dem dieses Cmdlet die öffentliche IP-Konfiguration entfernt.

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

### Microsoft. WindowsAzure. Commands. Servicemanagement. Model. IPersistentVM

## Notizen

## Verwandte Links

[Get-AzurePublicIP](./Get-AzurePublicIP.md)

[Get-AzureVM](./Get-AzureVM.md)

[Satz-AzurePublicIP](./Set-AzurePublicIP.md)

[Update-AzureVM](./Update-AzureVM.md)


