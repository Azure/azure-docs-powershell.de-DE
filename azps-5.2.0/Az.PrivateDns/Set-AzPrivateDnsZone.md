---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: 06b8a8bd7027b95d7f51e186b0184707ffd296a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298971"
---
# <span data-ttu-id="da493-101">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="da493-101">Set-AzPrivateDnsZone</span></span>

## <span data-ttu-id="da493-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da493-102">SYNOPSIS</span></span>
<span data-ttu-id="da493-103">Aktualisiert eine private DNS-Zone aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="da493-103">Updates a Private DNS zone from a resource group.</span></span>

## <span data-ttu-id="da493-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da493-104">SYNTAX</span></span>

### <span data-ttu-id="da493-105">Felder (Standard)</span><span class="sxs-lookup"><span data-stu-id="da493-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da493-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="da493-106">ResourceId</span></span>
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da493-107">Objekt</span><span class="sxs-lookup"><span data-stu-id="da493-107">Object</span></span>
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da493-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da493-108">DESCRIPTION</span></span>
<span data-ttu-id="da493-109">Das **Cmdlet Set-AzPrivateDnsZone** aktualisiert dauerhaft eine Private Domain Name System (DNS)-Zone aus einer angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="da493-109">The **Set-AzPrivateDnsZone** cmdlet permanently updates a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="da493-110">Sie können ein **PrivateDnsZone-Objekt** mit dem *Parameter "PrivateZone"* oder mit dem Pipelineoperator übergeben, oder Sie können die Parameter *"Name"* und *"ResourceGroupName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="da493-110">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="da493-111">Sie können den Parameter "Bestätigen" und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="da493-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="da493-112">Beim Angeben der Zone mit einem (über die Pipeline oder den Parameter *"Zone"* übergebenen) **PrivatenDnsZone-Objekt** wird die Zone nicht aktualisiert, wenn sie in Azure DNS geändert wurde, da das lokale **"PrivateDnsZone"-Objekt** abgerufen wurde (nur Vorgänge, die direkt mit der DNS-Zonenressourcenanzahl als Änderungen ausgeführt werden, Vorgänge für Datensatzsätze innerhalb der Zone nicht).</span><span class="sxs-lookup"><span data-stu-id="da493-112">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="da493-113">Dies bietet Schutz für Änderungen gleichzeitiger Zonen.</span><span class="sxs-lookup"><span data-stu-id="da493-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="da493-114">Dies kann mithilfe des Parameters *"Overwrite"* unterdrückt werden, der die Zone unabhängig von gleichzeitigen Änderungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="da493-114">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="da493-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="da493-115">EXAMPLES</span></span>

### <span data-ttu-id="da493-116">Beispiel 1: Aktualisieren einer privaten Zone</span><span class="sxs-lookup"><span data-stu-id="da493-116">Example 1: Updates a private zone</span></span>
```
PS C:\>Set-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup" -Tag @{tag1="value1";tag2="value2"}


This command updates the zone named myzone.com from the resource group named MyResourceGroup with the tags provided. Use Get-AzPrivateDnsZone to retrieve the updated zone. Updated zone would look something like this:

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {tag1="value1";tag2="value2"}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="da493-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da493-117">PARAMETERS</span></span>

### <span data-ttu-id="da493-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da493-118">-DefaultProfile</span></span>
<span data-ttu-id="da493-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="da493-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da493-120">-Name</span><span class="sxs-lookup"><span data-stu-id="da493-120">-Name</span></span>
<span data-ttu-id="da493-121">Gibt den Namen der privaten DNS-Zone an, die von diesem Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="da493-121">Specifies the name of the Private DNS zone that this cmdlet updates.</span></span>
<span data-ttu-id="da493-122">Sie müssen auch den Parameter *"ResourceGroupName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="da493-122">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="da493-123">Alternativ können Sie die private DNS-Zone mit dem Parameter *"Zone"* angeben.</span><span class="sxs-lookup"><span data-stu-id="da493-123">Alternatively, you can specify the private DNS zone using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da493-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="da493-124">-Overwrite</span></span>
<span data-ttu-id="da493-125">Wenn Sie die Zone mit einem **PrivateDnsZone-Objekt** angeben (das über die Pipeline oder den *Parameter "Zone"* übergeben wird), wird die Zone nicht aktualisiert, wenn sie in Azure DNS geändert wurde, da das lokale **"DnsZone"-Objekt** abgerufen wurde (nur Vorgänge direkt für die DNS-Zonenressourcenanzahl als Änderungen, Vorgänge mit Datensatzsätzen innerhalb der Zone nicht).</span><span class="sxs-lookup"><span data-stu-id="da493-125">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="da493-126">Dies bietet Schutz für Änderungen gleichzeitiger Zonen.</span><span class="sxs-lookup"><span data-stu-id="da493-126">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="da493-127">Dies kann mithilfe des Parameters *"Overwrite"* unterdrückt werden, der die Zone unabhängig von gleichzeitigen Änderungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="da493-127">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da493-128">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="da493-128">-PrivateZone</span></span>
<span data-ttu-id="da493-129">Das festgelegte Zonenobjekt.</span><span class="sxs-lookup"><span data-stu-id="da493-129">The zone object to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da493-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da493-130">-ResourceGroupName</span></span>
<span data-ttu-id="da493-131">Gibt den Namen der Ressourcengruppe an, die die zu aktualisierende Zone enthält.</span><span class="sxs-lookup"><span data-stu-id="da493-131">Specifies the name of the resource group that contains the zone to be updated.</span></span>
<span data-ttu-id="da493-132">Sie müssen auch den *Parameter "ZoneName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="da493-132">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="da493-133">Alternativ können Sie die private DNS-Zone mit einem **DnsZone-Objekt** angeben, das entweder über die Pipeline oder den Parameter *"Zone" übergeben* wird.</span><span class="sxs-lookup"><span data-stu-id="da493-133">Alternatively, you can specify the private DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da493-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da493-134">-ResourceId</span></span>
<span data-ttu-id="da493-135">Private DNS Zone ResourceID.</span><span class="sxs-lookup"><span data-stu-id="da493-135">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da493-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="da493-136">-Tag</span></span>
<span data-ttu-id="da493-137">Eine Hashtabelle, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="da493-137">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da493-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da493-138">-Confirm</span></span>
<span data-ttu-id="da493-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="da493-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da493-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="da493-140">-WhatIf</span></span>
<span data-ttu-id="da493-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da493-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da493-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da493-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da493-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da493-143">CommonParameters</span></span>
<span data-ttu-id="da493-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da493-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da493-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da493-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da493-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="da493-146">INPUTS</span></span>

### <span data-ttu-id="da493-147">System.String</span><span class="sxs-lookup"><span data-stu-id="da493-147">System.String</span></span>

### <span data-ttu-id="da493-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="da493-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="da493-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="da493-149">OUTPUTS</span></span>

### <span data-ttu-id="da493-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="da493-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="da493-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="da493-151">NOTES</span></span>

## <span data-ttu-id="da493-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="da493-152">RELATED LINKS</span></span>

[<span data-ttu-id="da493-153">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="da493-153">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="da493-154">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="da493-154">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="da493-155">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="da493-155">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
