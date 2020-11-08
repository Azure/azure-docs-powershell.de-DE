---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C7F08804-E177-4BC5-8F0E-DEC1B467C4BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20cb37fbba8fd3789c0932f9ff1e9352334662e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006050"
---
# Update-AzureApplicationGateway

## Synopsis
Aktualisiert ein Anwendungsgateway.

## Syntax

```
Update-AzureApplicationGateway -Name <String> [-VnetName <String>]
 [-Subnets <System.Collections.Generic.List`1[System.String]>] [-InstanceCount <UInt32>]
 [-GatewaySize <String>] [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Update-AzureApplicationGateway** aktualisiert ein vorhandenes Anwendungsgateway.

## Beispiele

### Beispiel 1: Ändern eines Anwendungs Gateways mithilfe des Namens
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork18" -Subnets @("Subnet05", "Subnet06")
```

Der erste Befehl beendet das Anwendungsgateway mit dem Namen ApplicationGateway06.
Ein Anwendungsgateway muss angehalten werden, bevor Sie das virtuelle Netzwerk oder die Subnetze ändern können.

Der zweite Befehl ändert das virtuelle Subnetz und die Subnetze für das Anwendungsgateway mit dem Namen ApplicationGateway06.

### Beispiel 2: ändern zusätzlicher Eigenschaften eines Anwendungs Gateways
```
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -InstanceCount 2 -GatewaySize "Large" -Description "Updated application gateway"
```

Mit diesem Befehl werden die Anzahl der Instanzen, die gatewaygröße und die Beschreibung für das Anwendungsgateway mit dem Namen ApplicationGateway06 geändert.
Mit diesem Befehl werden die virtuellen Netzwerke oder Subnetze für das Anwendungsgateway nicht geändert.
Daher müssen Sie das Anwendungsgateway nicht beenden, bevor Sie diesen Befehl ausführen.

### Beispiel 3: Ändern eines Anwendungs Gateways mithilfe der Pipeline
```
PS C:\> $ApplicationGateway = Get-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> $ApplicationGateway.GatewaySize = "Medium"
PS C:\> $ApplicationGateway | Update-AzureApplicationGateway
```

Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway06 mit dem Cmdlet **Get-AzureApplicationGateway** ab.
Der Befehl speichert Sie in der $ApplicationGateway-Variablen.

Der zweite Befehl weist der **GatewaySize** -Eigenschaft den Wert Medium zu.

Der letzte Befehl übergibt den aktualisierten $ApplicationGateway an das aktuelle Cmdlet.

## Parameter

### -Beschreibung
Gibt eine Beschreibung an, die dieses Cmdlet dem Anwendungsgateway zuweist.

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

### -GatewaySize
Gibt die Größe an, die dieses Cmdlet dem Anwendungsgateway zuweist.
Gültige Werte sind:

- Kleine
- Mittel
- Große

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

### -InstanceCount
Gibt die Anzahl der Instanzen an, die dieses Cmdlet dem Anwendungsgateway zuweist.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen des Anwendungs Gateways an, das vom Cmdlet aktualisiert wird.

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

### -Subnetze
Gibt ein Array von Subnetzen an, in denen dieses Cmdlet das Anwendungsgateway bereitstellt.

Sie können Subnets nicht aktualisieren, während das Anwendungsgateway ausgeführt wird.
Verwenden Sie das Stop-AzureApplicationGateway-Cmdlet, um das Anwendungsgateway zu beenden.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VnetName
Gibt das virtuelle Netzwerk an, in dem dieses Cmdlet das Anwendungsgateway bereitstellt.

Sie können ein virtuelles Netzwerk nicht aktualisieren, während das Anwendungsgateway ausgeführt wird.
Verwenden Sie **AzureApplicationGateway** , um das Anwendungsgateway zu beenden.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse

## Notizen

## Verwandte Links

[Get-AzureApplicationGateway](./Get-AzureApplicationGateway.md)

[Neu – AzureApplicationGateway](./New-AzureApplicationGateway.md)

[Remove-AzureApplicationGateway](./Remove-AzureApplicationGateway.md)

[Anfang-AzureApplicationGateway](./Start-AzureApplicationGateway.md)

[Stopp-AzureApplicationGateway](./Stop-AzureApplicationGateway.md)
