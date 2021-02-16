---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: b64432364b9c86a1153ba9a535d70645cf15d4d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163580"
---
# Get-AzDnsRecordSet

## SYNOPSIS
Ruft einen Satz eines DNS-Eintrags ab.

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
Das **Cmdlet "Get-AzDnsRecordSet"** ruft den Dns (Domain Name System)-Eintrag ab, der mit dem angegebenen Namen und Typ in der angegebenen Zone festgelegt ist.
Wenn Sie die Parameter *"Name"* oder *"RecordType"* nicht angeben, gibt dieses Cmdlet alle Datensatzsätze des angegebenen Typs in der Zone zurück.
Wenn Sie den *Parameter "RecordType",* aber nicht den Parameter *"Name"* angeben, gibt dieses Cmdlet alle Datensatzsätze des angegebenen Datensatztyps zurück.
Sie können den Pipelineoperator verwenden, um ein **"DnsZone"-Objekt** an dieses Cmdlet zu übergeben, oder Sie können ein **"DnsZone"-Objekt** als *Parameter "Zone"* übergeben, oder Sie können die Zone und Ressourcengruppe auch nach Namen angeben.

## BEISPIELE

### Beispiel 1: Erhalten von Datensatzsätzen mit einem angegebenen Namen und Typ
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

Dieser Befehl ruft den Datensatzsatz des Datensatztyps A mit dem Namen "www" in der angegebenen Ressourcengruppe und Zone ab und speichert ihn dann in $RecordSet Variable.
Da die *Parameter "Name"* und *"RecordType"* angegeben werden, wird nur ein **"RecordSet"-Objekt** zurückgegeben.

### Beispiel 2: Erhalten von Datensatzgruppen eines angegebenen Typs
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

Dieser Befehl ruft ein Array aller Datensatzsätze des Datensatztyps A in der Zone namens myzone.com in der Ressourcengruppe namens "MyResourceGroup" ab und speichert sie dann in der $RecordSets Variable.

### Beispiel 3: Alle Datensatzsätze in einer Zone erhalten
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

Dieser Befehl ruft ein Array aller Datensatzsätze in der Zone namens myzone.com in der Ressourcengruppe namens "MyResourceGroup" ab und speichert sie dann in der $RecordSets Variable.

### Beispiel 4: Erhalten aller Eintragssätze in einer Zone mithilfe eines DnsZone-Objekts
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

Dieses Beispiel entspricht Beispiel 3 oben.
Dieses Mal wird die Zone mithilfe eines Zonenobjekts angegeben.

## PARAMETERS

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
Gibt den Namen des zu erhaltenden **RecordSets** an.
Wenn Sie den Parameter *"Name" nicht angeben,* werden alle Datensatzsätze des angegebenen Typs zurückgegeben.

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
- TXT Wenn Sie den Parameter *"RecordType" nicht* angeben, müssen Sie auch den Parameter *"Name"* weglassen. Dieses Cmdlet gibt dann alle Datensatzsätze in der Zone (aller Namen und Typen) zurück.

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
Der Zonenname muss auch mit dem Parameter *"ZoneName" angegeben* werden.
Alternativ können Sie die Zone und Ressourcengruppe angeben, indem Sie ein **"DnsZone"-Objekt** mit dem Parameter *"Zone"* übergeben.

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
Alternativ können Sie die Zone mit den Parametern *"ZoneName"* und *"ResourceGroupName"* angeben.

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
Gibt den Namen der DNS-Zone an, die den zu erhaltenden Eintragssatz enthält.
Die Ressourcengruppe, die die Zone enthält, muss ebenfalls mit dem *Parameter "ResourceGroupName" angegeben* werden.
Alternativ können Sie die Zone und Ressourcengruppe angeben, indem Sie ein DNS -Zonenobjekt mit dem Parameter *"Zone"* übergeben.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

### System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## AUSGABEN

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)


