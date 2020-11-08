---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0DF54C9D-7A19-4591-A1FC-33C6A4C9BF33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 05a99e1a4965329c0eeb29fe0e014814fd1807b2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006143"
---
# Test-AzureName

## Synopsis
Testet, ob ein Microsoft Azure Cloud-Dienstname, ein Speicherdienst Name oder ein ServiceBus-Namespacename vorhanden ist.

## Syntax

### Dienst
```
Test-AzureName [-Service] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Speicher
```
Test-AzureName [-Storage] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ServiceBusNamespace
```
Test-AzureName [-ServiceBusNamespace] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Website
```
Test-AzureName [-Website] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Wenn der Name vorhanden ist, gibt das Cmdlet $true zurück.
Wenn der Name nicht vorhanden ist, wird $false zurückgegeben.

## Beispiele

### Beispiel 1
```
PS C:\> Test-AzureName -Service "MyNameService1"
```

Dieser Befehl testet, ob es sich bei dem "MyNameService1" um einen vorhandenen Microsoft Azure Cloud-Dienstnamen handelt.

### Beispiel 2
```
PS C:\> Test-AzureName -Storage "mystorename1"
```

Dieser Befehl testet, ob es sich bei dem "mystorename1" um einen vorhandenen Microsoft Azure-Speicherdienst Namen handelt.

### Beispiel 3
```
PS C:\> Test-AzureName -ServiceBusNamespace "mynamespace"
```

Dieser Befehl testet, ob es sich bei dem "MyNamespace" um einen vorhandenen Microsoft Azure Service Bus-Namespacenamen handelt.

## Parameter

### -Name
Gibt den Namen des Dienst-oder speicherkontos an, das getestet werden soll.

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

### -Service
Gibt an, dass ein vorhandenes Dienstkonto getestet werden soll.

```yaml
Type: SwitchParameter
Parameter Sets: Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceBusNamespace
Gibt an, dass ein vorhandener ServiceBus-Namespace getestet werden soll.

```yaml
Type: SwitchParameter
Parameter Sets: ServiceBusNamespace
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Speicher
Gibt an, dass ein vorhandenes Speicherkonto getestet werden soll.

```yaml
Type: SwitchParameter
Parameter Sets: Storage
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Website
Gibt an, dass eine vorhandene Website getestet werden soll.

```yaml
Type: SwitchParameter
Parameter Sets: Website
Aliases: 

Required: True
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
* Node-dev, php-dev, python-dev

## Verwandte Links

