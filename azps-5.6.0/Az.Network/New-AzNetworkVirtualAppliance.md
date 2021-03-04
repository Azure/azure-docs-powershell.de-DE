---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 3f95ad6b11e8ddf7baaf5bcdf312ec172a9d397a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946976"
---
# <span data-ttu-id="01421-101">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="01421-101">New-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="01421-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01421-102">SYNOPSIS</span></span>
<span data-ttu-id="01421-103">Erstellen Sie eine Virtuelle Netzwerkgeräteressource.</span><span class="sxs-lookup"><span data-stu-id="01421-103">Create a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="01421-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01421-104">SYNTAX</span></span>

### <span data-ttu-id="01421-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="01421-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> -Location <String>
 -VirtualHubId <String> -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32>
 [-Identity <PSManagedServiceIdentity>] [-BootStrapConfigurationBlob <String[]>]
 [-CloudInitConfigurationBlob <String[]>] [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01421-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01421-106">ResourceIdParameterSet</span></span>
```
New-AzNetworkVirtualAppliance -ResourceId <String> -Location <String> -VirtualHubId <String>
 -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32> [-Identity <PSManagedServiceIdentity>]
 [-BootStrapConfigurationBlob <String[]>] [-CloudInitConfigurationBlob <String[]>]
 [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01421-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01421-107">DESCRIPTION</span></span>
<span data-ttu-id="01421-108">Mit New-AzNetworkVirtualAppliance Befehl wird eine Virtuelle Netzwerkgeräteressource in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="01421-108">The New-AzNetworkVirtualAppliance command creates a Network Virtual Appliance resource in Azure.</span></span>

## <span data-ttu-id="01421-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="01421-109">EXAMPLES</span></span>

### <span data-ttu-id="01421-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="01421-110">Example 1</span></span>
```powershell
PS C:\> $sku=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
PS C:\> $hub=Get-AzVirtualHub -ResourceGroupName testrg -Name hub
PS C:\> $nva=New-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -Location eastus2 -VirtualApplianceAsn 1270 -VirtualHubId $hub.Id -Sku $sku -CloudInitConfiguration "echo Hello World!"

```

<span data-ttu-id="01421-111">Erstellt eine neue virtuelle Netzwerkgerätressource in der Ressourcengruppe: testrg.</span><span class="sxs-lookup"><span data-stu-id="01421-111">Creates a new Network Virtual Appliance resource in resource group: testrg.</span></span>

## <span data-ttu-id="01421-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="01421-112">PARAMETERS</span></span>

### <span data-ttu-id="01421-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01421-113">-AsJob</span></span>
<span data-ttu-id="01421-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="01421-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01421-115">-BootStrapConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="01421-115">-BootStrapConfigurationBlob</span></span>
<span data-ttu-id="01421-116">Die BOOTSTRAP-Konfigurations-BLOB-URL.</span><span class="sxs-lookup"><span data-stu-id="01421-116">The Bootstrap configuration blob URL.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01421-117">-CloudInitConfiguration</span><span class="sxs-lookup"><span data-stu-id="01421-117">-CloudInitConfiguration</span></span>
<span data-ttu-id="01421-118">Die Cloudinit-Konfiguration als Nur-Text.</span><span class="sxs-lookup"><span data-stu-id="01421-118">The Cloudinit configuration as plain text.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01421-119">-CloudInitConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="01421-119">-CloudInitConfigurationBlob</span></span>
<span data-ttu-id="01421-120">Die Cloudinit-Konfigurations-Blobspeicher-URL.</span><span class="sxs-lookup"><span data-stu-id="01421-120">The Cloudinit configuration blob storage URL.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01421-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01421-121">-DefaultProfile</span></span>
<span data-ttu-id="01421-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01421-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01421-123">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="01421-123">-Force</span></span>
<span data-ttu-id="01421-124">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="01421-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="01421-125">-Identity</span><span class="sxs-lookup"><span data-stu-id="01421-125">-Identity</span></span>
<span data-ttu-id="01421-126">Die verwaltete Identität.</span><span class="sxs-lookup"><span data-stu-id="01421-126">The Managed identity.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01421-127">-Location</span><span class="sxs-lookup"><span data-stu-id="01421-127">-Location</span></span>
<span data-ttu-id="01421-128">Der Speicherort der öffentlichen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="01421-128">The public IP address location.</span></span>

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

### <span data-ttu-id="01421-129">-Name</span><span class="sxs-lookup"><span data-stu-id="01421-129">-Name</span></span>
<span data-ttu-id="01421-130">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="01421-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01421-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01421-131">-ResourceGroupName</span></span>
<span data-ttu-id="01421-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="01421-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01421-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01421-133">-ResourceId</span></span>
<span data-ttu-id="01421-134">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="01421-134">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01421-135">-Sku</span><span class="sxs-lookup"><span data-stu-id="01421-135">-Sku</span></span>
<span data-ttu-id="01421-136">Die Sku der virtuellen Appliance.</span><span class="sxs-lookup"><span data-stu-id="01421-136">The Sku of the Virtual Appliance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01421-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="01421-137">-Tag</span></span>
<span data-ttu-id="01421-138">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="01421-138">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01421-139">-VirtualApplianceAsn</span><span class="sxs-lookup"><span data-stu-id="01421-139">-VirtualApplianceAsn</span></span>
<span data-ttu-id="01421-140">Die ASN-Nummer der virtuellen Appliance.</span><span class="sxs-lookup"><span data-stu-id="01421-140">The ASN number of the Virtual Appliance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01421-141">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="01421-141">-VirtualHubId</span></span>
<span data-ttu-id="01421-142">Die Ressourcen-ID des virtuellen Hubs.</span><span class="sxs-lookup"><span data-stu-id="01421-142">The Resource Id of the Virtual Hub.</span></span>

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

### <span data-ttu-id="01421-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="01421-143">-Confirm</span></span>
<span data-ttu-id="01421-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="01421-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01421-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01421-145">-WhatIf</span></span>
<span data-ttu-id="01421-146">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01421-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01421-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01421-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01421-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01421-148">CommonParameters</span></span>
<span data-ttu-id="01421-149">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01421-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01421-150">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01421-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01421-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="01421-151">INPUTS</span></span>

### <span data-ttu-id="01421-152">System.String</span><span class="sxs-lookup"><span data-stu-id="01421-152">System.String</span></span>

### <span data-ttu-id="01421-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="01421-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

### <span data-ttu-id="01421-154">System.Int32</span><span class="sxs-lookup"><span data-stu-id="01421-154">System.Int32</span></span>

### <span data-ttu-id="01421-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="01421-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

### <span data-ttu-id="01421-156">System.String[]</span><span class="sxs-lookup"><span data-stu-id="01421-156">System.String[]</span></span>

### <span data-ttu-id="01421-157">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="01421-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="01421-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="01421-158">OUTPUTS</span></span>

### <span data-ttu-id="01421-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="01421-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="01421-160">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="01421-160">NOTES</span></span>

## <span data-ttu-id="01421-161">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="01421-161">RELATED LINKS</span></span>
