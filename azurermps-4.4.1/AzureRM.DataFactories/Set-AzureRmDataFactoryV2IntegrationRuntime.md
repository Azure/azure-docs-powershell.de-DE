---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: ce842abf58dabb0bdd518f02e7030f3fb2feabc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665081"
---
# <span data-ttu-id="3a1ea-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3a1ea-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="3a1ea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a1ea-102">SYNOPSIS</span></span>
<span data-ttu-id="3a1ea-103">Aktualisiert eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a1ea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a1ea-104">SYNTAX</span></span>

### <span data-ttu-id="3a1ea-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a1ea-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3a1ea-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a1ea-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="3a1ea-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a1ea-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a1ea-108">DESCRIPTION</span></span>
<span data-ttu-id="3a1ea-109">Das Set-AzureRmDataFactoryV2IntegrationRuntime-Cmdlet aktualisiert eine Integrationslaufzeit mit bestimmten Parametern.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="3a1ea-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a1ea-110">EXAMPLES</span></span>

### <span data-ttu-id="3a1ea-111">Beispiel 1: Update-Integrationslauf Zeit Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="3a1ea-112">Das Cmdlet aktualisiert die Beschreibung der Integrationslaufzeit mit dem Namen "Test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="3a1ea-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="3a1ea-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a1ea-113">PARAMETERS</span></span>

### <span data-ttu-id="3a1ea-114">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="3a1ea-114">-CatalogAdminCredential</span></span>
<span data-ttu-id="3a1ea-115">Die Anmeldeinformationen für den Katalogdaten Bank Administrator der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-115">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a1ea-116">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="3a1ea-116">-CatalogPricingTier</span></span>
<span data-ttu-id="3a1ea-117">Die Preisstufe der Katalogdatenbank der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-117">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a1ea-118">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a1ea-118">-CatalogServerEndpoint</span></span>
<span data-ttu-id="3a1ea-119">Der Katalogdatenbankserver-Endpunkt der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-119">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a1ea-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3a1ea-120">-Confirm</span></span>
<span data-ttu-id="3a1ea-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a1ea-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="3a1ea-122">-DataFactoryName</span></span>
<span data-ttu-id="3a1ea-123">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-123">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a1ea-124">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a1ea-124">-Description</span></span>
<span data-ttu-id="3a1ea-125">Die Beschreibung der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-125">The integration runtime description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a1ea-126">-Force</span><span class="sxs-lookup"><span data-stu-id="3a1ea-126">-Force</span></span>
<span data-ttu-id="3a1ea-127">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-127">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3a1ea-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3a1ea-128">-InputObject</span></span>
<span data-ttu-id="3a1ea-129">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-129">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a1ea-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="3a1ea-130">-Location</span></span>
<span data-ttu-id="3a1ea-131">Der Speicherort der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-131">The integration runtime location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a1ea-132">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="3a1ea-132">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="3a1ea-133">Maximale parallele Ausführungsanzahl pro Knoten für eine verwaltete dedizierte Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-133">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a1ea-134">-Name</span><span class="sxs-lookup"><span data-stu-id="3a1ea-134">-Name</span></span>
<span data-ttu-id="3a1ea-135">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-135">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a1ea-136">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="3a1ea-136">-NodeCount</span></span>
<span data-ttu-id="3a1ea-137">Die Anzahl der Zielknoten der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-137">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a1ea-138">-Knoten</span><span class="sxs-lookup"><span data-stu-id="3a1ea-138">-NodeSize</span></span>
<span data-ttu-id="3a1ea-139">Die Knoten Größe der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-139">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a1ea-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a1ea-140">-ResourceGroupName</span></span>
<span data-ttu-id="3a1ea-141">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-141">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a1ea-142">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3a1ea-142">-ResourceId</span></span>
<span data-ttu-id="3a1ea-143">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-143">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a1ea-144">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="3a1ea-144">-Subnet</span></span>
<span data-ttu-id="3a1ea-145">Der Name des Subnets in der VNet.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-145">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a1ea-146">-Typ</span><span class="sxs-lookup"><span data-stu-id="3a1ea-146">-Type</span></span>
<span data-ttu-id="3a1ea-147">Der Typ der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-147">The integration runtime type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a1ea-148">-VNetId</span><span class="sxs-lookup"><span data-stu-id="3a1ea-148">-VNetId</span></span>
<span data-ttu-id="3a1ea-149">Die ID des VNet, dem die Integrationslaufzeit Beitritt.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-149">The ID of the VNet that the integration runtime joins.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a1ea-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a1ea-150">-WhatIf</span></span>
<span data-ttu-id="3a1ea-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-151">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3a1ea-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a1ea-152">-DefaultProfile</span></span>
<span data-ttu-id="3a1ea-153">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a1ea-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a1ea-154">CommonParameters</span></span>
<span data-ttu-id="3a1ea-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a1ea-156">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a1ea-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a1ea-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a1ea-157">INPUTS</span></span>

### <span data-ttu-id="3a1ea-158">System. String</span><span class="sxs-lookup"><span data-stu-id="3a1ea-158">System.String</span></span>
<span data-ttu-id="3a1ea-159">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3a1ea-159">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3a1ea-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a1ea-160">OUTPUTS</span></span>

### <span data-ttu-id="3a1ea-161">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3a1ea-161">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3a1ea-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a1ea-162">NOTES</span></span>

## <span data-ttu-id="3a1ea-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a1ea-163">RELATED LINKS</span></span>

[<span data-ttu-id="3a1ea-164">Satz-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3a1ea-164">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
