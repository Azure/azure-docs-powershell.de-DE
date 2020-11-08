---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 61CF7F95-F0BB-4282-A971-537CB73708B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d5774213054f3e9e56e9804a9319e31f095f868
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005753"
---
# Get-AzureStoreAddOn

## Synopsis
Ruft die verfügbaren Azure Store-Add-ons ab.

## Syntax

### ListAvailable
```
Get-AzureStoreAddOn [-ListAvailable] [-Country <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Getaddon
```
Get-AzureStoreAddOn [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

Ruft alle verfügbaren Add-ons für den Kauf aus dem Azure Store ab oder ruft die vorhandenen Add-on-Instanzen für das aktuelle Abonnement ab.

## Beispiele

### Beispiel 1
```
PS C:\> Get-AzureStoreAddOn
```

In diesem Beispiel werden alle gekauften Add-on-Instanzen für das aktuelle Abonnement abgerufen.

### Beispiel 2
```
PS C:\> Get-AzureStoreAddOn -ListAvailable
```

In diesem Beispiel werden alle verfügbaren Add-ons für den Kauf in den Vereinigten Staaten aus dem Azure Store abgerufen.

### Beispiel 3
```
PS C:\> Get-AzureStoreAddOn -Name MyAddOn
```

In diesem Beispiel wird ein Add-on mit dem Namen myaddon aus der gekauften Add-on-Instanz im aktuellen Abonnement abgerufen.

## Parameter

### -Land
Gibt bei Angabe nur die im angegebenen Land verfügbaren Azure Store-Add-on-Instanzen zurück.
Der Standardwert ist "US".

```yaml
Type: String
Parameter Sets: ListAvailable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ListAvailable
Wenn angegeben, werden die verfügbaren Add-ons für den Kauf aus dem Azure Store abgerufen.

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailable
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt das Add-on zurück, das dem angegebenen Namen entspricht.

```yaml
Type: String
Parameter Sets: GetAddOn
Aliases: 

Required: False
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

## Notizen

## Verwandte Links

[Neu – AzureStoreAddOn](./New-AzureStoreAddOn.md)

[Remove-AzureStoreAddOn](./Remove-AzureStoreAddOn.md)

[Satz-AzureStoreAddOn](./Set-AzureStoreAddOn.md)


