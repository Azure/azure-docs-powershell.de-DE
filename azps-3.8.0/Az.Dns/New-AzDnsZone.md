---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: dc110c8989951c6cf5a68e35fbc22c6545c84a1a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995654"
---
# <span data-ttu-id="3cd56-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="3cd56-101">New-AzDnsZone</span></span>

## <span data-ttu-id="3cd56-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3cd56-102">SYNOPSIS</span></span>
<span data-ttu-id="3cd56-103">Erstellt eine neue DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="3cd56-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="3cd56-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cd56-104">SYNTAX</span></span>

### <span data-ttu-id="3cd56-105">IDs (Standard)</span><span class="sxs-lookup"><span data-stu-id="3cd56-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cd56-106">Namen</span><span class="sxs-lookup"><span data-stu-id="3cd56-106">Names</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cd56-107">Objekte</span><span class="sxs-lookup"><span data-stu-id="3cd56-107">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cd56-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3cd56-108">DESCRIPTION</span></span>
<span data-ttu-id="3cd56-109">Das Cmdlet **New-AzDnsZone** erstellt eine neue DNS-Zone (Domain Name System) in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3cd56-109">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="3cd56-110">Sie müssen einen eindeutigen DNS-Zonennamen für den Parameter *Name* angeben, oder das Cmdlet gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="3cd56-110">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="3cd56-111">Verwenden Sie nach der Erstellung der Zone das New-AzDnsRecordSet-Cmdlet, um Daten Satz Sätze in der Zone zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3cd56-111">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="3cd56-112">Sie können den Parameter *Confirm* und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="3cd56-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="3cd56-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3cd56-113">EXAMPLES</span></span>

### <span data-ttu-id="3cd56-114">Beispiel 1: Erstellen einer DNS-Zone</span><span class="sxs-lookup"><span data-stu-id="3cd56-114">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="3cd56-115">Dieser Befehl erstellt eine neue DNS-Zone mit dem Namen MyZone.com in der angegebenen Ressourcengruppe und speichert Sie dann in der $Zone-Variablen.</span><span class="sxs-lookup"><span data-stu-id="3cd56-115">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="3cd56-116">Beispiel 2: Erstellen einer privaten DNS-Zone durch Angabe virtueller Netzwerk-IDs</span><span class="sxs-lookup"><span data-stu-id="3cd56-116">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="3cd56-117">Mit diesem Befehl wird eine neue private DNS-Zone mit dem Namen myprivatezone.com in der angegebenen Ressourcengruppe mit einem zugehörigen Auflösungs-virtuellen Netzwerk (Angabe der ID) erstellt und dann in der $Zone-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3cd56-117">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="3cd56-118">Beispiel 3: Erstellen einer privaten DNS-Zone durch angeben virtueller Netzwerkobjekte</span><span class="sxs-lookup"><span data-stu-id="3cd56-118">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="3cd56-119">Mit diesem Befehl wird eine neue private DNS-Zone mit dem Namen myprivatezone.com in der angegebenen Ressourcengruppe mit einem virtuellen Netzwerk für die Auflösung erstellt (auf das durch $ResVirtualNetwork Variable verwiesen wird) und dann in der $Zone-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3cd56-119">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="3cd56-120">Beispiel 4: Erstellen einer DNS-Zone mit Delegierung, indem Sie den Namen der übergeordneten Zone angeben</span><span class="sxs-lookup"><span data-stu-id="3cd56-120">Example 4: Create a DNS zone with delegation by specifying parent zone name</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

<span data-ttu-id="3cd56-121">Dieser Befehl erstellt eine neue untergeordnete DNS-Zone mit dem Namen myChild.Zone.com in der angegebenen Ressourcengruppe und speichert in der $Zone Variablen.</span><span class="sxs-lookup"><span data-stu-id="3cd56-121">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="3cd56-122">Außerdem wird die Delegierung in der übergeordneten DNS-Zone mit dem Namen Zone.com hinzugefügt, die sich in derselben Abonnement-und Ressourcengruppe wie untergeordnete Zone befindet.</span><span class="sxs-lookup"><span data-stu-id="3cd56-122">It also adds delegation in the parent DNS zone named zone.com residing in the same subscription and resource group as child zone.</span></span>

### <span data-ttu-id="3cd56-123">Beispiel 5: Erstellen einer DNS-Zone mit Delegierung durch Angeben der übergeordneten Zonen-ID</span><span class="sxs-lookup"><span data-stu-id="3cd56-123">Example 5: Create a DNS zone with delegation by specifying parent zone id</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

<span data-ttu-id="3cd56-124">Dieser Befehl erstellt eine neue untergeordnete DNS-Zone mit dem Namen myChild.Zone.com in der angegebenen Ressourcengruppe und speichert in der $Zone Variablen.</span><span class="sxs-lookup"><span data-stu-id="3cd56-124">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="3cd56-125">Darüber hinaus wird die Delegierung in der übergeordneten DNS-Zone mit dem Namen Zone.com in der Ressourcengruppe others-RG provided Subscription mit der der erstellten untergeordneten Zone hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3cd56-125">It also adds delegation in the parent DNS zone named zone.com in resource group other-rg provided subscription is same as that of child zone created.</span></span>

### <span data-ttu-id="3cd56-126">Beispiel 6: Erstellen einer DNS-Zone mit Delegierung durch Angeben eines übergeordneten Zonen Objekts</span><span class="sxs-lookup"><span data-stu-id="3cd56-126">Example 6: Create a DNS zone with delegation by specifying parent zone object</span></span>
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

<span data-ttu-id="3cd56-127">Dieser Befehl erstellt eine neue untergeordnete DNS-Zone mit dem Namen myChild.Zone.com in der angegebenen Ressourcengruppe und speichert in der $Zone Variablen.</span><span class="sxs-lookup"><span data-stu-id="3cd56-127">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="3cd56-128">Außerdem wird die Delegierung in der übergeordneten DNS-Zone mit dem Namen Zone.com hinzugefügt, wie im ParentZone-Objekt übergeben.</span><span class="sxs-lookup"><span data-stu-id="3cd56-128">It also adds delegation in the parent DNS zone named zone.com as passed in the ParentZone object</span></span>

## <span data-ttu-id="3cd56-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cd56-129">PARAMETERS</span></span>

### <span data-ttu-id="3cd56-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cd56-130">-DefaultProfile</span></span>
<span data-ttu-id="3cd56-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3cd56-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cd56-132">-Name</span><span class="sxs-lookup"><span data-stu-id="3cd56-132">-Name</span></span>
<span data-ttu-id="3cd56-133">Gibt den Namen der zu erstellende DNS-Zone an.</span><span class="sxs-lookup"><span data-stu-id="3cd56-133">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="3cd56-134">-ParentZone</span><span class="sxs-lookup"><span data-stu-id="3cd56-134">-ParentZone</span></span>
<span data-ttu-id="3cd56-135">Der vollständige Name der übergeordneten Zone, der Delegierung hinzugefügt werden soll (ohne Endpunkt).</span><span class="sxs-lookup"><span data-stu-id="3cd56-135">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="3cd56-136">-ParentZoneId</span><span class="sxs-lookup"><span data-stu-id="3cd56-136">-ParentZoneId</span></span>
<span data-ttu-id="3cd56-137">Die Ressourcen-ID der übergeordneten Zone, der eine Delegierung hinzugefügt werden soll (ohne Endpunkt).</span><span class="sxs-lookup"><span data-stu-id="3cd56-137">The resource id of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="3cd56-138">-ParentZoneName</span><span class="sxs-lookup"><span data-stu-id="3cd56-138">-ParentZoneName</span></span>
<span data-ttu-id="3cd56-139">Der vollständige Name der übergeordneten Zone, der Delegierung hinzugefügt werden soll (ohne Endpunkt).</span><span class="sxs-lookup"><span data-stu-id="3cd56-139">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="3cd56-140">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3cd56-140">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="3cd56-141">In der Liste der virtuellen Netzwerke, die die Hostnamen für virtuelle Maschinen registrieren, werden die Datensätze in dieser DNS-Zone nur für private Zonen zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="3cd56-141">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="3cd56-142">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="3cd56-142">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="3cd56-143">Die Liste der virtuellen Netzwerk-IDs, die Hostnamen für virtuelle Maschinen in dieser DNS-Zone registrieren, die nur für private Zonen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="3cd56-143">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="3cd56-144">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3cd56-144">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="3cd56-145">Die Liste der virtuellen Netzwerke, in denen Datensätze in dieser DNS-Zone aufgelöst werden können, die nur für private Zonen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="3cd56-145">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="3cd56-146">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="3cd56-146">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="3cd56-147">Die Liste der virtuellen Netzwerk-IDs, mit denen Datensätze in dieser DNS-Zone aufgelöst werden können, die nur für private Zonen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="3cd56-147">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="3cd56-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cd56-148">-ResourceGroupName</span></span>
<span data-ttu-id="3cd56-149">Gibt die Ressourcengruppe an, in der die Zone erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3cd56-149">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="3cd56-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="3cd56-150">-Tag</span></span>
<span data-ttu-id="3cd56-151">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="3cd56-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3cd56-152">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="3cd56-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3cd56-153">-Zonetype</span><span class="sxs-lookup"><span data-stu-id="3cd56-153">-ZoneType</span></span>
<span data-ttu-id="3cd56-154">Der Typ der Zone, öffentlich oder privat.</span><span class="sxs-lookup"><span data-stu-id="3cd56-154">The type of the zone, Public or Private.</span></span> <span data-ttu-id="3cd56-155">Zonen ohne Typ oder mit einem öffentlichen Typ werden auf der öffentlichen DNS-Dienstebene zur Verwendung in der DNS-Hierarchie zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="3cd56-155">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="3cd56-156">Zonen mit einem privaten Typ werden nur aus dem Satz der zugeordneten virtuellen Netzwerke angezeigt (dieses Feature befindet sich in der Vorschau).</span><span class="sxs-lookup"><span data-stu-id="3cd56-156">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="3cd56-157">Diese Eigenschaft kann für eine Zone nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3cd56-157">This property cannot be changed for a zone.</span></span>

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

### <span data-ttu-id="3cd56-158">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3cd56-158">-Confirm</span></span>
<span data-ttu-id="3cd56-159">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3cd56-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cd56-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cd56-160">-WhatIf</span></span>
<span data-ttu-id="3cd56-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3cd56-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cd56-162">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3cd56-162">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cd56-163">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3cd56-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cd56-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cd56-164">CommonParameters</span></span>
<span data-ttu-id="3cd56-165">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cd56-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cd56-166">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cd56-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cd56-167">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3cd56-167">INPUTS</span></span>

### <span data-ttu-id="3cd56-168">System. String</span><span class="sxs-lookup"><span data-stu-id="3cd56-168">System.String</span></span>

### <span data-ttu-id="3cd56-169">System. Nullable ' 1 [[Microsoft. Azure. Management. DNS. Models. zonetype, Microsoft. Azure. Management. DNS, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="3cd56-169">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="3cd56-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3cd56-170">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3cd56-171">System. Collections. Generic. List ' 1 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3cd56-171">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3cd56-172">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Management. Internal. Network. Common. IResourceReference, Microsoft. Azure. PowerShell. Clients. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="3cd56-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="3cd56-173">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3cd56-173">OUTPUTS</span></span>

### <span data-ttu-id="3cd56-174">Microsoft. Azure. Commands. DNS. dnsZone</span><span class="sxs-lookup"><span data-stu-id="3cd56-174">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="3cd56-175">Notizen</span><span class="sxs-lookup"><span data-stu-id="3cd56-175">NOTES</span></span>
<span data-ttu-id="3cd56-176">Sie können den Parameter *Confirm* verwenden, um zu steuern, ob dieses Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="3cd56-176">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="3cd56-177">Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn die $ConfirmPreference Windows PowerShell-Variable einen Wert von Mittel oder niedriger aufweist.</span><span class="sxs-lookup"><span data-stu-id="3cd56-177">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="3cd56-178">Wenn Sie *bestätigen* oder *bestätigen: $true* angeben, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3cd56-178">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="3cd56-179">Wenn Sie *Confirm: $false* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="3cd56-179">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="3cd56-180">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3cd56-180">RELATED LINKS</span></span>

[<span data-ttu-id="3cd56-181">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="3cd56-181">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="3cd56-182">Neu – AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3cd56-182">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="3cd56-183">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="3cd56-183">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
