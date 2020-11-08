---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E771D1F2-A06B-44BB-AAFF-9459DC6303E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 273edfe08e4d2476cd4c1baa2967a829ec1bbcc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005654"
---
# Select-AzureStorSimpleResource

## Synopsis
Legt eine Ressource als aktuelle Ressource fest.

## Syntax

```
Select-AzureStorSimpleResource -ResourceName <String> [-RegistrationKey <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Select-AzureStorSimpleResource** legt eine Ressource als aktuelle Ressource fest.
Nachdem Sie eine Ressource ausgewählt haben, gelten andere Cmdlets innerhalb dieses Ressourcen Kontexts.

## Beispiele

### Beispiel 1: Erstmaliges Auswählen einer Ressource
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa" -RegistrationKey "<your registration key>"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

Dieser Befehl wählt die Ressource mit dem Namen Contoso64-Tsqa als aktuellen Kontext aus.
In diesem Beispiel hat der Computer diesen Kontext nicht zuvor initialisiert, und daher müssen Sie einen Wert für den *RegistrationKey* -Parameter angeben.

### Beispiel 2: Versuch, eine Ressource auszuwählen
```
This command gets the current context for this computer by using the **Get-AzureStorSimpleResourceContext** cmdlet. The current selected resource is Contoso64-Tsqa. This is consistent with the previous example. 
PS C:\>Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa 

This command attempts to reset the resource to be Contoso02-Resource. For this example, this resource has not been previously selected. The registration key is not saved or included in the command. The command cannot select the resource. 
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso02-Resource"
Select-AzureStorSimpleResource : Could not find the persisted secret. Please use Select-AzureStorSimpleResource and
provide the Registration key once again.
```

### Beispiel 3: Auswählen einer zuvor ausgewählten Ressource
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

Dieser Befehl wählt die Ressource mit dem Namen Contoso64-Tsqa als aktuellen Kontext aus.
In diesem Beispiel wurde dieser Kontext zuvor ausgewählt, und Sie müssen daher keinen Wert für den *RegistrationKey* -Parameter angeben.

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

### -RegistrationKey
Gibt einen Registrierungsschlüssel an.
Geben Sie einen Schlüssel an, wenn Sie eine Ressource zum ersten Mal auswählen.
Nachdem dieses Cmdlet die aktuelle Ressource ausgewählt hat, verwenden Cmdlets diesen Schlüssel nach Bedarf.
Weitere Informationen finden Sie unter [Abrufen des Dienst Registrierungsschlüssels](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  ( https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) im Microsoft Developer Network.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceName
Gibt den Namen der Ressource an, die als aktuelle Ressource ausgewählt werden soll.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### StorSimpleResourceContext
Dieses Cmdlet gibt ein **StorSimpleResourceContext** -Objekt zurück, das Details für den Ressourcenkontext enthält.

## Notizen

## Verwandte Links

[Get-AzureStorSimpleResource](./Get-AzureStorSimpleResource.md)

[Get-AzureStorSimpleResourceContext](./Get-AzureStorSimpleResourceContext.md)


