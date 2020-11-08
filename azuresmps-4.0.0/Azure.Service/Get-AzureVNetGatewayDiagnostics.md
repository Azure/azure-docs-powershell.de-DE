---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 22E8CB18-8CDD-4992-AB81-E1BB400E6BC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 294e931529b7de939a6a5c20181d48b18da1e892
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006483"
---
# Get-AzureVNetGatewayDiagnostics

## Synopsis
Ruft den aktuellen Status der Diagnose für ein virtuelles Netzwerkgateway ab.

## Syntax

```
Get-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureVNetGatewayDiagnostics** " Ruft den aktuellen Status der Diagnose für ein virtuelles Netzwerkgateway ab.
Wenn ein BLOB (Binary Large Object) vorhanden ist, in dem die **Start-AzureVNetGatewayDiagnostics** eine vorherige Diagnosesitzung gespeichert haben, gibt dieses Cmdlet auch die URL des BLOB zurück, in dem dieses Cmdlet diese Diagnosesitzung gespeichert hat.

## Beispiele

## Parameter

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest. Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

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

### -VNetName
Gibt das virtuelle Netzwerk an, das ein virtuelles Netzwerkgateway enthält, für das dieses Cmdlet Diagnosen erhält.

```yaml
Type: String
Parameter Sets: (All)
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

## Verwandte Links

[Anfang-AzureVNetGatewayDiagnostics](./Start-AzureVNetGatewayDiagnostics.md)

[Stopp-AzureVNetGatewayDiagnostics](./Stop-AzureVNetGatewayDiagnostics.md)


