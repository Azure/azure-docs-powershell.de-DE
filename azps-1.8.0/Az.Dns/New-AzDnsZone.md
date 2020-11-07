---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: eb7a2f3494521a5505db0224bb1ae0ff948d406f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661097"
---
# <span data-ttu-id="2fe40-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="2fe40-101">New-AzDnsZone</span></span>

## <span data-ttu-id="2fe40-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2fe40-102">SYNOPSIS</span></span>
<span data-ttu-id="2fe40-103">Erstellt eine neue DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="2fe40-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="2fe40-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fe40-104">SYNTAX</span></span>

### <span data-ttu-id="2fe40-105">IDs (Standard)</span><span class="sxs-lookup"><span data-stu-id="2fe40-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fe40-106">Objekte</span><span class="sxs-lookup"><span data-stu-id="2fe40-106">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fe40-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2fe40-107">DESCRIPTION</span></span>
<span data-ttu-id="2fe40-108">Das Cmdlet **New-AzDnsZone** erstellt eine neue DNS-Zone (Domain Name System) in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2fe40-108">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="2fe40-109">Sie müssen einen eindeutigen DNS-Zonennamen für den Parameter *Name* angeben, oder das Cmdlet gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="2fe40-109">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="2fe40-110">Verwenden Sie nach der Erstellung der Zone das New-AzDnsRecordSet-Cmdlet, um Daten Satz Sätze in der Zone zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2fe40-110">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="2fe40-111">Sie können den Parameter *Confirm* und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="2fe40-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="2fe40-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2fe40-112">EXAMPLES</span></span>

### <span data-ttu-id="2fe40-113">Beispiel 1: Erstellen einer DNS-Zone</span><span class="sxs-lookup"><span data-stu-id="2fe40-113">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="2fe40-114">Dieser Befehl erstellt eine neue DNS-Zone mit dem Namen MyZone.com in der angegebenen Ressourcengruppe und speichert Sie dann in der $Zone-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2fe40-114">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="2fe40-115">Beispiel 2: Erstellen einer privaten DNS-Zone durch Angabe virtueller Netzwerk-IDs</span><span class="sxs-lookup"><span data-stu-id="2fe40-115">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="2fe40-116">Mit diesem Befehl wird eine neue private DNS-Zone mit dem Namen myprivatezone.com in der angegebenen Ressourcengruppe mit einem zugehörigen Auflösungs-virtuellen Netzwerk (Angabe der ID) erstellt und dann in der $Zone-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2fe40-116">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="2fe40-117">Beispiel 3: Erstellen einer privaten DNS-Zone durch angeben virtueller Netzwerkobjekte</span><span class="sxs-lookup"><span data-stu-id="2fe40-117">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="2fe40-118">Mit diesem Befehl wird eine neue private DNS-Zone mit dem Namen myprivatezone.com in der angegebenen Ressourcengruppe mit einem virtuellen Netzwerk für die Auflösung erstellt (auf das durch $ResVirtualNetwork Variable verwiesen wird) und dann in der $Zone-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2fe40-118">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="2fe40-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fe40-119">PARAMETERS</span></span>

### <span data-ttu-id="2fe40-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fe40-120">-DefaultProfile</span></span>
<span data-ttu-id="2fe40-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2fe40-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fe40-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2fe40-122">-Name</span></span>
<span data-ttu-id="2fe40-123">Gibt den Namen der zu erstellende DNS-Zone an.</span><span class="sxs-lookup"><span data-stu-id="2fe40-123">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="2fe40-124">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2fe40-124">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="2fe40-125">In der Liste der virtuellen Netzwerke, die die Hostnamen für virtuelle Maschinen registrieren, werden die Datensätze in dieser DNS-Zone nur für private Zonen zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="2fe40-125">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fe40-126">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="2fe40-126">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="2fe40-127">Die Liste der virtuellen Netzwerk-IDs, die Hostnamen für virtuelle Maschinen in dieser DNS-Zone registrieren, die nur für private Zonen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="2fe40-127">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fe40-128">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2fe40-128">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="2fe40-129">Die Liste der virtuellen Netzwerke, in denen Datensätze in dieser DNS-Zone aufgelöst werden können, die nur für private Zonen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="2fe40-129">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fe40-130">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="2fe40-130">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="2fe40-131">Die Liste der virtuellen Netzwerk-IDs, mit denen Datensätze in dieser DNS-Zone aufgelöst werden können, die nur für private Zonen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="2fe40-131">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fe40-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fe40-132">-ResourceGroupName</span></span>
<span data-ttu-id="2fe40-133">Gibt die Ressourcengruppe an, in der die Zone erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2fe40-133">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="2fe40-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="2fe40-134">-Tag</span></span>
<span data-ttu-id="2fe40-135">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="2fe40-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2fe40-136">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="2fe40-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2fe40-137">-Zonetype</span><span class="sxs-lookup"><span data-stu-id="2fe40-137">-ZoneType</span></span>
<span data-ttu-id="2fe40-138">Der Typ der Zone, öffentlich oder privat.</span><span class="sxs-lookup"><span data-stu-id="2fe40-138">The type of the zone, Public or Private.</span></span> <span data-ttu-id="2fe40-139">Zonen ohne Typ oder mit einem öffentlichen Typ werden auf der öffentlichen DNS-Dienstebene zur Verwendung in der DNS-Hierarchie zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="2fe40-139">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="2fe40-140">Zonen mit einem privaten Typ werden nur aus dem Satz der zugeordneten virtuellen Netzwerke angezeigt (dieses Feature befindet sich in der Vorschau).</span><span class="sxs-lookup"><span data-stu-id="2fe40-140">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="2fe40-141">Diese Eigenschaft kann für eine Zone nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2fe40-141">This property cannot be changed for a zone.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.ZoneType]
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fe40-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2fe40-142">-Confirm</span></span>
<span data-ttu-id="2fe40-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2fe40-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fe40-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fe40-144">-WhatIf</span></span>
<span data-ttu-id="2fe40-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fe40-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2fe40-146">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fe40-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2fe40-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2fe40-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fe40-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fe40-148">CommonParameters</span></span>
<span data-ttu-id="2fe40-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fe40-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fe40-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fe40-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fe40-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2fe40-151">INPUTS</span></span>

### <span data-ttu-id="2fe40-152">System. String</span><span class="sxs-lookup"><span data-stu-id="2fe40-152">System.String</span></span>

### <span data-ttu-id="2fe40-153">System. Nullable ' 1 [[Microsoft. Azure. Management. DNS. Models. zonetype, Microsoft. Azure. Management. DNS, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2fe40-153">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="2fe40-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2fe40-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2fe40-155">System. Collections. Generic. List ' 1 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2fe40-155">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2fe40-156">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Management. Internal. Network. Common. IResourceReference, Microsoft. Azure. PowerShell. Clients. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2fe40-156">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="2fe40-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2fe40-157">OUTPUTS</span></span>

### <span data-ttu-id="2fe40-158">Microsoft. Azure. Commands. DNS. dnsZone</span><span class="sxs-lookup"><span data-stu-id="2fe40-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="2fe40-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="2fe40-159">NOTES</span></span>
<span data-ttu-id="2fe40-160">Sie können den Parameter *Confirm* verwenden, um zu steuern, ob dieses Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="2fe40-160">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="2fe40-161">Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn die $ConfirmPreference Windows PowerShell-Variable einen Wert von Mittel oder niedriger aufweist.</span><span class="sxs-lookup"><span data-stu-id="2fe40-161">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="2fe40-162">Wenn Sie *bestätigen* oder *bestätigen: $true* angeben, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fe40-162">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="2fe40-163">Wenn Sie *Confirm: $false* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="2fe40-163">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="2fe40-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2fe40-164">RELATED LINKS</span></span>

[<span data-ttu-id="2fe40-165">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="2fe40-165">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="2fe40-166">Neu – AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2fe40-166">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="2fe40-167">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="2fe40-167">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
