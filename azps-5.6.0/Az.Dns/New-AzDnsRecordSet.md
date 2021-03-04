---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: f1731cb0eceb4474c233db859c3f4edb10461fe4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935043"
---
# New-AzDnsRecordSet

## SYNOPSIS
Erstellt einen DNS-Eintragssatz.

## SYNTAX

### Felder (Standard)
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AliasFields
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objekt
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AliasObject
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet New-AzDnsRecordSet** erstellt einen neuen DNS-Eintrag (Domain Name System) mit dem angegebenen Namen und Typ in der angegebenen Zone.
Ein **RecordSet-Objekt** ist eine Gruppe von DNS-Einträgen mit demselben Namen und Typ.
Beachten Sie, dass der Name relativ zur Zone und nicht zum vollqualifizierten Namen ist.
Der *Parameter DnsRecords* gibt die Datensätze im Datensatzsatz an.
Dieser Parameter verwendet ein Array von DNS-Einträgen, das mit New-AzDnsRecordConfig erstellt wurde.
Sie können den Pipelineoperator verwenden, um ein **DnsZone-Objekt** an dieses Cmdlet zu übergeben, oder Sie können ein **DnsZone-Objekt** als Parameter *Zone* übergeben, oder Sie können die Zone auch nach Namen angeben.
Sie können den Parameter *Bestätigen* und die $ConfirmPreference Windows PowerShell verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung aufgefordert.
Wenn bereits ein übereinstimmender **RecordSet** (derselbe Name und Datensatztyp) vorhanden ist, müssen Sie den Parameter *Überschreiben* angeben, andernfalls erstellt das Cmdlet kein neues **RecordSet.**

## BEISPIELE

### Beispiel 1: Erstellen eines Datensatzes vom Typ A
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzDnsRecordConfig to add each record to the $Records array,
# then call New-AzDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

In diesem Beispiel wird ein **RecordSet** mit dem Namen www in der Zone myzone.com.
Der Datensatzsatz ist vom Typ A und hat eine TTL von 1 Stunde (3600 Sekunden).
Er enthält einen einzelnen DNS-Eintrag.

### Beispiel 2: Erstellen eines Datensatzes vom Typ AAAA
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

In diesem Beispiel wird ein **RecordSet** mit dem Namen www in der Zone myzone.com.
Der Datensatzsatz ist vom Typ AAAA und hat eine TTL von 1 Stunde (3600 Sekunden).
Er enthält einen einzelnen DNS-Eintrag.
Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzsatzs mit mehreren Datensätzen finden Sie unter Beispiel 1.

### Beispiel 3: Erstellen eines Datensatzes vom Typ CNAME
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

In diesem Beispiel wird ein **RecordSet** mit dem Namen www in der Zone myzone.com.
Der Datensatzsatz hat den Typ CNAME und hat eine TTL von 1 Stunde (3600 Sekunden).
Er enthält einen einzelnen DNS-Eintrag.
Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzsatzs mit mehreren Datensätzen finden Sie unter Beispiel 1.

### Beispiel 4: Erstellen eines RecordSets vom Typ MX
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Mit diesem Befehl wird ein **RecordSet** mit dem Namen www in der Zone myzone.com.
Der Datensatzsatz ist vom Typ MX und hat eine TTL von 1 Stunde (3600 Sekunden).
Er enthält einen einzelnen DNS-Eintrag.
Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzsatzs mit mehreren Datensätzen finden Sie unter Beispiel 1.

### Beispiel 5: Erstellen eines Datensatzes vom Typ NS
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Mit diesem Befehl wird **ein RecordSet** mit dem Namen ns1 in der Zone myzone.com.
Der Datensatzsatz ist vom Typ NS und hat eine TTL von 1 Stunde (3600 Sekunden).
Er enthält einen einzelnen DNS-Eintrag.
Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzsatzs mit mehreren Datensätzen finden Sie unter Beispiel 1.

### Beispiel 6: Erstellen eines Datensatzes vom Typ PTR
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

Mit diesem Befehl wird ein **RecordSet** mit dem Namen 4 in der Zone 3.2.1.in-addr.arpa erstellt.
Der Datensatzsatz ist vom Typ PTR und hat eine TTL von 1 Stunde (3600 Sekunden).
Er enthält einen einzelnen DNS-Eintrag.
Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzsatzs mit mehreren Datensätzen finden Sie unter Beispiel 1.

### Beispiel 7: Erstellen eines Datensatzes vom Typ SRV
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Mit diesem Befehl wird ein **RecordSet** namens _sip._tcp in der Zone myzone.com.
Der Datensatzsatz ist vom Typ SRV und hat eine TTL von 1 Stunde (3600 Sekunden).
Er enthält einen einzelnen DNS-Eintrag, der auf die IP-Adresse 2001.2.3.4 zeigt.
Der Dienst (sip) und das Protokoll (tcp) werden als Teil des Datensatzsatznamens und nicht als Teil der Datensatzdaten angegeben.
Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzsatzs mit mehreren Datensätzen finden Sie unter Beispiel 1.

### Beispiel 8: Erstellen eines RecordSets vom Typ TXT
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Mit diesem Befehl wird ein **RecordSet** namens Text in der Zone myzone.com.
Der Datensatzsatz ist vom Typ TXT und hat eine TTL von 1 Stunde (3600 Sekunden).
Er enthält einen einzelnen DNS-Eintrag.
Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzsatzs mit mehreren Datensätzen finden Sie unter Beispiel 1.

### Beispiel 9: Erstellen eines RecordSets am Scheitelpunkt der Zone
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Mit diesem Befehl wird **ein RecordSet** am Scheitelpunkt (oder Stamm) der Zone erstellt, myzone.com.
Dazu wird der Datensatzsatzname als "@" (einschließlich der doppelten Anführungszeichen) angegeben.
Sie können keine #A0 am Scheitelpunkt einer Zone erstellen.
Dies ist eine Einschränkung der #A0 es ist keine Einschränkung von Azure DNS.
Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzsatzs mit mehreren Datensätzen finden Sie unter Beispiel 1.

### Beispiel 10: Erstellen eines Platzhalterdatensatzsatzs
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Mit diesem Befehl wird ein **RecordSet** mit dem Namen * in der Zone myzone.com.
Dies ist ein Platzhalterdatensatz.
Informationen zum Erstellen **eines Datensatzes** mit nur einer Zeile pn_PowerShell_short oder zum Erstellen eines Datensatzsatzs mit mehreren Datensätzen finden Sie unter Beispiel 1.

### Beispiel 11: Erstellen eines leeren Datensatzsatzs
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

Mit diesem Befehl wird ein **RecordSet** mit dem Namen www in der Zone myzone.com.
Der Datensatzsatz ist vom Typ A und hat eine TTL von 1 Stunde (3600 Sekunden).
Dies ist ein leerer Datensatzsatz, der als Platzhalter fungiert, dem Sie später Datensätze hinzufügen können.

### Beispiel 12: Erstellen eines Datensatzsatzs und Unterdrücken aller Bestätigungen
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

Mit diesem Befehl wird ein **RecordSet erstellt.**
Der *Parameter Überschreiben* stellt sicher, dass dieser Datensatzsatz alle bereits vorhandenen Datensatzsätze mit demselben Namen und Typ überschreibt (vorhandene Datensätze in diesem Datensatzsatz gehen verloren).
Der *Parameter Bestätigen* mit dem Wert $False die Bestätigungsaufforderung unterdrückt.

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

### -DnsRecords
Gibt das Array von DNS-Einträgen an, das in den Datensatzsatz aufgenommen werden soll.
Sie können das cmdlet New-AzDnsRecordConfig verwenden, um DNS-Eintragsobjekte zu erstellen.
Weitere Informationen finden Sie in den Beispielen.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordBase[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Metadaten
Gibt ein Array von Metadaten an, das dem RecordSet zugeordnet werden soll.
Metadaten werden mithilfe von Namen-Wert-Paaren angegeben, die als Hashtabellen dargestellt werden, z. B. @{"dept"="shopping";" env"="production"}.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen des zu erstellenden **RecordSets** an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
Gibt an, dass dieses Cmdlet das angegebene **RecordSet** überschreibt, wenn es bereits vorhanden ist.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecordType
Gibt den Typ des zu erstellenden DNS-Eintrags an.
Gültige Werte sind:
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SRV
- TXT-SOA-Einträge werden beim Erstellen der Zone automatisch erstellt und können nicht manuell erstellt werden.

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt die Ressourcengruppe an, die die DNS-Zone enthält.
Sie müssen auch den *Parameter ZoneName angeben,* um den Zonennamen anzugeben.
Alternativ können Sie die Zone und ressourcengruppe angeben, indem Sie ein DNS Zone-Objekt mit dem Parameter *Zone* übergeben.

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetResourceId
Alias Target Resource Id.

```yaml
Type: System.String
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ttl
Gibt die Time to Live (TTL) für das DNS RecordSet an.

```yaml
Type: System.UInt32
Parameter Sets: Fields, Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Gibt die DnsZone an, in der das **RecordSet erstellt werden soll.**
Alternativ können Sie die Zone mithilfe der *Parameter ZoneName* und *ResourceGroupName* angeben.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
Gibt den Namen der Zone an, in der das **RecordSet erstellt werden soll.**
Sie müssen auch die Ressourcengruppe angeben, die die Zone enthält, indem Sie den *Parameter ResourceGroupName* verwenden.
Alternativ können Sie die Zone und ressourcengruppe angeben, indem Sie ein DNS Zone-Objekt mit dem Parameter *Zone* übergeben.

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

### System.UInt32

### Microsoft.Azure.Management.Dns.Models.RecordType

### System.Collections.Hashtable

### Microsoft.Azure.Commands.Dns.DnsRecordBase[]

## AUSGABEN

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## NOTIZEN
Sie können den Parameter *Bestätigen* verwenden, um zu steuern, ob Sie von diesem Cmdlet zur Bestätigung aufgefordert werden.
Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn die $ConfirmPreference Windows PowerShell den Wert Mittel oder niedriger hat.
Wenn Sie *Bestätigen* oder *Bestätigen:$True,* werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.
Wenn Sie *Confirm:$False* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.

## VERWANDTE LINKS

[Add-AzDnsRecordConfig](./Add-AzDnsRecordConfig.md)

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordConfig](./New-AzDnsRecordConfig.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
