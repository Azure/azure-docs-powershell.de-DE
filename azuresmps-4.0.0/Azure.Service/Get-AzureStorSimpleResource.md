---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 482E8CD6-C38F-4BD5-8214-016D0D8C7FD0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6381b8e0fac5ebf047122f131af6087d5bb5a9fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005760"
---
# Get-AzureStorSimpleResource

## Synopsis
Ruft alle von Ihnen erstellten Ressourcen ab.

## Syntax

```
Get-AzureStorSimpleResource [-ResourceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureStorSimpleResource** " ruft alle Ressourcen ab, die Sie mithilfe von Azure Portal erstellt haben.
Das Cmdlet ruft Details ab, die Sie zum Herstellen einer Verbindung mit den Ressourcen verwenden können.

## Beispiele

### Beispiel 1: Abrufen aller Ressourcen
```
PS C:\>Get-AzureStorSimpleResource
VERBOSE: ClientRequestId: 5cd61b91-ef40-43b4-986d-156e06d2ed65_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    8838459798595306468  Started
Contoso68-Tsqa                                    2859070203638134681  Started
Contoso73-Tsqa                                    7871392677286863733  Started
Contoso87-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 4 StorSimple resources.
```

Dieser Befehl ruft alle von Ihnen erstellten Ressourcen ab.
In diesem Beispiel gibt es drei Ressourcen.

### Beispiel 2: Abrufen einer Ressource mithilfe Ihres Namens
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa"
VERBOSE: ClientRequestId: efc3c85c-12aa-4345-b6eb-ccc532de4825_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 1 StorSimple resource.
```

Dieser Befehl ruft die Ressource mit dem Namen Contoso63-Tsqa.

### Beispiel 3: Versuch, eine nicht vorhandene Ressource abzurufen
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
VERBOSE: ClientRequestId: 5d08d40b-f9d7-4d43-956f-13f01e89625b_PS
VERBOSE: Invalid input : Could not find a resource named Contoso64-Tsqa in your subscription.
```

Dieser Befehl versucht, die Ressource mit dem Namen Contoso64-Tsqa abzurufen.
Es gibt keine Ressource mit diesem Namen.
In diesem Beispiel wird keine Ressource zurückgegeben.

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

### -ResourceName
Gibt den Namen der Ressource an, die dieses Cmdlet erhält.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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

### IEnumerable \<ResourceCredentials\> , ResourceCredentials
Dieses Cmdlet gibt **ResourceCredentials** -Objekte zurück, die die folgenden Eigenschaften enthalten: 

- **ResourceName**
- **ResouceId**
- **ResourceState**

## Notizen

## Verwandte Links

[Get-AzureStorSimpleResourceContext](./Get-AzureStorSimpleResourceContext.md)

[SELECT-AzureStorSimpleResource](./Select-AzureStorSimpleResource.md)


