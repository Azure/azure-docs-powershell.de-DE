---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/get-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
ms.openlocfilehash: d25cca457adb70398d29b1b2a8044ac14af893db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663488"
---
# Get-AzureRmDnsZone

## Synopsis
Ruft eine DNS-Zone ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Standard (Standard)
```
Get-AzureRmDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroup
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmDnsZone** " Ruft eine DNS-Zone (Domain Name System) aus der angegebenen Ressourcengruppe ab.
Wenn Sie den Parameter *Name* angeben, wird ein einzelnes **dnsZone** -Objekt zurückgegeben.
Wenn Sie den Parameter *Name* nicht angeben, wird ein Array zurückgegeben, das alle Zonen in der angegebenen Ressourcengruppe enthält.
Sie können das **dnsZone** -Objekt verwenden, um die Zone zu aktualisieren, beispielsweise können Sie **Recordset** -Objekte hinzufügen.

## Beispiele

### Beispiel 1: Abrufen einer Zone
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

In diesem Beispiel wird die DNS-Zone mit dem Namen MyZone.com aus der angegebenen Ressourcengruppe abgerufen und dann in der $Zone-Variablen gespeichert.

### Beispiel 2: Abrufen aller Zonen in einer Ressourcengruppe
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

In diesem Beispiel werden alle DNS-Zonen in der angegebenen Ressourcengruppe abgerufen und dann in der $Zones-Variablen gespeichert.

### Beispiel 3: Abrufen aller Zonen in einem Abonnement
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

In diesem Beispiel werden alle DNS-Zonen im aktuellen Azure-Abonnement abgerufen und dann in der $Zones-Variablen gespeichert.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Name
Gibt den Namen der abzurufenden DNS-Zone an.

Wenn Sie keinen Wert für den Parameter *Name* angeben, ruft dieses Cmdlet alle DNS-Zonen in der angegebenen Ressourcengruppe ab.
Wenn Sie auch den *ResourceGroupName* -Parameter weglassen, ruft dieses Cmdlet alle DNS-Zonen im aktuellen Azure-Abonnement ab.

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die die DNS-Zone enthält, die abgerufen werden soll.

Wenn Sie das *ResourceGroupName* nicht angeben, müssen Sie auch den Parameter *Name* weglassen.
In diesem Fall ruft dieses Cmdlet alle DNS-Zonen im aktuellen Azure-Abonnement ab.

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Mit diesem Cmdlet können Sie keine Pipe-Eingabe durchleiten.

## Ausgaben

### Microsoft. Azure. Commands. DNS. dnsZone
Dieses Cmdlet gibt ein Objekt zurück, das die DNS-Zone darstellt.
Wenn der Zonen Name nicht angegeben wird, wird ein Array von Zone-Objekten zurückgegeben.

## Notizen

## Verwandte Links

[Neu – AzureRmDnsZone](./New-AzureRmDnsZone.md)

[Remove-AzureRmDnsZone](./Remove-AzureRmDnsZone.md)

[Satz-AzureRmDnsZone](./Set-AzureRmDnsZone.md)
