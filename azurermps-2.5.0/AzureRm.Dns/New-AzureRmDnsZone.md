---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46b14399d1cae624f4735111d809702cfd14180e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849356"
---
# <span data-ttu-id="db1e8-101">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="db1e8-101">New-AzureRmDnsZone</span></span>

## <span data-ttu-id="db1e8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="db1e8-102">SYNOPSIS</span></span>
<span data-ttu-id="db1e8-103">Erstellt eine neue DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="db1e8-103">Creates a new DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db1e8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="db1e8-104">SYNTAX</span></span>

```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db1e8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="db1e8-105">DESCRIPTION</span></span>
<span data-ttu-id="db1e8-106">Das Cmdlet **New-AzureRmDnsZone** erstellt eine neue DNS-Zone (Domain Name System) in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="db1e8-106">The **New-AzureRmDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="db1e8-107">Sie müssen einen eindeutigen DNS-Zonennamen für den Parameter *Name* angeben, oder das Cmdlet gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="db1e8-107">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="db1e8-108">Verwenden Sie nach der Erstellung der Zone das New-AzureRmDnsRecordSet-Cmdlet, um Daten Satz Sätze in der Zone zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="db1e8-108">After the zone is created, use the New-AzureRmDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="db1e8-109">Sie können den Parameter *Confirm* und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="db1e8-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="db1e8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="db1e8-110">EXAMPLES</span></span>

### <span data-ttu-id="db1e8-111">Beispiel 1: Erstellen einer DNS-Zone</span><span class="sxs-lookup"><span data-stu-id="db1e8-111">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="db1e8-112">Dieser Befehl erstellt eine neue DNS-Zone mit dem Namen MyZone.com in der angegebenen Ressourcengruppe und speichert Sie dann in der $Zone-Variablen.</span><span class="sxs-lookup"><span data-stu-id="db1e8-112">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="db1e8-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="db1e8-113">PARAMETERS</span></span>

### <span data-ttu-id="db1e8-114">-Name</span><span class="sxs-lookup"><span data-stu-id="db1e8-114">-Name</span></span>
<span data-ttu-id="db1e8-115">Gibt den Namen der zu erstellende DNS-Zone an.</span><span class="sxs-lookup"><span data-stu-id="db1e8-115">Specifies the name of the DNS zone to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db1e8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db1e8-116">-ResourceGroupName</span></span>
<span data-ttu-id="db1e8-117">Gibt die Ressourcengruppe an, in der die Zone erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="db1e8-117">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db1e8-118">-Tag</span><span class="sxs-lookup"><span data-stu-id="db1e8-118">-Tag</span></span>
<span data-ttu-id="db1e8-119">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="db1e8-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="db1e8-120">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="db1e8-120">For example:</span></span>

<span data-ttu-id="db1e8-121">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="db1e8-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db1e8-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="db1e8-122">-Confirm</span></span>
<span data-ttu-id="db1e8-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="db1e8-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db1e8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db1e8-124">-WhatIf</span></span>
<span data-ttu-id="db1e8-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="db1e8-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db1e8-126">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="db1e8-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db1e8-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="db1e8-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db1e8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db1e8-128">CommonParameters</span></span>
<span data-ttu-id="db1e8-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db1e8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db1e8-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db1e8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db1e8-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="db1e8-131">INPUTS</span></span>

### <span data-ttu-id="db1e8-132">Keine</span><span class="sxs-lookup"><span data-stu-id="db1e8-132">None</span></span>

<span data-ttu-id="db1e8-133">Sie können keine Eingabe an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="db1e8-133">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="db1e8-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="db1e8-134">OUTPUTS</span></span>

### <span data-ttu-id="db1e8-135">Microsoft. Azure. Commands. DNS. dnsZone</span><span class="sxs-lookup"><span data-stu-id="db1e8-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

<span data-ttu-id="db1e8-136">Dieses Cmdlet gibt ein Microsoft. Azure. Commands. DNS. dnsZone-Objekt zurück, das die neue DNS-Zone darstellt.</span><span class="sxs-lookup"><span data-stu-id="db1e8-136">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="db1e8-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="db1e8-137">NOTES</span></span>
<span data-ttu-id="db1e8-138">Sie können den Parameter *Confirm* verwenden, um zu steuern, ob dieses Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="db1e8-138">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="db1e8-139">Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn die $ConfirmPreference Windows PowerShell-Variable einen Wert von Mittel oder niedriger aufweist.</span><span class="sxs-lookup"><span data-stu-id="db1e8-139">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="db1e8-140">Wenn Sie *bestätigen* oder *bestätigen: $true* angeben, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="db1e8-140">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="db1e8-141">Wenn Sie *Confirm: $false* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="db1e8-141">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="db1e8-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="db1e8-142">RELATED LINKS</span></span>

[<span data-ttu-id="db1e8-143">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="db1e8-143">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="db1e8-144">Neu – AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="db1e8-144">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="db1e8-145">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="db1e8-145">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
