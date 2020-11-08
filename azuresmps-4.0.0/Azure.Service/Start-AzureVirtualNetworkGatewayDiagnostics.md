---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: DA5689DF-AA4A-4161-89B0-8055BF384274
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b71367ac18a753fad5425d0073b55cacb413e4b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005978"
---
# Start-AzureVirtualNetworkGatewayDiagnostics

## Synopsis
Startet die Diagnose für ein virtuelles Netzwerkgateway.

## Syntax

```
Start-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-CaptureDurationInSeconds <Int32>]
 [-ContainerName <String>] [-StorageContext <AzureStorageContext>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Start-AzureVirtualNetworkGatewayDiagnostics** startet eine neue Gateway-Diagnosesitzung für ein virtuelles Netzwerkgateway.
Es kann immer nur eine Gateway-Diagnosesitzung ausgeführt werden.
Wenn Sie dieses Cmdlet ausführen, während eine Gateway-Diagnosesitzung ausgeführt wird, gibt dieses Cmdlet einen Fehler zurück.

## Beispiele

## Parameter

### -CaptureDurationInSeconds
Gibt die Aufnahmedauer in Sekunden an.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Containername
Gibt den Namen eines Azure-Containers an.
Dieses Cmdlet speichert Ergebnisse in dem Container, den dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Gatewayserver
Gibt die ID eines Gateways an.

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

### -Storagecontext
Gibt einen Azure-Speicherkontext an.
Dieses Cmdlet speichert Ergebnisse unter Verwendung des Speicher Kontexts, den dieser Parameter angibt.

```yaml
Type: AzureStorageContext
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

## Notizen

## Verwandte Links

[Get-AzureVirtualNetworkGatewayDiagnostics](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[Stopp-AzureVirtualNetworkGatewayDiagnostics](./Stop-AzureVirtualNetworkGatewayDiagnostics.md)


