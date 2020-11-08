---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/new-azsippool
schema: 2.0.0
ms.openlocfilehash: 2b04c5c1eb4d0a2b79543bf81bbfc02d1f0fb4ad
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007090"
---
# <span data-ttu-id="5f9e3-101">New-AzsIPPool</span><span class="sxs-lookup"><span data-stu-id="5f9e3-101">New-AzsIPPool</span></span>

## <span data-ttu-id="5f9e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f9e3-102">SYNOPSIS</span></span>
<span data-ttu-id="5f9e3-103">Erstellen eines IP-Pools</span><span class="sxs-lookup"><span data-stu-id="5f9e3-103">Create an IP pool.</span></span>
<span data-ttu-id="5f9e3-104">Nach dem Erstellen eines IP-Pools kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-104">Once created an IP pool cannot be deleted.</span></span>

## <span data-ttu-id="5f9e3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f9e3-105">SYNTAX</span></span>

### <span data-ttu-id="5f9e3-106">Createexpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="5f9e3-106">CreateExpanded (Default)</span></span>
```
New-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AddressPrefix <String>] [-EndIPAddress <String>]
 [-NumberOfAllocatedIPAddress <Int64>] [-NumberOfIPAddress <Int64>] [-NumberOfIPAddressesInTransition <Int64>]
 [-StartIPAddress <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5f9e3-107">Erstellen</span><span class="sxs-lookup"><span data-stu-id="5f9e3-107">Create</span></span>
```
New-AzsIPPool -Name <String> -Pool <IIPPool> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="5f9e3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f9e3-108">DESCRIPTION</span></span>
<span data-ttu-id="5f9e3-109">Erstellen eines IP-Pools</span><span class="sxs-lookup"><span data-stu-id="5f9e3-109">Create an IP pool.</span></span>
<span data-ttu-id="5f9e3-110">Nach dem Erstellen eines IP-Pools kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-110">Once created an IP pool cannot be deleted.</span></span>

## <span data-ttu-id="5f9e3-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f9e3-111">EXAMPLES</span></span>

### <span data-ttu-id="5f9e3-112">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="5f9e3-112">Example 1:</span></span>
```powershell
PS C:\> New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24

```

<span data-ttu-id="5f9e3-113">Erstellen Sie einen neuen IP-Pool.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-113">Create a new IP pool.</span></span>



## <span data-ttu-id="5f9e3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f9e3-114">PARAMETERS</span></span>

### <span data-ttu-id="5f9e3-115">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5f9e3-115">-AddressPrefix</span></span>
<span data-ttu-id="5f9e3-116">Das Adresspräfix.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-116">The address prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f9e3-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f9e3-117">-AsJob</span></span>
<span data-ttu-id="5f9e3-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="5f9e3-118">Run the command as a job</span></span>

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

### <span data-ttu-id="5f9e3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f9e3-119">-DefaultProfile</span></span>
<span data-ttu-id="5f9e3-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f9e3-121">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="5f9e3-121">-EndIPAddress</span></span>
<span data-ttu-id="5f9e3-122">Die letzte IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-122">The ending IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f9e3-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="5f9e3-123">-Location</span></span>
<span data-ttu-id="5f9e3-124">Der Bereich, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-124">The region where the resource is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f9e3-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5f9e3-125">-Name</span></span>
<span data-ttu-id="5f9e3-126">Name des IP-Pools.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-126">IP pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f9e3-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="5f9e3-127">-NoWait</span></span>
<span data-ttu-id="5f9e3-128">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="5f9e3-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5f9e3-129">-NumberOfAllocatedIPAddress</span><span class="sxs-lookup"><span data-stu-id="5f9e3-129">-NumberOfAllocatedIPAddress</span></span>
<span data-ttu-id="5f9e3-130">Die Anzahl der aktuell zugeordneten IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-130">The number of currently allocated IP addresses.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f9e3-131">-NumberOfIPAddress</span><span class="sxs-lookup"><span data-stu-id="5f9e3-131">-NumberOfIPAddress</span></span>
<span data-ttu-id="5f9e3-132">Die Gesamtzahl der IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-132">The total number of IP addresses.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f9e3-133">-NumberOfIPAddressesInTransition</span><span class="sxs-lookup"><span data-stu-id="5f9e3-133">-NumberOfIPAddressesInTransition</span></span>
<span data-ttu-id="5f9e3-134">Die aktuelle Anzahl von IP-Adressen im Übergang.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-134">The current number of IP addresses in transition.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f9e3-135">-Pool</span><span class="sxs-lookup"><span data-stu-id="5f9e3-135">-Pool</span></span>
<span data-ttu-id="5f9e3-136">Diese Ressource definiert den Bereich von IP-Adressen, aus denen Adressen für Knoten innerhalb eines Subnetzes zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-136">This resource defines the range of IP addresses from which addresses are allocated for nodes within a subnet.</span></span>
<span data-ttu-id="5f9e3-137">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Pool Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-137">To construct, see NOTES section for POOL properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5f9e3-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f9e3-138">-ResourceGroupName</span></span>
<span data-ttu-id="5f9e3-139">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-139">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f9e3-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="5f9e3-140">-StartIPAddress</span></span>
<span data-ttu-id="5f9e3-141">Die Start-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-141">The starting IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f9e3-142">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="5f9e3-142">-SubscriptionId</span></span>
<span data-ttu-id="5f9e3-143">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-143">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5f9e3-144">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f9e3-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="5f9e3-145">-Tag</span></span>
<span data-ttu-id="5f9e3-146">Liste der Schlüssel-Wert-Paare</span><span class="sxs-lookup"><span data-stu-id="5f9e3-146">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f9e3-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5f9e3-147">-Confirm</span></span>
<span data-ttu-id="5f9e3-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f9e3-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f9e3-149">-WhatIf</span></span>
<span data-ttu-id="5f9e3-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f9e3-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5f9e3-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f9e3-152">CommonParameters</span></span>
<span data-ttu-id="5f9e3-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f9e3-154">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f9e3-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f9e3-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f9e3-155">INPUTS</span></span>

### <span data-ttu-id="5f9e3-156">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="5f9e3-156">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>

## <span data-ttu-id="5f9e3-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f9e3-157">OUTPUTS</span></span>

### <span data-ttu-id="5f9e3-158">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="5f9e3-158">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>



## <span data-ttu-id="5f9e3-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f9e3-159">NOTES</span></span>

<span data-ttu-id="5f9e3-160">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-160">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5f9e3-161">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5f9e3-162">Pool <IIPPool> : diese Ressource definiert den Bereich von IP-Adressen, aus denen Adressen für Knoten in einem Subnetz zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-162">POOL <IIPPool>: This resource defines the range of IP addresses from which addresses are allocated for nodes within a subnet.</span></span>
  - <span data-ttu-id="5f9e3-163">`[Location <String>]`: Der Bereich, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-163">`[Location <String>]`: The region where the resource is located.</span></span>
  - <span data-ttu-id="5f9e3-164">`[Tag <IResourceTags>]`: Liste von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-164">`[Tag <IResourceTags>]`: List of key-value pairs.</span></span>
    - <span data-ttu-id="5f9e3-165">`[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-165">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="5f9e3-166">`[AddressPrefix <String>]`: Das Adresspräfix.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-166">`[AddressPrefix <String>]`: The address prefix.</span></span>
  - <span data-ttu-id="5f9e3-167">`[EndIPAddress <String>]`: Die letzte IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-167">`[EndIPAddress <String>]`: The ending IP address.</span></span>
  - <span data-ttu-id="5f9e3-168">`[NumberOfAllocatedIPAddresses <Int64?>]`: Die Anzahl der derzeit zugeordneten IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-168">`[NumberOfAllocatedIPAddresses <Int64?>]`: The number of currently allocated IP addresses.</span></span>
  - <span data-ttu-id="5f9e3-169">`[NumberOfIPAddresses <Int64?>]`: Die Gesamtzahl der IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-169">`[NumberOfIPAddresses <Int64?>]`: The total number of IP addresses.</span></span>
  - <span data-ttu-id="5f9e3-170">`[NumberOfIPAddressesInTransition <Int64?>]`: Die aktuelle Anzahl von IP-Adressen im Übergang.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-170">`[NumberOfIPAddressesInTransition <Int64?>]`: The current number of IP addresses in transition.</span></span>
  - <span data-ttu-id="5f9e3-171">`[StartIPAddress <String>]`: Die Start-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="5f9e3-171">`[StartIPAddress <String>]`: The starting IP address.</span></span>

## <span data-ttu-id="5f9e3-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f9e3-172">RELATED LINKS</span></span>

