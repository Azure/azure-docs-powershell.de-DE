---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/powershell/module/az.dns/new-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
ms.openlocfilehash: c85cc0b4ad60529cc57becb9ca864751d90a37c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935048"
---
# New-AzDnsRecordConfig

## SYNOPSIS
Erstellt ein neues lokales DNS-Eintrag-Objekt.

## SYNTAX

### A
```
New-AzDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Aaaa
```
New-AzDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Ns
```
New-AzDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Mx
```
New-AzDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Ptr
```
New-AzDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Txt
```
New-AzDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Srv
```
New-AzDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CName
```
New-AzDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Caa
```
New-AzDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet New-AzDnsRecordConfig** erstellt ein lokales **DnsRecord-Objekt.**
Ein Array dieser Objekte wird an das cmdlet New-AzDnsRecordSet übergeben, das den *Parameter DnsRecords* verwendet, um die datensätze anzugeben, die im Datensatzsatz erstellt werden müssen.

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
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
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

## PARAMETER

### -CaaFlags
Die Kennzeichnungen für den hinzuzufügende CAA-Eintrag. Muss eine Zahl zwischen 0 und 255 sein.

```yaml
Type: System.Byte
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CaaTag
Das Tagfeld des hinzuzufügende CAA-Eintrags.

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CaaValue
Das Wertfeld für den hinzuzufügende CAA-Eintrag.

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Cname
Gibt den Domänennamen für einen Kanonischen Namen (CNAME)-Eintrag an.

```yaml
Type: System.String
Parameter Sets: CName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Exchange
Gibt den Namen des E-Mail-Exchange-Servers für einen Mail Exchange (MX)-Eintrag an.

```yaml
Type: System.String
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ipv4Address
Gibt eine IPv4-Adresse für einen A-Eintrag an.

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ipv6Address
Gibt eine IPv6-Adresse für einen AAAA-Eintrag an.

```yaml
Type: System.String
Parameter Sets: Aaaa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nsdname
Gibt den Namen des Namenservers für einen Namenserverdatensatz (NS) an.

```yaml
Type: System.String
Parameter Sets: Ns
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Port
Gibt den Port für einen Dienstdatensatz (SRV) an.

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Preference
Gibt die Einstellung für einen MX-Eintrag an.

```yaml
Type: System.UInt16
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Priorität
Gibt die Priorität für einen SRV-Eintrag an.

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ptrdname
Gibt den Zieldomänennamen eines Zeigerressourcendatensatzs (PTR) an.

```yaml
Type: System.String
Parameter Sets: Ptr
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Target
Gibt das Ziel für einen SRV-Eintrag an.

```yaml
Type: System.String
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Wert
Gibt den Wert für einen TXT-Eintrag an.

```yaml
Type: System.String
Parameter Sets: Txt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Weight
Gibt die Gewichtung für einen SRV-Eintrag an.

```yaml
Type: System.UInt16
Parameter Sets: Srv
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

### System.UInt16

### System.Byte

## AUSGABEN

### Microsoft.Azure.Commands.Dns.DnsRecordBase

## NOTIZEN

## VERWANDTE LINKS

[Add-AzDnsRecordConfig](./Add-AzDnsRecordConfig.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordConfig](./Remove-AzDnsRecordConfig.md)
