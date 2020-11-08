---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8EF86C66-498F-4183-9070-F178628483F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91c32ca5207efdff7fa65fbba599f44d276dab6d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006536"
---
# Get-AzureRemoteAppCollectionUsageSummary

## Synopsis
Ruft eine Zusammenfassung der Verwendung für eine Azure RemoteApp-Sammlung ab.

## Syntax

```
Get-AzureRemoteAppCollectionUsageSummary [-CollectionName] <String> [[-UsageMonth] <String>]
 [[-UsageYear] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRemoteAppCollectionUsageSummary** " Ruft eine Zusammenfassung der Verwendung für eine Azure RemoteApp-Sammlung ab.

## Beispiele

### Beispiel 1: Abrufen einer Verwendungszusammenfassung
```
PS C:\> Get-AzureRemoteAppCollectionUsageSummary -CollectionName Contoso -UsageMonth 12 -UsageYear 2014
```

Dieser Befehl ruft eine Zusammenfassung der Verwendung für den Monat Dezember im Jahr 2014 für eine Sammlung mit dem Namen contoso ab.

## Parameter

### -CollectionName
Gibt den Namen der Azure RemoteApp-Sammlung an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
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

### -UsageMonth
Gibt eine zweistellige Zahl für den Monat an, für den eine Verwendungszusammenfassung abgerufen werden soll.
Wenn dieser Parameter nicht angegeben ist, stellt dieses Cmdlet die Verwendung für den aktuellen Monat bereit.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UsageYear
Gibt das vierstellige Jahr an, für das eine Verwendungszusammenfassung abgerufen werden soll.
Wenn dieser Parameter nicht angegeben ist, wird mit diesem Cmdlet eine Verwendungszusammenfassung für das aktuelle Jahr verwendet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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

[Get-AzureRemoteAppCollection](./Get-AzureRemoteAppCollection.md)

[Get-AzureRemoteAppCollectionUsageDetails](./Get-AzureRemoteAppCollectionUsageDetails.md)


