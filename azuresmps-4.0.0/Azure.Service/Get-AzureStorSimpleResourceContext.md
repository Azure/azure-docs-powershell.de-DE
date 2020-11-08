---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7CB42968-8F6F-4D84-9AE2-1000F280BF3C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 586abbd5f203ce00f6faa7975d9e2adbd0c7940e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006755"
---
# Get-AzureStorSimpleResourceContext

## Synopsis
Ruft den aktuellen Ressourcenkontext ab.

## Syntax

```
Get-AzureStorSimpleResourceContext [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureStorSimpleResourceContext** " Ruft den aktuellen Ressourcenkontext ab.

## Beispiele

### Beispiel 1: Abrufen des aktuellen Kontexts
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa" 
PS C:\> Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso63-Tsqa
```

Mit dem ersten Befehl wird der aktuelle Kontext mithilfe des Cmdlets **Select-AzureStorSimpleResource** auf die Ressource mit dem Namen "Contoso63-Tsqa" festgelegt.

Der zweite Befehl ruft den aktuellen Ressourcenkontext ab.

### Beispiel 2: Versuch, den aktuellen Kontext abzurufen
```
PS C:\>Get-AzureStorSimpleResourceContext
Get-AzureStorSimpleResourceContext : Resource Context is not set for your subscription. Please use
Select-AzureStorSimpleResource -ResourceName <<name>> to set
```

Mit diesem Befehl wird der aktuelle Kontext abgerufen.
In diesem Beispiel wurde kein Kontext gesetzt.
Der Befehl gibt eine Meldung zurück, die das Problem erläutert.

## Parameter

### -Profil
Gibt ein Azure-Profil an.

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

### Keine

## Ausgaben

### StorSimpleResourceContext
Dieses Cmdlet gibt ein **resourcecontext** -Objekt zurück.

## Notizen

## Verwandte Links

[Get-AzureStorSimpleResource](./Get-AzureStorSimpleResource.md)

[SELECT-AzureStorSimpleResource](./Select-AzureStorSimpleResource.md)


