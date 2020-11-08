---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2261AD64-196A-402E-9703-EFB3A6D75FA7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83ed3e336ca72e38fc16c27ec696eea0f84f746
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006424"
---
# New-AzureServiceProject

## Synopsis
Erstellt die erforderlichen Dateien und die Konfiguration für einen neuen Dienst.

## Syntax

```
New-AzureServiceProject -ServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

Das Cmdlet **New-AzureServiceProject** erstellt die erforderlichen Dateien und die Konfiguration für einen neuen Azure-Dienst im aktuellen Verzeichnis.

## Beispiele

### Beispiel 1: Erstellen eines Gerüsts für einen Dienst
```
PS C:\> New-AzureServiceProject MyService1
```

In diesem Beispiel wird ein Gerüst für einen neuen Azure-Dienst mit dem Namen MyService1 im aktuellen Verzeichnis erstellt.

## Parameter

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

### -ServiceName
Gibt den Namen des Diensts an.
Sie bestimmt den ersten Abschnitt des Hostnamens für Ihren Dienst (beispielsweise Name.cloudapp.net) und das Verzeichnis, in dem Ihr Dienst enthalten ist.
Der Name darf nur Buchstaben, Ziffern und das Bindestrichzeichen (-) enthalten.

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

## Ausgaben

## Notizen

## Verwandte Links

[Add-AzureNodeWebRole](./Add-AzureNodeWebRole.md)

[Add-AzureNodeWorkerRole](./Add-AzureNodeWorkerRole.md)

[Publish-AzureServiceProject](./Publish-AzureServiceProject.md)

[Satz-AzureServiceProject](./Set-AzureServiceProject.md)

[Satz-AzureServiceProjectRole](./Set-AzureServiceProjectRole.md)


