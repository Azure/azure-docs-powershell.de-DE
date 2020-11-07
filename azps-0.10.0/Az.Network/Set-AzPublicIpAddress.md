---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 53d5e15e6354e359461e59728e0776b7d3ec99ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843587"
---
# Set-AzPublicIpAddress

## Synopsis
Legt den Zielstatus für eine öffentliche IP-Adresse fest.

## Syntax

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzPublicIpAddress** " legt den Zielstatus für eine öffentliche IP-Adresse fest.

## Beispiele

### 1: Ändern der Zuordnungsmethode einer öffentlichen IP-Adresse
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 Erster Befehl ruft die Ressource für öffentliche IP-Adressen mit dem Namen $publicIPName in der Ressourcengruppe $rgName ab.
Der zweite Befehl legt die Zuordnungsmethode des öffentlichen IP-Adressen Objekts auf "static" fest.
Set-AzPublicIPAddress Befehl aktualisiert die Ressource für öffentliche IP-Adressen mit dem aktualisierten Objekt und ändert die Zuordnungsmethode auf "statisch". Eine öffentliche IP-Adresse wird sofort zugeteilt.

### 2: Ändern der DNS-Domänen Beschriftung einer öffentlichen IP-Adresse
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

Erster Befehl ruft die Ressource für öffentliche IP-Adressen mit dem Namen $publicIPName in der Ressourcengruppe $rgName ab.
Der zweite Befehl legt die DomainNameLabel-Eigenschaft auf das erforderliche DNS-Präfix fest.
Set-AzPublicIPAddress Befehl aktualisiert die Ressource für öffentliche IP-Adressen mit dem aktualisierten Objekt. DomainNameLabel & FQDN werden wie erwartet geändert.

## Parameter

### -AsJob
Ausführen eines Cmdlets im Hintergrund

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -PublicIpAddress
Gibt ein **PublicIpAddress** -Objekt an, das den Zielzustand darstellt, für den die öffentliche IP-Adresse festgelegt werden soll.

```yaml
Type: PSPublicIpAddress
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### PSPublicIpAddress
Der Parameter "PublicIpAddress" akzeptiert den Wert vom Typ "PSPublicIpAddress" aus der Pipeline.

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress

## Notizen

## Verwandte Links

[Get-AzPublicIpAddress](./Get-AzPublicIpAddress.md)

[Neu – AzPublicIpAddress](./New-AzPublicIpAddress.md)

[Remove-AzPublicIpAddress](./Remove-AzPublicIpAddress.md)


