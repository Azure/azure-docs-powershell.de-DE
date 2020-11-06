---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/get-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
ms.openlocfilehash: 5c7a2a42964be10aa02f4c3205e701b310febb78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500617"
---
# Get-AzureRmDnsRecordSet

## Synopsis
Ruft einen DNS-Eintragssatz ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Felder
```
Get-AzureRmDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Objekt
```
Get-AzureRmDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmDnsRecordSet** " Ruft den DNS-Eintragssatz (Domain Name System) mit dem angegebenen Namen und Typ in der angegebenen Zone ab.

Wenn Sie die Parameter *Name* oder *RecordType* nicht angeben, gibt dieses Cmdlet alle Daten Satz Sätze des angegebenen Typs in der Zone zurück.
Wenn Sie den Parameter *RecordType* , aber nicht den Parameter *Name* angeben, gibt dieses Cmdlet alle Daten Satz Sätze des angegebenen Datensatztyps zurück.

Sie können den Pipelineoperator verwenden, um ein **dnsZone** -Objekt an dieses Cmdlet zu übergeben, oder Sie können ein **dnsZone** -Objekt als *Zone* -Parameter übergeben, oder Alternativ können Sie die Zone und die Ressourcengruppe nach Namen angeben.

## Beispiele

### Beispiel 1: Abrufen von Daten Satz Sätzen mit einem angegebenen Namen und Typ
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

Dieser Befehl ruft den Daten Satz Satz des Datensatztyps A mit dem Namen www in der angegebenen Ressourcengruppe und Zone ab und speichert ihn dann in der $Recordset-Variablen.
Da die Parameter *Name* und *RecordType* angegeben werden, wird nur ein **Recordset** -Objekt zurückgegeben.

### Beispiel 2: Abrufen von Daten Satz Sätzen eines angegebenen Typs
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

Dieser Befehl ruft ein Array aller Daten Satz Sätze des Datensatztyps A in der Zone mit dem Namen MyZone.com in der Ressourcengruppe myresourcegroup ab und speichert Sie dann in der $Recordsets Variablen.

### Beispiel 3: Abrufen aller Daten Satz Sätze in einer Zone
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

Dieser Befehl ruft ein Array aller Datensatzgruppen in der Zone mit dem Namen MyZone.com in der Ressourcengruppe mit dem Namen myresourcegroup ab und speichert Sie dann in der $Recordsets-Variablen.

### Beispiel 4: Abrufen aller Daten Satz Sätze in einer Zone mithilfe eines dnsZone-Objekts
```
PS C:\> $Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzureRmDnsRecordSet -Zone $Zone
```

Dieses Beispiel entspricht Beispiel 3 oben.
Dieses Mal wird die Zone mithilfe eines Zone-Objekts angegeben.

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
Gibt den Namen des abzurufenden **Recordsets** an.
Wenn Sie den Parameter *Name* nicht angeben, werden alle Daten Satz Sätze des angegebenen Typs zurückgegeben.

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecordType
Gibt den Typ des DNS-Eintrags an, den dieses Cmdlet erhält.

Gültige Werte sind: 

- Eine
- AAAA
- CNAME
- MX
- NS
- PTR
- SOA
- SRV
- TXT

Wenn Sie den *RecordType* -Parameter nicht angeben, müssen Sie auch den Parameter *Name* weglassen. Dieses Cmdlet gibt dann alle Daten Satz Sätze in der Zone (aller Namen und Typen) zurück.

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt die Ressourcengruppe an, die die DNS-Zone enthält.
Der Zonen Name muss auch mit dem Parameter *zonename* angegeben werden.

Alternativ können Sie die Zone und die Ressourcengruppe angeben, indem Sie ein **dnsZone** -Objekt mit dem *Zone* -Parameter übergeben.

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Gibt die DNS-Zone an, die den Daten Satz Satz enthält, den dieses Cmdlet erhält.
Alternativ können Sie die Zone mithilfe der Parameter *zonename* und *ResourceGroupName* angeben.

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
Gibt den Namen der DNS-Zone an, die den aufzurufenden Daten Satz Satz enthält.
Die Ressourcengruppe mit der Zone muss ebenfalls mithilfe des *ResourceGroupName* -Parameters angegeben werden.

Alternativ können Sie die Zone und die Ressourcengruppe angeben, indem Sie ein DNS-Zonenobjekt mit dem *Zone* -Parameter übergeben.

```yaml
Type: String
Parameter Sets: Fields
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

### Microsoft. Azure. Commands. DNS. dnsZone
Sie können ein **dnsZone** -Objekt an dieses Cmdlet übergeben.
Das **dnsZone** -Objekt stellt die Zone dar, in der nach dem **Recordset** -Objekt gesucht werden soll.

## Ausgaben

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Dieses Cmdlet gibt ein oder mehrere Objekte zurück, die die gefundenen Daten Satz Sätze darstellen.
Es wird höchstens ein **Recordset** zurückgegeben, wenn die Parameter *Name* und *RecordType* angegeben werden, da andernfalls mehrere **Recordset** -Objekte als Array zurückgegeben werden.

## Notizen

## Verwandte Links

[Neu – AzureRmDnsRecordSet](./New-AzureRmDnsRecordSet.md)

[Remove-AzureRmDnsRecordSet](./Remove-AzureRmDnsRecordSet.md)

[Satz-AzureRmDnsRecordSet](./Set-AzureRmDnsRecordSet.md)


