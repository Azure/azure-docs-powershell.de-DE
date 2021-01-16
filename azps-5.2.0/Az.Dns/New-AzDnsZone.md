---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: dc110c8989951c6cf5a68e35fbc22c6545c84a1a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302371"
---
# <span data-ttu-id="0e25d-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="0e25d-101">New-AzDnsZone</span></span>

## <span data-ttu-id="0e25d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e25d-102">SYNOPSIS</span></span>
<span data-ttu-id="0e25d-103">Erstellt eine neue DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="0e25d-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="0e25d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e25d-104">SYNTAX</span></span>

### <span data-ttu-id="0e25d-105">Ids (Standard)</span><span class="sxs-lookup"><span data-stu-id="0e25d-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e25d-106">Namen</span><span class="sxs-lookup"><span data-stu-id="0e25d-106">Names</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e25d-107">Objekte</span><span class="sxs-lookup"><span data-stu-id="0e25d-107">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e25d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e25d-108">DESCRIPTION</span></span>
<span data-ttu-id="0e25d-109">Das **Cmdlet "New-AzDnsZone"** erstellt eine neue Domain Name System (DNS)-Zone in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0e25d-109">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="0e25d-110">Sie müssen einen eindeutigen Namen für die DNS-Zone für den *Parameter "Name"* angeben, da das Cmdlet einen Fehler zurück gibt.</span><span class="sxs-lookup"><span data-stu-id="0e25d-110">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="0e25d-111">Nachdem die Zone erstellt wurde, verwenden Sie das New-AzDnsRecordSet-Cmdlet, um Datensatzsätze in der Zone zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0e25d-111">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="0e25d-112">Sie können den Parameter *"Bestätigen"* und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="0e25d-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="0e25d-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0e25d-113">EXAMPLES</span></span>

### <span data-ttu-id="0e25d-114">Beispiel 1: Erstellen einer DNS-Zone</span><span class="sxs-lookup"><span data-stu-id="0e25d-114">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="0e25d-115">Dieser Befehl erstellt eine neue DNS-Zone namens myzone.com in der angegebenen Ressourcengruppe und speichert sie dann in $Zone Variable.</span><span class="sxs-lookup"><span data-stu-id="0e25d-115">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="0e25d-116">Beispiel 2: Erstellen einer privaten DNS-Zone durch Angeben virtueller Netzwerk-IDs</span><span class="sxs-lookup"><span data-stu-id="0e25d-116">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="0e25d-117">Mit diesem Befehl wird eine neue private DNS-Zone namens myprivatezone.com in der angegebenen Ressourcengruppe mit einem zugeordneten virtuellen Auflösungsnetzwerk erstellt (die ID wird angegeben) und dann in der variablen $Zone gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0e25d-117">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="0e25d-118">Beispiel 3: Erstellen einer privaten DNS-Zone durch Angeben virtueller Netzwerkobjekte</span><span class="sxs-lookup"><span data-stu-id="0e25d-118">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="0e25d-119">Dieser Befehl erstellt eine neue private DNS-Zone namens myprivatezone.com in der angegebenen Ressourcengruppe mit einem zugeordneten virtuellen Auflösungsnetzwerk (bezeichnet von $ResVirtualNetwork-Variable) und speichert es dann in der $Zone-Variable.</span><span class="sxs-lookup"><span data-stu-id="0e25d-119">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="0e25d-120">Beispiel 4: Erstellen einer DNS-Zone mit Delegierung durch Angabe des übergeordneten Zonennamens</span><span class="sxs-lookup"><span data-stu-id="0e25d-120">Example 4: Create a DNS zone with delegation by specifying parent zone name</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

<span data-ttu-id="0e25d-121">Mit diesem Befehl wird eine neue untergeordnete DNS-Zone namens mychild.zone.com in der angegebenen Ressourcengruppe erstellt und in der $Zone gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0e25d-121">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="0e25d-122">Außerdem wird delegierung in der übergeordneten DNS-Zone zone.com, die sich in derselben Abonnement- und Ressourcengruppe wie die untergeordnete Zone befinden.</span><span class="sxs-lookup"><span data-stu-id="0e25d-122">It also adds delegation in the parent DNS zone named zone.com residing in the same subscription and resource group as child zone.</span></span>

### <span data-ttu-id="0e25d-123">Beispiel 5: Erstellen einer DNS-Zone mit Delegierung durch Angabe der übergeordneten Zonen-ID</span><span class="sxs-lookup"><span data-stu-id="0e25d-123">Example 5: Create a DNS zone with delegation by specifying parent zone id</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

<span data-ttu-id="0e25d-124">Dieser Befehl erstellt eine neue untergeordnete DNS-Zone namens mychild.zone.com in der angegebenen Ressourcengruppe und speichert in der $Zone Variable.</span><span class="sxs-lookup"><span data-stu-id="0e25d-124">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="0e25d-125">Außerdem wird delegierung in der übergeordneten DNS-Zone mit dem Namen "zone.com in der Ressourcengruppe "andere-rg" bereitgestellte Abonnements mit der der erstellten untergeordneten Zone ergänzt.</span><span class="sxs-lookup"><span data-stu-id="0e25d-125">It also adds delegation in the parent DNS zone named zone.com in resource group other-rg provided subscription is same as that of child zone created.</span></span>

### <span data-ttu-id="0e25d-126">Beispiel 6: Erstellen einer DNS-Zone mit Delegierung durch Angeben des übergeordneten Zonenobjekts</span><span class="sxs-lookup"><span data-stu-id="0e25d-126">Example 6: Create a DNS zone with delegation by specifying parent zone object</span></span>
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

<span data-ttu-id="0e25d-127">Mit diesem Befehl wird eine neue untergeordnete DNS-Zone namens mychild.zone.com in der angegebenen Ressourcengruppe erstellt und in der $Zone gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0e25d-127">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="0e25d-128">Außerdem wird delegierung in der übergeordneten DNS-Zone namens zone.com, die im ParentZone-Objekt übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="0e25d-128">It also adds delegation in the parent DNS zone named zone.com as passed in the ParentZone object</span></span>

## <span data-ttu-id="0e25d-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e25d-129">PARAMETERS</span></span>

### <span data-ttu-id="0e25d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e25d-130">-DefaultProfile</span></span>
<span data-ttu-id="0e25d-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0e25d-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e25d-132">-Name</span><span class="sxs-lookup"><span data-stu-id="0e25d-132">-Name</span></span>
<span data-ttu-id="0e25d-133">Gibt den Namen der zu erstellenden DNS-Zone an.</span><span class="sxs-lookup"><span data-stu-id="0e25d-133">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="0e25d-134">-ParentZone</span><span class="sxs-lookup"><span data-stu-id="0e25d-134">-ParentZone</span></span>
<span data-ttu-id="0e25d-135">Der vollständige Name der übergeordneten Zone, der delegierung hinzugefügt werden soll (ohne Endpunkt).</span><span class="sxs-lookup"><span data-stu-id="0e25d-135">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e25d-136">-ParentZoneId</span><span class="sxs-lookup"><span data-stu-id="0e25d-136">-ParentZoneId</span></span>
<span data-ttu-id="0e25d-137">Die Ressourcen-ID der übergeordneten Zone, der Delegierung hinzugefügt werden soll (ohne Endpunkt).</span><span class="sxs-lookup"><span data-stu-id="0e25d-137">The resource id of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e25d-138">-ParentZoneName</span><span class="sxs-lookup"><span data-stu-id="0e25d-138">-ParentZoneName</span></span>
<span data-ttu-id="0e25d-139">Der vollständige Name der übergeordneten Zone, der delegierung hinzugefügt werden soll (ohne Endpunkt).</span><span class="sxs-lookup"><span data-stu-id="0e25d-139">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Names
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e25d-140">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0e25d-140">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="0e25d-141">Die Liste der virtuellen Netzwerke, die Hostnameneinträge für virtuelle Computer in dieser DNS-Zone registrieren, nur für private Zonen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0e25d-141">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="0e25d-142">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="0e25d-142">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="0e25d-143">Die Liste der virtuellen Netzwerk-IDs, die Hostnameneinträge für virtuelle Computer in dieser DNS-Zone registrieren, nur für private Zonen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0e25d-143">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="0e25d-144">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0e25d-144">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="0e25d-145">Die Liste der virtuellen Netzwerke, die Einträge in dieser DNS-Zone auflösen können, nur für private Zonen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0e25d-145">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="0e25d-146">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="0e25d-146">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="0e25d-147">Die Liste der virtuellen Netzwerk-IDs, die Einträge in dieser DNS-Zone auflösen können, nur für private Zonen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0e25d-147">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="0e25d-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e25d-148">-ResourceGroupName</span></span>
<span data-ttu-id="0e25d-149">Gibt die Ressourcengruppe an, in der die Zone erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0e25d-149">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="0e25d-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="0e25d-150">-Tag</span></span>
<span data-ttu-id="0e25d-151">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="0e25d-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0e25d-152">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="0e25d-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0e25d-153">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="0e25d-153">-ZoneType</span></span>
<span data-ttu-id="0e25d-154">Der Typ der Zone, "Öffentlich" oder "Privat".</span><span class="sxs-lookup"><span data-stu-id="0e25d-154">The type of the zone, Public or Private.</span></span> <span data-ttu-id="0e25d-155">Zonen ohne Typ oder mit einem öffentlichen Typ werden auf dem öffentlichen DNS-Dienstebene zur Verwendung in der DNS-Hierarchie verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="0e25d-155">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="0e25d-156">Zonen mit dem Typ "Privat" sind nur über die Gruppe der zugeordneten virtuellen Netzwerke sichtbar (dieses Feature befindet sich in der Vorschau).</span><span class="sxs-lookup"><span data-stu-id="0e25d-156">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="0e25d-157">Diese Eigenschaft kann für eine Zone nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="0e25d-157">This property cannot be changed for a zone.</span></span>

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

### <span data-ttu-id="0e25d-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e25d-158">-Confirm</span></span>
<span data-ttu-id="0e25d-159">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0e25d-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e25d-160">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0e25d-160">-WhatIf</span></span>
<span data-ttu-id="0e25d-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0e25d-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e25d-162">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0e25d-162">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e25d-163">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e25d-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e25d-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e25d-164">CommonParameters</span></span>
<span data-ttu-id="0e25d-165">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e25d-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e25d-166">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e25d-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e25d-167">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0e25d-167">INPUTS</span></span>

### <span data-ttu-id="0e25d-168">System.String</span><span class="sxs-lookup"><span data-stu-id="0e25d-168">System.String</span></span>

### <span data-ttu-id="0e25d-169">System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0e25d-169">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="0e25d-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0e25d-170">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0e25d-171">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0e25d-171">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0e25d-172">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0e25d-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="0e25d-173">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0e25d-173">OUTPUTS</span></span>

### <span data-ttu-id="0e25d-174">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="0e25d-174">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="0e25d-175">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0e25d-175">NOTES</span></span>
<span data-ttu-id="0e25d-176">Mit dem Parameter *"Bestätigen"* können Sie steuern, ob Sie von diesem Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="0e25d-176">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="0e25d-177">Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn $ConfirmPreference Windows PowerShell Variable den Wert "Mittel" oder "Niedriger" hat.</span><span class="sxs-lookup"><span data-stu-id="0e25d-177">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="0e25d-178">Wenn Sie *"Bestätigen"* oder *"Bestätigen:$True" angeben,* fordert Sie dieses Cmdlet zur Bestätigung auf, bevor es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0e25d-178">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="0e25d-179">Wenn Sie *"Confirm:$False" angeben,* werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="0e25d-179">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="0e25d-180">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0e25d-180">RELATED LINKS</span></span>

[<span data-ttu-id="0e25d-181">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="0e25d-181">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="0e25d-182">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0e25d-182">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="0e25d-183">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="0e25d-183">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
