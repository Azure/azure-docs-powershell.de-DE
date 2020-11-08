---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D7D99AFA-A85E-43DA-9F2F-8FFD34048E00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ede675ab58905f102fb9d0029669115acdb9e85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006635"
---
# Set-AzureApplicationGatewayConfig

## Synopsis
Konfiguriert ein Anwendungsgateway.

## Syntax

### configFile
```
Set-AzureApplicationGatewayConfig -Name <String> -ConfigFile <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### configobject
```
Set-AzureApplicationGatewayConfig -Name <String> -Config <ApplicationGatewayConfiguration>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureApplicationGatewayConfig** " konfiguriert ein Anwendungsgateway.

## Beispiele

### Beispiel 1: Konfigurieren eines Anwendungs Gateways mithilfe eines Configuration-Objekts
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway02"
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -Config $ConfigReturnObject
```

Der erste Befehl ruft das Konfigurationsobjekt für das Anwendungsgateway mit dem Namen ApplicationGateway02 mit dem Cmdlet **Get-AzureApplicationGatewayConfig** ab.
Der Befehl speichert Sie in der $ConfigReturnObject-Variablen.

Der zweite Befehl legt die Konfiguration für die Anwendung mit dem Namen ApplicationGateway06 mithilfe eines in der $ConfigReturnObject Variablen gespeicherten Application Gateway-Konfigurationsobjekts fest.

### Beispiel 2: Konfigurieren eines Anwendungs Gateways mithilfe einer Konfigurationsdatei
```
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ConfigFile "D:\config.xml"
```

Mit diesem Befehl wird die Konfiguration für die Anwendung mit dem Namen ApplicationGateway06 unter Verwendung einer Application Gateway-Konfigurationsdatei am angegebenen Speicherort festgelegt.

### Beispiel 3: Ändern einer Konfiguration mithilfe eines Configuration-Objekts
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
PS C:\> $ConfigReturnObject.Config.FrontendPorts[0].Port = 443
PS C:\> $ConfigReturnObject | Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
```

Der erste Befehl ruft das Konfigurationsobjekt für das Anwendungsgateway mit dem Namen ApplicationGateway06 mit dem Cmdlet **Get-AzureApplicationGatewayConfig** ab.
Der Befehl speichert Sie in der $ConfigReturnObject-Variablen.

Der zweite Befehl weist einer **Port** -Eigenschaft in dem in $ConfigReturnObject gespeicherten Objekt einen Port Wert zu.

Der letzte Befehl übergibt den aktualisierten $ConfigReturnObject an das aktuelle Cmdlet.

## Parameter

### -Config
Gibt ein Configuration-Objekt für das Anwendungsgateway an.
Dieses Cmdlet weist die Konfiguration zu, die dieser Parameter einem Anwendungsgateway angibt.

```yaml
Type: ApplicationGatewayConfiguration
Parameter Sets: configObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Configdatei
Gibt den Pfad einer Konfigurationsdatei im XML-Format für ein Anwendungsgateway an.
Dieses Cmdlet weist die Konfiguration zu, die dieser Parameter einem Anwendungsgateway angibt.

```yaml
Type: String
Parameter Sets: configFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen des Anwendungs Gateways an, das von diesem Cmdlet konfiguriert wird.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String, Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfiguration

## Ausgaben

### Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse

## Notizen

## Verwandte Links

[Get-AzureApplicationGatewayConfig](./Get-AzureApplicationGatewayConfig.md)


