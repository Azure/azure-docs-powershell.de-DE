---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9FCECA04-9855-461C-9470-85312993C4B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bb7bb3e708720b481edc4489d858c70736eac95
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006232"
---
# Start-AzureVNetGatewayDiagnostics

## Synopsis
Startet die Gateway-Diagnose für ein VPN-Gateway.

## Syntax

```
Start-AzureVNetGatewayDiagnostics -VNetName <String> -CaptureDurationInSeconds <Int32>
 [-ContainerName <String>] -StorageContext <AzureStorageContext> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Start-AzureVNetGatewayDiagnostics** startet eine neue Gateway-Diagnosesitzung für ein VPN-Gateway (virtuelles privates Netzwerk).
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

Required: True
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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VNetName
Gibt das virtuelle Netzwerk an, das ein virtuelles Netzwerkgateway enthält, für das dieses Cmdlet eine Diagnose ausführt.

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

[Stopp-AzureVNetGatewayDiagnostics](./Stop-AzureVNetGatewayDiagnostics.md)


