---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: e75d394596b85c75dc79b0eb0d2b19525aa9c7c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147972"
---
# <span data-ttu-id="ca840-101">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ca840-101">Set-AzDnsRecordSet</span></span>

## <span data-ttu-id="ca840-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca840-102">SYNOPSIS</span></span>
<span data-ttu-id="ca840-103">Aktualisiert einen DNS-Eintragssatz.</span><span class="sxs-lookup"><span data-stu-id="ca840-103">Updates a DNS record set.</span></span>

## <span data-ttu-id="ca840-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca840-104">SYNTAX</span></span>

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca840-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ca840-105">DESCRIPTION</span></span>
<span data-ttu-id="ca840-106">Das **Cmdlet Set-AzDnsRecordSet** aktualisiert einen Datensatzsatz im Azure-DNS-Dienst von einem lokalen **RecordSet-Objekt.**</span><span class="sxs-lookup"><span data-stu-id="ca840-106">The **Set-AzDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>
<span data-ttu-id="ca840-107">Sie können ein **"RecordSet"-Objekt** als Parameter oder mithilfe des Pipelineoperators übergeben.</span><span class="sxs-lookup"><span data-stu-id="ca840-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>
<span data-ttu-id="ca840-108">Sie können den Parameter *"Bestätigen"* und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="ca840-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="ca840-109">Der Datensatzsatz wird nicht aktualisiert, wenn er seit dem Abrufen des lokalen **"RecordSet"-Objekts** in Azure DNS geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="ca840-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="ca840-110">Dies bietet Schutz für gleichzeitige Änderungen.</span><span class="sxs-lookup"><span data-stu-id="ca840-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="ca840-111">Sie können dieses Verhalten mithilfe des Parameters *"Overwrite"* unterdrücken, der den Datensatzsatz unabhängig von gleichzeitigen Änderungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ca840-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="ca840-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ca840-112">EXAMPLES</span></span>

### <span data-ttu-id="ca840-113">Beispiel 1: Aktualisieren eines Datensatzes</span><span class="sxs-lookup"><span data-stu-id="ca840-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

<span data-ttu-id="ca840-114">Der erste Befehl verwendet das Get-AzDnsRecordSet Cmdlet, um den angegebenen Datensatzsatz zu erhalten, und speichert ihn dann in der $RecordSet Variable.</span><span class="sxs-lookup"><span data-stu-id="ca840-114">The first command uses the Get-AzDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="ca840-115">Der zweite und dritte Befehl sind Off-Line-Vorgänge, um dem Datensatzsatz zwei A-Datensätze hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ca840-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>
<span data-ttu-id="ca840-116">Der letzte Befehl verwendet das **Cmdlet "Set-AzDnsRecordSet",** um das Update zu commiten.</span><span class="sxs-lookup"><span data-stu-id="ca840-116">The final command uses the **Set-AzDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="ca840-117">Beispiel 2: Aktualisieren eines SOA-Eintrags</span><span class="sxs-lookup"><span data-stu-id="ca840-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="ca840-118">Der erste Befehl verwendet das **Cmdlet "Get-AzDnsRecordset",** um den angegebenen Datensatzsatz zu erhalten, und speichert ihn dann in der $RecordSet Variable.</span><span class="sxs-lookup"><span data-stu-id="ca840-118">The first command uses the **Get-AzDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="ca840-119">Der zweite Befehl aktualisiert den angegebenen SOA-Eintrag in $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="ca840-119">The second command updates the specified SOA record in $RecordSet.</span></span>
<span data-ttu-id="ca840-120">Der letzte Befehl verwendet das **Cmdlet "Set-AzDnsRecordSet",** um das Update in $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="ca840-120">The final command uses the **Set-AzDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="ca840-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca840-121">PARAMETERS</span></span>

### <span data-ttu-id="ca840-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca840-122">-DefaultProfile</span></span>
<span data-ttu-id="ca840-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ca840-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca840-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="ca840-124">-Overwrite</span></span>
<span data-ttu-id="ca840-125">Gibt an, dass der Datensatzsatz unabhängig von gleichzeitigen Änderungen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ca840-125">Indicates to update the record set regardless of concurrent changes.</span></span>
<span data-ttu-id="ca840-126">Der Datensatzsatz wird nicht aktualisiert, wenn er in Azure DNS seit dem Abrufen des lokalen **Objekts "RecordSet"** geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="ca840-126">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="ca840-127">Dies bietet Schutz für gleichzeitige Änderungen.</span><span class="sxs-lookup"><span data-stu-id="ca840-127">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="ca840-128">Um dieses Verhalten zu unterdrücken, können Sie den Parameter *"Overwrite"* verwenden, der unabhängig von gleichzeitigen Änderungen dazu führt, dass der Datensatzsatz aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ca840-128">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="ca840-129">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="ca840-129">-RecordSet</span></span>
<span data-ttu-id="ca840-130">Gibt das zu **aktualisierende RecordSet** an.</span><span class="sxs-lookup"><span data-stu-id="ca840-130">Specifies the **RecordSet** to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca840-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca840-131">-Confirm</span></span>
<span data-ttu-id="ca840-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ca840-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca840-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ca840-133">-WhatIf</span></span>
<span data-ttu-id="ca840-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca840-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca840-135">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca840-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca840-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ca840-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca840-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca840-137">CommonParameters</span></span>
<span data-ttu-id="ca840-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca840-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca840-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca840-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca840-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ca840-140">INPUTS</span></span>

### <span data-ttu-id="ca840-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ca840-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="ca840-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ca840-142">OUTPUTS</span></span>

### <span data-ttu-id="ca840-143">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ca840-143">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="ca840-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ca840-144">NOTES</span></span>
<span data-ttu-id="ca840-145">Mit dem Parameter *"Bestätigen"* können Sie steuern, ob Sie von diesem Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="ca840-145">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="ca840-146">Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn $ConfirmPreference Windows PowerShell Variable den Wert "Mittel" oder "Niedriger" hat.</span><span class="sxs-lookup"><span data-stu-id="ca840-146">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="ca840-147">Wenn Sie *"Bestätigen"* oder *"Bestätigen:$True"* angeben, fordert Sie dieses Cmdlet zur Bestätigung auf, bevor es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca840-147">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="ca840-148">Wenn Sie *"Confirm:$False" angeben,* werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="ca840-148">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="ca840-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ca840-149">RELATED LINKS</span></span>

[<span data-ttu-id="ca840-150">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ca840-150">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="ca840-151">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ca840-151">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="ca840-152">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ca840-152">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)
