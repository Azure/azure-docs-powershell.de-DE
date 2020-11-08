---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4136A0EF-2682-4B17-BC37-53CD43F5940B
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b884da0395313ddc8aa4d0e301b37849ec3d57
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006528"
---
# Get-AzureRemoteAppOperationResult

## Synopsis
Ruft das Ergebnis eines Azure RemoteApp-Vorgangs ab.

## Syntax

```
Get-AzureRemoteAppOperationResult [-TrackingId] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Get-AzureRemoteAppOperationResult** wird das Ergebnis eines Azure-RemoteApp-Vorgangs mit langer Laufzeit abgerufen.
Azure RemoteApp verwendet langlebige Vorgänge für viele Aktionen, die die Verarbeitung durch den Dienst erfordern und nicht sofort zurückgegeben werden können.
Beispiele für Cmdlets, die nach Verfolgungs-IDs zurückgeben, sind **Update-AzureRemoteAppCollection** , **AzureRemoteAppWorkspace** , **Disconnect-AzureRemoteAppSession** und andere.

## Beispiele

### Beispiel 1: Verwenden einer Tracking-ID zum Abrufen eines Vorgangs Ergebnisses
```
PS C:\> $result = New-AzureRemoteAppCollection -CollectionName Contoso -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
PS C:\> Get-AzureRemoteAppOperationResult -TrackingId $result.Tracking
```

Dieser Befehl speichert die nach Verfolgungs-ID, die von einem Azure RemoteApp-Vorgang zurückgegeben wird.
Die Tracking-ID wird im folgenden Befehl an **Get-AzureRemoteAppOperationResult** übergeben.

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

### -Tracking-Nummer
Gibt die nach Verfolgungs-ID eines Vorgangs an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

[Trennen-AzureRemoteAppSession](./Disconnect-AzureRemoteAppSession.md)

[Satz-AzureRemoteAppWorkspace](./Set-AzureRemoteAppWorkspace.md)

[Update-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


