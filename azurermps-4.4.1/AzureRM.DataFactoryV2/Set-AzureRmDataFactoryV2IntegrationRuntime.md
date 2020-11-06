---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: f24d42f1c4648343b979586ee906913f5d6a07f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505977"
---
# <span data-ttu-id="2e3d8-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2e3d8-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="2e3d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2e3d8-102">SYNOPSIS</span></span>
<span data-ttu-id="2e3d8-103">Aktualisiert eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="2e3d8-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e3d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e3d8-104">SYNTAX</span></span>

### <span data-ttu-id="2e3d8-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2e3d8-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2e3d8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2e3d8-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2e3d8-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="2e3d8-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="2e3d8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e3d8-108">DESCRIPTION</span></span>
<span data-ttu-id="2e3d8-109">Das Set-AzureRmDataFactoryV2IntegrationRuntime-Cmdlet aktualisiert eine Integrationslaufzeit mit bestimmten Parametern.</span><span class="sxs-lookup"><span data-stu-id="2e3d8-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="2e3d8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e3d8-110">EXAMPLES</span></span>

### <span data-ttu-id="2e3d8-111">Beispiel 1: Update-Integrationslauf Zeit Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="2e3d8-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description

```

<span data-ttu-id="2e3d8-112">Das Cmdlet aktualisiert die Beschreibung der Integrationslaufzeit mit dem Namen "Test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="2e3d8-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="2e3d8-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e3d8-113">PARAMETERS</span></span>

### <span data-ttu-id="2e3d8-114">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="2e3d8-114">-CatalogAdminCredential</span></span>
<span data-ttu-id="2e3d8-115">Die Anmeldeinformationen für den Katalogdaten Bank Administrator der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="2e3d8-115">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3d8-116">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="2e3d8-116">-CatalogPricingTier</span></span>
<span data-ttu-id="2e3d8-117">Die Preisstufe der Katalogdatenbank der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="2e3d8-117">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3d8-118">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e3d8-118">-CatalogServerEndpoint</span></span>
<span data-ttu-id="2e3d8-119">Der Katalogdatenbankserver-Endpunkt der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="2e3d8-119">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3d8-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2e3d8-120">-Confirm</span></span>
<span data-ttu-id="2e3d8-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2e3d8-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3d8-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="2e3d8-122">-DataFactoryName</span></span>
<span data-ttu-id="2e3d8-123">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="2e3d8-123">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e3d8-124">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e3d8-124">-Description</span></span>
<span data-ttu-id="2e3d8-125">Die Beschreibung der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="2e3d8-125">The integration runtime description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3d8-126">-Force</span><span class="sxs-lookup"><span data-stu-id="2e3d8-126">-Force</span></span>
<span data-ttu-id="2e3d8-127">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="2e3d8-127">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3d8-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2e3d8-128">-InputObject</span></span>
<span data-ttu-id="2e3d8-129">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="2e3d8-129">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e3d8-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="2e3d8-130">-Location</span></span>
<span data-ttu-id="2e3d8-131">Der Speicherort der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="2e3d8-131">The integration runtime location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3d8-132">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="2e3d8-132">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="2e3d8-133">Maximale parallele Ausführungsanzahl pro Knoten für eine verwaltete dedizierte Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="2e3d8-133">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3d8-134">-Name</span><span class="sxs-lookup"><span data-stu-id="2e3d8-134">-Name</span></span>
<span data-ttu-id="2e3d8-135">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="2e3d8-135">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e3d8-136">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="2e3d8-136">-NodeCount</span></span>
<span data-ttu-id="2e3d8-137">Die Anzahl der Zielknoten der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="2e3d8-137">Target nodes count of the integration runtime.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3d8-138">-Knoten</span><span class="sxs-lookup"><span data-stu-id="2e3d8-138">-NodeSize</span></span>
<span data-ttu-id="2e3d8-139">Die Knoten Größe der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="2e3d8-139">The integration runtime node size.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3d8-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e3d8-140">-ResourceGroupName</span></span>
<span data-ttu-id="2e3d8-141">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2e3d8-141">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e3d8-142">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2e3d8-142">-ResourceId</span></span>
<span data-ttu-id="2e3d8-143">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="2e3d8-143">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e3d8-144">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="2e3d8-144">-Subnet</span></span>
<span data-ttu-id="2e3d8-145">Der Name des Subnets in der VNet.</span><span class="sxs-lookup"><span data-stu-id="2e3d8-145">The name of the subnet in the VNet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3d8-146">-Typ</span><span class="sxs-lookup"><span data-stu-id="2e3d8-146">-Type</span></span>
<span data-ttu-id="2e3d8-147">Der Typ der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="2e3d8-147">The integration runtime type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3d8-148">-VNetId</span><span class="sxs-lookup"><span data-stu-id="2e3d8-148">-VNetId</span></span>
<span data-ttu-id="2e3d8-149">Die ID des VNet, dem die Integrationslaufzeit Beitritt.</span><span class="sxs-lookup"><span data-stu-id="2e3d8-149">The ID of the VNet that the integration runtime joins.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3d8-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e3d8-150">-WhatIf</span></span>
<span data-ttu-id="2e3d8-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2e3d8-151">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="2e3d8-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2e3d8-152">INPUTS</span></span>

### <span data-ttu-id="2e3d8-153">System. String</span><span class="sxs-lookup"><span data-stu-id="2e3d8-153">System.String</span></span>
<span data-ttu-id="2e3d8-154">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2e3d8-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2e3d8-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2e3d8-155">OUTPUTS</span></span>

### <span data-ttu-id="2e3d8-156">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2e3d8-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2e3d8-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="2e3d8-157">NOTES</span></span>

## <span data-ttu-id="2e3d8-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2e3d8-158">RELATED LINKS</span></span>
[<span data-ttu-id="2e3d8-159">Satz-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2e3d8-159">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
