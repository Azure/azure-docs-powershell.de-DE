---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 706CBF65-C796-4525-BAEB-AAFAD44C0464
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37c2ce3b32d23f7c5bb682d2116de84cc90f047
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006225"
---
# Stop-AzureVNetGatewayDiagnostics

## Synopsis
Beendet eine ausgeführte VPN-Gateway-Diagnosesitzung.

## Syntax

```
Stop-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Stop-AzureVNetGatewayDiagnostics** beendet eine ausgeführte VPN-Gateway-Diagnosesitzung (virtuelles privates Netzwerk).
Dieser Befehl speichert die Ergebnisse der Diagnosesitzung auf dem Speicherkonto, das vom Cmdlet **Start-AzureVNetGatewayDiagnostics** angegeben wird.

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
Gibt das virtuelle Netzwerk an, das ein virtuelles Netzwerkgateway enthält, für das dieses Cmdlet die Diagnose beendet.

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

[Get-AzureVNetGatewayDiagnostics](./Get-AzureVNetGatewayDiagnostics.md)

[Anfang-AzureVNetGatewayDiagnostics](./Start-AzureVNetGatewayDiagnostics.md)


