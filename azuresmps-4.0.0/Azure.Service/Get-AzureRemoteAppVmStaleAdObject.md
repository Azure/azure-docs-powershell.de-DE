---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: EC6AB7E9-BC9F-4FA2-8172-144C9842D74C
online version: ''
schema: 2.0.0
ms.openlocfilehash: da7ed2c382bfcec8327b291c46a51699b77b9373
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005836"
---
# Get-AzureRemoteAppVmStaleAdObject

## Synopsis
Ruft Objekte in Azure Active Directory ab, die Azure RemoteApp-virtuellen Computern zugeordnet sind, die nicht mehr vorhanden sind.

## Syntax

```
Get-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRemoteAppVmStaleAdObject** " Ruft Objekte in Azure Active Directory ab, die Azure RemoteApp-virtuellen Computern zugeordnet sind, die nicht mehr vorhanden sind.
Dieses Cmdlet zeigt den Namen jedes Objekts an, das er erhält.

## Beispiele

### Beispiel 1: Abrufen veralteter Objekte für eine Sammlung
```
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso"
```

Dieser zweite Befehl ruft die veralteten Objekte für die Sammlung mit dem Namen contoso ab.

## Parameter

### -CollectionName
Gibt den Namen der Azure RemoteApp-Sammlung an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Anmeldeinformationen
Gibt eine Anmeldeinformation an, die Rechte zum Ausführen dieser Aktion aufweist.
Verwenden Sie das Cmdlet **Get-Credential** , um ein **PSCredential** -Objekt zu erhalten.
Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet die aktuellen Anmeldeinformationen des Benutzers.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Zeichenfolge

## Notizen

## Verwandte Links

[Löschen-AzureRemoteAppVmStaleAdObject](./Clear-AzureRemoteAppVmStaleAdObject.md)


