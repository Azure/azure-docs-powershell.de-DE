---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
ms.openlocfilehash: f4b29849109959a8b06a8d0339c8927b8a840a7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662963"
---
# Get-AzureRmRemoteDesktopFile

## Synopsis
Ruft eine RDP-Datei ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Download
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [<CommonParameters>]
```

### Starten
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmRemoteDesktopFile** " Ruft eine RDP-Datei (Remote Desktop Protocol) ab.

## Beispiele

### Beispiel 1: Abrufen einer Remote Desktop Datei
```
PS C:\> Get-AzureRmRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

Dieser Befehl ruft die Remote Desktop Datei für den virtuellen Computer mit dem Namen VirtualMachine07 ab.
Der Befehl speichert das Ergebnis in der Datei mit dem Namen D:\RemoteDesktopFile07.RDP.

## Parameter

### -Start
Gibt an, dass dieses Cmdlet den Remote Desktop startet, nachdem die RDP-Datei abgerufen wurde.

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalPath
Gibt den lokalen vollständigen Pfad an, in dem dieses Cmdlet die RDP-Datei speichert.

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen des Verfügbarkeits Satzes an, den dieses Cmdlet erhält.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

## Notizen

## Verwandte Links

