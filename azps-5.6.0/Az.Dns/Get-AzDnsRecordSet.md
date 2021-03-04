---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 447b1e32473d00504446478a9efaa5634e3b1c65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935064"
---
# Get-AzDnsRecordSet

## SYNOPSIS
Ruft einen DNS-Eintragssatz ab.

## SYNTAX

### Felder
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Objekt
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzDnsRecordSet-Cmdlet** ruft den Eintrag Domain Name System (DNS) mit dem angegebenen Namen und Typ in der angegebenen Zone ab.
Wenn Sie die Parameter *Name* oder *RecordType* nicht angeben, gibt dieses Cmdlet alle Datensatzsätze des angegebenen Typs in der Zone zurück.
Wenn Sie den *Parameter RecordType,* aber nicht den *Parameter Name* angeben, gibt dieses Cmdlet alle Datensatzsätze des angegebenen Datensatztyps zurück.
Sie können den Pipelineoperator verwenden, um ein **DnsZone-Objekt** an dieses Cmdlet zu übergeben, oder Sie können ein **DnsZone-Objekt** als Parameter *Zone* übergeben oder alternativ die Zone und Ressourcengruppe nach Namen angeben.

## BEISPIELE

### Beispiel 1: Get record sets with a specified name and type
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

Dieser Befehl ruft den Datensatzsatz des Datensatztyps A mit dem Namen www in der angegebenen Ressourcengruppe und Zone ab und speichert ihn dann in der $RecordSet Variablen.
Da die *Parameter Name* und *RecordType* angegeben werden, wird nur ein **RecordSet-Objekt** zurückgegeben.

### Beispiel 2: Get record sets of a specified type
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

Dieser Befehl ruft ein Array aller Datensatzsätze des Datensatztyps A in der Zone mit dem Namen myzone.com in der Ressourcengruppe mit dem Namen MyResourceGroup ab und speichert sie dann in der $RecordSets-Variable.

### Beispiel 3: Alle Datensatzsätze in einer Zone erhalten
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

Dieser Befehl ruft ein Array aller Datensatzsätze in der Zone mit dem Namen myzone.com in der Ressourcengruppe mit dem Namen MyResourceGroup ab und speichert sie dann in der $RecordSets Variablen.

### Beispiel 4: Alle Datensatzsätze in einer Zone mithilfe eines DnsZone-Objekts
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

Dieses Beispiel entspricht dem obigen Beispiel 3.
Dieses Mal wird die Zone mit einem Zonenobjekt angegeben.

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen des **zu erhaltenden RecordSets** an.
Wenn Sie den Parameter Name *nicht angeben,* werden alle Datensatzsätze des angegebenen Typs zurückgegeben.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
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
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SOA
- SRV
- TXT Wenn Sie den Parameter *RecordType nicht* angeben, müssen Sie auch den Parameter *Name weglassen.* Dieses Cmdlet gibt dann alle Datensatzsätze in der Zone (aller Namen und Typen) zurück.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt die Ressourcengruppe an, die die DNS-Zone enthält.
Der Zonenname muss auch mit dem Parameter *ZoneName angegeben* werden.
Alternativ können Sie die Zone und ressourcengruppe angeben, indem Sie ein **DnsZone-Objekt** mit dem Parameter *Zone* übergeben.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Gibt die DNS-Zone an, die den Datensatzsatz enthält, den dieses Cmdlet erhält.
Alternativ können Sie die Zone mithilfe der *Parameter ZoneName* und *ResourceGroupName* angeben.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
Gibt den Namen der DNS-Zone an, die den zu erhaltenden Eintrag enthält.
Die Ressourcengruppe, die die Zone enthält, muss auch mithilfe des *Parameters ResourceGroupName angegeben* werden.
Alternativ können Sie die Zone und ressourcengruppe angeben, indem Sie ein DNS Zone-Objekt mit dem Parameter *Zone* übergeben.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

### System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## AUSGABEN

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## NOTIZEN

## VERWANDTE LINKS

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)


