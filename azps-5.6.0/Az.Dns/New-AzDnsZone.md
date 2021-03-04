---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: 40f1b40bbb5546e1d38b9c2916ea635aab80c144
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935040"
---
# <span data-ttu-id="f782c-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="f782c-101">New-AzDnsZone</span></span>

## <span data-ttu-id="f782c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f782c-102">SYNOPSIS</span></span>
<span data-ttu-id="f782c-103">Erstellt eine neue DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="f782c-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="f782c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f782c-104">SYNTAX</span></span>

### <span data-ttu-id="f782c-105">Ids (Standard)</span><span class="sxs-lookup"><span data-stu-id="f782c-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f782c-106">Namen</span><span class="sxs-lookup"><span data-stu-id="f782c-106">Names</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f782c-107">Objekte</span><span class="sxs-lookup"><span data-stu-id="f782c-107">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f782c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f782c-108">DESCRIPTION</span></span>
<span data-ttu-id="f782c-109">Das **Cmdlet New-AzDnsZone** erstellt eine neue Zone des Domain Name System (DNS) in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f782c-109">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="f782c-110">Sie müssen einen eindeutigen DNS-Zonennamen für den *Parameter Name* angeben, oder das Cmdlet gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="f782c-110">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="f782c-111">Nachdem die Zone erstellt wurde, verwenden Sie das cmdlet New-AzDnsRecordSet, um Datensatzsätze in der Zone zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f782c-111">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="f782c-112">Sie können den Parameter *Bestätigen* und die $ConfirmPreference Windows PowerShell verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="f782c-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="f782c-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f782c-113">EXAMPLES</span></span>

### <span data-ttu-id="f782c-114">Beispiel 1: Erstellen einer DNS-Zone</span><span class="sxs-lookup"><span data-stu-id="f782c-114">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="f782c-115">Mit diesem Befehl wird eine neue DNS-Zone myzone.com in der angegebenen Ressourcengruppe erstellt und dann in der $Zone gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f782c-115">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="f782c-116">Beispiel 2: Erstellen einer privaten DNS-Zone durch Angeben virtueller Netzwerk-IDs</span><span class="sxs-lookup"><span data-stu-id="f782c-116">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="f782c-117">Mit diesem Befehl wird eine neue private DNS-Zone mit dem Namen myprivatezone.com in der angegebenen Ressourcengruppe mit einem zugeordneten virtuellen Auflösungsnetzwerk erstellt (mit der zugehörigen ID) und dann in der $Zone gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f782c-117">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="f782c-118">Beispiel 3: Erstellen einer privaten DNS-Zone durch Angeben virtueller Netzwerkobjekte</span><span class="sxs-lookup"><span data-stu-id="f782c-118">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="f782c-119">Mit diesem Befehl wird eine neue private DNS-Zone mit dem Namen myprivatezone.com in der angegebenen Ressourcengruppe mit einem zugeordneten virtuellen Auflösungsnetzwerk (auf das von der $ResVirtualNetwork-Variable verwiesen wird) erstellt und dann in der variablen $Zone gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f782c-119">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="f782c-120">Beispiel 4: Erstellen einer DNS-Zone mit Delegierung durch Angeben des übergeordneten Zonennamens</span><span class="sxs-lookup"><span data-stu-id="f782c-120">Example 4: Create a DNS zone with delegation by specifying parent zone name</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

<span data-ttu-id="f782c-121">Mit diesem Befehl wird eine neue untergeordnete DNS-Zone mychild.zone.com in der angegebenen Ressourcengruppe erstellt und in der $Zone gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f782c-121">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="f782c-122">Außerdem wird die Delegierung in der übergeordneten DNS-Zone zone.com, die sich in derselben Abonnement- und Ressourcengruppe wie die untergeordnete Zone befindet.</span><span class="sxs-lookup"><span data-stu-id="f782c-122">It also adds delegation in the parent DNS zone named zone.com residing in the same subscription and resource group as child zone.</span></span>

### <span data-ttu-id="f782c-123">Beispiel 5: Erstellen einer DNS-Zone mit Delegierung durch Angeben der übergeordneten Zonen-ID</span><span class="sxs-lookup"><span data-stu-id="f782c-123">Example 5: Create a DNS zone with delegation by specifying parent zone id</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

<span data-ttu-id="f782c-124">Mit diesem Befehl wird eine neue untergeordnete DNS-Zone mychild.zone.com in der angegebenen Ressourcengruppe erstellt und in der $Zone gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f782c-124">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="f782c-125">Außerdem wird die Delegierung in der übergeordneten DNS-Zone mit dem Namen zone.com in der Ressourcengruppe andere rg hinzu, vorausgesetzt, das Abonnement ist identisch mit der der erstellten untergeordneten Zone.</span><span class="sxs-lookup"><span data-stu-id="f782c-125">It also adds delegation in the parent DNS zone named zone.com in resource group other-rg provided subscription is same as that of child zone created.</span></span>

### <span data-ttu-id="f782c-126">Beispiel 6: Erstellen einer DNS-Zone mit Delegierung durch Angeben des übergeordneten Zonenobjekts</span><span class="sxs-lookup"><span data-stu-id="f782c-126">Example 6: Create a DNS zone with delegation by specifying parent zone object</span></span>
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

<span data-ttu-id="f782c-127">Mit diesem Befehl wird eine neue untergeordnete DNS-Zone mychild.zone.com in der angegebenen Ressourcengruppe erstellt und in der $Zone gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f782c-127">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="f782c-128">Außerdem wird eine Delegierung in der übergeordneten DNS-Zone zone.com die im ParentZone-Objekt übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f782c-128">It also adds delegation in the parent DNS zone named zone.com as passed in the ParentZone object</span></span>

## <span data-ttu-id="f782c-129">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f782c-129">PARAMETERS</span></span>

### <span data-ttu-id="f782c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f782c-130">-DefaultProfile</span></span>
<span data-ttu-id="f782c-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f782c-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f782c-132">-Name</span><span class="sxs-lookup"><span data-stu-id="f782c-132">-Name</span></span>
<span data-ttu-id="f782c-133">Gibt den Namen der zu erstellenden DNS-Zone an.</span><span class="sxs-lookup"><span data-stu-id="f782c-133">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="f782c-134">-ParentZone</span><span class="sxs-lookup"><span data-stu-id="f782c-134">-ParentZone</span></span>
<span data-ttu-id="f782c-135">Der vollständige Name der übergeordneten Zone, die delegierung hinzugefügt werden soll (ohne einen endenden Punkt).</span><span class="sxs-lookup"><span data-stu-id="f782c-135">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="f782c-136">-ParentZoneId</span><span class="sxs-lookup"><span data-stu-id="f782c-136">-ParentZoneId</span></span>
<span data-ttu-id="f782c-137">Die Ressourcen-ID der übergeordneten Zone, die delegierung hinzugefügt werden soll (ohne einen endenden Punkt).</span><span class="sxs-lookup"><span data-stu-id="f782c-137">The resource id of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="f782c-138">-ParentZoneName</span><span class="sxs-lookup"><span data-stu-id="f782c-138">-ParentZoneName</span></span>
<span data-ttu-id="f782c-139">Der vollständige Name der übergeordneten Zone, die delegierung hinzugefügt werden soll (ohne einen endenden Punkt).</span><span class="sxs-lookup"><span data-stu-id="f782c-139">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="f782c-140">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f782c-140">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="f782c-141">Die Liste der virtuellen Netzwerke, in der Hostnamen für virtuelle Computer registriert werden, enthält Einträge in dieser DNS-Zone, die nur für private Zonen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f782c-141">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="f782c-142">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="f782c-142">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="f782c-143">Die Liste der virtuellen Netzwerk-IDs, die Hostnamen für virtuelle Computer in dieser DNS-Zone registrieren, ist nur für private Zonen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f782c-143">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="f782c-144">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f782c-144">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="f782c-145">Die Liste der virtuellen Netzwerke, die Datensätze in dieser DNS-Zone auflösen können, die nur für private Zonen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f782c-145">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="f782c-146">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="f782c-146">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="f782c-147">Die Liste der virtuellen Netzwerk-IDs, die Datensätze in dieser DNS-Zone auflösen können, die nur für private Zonen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f782c-147">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="f782c-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f782c-148">-ResourceGroupName</span></span>
<span data-ttu-id="f782c-149">Gibt die Ressourcengruppe an, in der die Zone erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f782c-149">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="f782c-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="f782c-150">-Tag</span></span>
<span data-ttu-id="f782c-151">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f782c-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f782c-152">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="f782c-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f782c-153">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="f782c-153">-ZoneType</span></span>
<span data-ttu-id="f782c-154">Der Typ der Zone( Öffentlich oder Privat).</span><span class="sxs-lookup"><span data-stu-id="f782c-154">The type of the zone, Public or Private.</span></span> <span data-ttu-id="f782c-155">Zonen ohne Typ oder mit einem öffentlichen Typ werden auf dem öffentlichen DNS-Dienstebenen zur Verwendung in der DNS-Hierarchie verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="f782c-155">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="f782c-156">Zonen mit einem Typ "Privat" sind nur mit der Gruppe der zugeordneten virtuellen Netzwerke sichtbar (dieses Feature befindet sich in der Vorschau).</span><span class="sxs-lookup"><span data-stu-id="f782c-156">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="f782c-157">Diese Eigenschaft kann für eine Zone nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f782c-157">This property cannot be changed for a zone.</span></span>

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

### <span data-ttu-id="f782c-158">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f782c-158">-Confirm</span></span>
<span data-ttu-id="f782c-159">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f782c-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f782c-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f782c-160">-WhatIf</span></span>
<span data-ttu-id="f782c-161">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f782c-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f782c-162">Das Cmdlet wird nicht ausgeführt. Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f782c-162">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f782c-163">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f782c-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f782c-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f782c-164">CommonParameters</span></span>
<span data-ttu-id="f782c-165">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f782c-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f782c-166">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f782c-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f782c-167">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f782c-167">INPUTS</span></span>

### <span data-ttu-id="f782c-168">System.String</span><span class="sxs-lookup"><span data-stu-id="f782c-168">System.String</span></span>

### <span data-ttu-id="f782c-169">System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f782c-169">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="f782c-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f782c-170">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f782c-171">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f782c-171">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f782c-172">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f782c-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="f782c-173">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f782c-173">OUTPUTS</span></span>

### <span data-ttu-id="f782c-174">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="f782c-174">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="f782c-175">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f782c-175">NOTES</span></span>
<span data-ttu-id="f782c-176">Sie können den Parameter *Bestätigen* verwenden, um zu steuern, ob Sie von diesem Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f782c-176">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="f782c-177">Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn die $ConfirmPreference Windows PowerShell den Wert Mittel oder niedriger hat.</span><span class="sxs-lookup"><span data-stu-id="f782c-177">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="f782c-178">Wenn Sie *Bestätigen* oder *Bestätigen:$True,* werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f782c-178">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="f782c-179">Wenn Sie *Confirm:$False* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="f782c-179">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f782c-180">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f782c-180">RELATED LINKS</span></span>

[<span data-ttu-id="f782c-181">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="f782c-181">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="f782c-182">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f782c-182">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="f782c-183">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="f782c-183">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
