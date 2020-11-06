---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: C579BF90-FD8B-4384-96EB-46154E308492
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/get-azurermservermanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
ms.openlocfilehash: 9dc7e38cf169e79ec7dae279c6fa09f069b1ade7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476585"
---
# Get-AzureRmServerManagementGateway

## Synopsis
Ruft mindestens ein Server Verwaltungs Gateway ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Noparams (Standard)
```
Get-AzureRmServerManagementGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Many-ByResourceGroup
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Single-ByName
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Single-ByObject
```
Get-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmServerManagementGateway** " ruft mindestens ein Azure Server Management-Gateway ab.

## Beispiele

### Beispiel 1: Abrufen aller Gateways in einem Abonnement
```
PS C:\>Get-AzureRmServerManagementGateway
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
groupOne       centralus      Off          mygateway
groupOne       centralus      Off          othergateway
groupTwo       centralus      On           privategateway
```

Dieser Befehl ruft alle Server Verwaltungs Gateways im Abonnement ab.

### Beispiel 2: Abrufen von Gateways in einer Ressourcengruppe
```
PS C:\>Get-AzureRmServerManagementGateway -ResourceGroupName "Group001"
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
myGroup        centralus      Off          mygateway
```

Dieser Befehl ruft alle Server Verwaltungs Gateways ab, die zur Ressourcengruppe mit dem Namen Group001 gehören.

### Beispiel 3: Abrufen aller installierten Instanzen eines Gateways
```
PS C:\>(Get-AzureRmServerManagementGateway -ResourceGroupName "Group002" -GatewayName "Gateway01").Instances
Name             Installed              Version         Operating System
----             ---------              -------         ----------------
GATEWAYPC        4/13/2016 6:35:04 PM   1.0.1104.0      Microsoft Windows 10 Enterprise
```

Dieser Befehl ruft alle Instanzen eines Server Verwaltungs Gateways mit dem Namen Gateway01 ab, die zur Ressourcengruppe namens Group002 gehören.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Gateway
Gibt ein Gateway an, das dieses Cmdlet erhält.

Das Cmdlet verwendet die Parameter *ResourceGroupName* und *GatewayName* über das angegebene Gateway, um die Aktion auszuführen.

Wenn dieser Parameter angegeben wird, enthält dieses Cmdlet den detaillierten Status für das Gateway.

```yaml
Type: Gateway
Parameter Sets: Single-ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Gatewayname
Gibt den Namen des Server Verwaltungs Gateways an, für das dieses Cmdlet Gate erhält.

Wenn Sie den Parameter *GatewayName* angeben, enthält dieses Cmdlet den detaillierten Status auf dem Gateway.

```yaml
Type: String
Parameter Sets: Single-ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet Gateways erhält.

```yaml
Type: String
Parameter Sets: Many-ByResourceGroup, Single-ByName
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

### Gateway
Der Parameter "Gateway" akzeptiert den Wert vom Typ "Gateway" aus der Pipeline.

## Ausgaben

### Microsoft. Azure. Commands. Servermanagement. Model. Gateway

## Notizen
* Wenn dieses Cmdlet ohne Parameter verwendet wird, gibt es alle Gateways zurück, die dem Abonnement zugeordnet sind.

## Verwandte Links

[Neu – AzureRmServerManagementGateway](./New-AzureRmServerManagementGateway.md)

[Remove-AzureRmServerManagementGateway](./Remove-AzureRmServerManagementGateway.md)


