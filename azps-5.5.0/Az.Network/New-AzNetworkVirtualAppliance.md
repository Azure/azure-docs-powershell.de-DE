---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 9b3991a24430afa74853f742bffa12b772dbeaf2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169823"
---
# <span data-ttu-id="ceb51-101">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="ceb51-101">New-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="ceb51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceb51-102">SYNOPSIS</span></span>
<span data-ttu-id="ceb51-103">Erstellen Sie eine Network Virtual Appliance-Ressource.</span><span class="sxs-lookup"><span data-stu-id="ceb51-103">Create a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="ceb51-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ceb51-104">SYNTAX</span></span>

### <span data-ttu-id="ceb51-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ceb51-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> -Location <String>
 -VirtualHubId <String> -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32>
 [-Identity <PSManagedServiceIdentity>] [-BootStrapConfigurationBlob <String[]>]
 [-CloudInitConfigurationBlob <String[]>] [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ceb51-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ceb51-106">ResourceIdParameterSet</span></span>
```
New-AzNetworkVirtualAppliance -ResourceId <String> -Location <String> -VirtualHubId <String>
 -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32> [-Identity <PSManagedServiceIdentity>]
 [-BootStrapConfigurationBlob <String[]>] [-CloudInitConfigurationBlob <String[]>]
 [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceb51-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ceb51-107">DESCRIPTION</span></span>
<span data-ttu-id="ceb51-108">Mit New-AzNetworkVirtualAppliance Befehl wird eine Ressource für virtuelle Network Appliance in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="ceb51-108">The New-AzNetworkVirtualAppliance command creates a Network Virtual Appliance resource in Azure.</span></span>

## <span data-ttu-id="ceb51-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ceb51-109">EXAMPLES</span></span>

### <span data-ttu-id="ceb51-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ceb51-110">Example 1</span></span>
```powershell
PS C:\> $sku=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
PS C:\> $hub=Get-AzVirtualHub -ResourceGroupName testrg -Name hub
PS C:\> $nva=New-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -Location eastus2 -VirtualApplianceAsn 1270 -VirtualHubId $hub.Id -Sku $sku -CloudInitConfiguration "echo Hello World!"

```

<span data-ttu-id="ceb51-111">Erstellt eine neue Virtuelle Netzwerkgeräteressource in der Ressourcengruppe: testrg.</span><span class="sxs-lookup"><span data-stu-id="ceb51-111">Creates a new Network Virtual Appliance resource in resource group: testrg.</span></span>

## <span data-ttu-id="ceb51-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ceb51-112">PARAMETERS</span></span>

### <span data-ttu-id="ceb51-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ceb51-113">-AsJob</span></span>
<span data-ttu-id="ceb51-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ceb51-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ceb51-115">-BootStrapConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="ceb51-115">-BootStrapConfigurationBlob</span></span>
<span data-ttu-id="ceb51-116">Die BOOTSTRAP-Konfigurations-BLOB-URL.</span><span class="sxs-lookup"><span data-stu-id="ceb51-116">The Bootstrap configuration blob URL.</span></span>

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

### <span data-ttu-id="ceb51-117">-CloudInitConfiguration</span><span class="sxs-lookup"><span data-stu-id="ceb51-117">-CloudInitConfiguration</span></span>
<span data-ttu-id="ceb51-118">Die Cloudinit-Konfiguration als unformatierungsbasierter Text.</span><span class="sxs-lookup"><span data-stu-id="ceb51-118">The Cloudinit configuration as plain text.</span></span>

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

### <span data-ttu-id="ceb51-119">-CloudInitConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="ceb51-119">-CloudInitConfigurationBlob</span></span>
<span data-ttu-id="ceb51-120">Die URL für die Cloudinit-Konfiguration des BLOB-Speichers.</span><span class="sxs-lookup"><span data-stu-id="ceb51-120">The Cloudinit configuration blob storage URL.</span></span>

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

### <span data-ttu-id="ceb51-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceb51-121">-DefaultProfile</span></span>
<span data-ttu-id="ceb51-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ceb51-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ceb51-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ceb51-123">-Force</span></span>
<span data-ttu-id="ceb51-124">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="ceb51-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ceb51-125">-Identity</span><span class="sxs-lookup"><span data-stu-id="ceb51-125">-Identity</span></span>
<span data-ttu-id="ceb51-126">Die verwaltete Identität.</span><span class="sxs-lookup"><span data-stu-id="ceb51-126">The Managed identity.</span></span>

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

### <span data-ttu-id="ceb51-127">-Location</span><span class="sxs-lookup"><span data-stu-id="ceb51-127">-Location</span></span>
<span data-ttu-id="ceb51-128">Der Speicherort der öffentlichen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="ceb51-128">The public IP address location.</span></span>

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

### <span data-ttu-id="ceb51-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ceb51-129">-Name</span></span>
<span data-ttu-id="ceb51-130">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="ceb51-130">The resource name.</span></span>

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

### <span data-ttu-id="ceb51-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceb51-131">-ResourceGroupName</span></span>
<span data-ttu-id="ceb51-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ceb51-132">The resource group name.</span></span>

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

### <span data-ttu-id="ceb51-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ceb51-133">-ResourceId</span></span>
<span data-ttu-id="ceb51-134">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ceb51-134">The resource Id.</span></span>

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

### <span data-ttu-id="ceb51-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="ceb51-135">-Sku</span></span>
<span data-ttu-id="ceb51-136">Die SKU des virtuellen Geräts.</span><span class="sxs-lookup"><span data-stu-id="ceb51-136">The Sku of the Virtual Appliance.</span></span>

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

### <span data-ttu-id="ceb51-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="ceb51-137">-Tag</span></span>
<span data-ttu-id="ceb51-138">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="ceb51-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ceb51-139">-VirtualApplianceAsn</span><span class="sxs-lookup"><span data-stu-id="ceb51-139">-VirtualApplianceAsn</span></span>
<span data-ttu-id="ceb51-140">Die ASN-Nummer des virtuellen Geräts.</span><span class="sxs-lookup"><span data-stu-id="ceb51-140">The ASN number of the Virtual Appliance.</span></span>

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

### <span data-ttu-id="ceb51-141">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="ceb51-141">-VirtualHubId</span></span>
<span data-ttu-id="ceb51-142">Die Ressourcen-ID des virtuellen Hubs.</span><span class="sxs-lookup"><span data-stu-id="ceb51-142">The Resource Id of the Virtual Hub.</span></span>

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

### <span data-ttu-id="ceb51-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ceb51-143">-Confirm</span></span>
<span data-ttu-id="ceb51-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ceb51-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceb51-145">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ceb51-145">-WhatIf</span></span>
<span data-ttu-id="ceb51-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ceb51-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ceb51-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ceb51-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ceb51-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceb51-148">CommonParameters</span></span>
<span data-ttu-id="ceb51-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceb51-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceb51-150">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ceb51-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceb51-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ceb51-151">INPUTS</span></span>

### <span data-ttu-id="ceb51-152">System.String</span><span class="sxs-lookup"><span data-stu-id="ceb51-152">System.String</span></span>

### <span data-ttu-id="ceb51-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="ceb51-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

### <span data-ttu-id="ceb51-154">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ceb51-154">System.Int32</span></span>

### <span data-ttu-id="ceb51-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="ceb51-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

### <span data-ttu-id="ceb51-156">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ceb51-156">System.String[]</span></span>

### <span data-ttu-id="ceb51-157">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ceb51-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ceb51-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ceb51-158">OUTPUTS</span></span>

### <span data-ttu-id="ceb51-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="ceb51-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="ceb51-160">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ceb51-160">NOTES</span></span>

## <span data-ttu-id="ceb51-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ceb51-161">RELATED LINKS</span></span>
