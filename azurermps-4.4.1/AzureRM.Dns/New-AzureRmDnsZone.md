---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
ms.openlocfilehash: 2b04478e80010f0edfac9488d45b36700db45eec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500853"
---
# <span data-ttu-id="0d1b2-101">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="0d1b2-101">New-AzureRmDnsZone</span></span>

## <span data-ttu-id="0d1b2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d1b2-102">SYNOPSIS</span></span>
<span data-ttu-id="0d1b2-103">Erstellt eine neue DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-103">Creates a new DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d1b2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d1b2-104">SYNTAX</span></span>

```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d1b2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d1b2-105">DESCRIPTION</span></span>
<span data-ttu-id="0d1b2-106">Das Cmdlet **New-AzureRmDnsZone** erstellt eine neue DNS-Zone (Domain Name System) in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-106">The **New-AzureRmDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="0d1b2-107">Sie müssen einen eindeutigen DNS-Zonennamen für den Parameter *Name* angeben, oder das Cmdlet gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-107">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="0d1b2-108">Verwenden Sie nach der Erstellung der Zone das New-AzureRmDnsRecordSet-Cmdlet, um Daten Satz Sätze in der Zone zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-108">After the zone is created, use the New-AzureRmDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="0d1b2-109">Sie können den Parameter *Confirm* und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="0d1b2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d1b2-110">EXAMPLES</span></span>

### <span data-ttu-id="0d1b2-111">Beispiel 1: Erstellen einer DNS-Zone</span><span class="sxs-lookup"><span data-stu-id="0d1b2-111">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="0d1b2-112">Dieser Befehl erstellt eine neue DNS-Zone mit dem Namen MyZone.com in der angegebenen Ressourcengruppe und speichert Sie dann in der $Zone-Variablen.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-112">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="0d1b2-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d1b2-113">PARAMETERS</span></span>

### <span data-ttu-id="0d1b2-114">-Name</span><span class="sxs-lookup"><span data-stu-id="0d1b2-114">-Name</span></span>
<span data-ttu-id="0d1b2-115">Gibt den Namen der zu erstellende DNS-Zone an.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-115">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="0d1b2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d1b2-116">-ResourceGroupName</span></span>
<span data-ttu-id="0d1b2-117">Gibt die Ressourcengruppe an, in der die Zone erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-117">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="0d1b2-118">-Tag</span><span class="sxs-lookup"><span data-stu-id="0d1b2-118">-Tag</span></span>
<span data-ttu-id="0d1b2-119">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="0d1b2-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0d1b2-120">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="0d1b2-120">For example:</span></span>

<span data-ttu-id="0d1b2-121">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="0d1b2-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d1b2-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0d1b2-122">-Confirm</span></span>
<span data-ttu-id="0d1b2-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d1b2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d1b2-124">-WhatIf</span></span>
<span data-ttu-id="0d1b2-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d1b2-126">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d1b2-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d1b2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d1b2-128">-DefaultProfile</span></span>
<span data-ttu-id="0d1b2-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d1b2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d1b2-130">CommonParameters</span></span>
<span data-ttu-id="0d1b2-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d1b2-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d1b2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d1b2-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d1b2-133">INPUTS</span></span>

### <span data-ttu-id="0d1b2-134">Keine</span><span class="sxs-lookup"><span data-stu-id="0d1b2-134">None</span></span>
<span data-ttu-id="0d1b2-135">Sie können keine Eingabe an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-135">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="0d1b2-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d1b2-136">OUTPUTS</span></span>

### <span data-ttu-id="0d1b2-137">Microsoft. Azure. Commands. DNS. dnsZone</span><span class="sxs-lookup"><span data-stu-id="0d1b2-137">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="0d1b2-138">Dieses Cmdlet gibt ein Microsoft. Azure. Commands. DNS. dnsZone-Objekt zurück, das die neue DNS-Zone darstellt.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-138">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="0d1b2-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d1b2-139">NOTES</span></span>
<span data-ttu-id="0d1b2-140">Sie können den Parameter *Confirm* verwenden, um zu steuern, ob dieses Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-140">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="0d1b2-141">Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn die $ConfirmPreference Windows PowerShell-Variable einen Wert von Mittel oder niedriger aufweist.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-141">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="0d1b2-142">Wenn Sie *bestätigen* oder *bestätigen: $true* angeben, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-142">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="0d1b2-143">Wenn Sie *Confirm: $false* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-143">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="0d1b2-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d1b2-144">RELATED LINKS</span></span>

[<span data-ttu-id="0d1b2-145">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="0d1b2-145">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="0d1b2-146">Neu – AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0d1b2-146">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="0d1b2-147">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="0d1b2-147">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
