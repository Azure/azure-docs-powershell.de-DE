---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 9b3991a24430afa74853f742bffa12b772dbeaf2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175030"
---
# <span data-ttu-id="42c66-101">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="42c66-101">New-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="42c66-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42c66-102">SYNOPSIS</span></span>
<span data-ttu-id="42c66-103">Erstellen Sie eine virtuelle Netzwerk-Appliance-Ressource.</span><span class="sxs-lookup"><span data-stu-id="42c66-103">Create a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="42c66-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42c66-104">SYNTAX</span></span>

### <span data-ttu-id="42c66-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="42c66-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> -Location <String>
 -VirtualHubId <String> -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32>
 [-Identity <PSManagedServiceIdentity>] [-BootStrapConfigurationBlob <String[]>]
 [-CloudInitConfigurationBlob <String[]>] [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42c66-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42c66-106">ResourceIdParameterSet</span></span>
```
New-AzNetworkVirtualAppliance -ResourceId <String> -Location <String> -VirtualHubId <String>
 -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32> [-Identity <PSManagedServiceIdentity>]
 [-BootStrapConfigurationBlob <String[]>] [-CloudInitConfigurationBlob <String[]>]
 [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42c66-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42c66-107">DESCRIPTION</span></span>
<span data-ttu-id="42c66-108">Mit dem Befehl New-AzNetworkVirtualAppliance wird eine virtuelle Netzwerk-Appliance-Ressource in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="42c66-108">The New-AzNetworkVirtualAppliance command creates a Network Virtual Appliance resource in Azure.</span></span>

## <span data-ttu-id="42c66-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42c66-109">EXAMPLES</span></span>

### <span data-ttu-id="42c66-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="42c66-110">Example 1</span></span>
```powershell
PS C:\> $sku=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
PS C:\> $hub=Get-AzVirtualHub -ResourceGroupName testrg -Name hub
PS C:\> $nva=New-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -Location eastus2 -VirtualApplianceAsn 1270 -VirtualHubId $hub.Id -Sku $sku -CloudInitConfiguration "echo Hello World!"

```

<span data-ttu-id="42c66-111">Erstellt eine neue virtuelle Netzwerk-Appliance-Ressource in der Ressourcengruppe: testrg.</span><span class="sxs-lookup"><span data-stu-id="42c66-111">Creates a new Network Virtual Appliance resource in resource group: testrg.</span></span>

## <span data-ttu-id="42c66-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="42c66-112">PARAMETERS</span></span>

### <span data-ttu-id="42c66-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42c66-113">-AsJob</span></span>
<span data-ttu-id="42c66-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="42c66-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42c66-115">-BootStrapConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="42c66-115">-BootStrapConfigurationBlob</span></span>
<span data-ttu-id="42c66-116">Die BLOB-URL für die Bootstrap-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="42c66-116">The Bootstrap configuration blob URL.</span></span>

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

### <span data-ttu-id="42c66-117">-CloudInitConfiguration</span><span class="sxs-lookup"><span data-stu-id="42c66-117">-CloudInitConfiguration</span></span>
<span data-ttu-id="42c66-118">Die Cloudinit-Konfiguration als nur-Text.</span><span class="sxs-lookup"><span data-stu-id="42c66-118">The Cloudinit configuration as plain text.</span></span>

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

### <span data-ttu-id="42c66-119">-CloudInitConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="42c66-119">-CloudInitConfigurationBlob</span></span>
<span data-ttu-id="42c66-120">Die Cloudinit-Konfigurations-BLOB-Speicher-URL.</span><span class="sxs-lookup"><span data-stu-id="42c66-120">The Cloudinit configuration blob storage URL.</span></span>

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

### <span data-ttu-id="42c66-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42c66-121">-DefaultProfile</span></span>
<span data-ttu-id="42c66-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42c66-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42c66-123">-Force</span><span class="sxs-lookup"><span data-stu-id="42c66-123">-Force</span></span>
<span data-ttu-id="42c66-124">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="42c66-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="42c66-125">-Identity</span><span class="sxs-lookup"><span data-stu-id="42c66-125">-Identity</span></span>
<span data-ttu-id="42c66-126">Die verwaltete Identität.</span><span class="sxs-lookup"><span data-stu-id="42c66-126">The Managed identity.</span></span>

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

### <span data-ttu-id="42c66-127">-Standort</span><span class="sxs-lookup"><span data-stu-id="42c66-127">-Location</span></span>
<span data-ttu-id="42c66-128">Der Speicherort der öffentlichen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="42c66-128">The public IP address location.</span></span>

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

### <span data-ttu-id="42c66-129">-Name</span><span class="sxs-lookup"><span data-stu-id="42c66-129">-Name</span></span>
<span data-ttu-id="42c66-130">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="42c66-130">The resource name.</span></span>

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

### <span data-ttu-id="42c66-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42c66-131">-ResourceGroupName</span></span>
<span data-ttu-id="42c66-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="42c66-132">The resource group name.</span></span>

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

### <span data-ttu-id="42c66-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="42c66-133">-ResourceId</span></span>
<span data-ttu-id="42c66-134">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="42c66-134">The resource Id.</span></span>

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

### <span data-ttu-id="42c66-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="42c66-135">-Sku</span></span>
<span data-ttu-id="42c66-136">Die SKU der virtuellen Appliance.</span><span class="sxs-lookup"><span data-stu-id="42c66-136">The Sku of the Virtual Appliance.</span></span>

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

### <span data-ttu-id="42c66-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="42c66-137">-Tag</span></span>
<span data-ttu-id="42c66-138">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="42c66-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="42c66-139">-VirtualApplianceAsn</span><span class="sxs-lookup"><span data-stu-id="42c66-139">-VirtualApplianceAsn</span></span>
<span data-ttu-id="42c66-140">Die ASN-Nummer der virtuellen Appliance.</span><span class="sxs-lookup"><span data-stu-id="42c66-140">The ASN number of the Virtual Appliance.</span></span>

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

### <span data-ttu-id="42c66-141">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="42c66-141">-VirtualHubId</span></span>
<span data-ttu-id="42c66-142">Die Ressourcen-ID des virtuellen Hubs.</span><span class="sxs-lookup"><span data-stu-id="42c66-142">The Resource Id of the Virtual Hub.</span></span>

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

### <span data-ttu-id="42c66-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="42c66-143">-Confirm</span></span>
<span data-ttu-id="42c66-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="42c66-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42c66-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42c66-145">-WhatIf</span></span>
<span data-ttu-id="42c66-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42c66-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42c66-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42c66-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42c66-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42c66-148">CommonParameters</span></span>
<span data-ttu-id="42c66-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42c66-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42c66-150">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42c66-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42c66-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42c66-151">INPUTS</span></span>

### <span data-ttu-id="42c66-152">System. String</span><span class="sxs-lookup"><span data-stu-id="42c66-152">System.String</span></span>

### <span data-ttu-id="42c66-153">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="42c66-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

### <span data-ttu-id="42c66-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="42c66-154">System.Int32</span></span>

### <span data-ttu-id="42c66-155">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="42c66-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

### <span data-ttu-id="42c66-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="42c66-156">System.String[]</span></span>

### <span data-ttu-id="42c66-157">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="42c66-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="42c66-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42c66-158">OUTPUTS</span></span>

### <span data-ttu-id="42c66-159">Microsoft. Azure. Commands. Network. Models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="42c66-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="42c66-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="42c66-160">NOTES</span></span>

## <span data-ttu-id="42c66-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42c66-161">RELATED LINKS</span></span>
