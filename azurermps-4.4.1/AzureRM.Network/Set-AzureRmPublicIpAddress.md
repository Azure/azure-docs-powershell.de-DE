---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
ms.openlocfilehash: 1460b4497909d56e2d10d03e33df71518c52b796
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662636"
---
# Set-AzureRmPublicIpAddress

## Synopsis
Legt den Zielstatus für eine öffentliche IP-Adresse fest.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzureRmPublicIpAddress** " legt den Zielstatus für eine öffentliche IP-Adresse fest.

## Beispiele

### 1: Ändern der Zuordnungsmethode einer öffentlichen IP-Adresse
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 Erster Befehl ruft die Ressource für öffentliche IP-Adressen mit dem Namen $publicIPName in der Ressourcengruppe $rgName ab.
Der zweite Befehl legt die Zuordnungsmethode des öffentlichen IP-Adressen Objekts auf "static" fest.
Set-AzureRmPublicIPAddress Befehl aktualisiert die Ressource für öffentliche IP-Adressen mit dem aktualisierten Objekt und ändert die Zuordnungsmethode auf "statisch". Eine öffentliche IP-Adresse wird sofort zugeteilt.

### 2: Ändern der DNS-Domänen Beschriftung einer öffentlichen IP-Adresse
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

Erster Befehl ruft die Ressource für öffentliche IP-Adressen mit dem Namen $publicIPName in der Ressourcengruppe $rgName ab.
Der zweite Befehl legt die DomainNameLabel-Eigenschaft auf das erforderliche DNS-Präfix fest.
Set-AzureRmPublicIPAddress Befehl aktualisiert die Ressource für öffentliche IP-Adressen mit dem aktualisierten Objekt. DomainNameLabel & FQDN werden wie erwartet geändert.

## Parameter

### -PublicIpAddress
Gibt ein **PublicIpAddress** -Objekt an, das den Zielzustand darstellt, für den die öffentliche IP-Adresse festgelegt werden soll.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### PSPublicIpAddress
Der Parameter "PublicIpAddress" akzeptiert den Wert vom Typ "PSPublicIpAddress" aus der Pipeline.

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress

## Notizen

## Verwandte Links

[Get-AzureRmPublicIpAddress](./Get-AzureRmPublicIpAddress.md)

[Get-AzureRmPublicIpAddress](./Get-AzureRmPublicIpAddress.md)

[Neu – AzureRmPublicIpAddress](./New-AzureRmPublicIpAddress.md)

[Remove-AzureRmPublicIpAddress](./Remove-AzureRmPublicIpAddress.md)


