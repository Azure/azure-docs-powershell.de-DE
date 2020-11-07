---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
ms.openlocfilehash: e678ceabefac101a70724a8a901a9bf3db08a59b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664272"
---
# <span data-ttu-id="be47f-101">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="be47f-101">Get-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="be47f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="be47f-102">SYNOPSIS</span></span>
<span data-ttu-id="be47f-103">Ruft einen DNS-Eintragssatz ab.</span><span class="sxs-lookup"><span data-stu-id="be47f-103">Gets a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be47f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="be47f-104">SYNTAX</span></span>

### <span data-ttu-id="be47f-105">Felder</span><span class="sxs-lookup"><span data-stu-id="be47f-105">Fields</span></span>
```
Get-AzureRmDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be47f-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="be47f-106">Object</span></span>
```
Get-AzureRmDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be47f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be47f-107">DESCRIPTION</span></span>
<span data-ttu-id="be47f-108">Das Cmdlet " **Get-AzureRmDnsRecordSet** " Ruft den DNS-Eintragssatz (Domain Name System) mit dem angegebenen Namen und Typ in der angegebenen Zone ab.</span><span class="sxs-lookup"><span data-stu-id="be47f-108">The **Get-AzureRmDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>

<span data-ttu-id="be47f-109">Wenn Sie die Parameter *Name* oder *RecordType* nicht angeben, gibt dieses Cmdlet alle Daten Satz Sätze des angegebenen Typs in der Zone zurück.</span><span class="sxs-lookup"><span data-stu-id="be47f-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="be47f-110">Wenn Sie den Parameter *RecordType* , aber nicht den Parameter *Name* angeben, gibt dieses Cmdlet alle Daten Satz Sätze des angegebenen Datensatztyps zurück.</span><span class="sxs-lookup"><span data-stu-id="be47f-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>

<span data-ttu-id="be47f-111">Sie können den Pipelineoperator verwenden, um ein **dnsZone** -Objekt an dieses Cmdlet zu übergeben, oder Sie können ein **dnsZone** -Objekt als *Zone* -Parameter übergeben, oder Alternativ können Sie die Zone und die Ressourcengruppe nach Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="be47f-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="be47f-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be47f-112">EXAMPLES</span></span>

### <span data-ttu-id="be47f-113">Beispiel 1: Abrufen von Daten Satz Sätzen mit einem angegebenen Namen und Typ</span><span class="sxs-lookup"><span data-stu-id="be47f-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="be47f-114">Dieser Befehl ruft den Daten Satz Satz des Datensatztyps A mit dem Namen www in der angegebenen Ressourcengruppe und Zone ab und speichert ihn dann in der $Recordset-Variablen.</span><span class="sxs-lookup"><span data-stu-id="be47f-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="be47f-115">Da die Parameter *Name* und *RecordType* angegeben werden, wird nur ein **Recordset** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="be47f-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="be47f-116">Beispiel 2: Abrufen von Daten Satz Sätzen eines angegebenen Typs</span><span class="sxs-lookup"><span data-stu-id="be47f-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="be47f-117">Dieser Befehl ruft ein Array aller Daten Satz Sätze des Datensatztyps A in der Zone mit dem Namen MyZone.com in der Ressourcengruppe myresourcegroup ab und speichert Sie dann in der $Recordsets Variablen.</span><span class="sxs-lookup"><span data-stu-id="be47f-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="be47f-118">Beispiel 3: Abrufen aller Daten Satz Sätze in einer Zone</span><span class="sxs-lookup"><span data-stu-id="be47f-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="be47f-119">Dieser Befehl ruft ein Array aller Datensatzgruppen in der Zone mit dem Namen MyZone.com in der Ressourcengruppe mit dem Namen myresourcegroup ab und speichert Sie dann in der $Recordsets-Variablen.</span><span class="sxs-lookup"><span data-stu-id="be47f-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="be47f-120">Beispiel 4: Abrufen aller Daten Satz Sätze in einer Zone mithilfe eines dnsZone-Objekts</span><span class="sxs-lookup"><span data-stu-id="be47f-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzureRmDnsRecordSet -Zone $Zone
```

<span data-ttu-id="be47f-121">Dieses Beispiel entspricht Beispiel 3 oben.</span><span class="sxs-lookup"><span data-stu-id="be47f-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="be47f-122">Dieses Mal wird die Zone mithilfe eines Zone-Objekts angegeben.</span><span class="sxs-lookup"><span data-stu-id="be47f-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="be47f-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="be47f-123">PARAMETERS</span></span>

### <span data-ttu-id="be47f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="be47f-124">-Name</span></span>
<span data-ttu-id="be47f-125">Gibt den Namen des abzurufenden **Recordsets** an.</span><span class="sxs-lookup"><span data-stu-id="be47f-125">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="be47f-126">Wenn Sie den Parameter *Name* nicht angeben, werden alle Daten Satz Sätze des angegebenen Typs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="be47f-126">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

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

### <span data-ttu-id="be47f-127">-RecordType</span><span class="sxs-lookup"><span data-stu-id="be47f-127">-RecordType</span></span>
<span data-ttu-id="be47f-128">Gibt den Typ des DNS-Eintrags an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="be47f-128">Specifies the type of DNS record that this cmdlet gets.</span></span>

<span data-ttu-id="be47f-129">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="be47f-129">Valid values are:</span></span> 

- <span data-ttu-id="be47f-130">Eine</span><span class="sxs-lookup"><span data-stu-id="be47f-130">A</span></span>
- <span data-ttu-id="be47f-131">AAAA</span><span class="sxs-lookup"><span data-stu-id="be47f-131">AAAA</span></span>
- <span data-ttu-id="be47f-132">CNAME</span><span class="sxs-lookup"><span data-stu-id="be47f-132">CNAME</span></span>
- <span data-ttu-id="be47f-133">MX</span><span class="sxs-lookup"><span data-stu-id="be47f-133">MX</span></span>
- <span data-ttu-id="be47f-134">NS</span><span class="sxs-lookup"><span data-stu-id="be47f-134">NS</span></span>
- <span data-ttu-id="be47f-135">PTR</span><span class="sxs-lookup"><span data-stu-id="be47f-135">PTR</span></span>
- <span data-ttu-id="be47f-136">SOA</span><span class="sxs-lookup"><span data-stu-id="be47f-136">SOA</span></span>
- <span data-ttu-id="be47f-137">SRV</span><span class="sxs-lookup"><span data-stu-id="be47f-137">SRV</span></span>
- <span data-ttu-id="be47f-138">TXT</span><span class="sxs-lookup"><span data-stu-id="be47f-138">TXT</span></span>

<span data-ttu-id="be47f-139">Wenn Sie den *RecordType* -Parameter nicht angeben, müssen Sie auch den Parameter *Name* weglassen.</span><span class="sxs-lookup"><span data-stu-id="be47f-139">If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="be47f-140">Dieses Cmdlet gibt dann alle Daten Satz Sätze in der Zone (aller Namen und Typen) zurück.</span><span class="sxs-lookup"><span data-stu-id="be47f-140">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be47f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be47f-141">-ResourceGroupName</span></span>
<span data-ttu-id="be47f-142">Gibt die Ressourcengruppe an, die die DNS-Zone enthält.</span><span class="sxs-lookup"><span data-stu-id="be47f-142">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="be47f-143">Der Zonen Name muss auch mit dem Parameter *zonename* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="be47f-143">The zone name must also be specified, using the *ZoneName* parameter.</span></span>

<span data-ttu-id="be47f-144">Alternativ können Sie die Zone und die Ressourcengruppe angeben, indem Sie ein **dnsZone** -Objekt mit dem *Zone* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="be47f-144">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="be47f-145">-Zone</span><span class="sxs-lookup"><span data-stu-id="be47f-145">-Zone</span></span>
<span data-ttu-id="be47f-146">Gibt die DNS-Zone an, die den Daten Satz Satz enthält, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="be47f-146">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="be47f-147">Alternativ können Sie die Zone mithilfe der Parameter *zonename* und *ResourceGroupName* angeben.</span><span class="sxs-lookup"><span data-stu-id="be47f-147">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="be47f-148">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="be47f-148">-ZoneName</span></span>
<span data-ttu-id="be47f-149">Gibt den Namen der DNS-Zone an, die den aufzurufenden Daten Satz Satz enthält.</span><span class="sxs-lookup"><span data-stu-id="be47f-149">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="be47f-150">Die Ressourcengruppe mit der Zone muss ebenfalls mithilfe des *ResourceGroupName* -Parameters angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="be47f-150">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="be47f-151">Alternativ können Sie die Zone und die Ressourcengruppe angeben, indem Sie ein DNS-Zonenobjekt mit dem *Zone* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="be47f-151">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="be47f-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be47f-152">-DefaultProfile</span></span>
<span data-ttu-id="be47f-153">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="be47f-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be47f-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be47f-154">CommonParameters</span></span>
<span data-ttu-id="be47f-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be47f-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be47f-156">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be47f-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be47f-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="be47f-157">INPUTS</span></span>

### <span data-ttu-id="be47f-158">Microsoft. Azure. Commands. DNS. dnsZone</span><span class="sxs-lookup"><span data-stu-id="be47f-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="be47f-159">Sie können ein **dnsZone** -Objekt an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="be47f-159">You can pipe a **DnsZone** object to this cmdlet.</span></span>
<span data-ttu-id="be47f-160">Das **dnsZone** -Objekt stellt die Zone dar, in der nach dem **Recordset** -Objekt gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="be47f-160">The **DnsZone** object represents the zone in which to look for the **RecordSet** object.</span></span>

## <span data-ttu-id="be47f-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="be47f-161">OUTPUTS</span></span>

### <span data-ttu-id="be47f-162">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="be47f-162">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="be47f-163">Dieses Cmdlet gibt ein oder mehrere Objekte zurück, die die gefundenen Daten Satz Sätze darstellen.</span><span class="sxs-lookup"><span data-stu-id="be47f-163">This cmdlet returns one or more objects that represents the record sets that are found.</span></span>
<span data-ttu-id="be47f-164">Es wird höchstens ein **Recordset** zurückgegeben, wenn die Parameter *Name* und *RecordType* angegeben werden, da andernfalls mehrere **Recordset** -Objekte als Array zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="be47f-164">There will be at most one **RecordSet** returned if the *Name* and *RecordType* parameters are specified, otherwise multiple **RecordSet** objects are returned as an array.</span></span>

## <span data-ttu-id="be47f-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="be47f-165">NOTES</span></span>

## <span data-ttu-id="be47f-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="be47f-166">RELATED LINKS</span></span>

[<span data-ttu-id="be47f-167">Neu – AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="be47f-167">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="be47f-168">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="be47f-168">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="be47f-169">Satz-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="be47f-169">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)


