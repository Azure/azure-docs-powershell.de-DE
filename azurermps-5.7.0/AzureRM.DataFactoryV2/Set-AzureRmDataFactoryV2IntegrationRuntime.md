---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 8b91e1a68fc731476240021889cc80c9c4848357
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483054"
---
# <span data-ttu-id="89cab-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="89cab-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="89cab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="89cab-102">SYNOPSIS</span></span>
<span data-ttu-id="89cab-103">Aktualisiert eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="89cab-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89cab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="89cab-104">SYNTAX</span></span>

### <span data-ttu-id="89cab-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="89cab-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89cab-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="89cab-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89cab-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="89cab-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89cab-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89cab-108">DESCRIPTION</span></span>
<span data-ttu-id="89cab-109">Das Set-AzureRmDataFactoryV2IntegrationRuntime-Cmdlet aktualisiert eine Integrationslaufzeit mit bestimmten Parametern.</span><span class="sxs-lookup"><span data-stu-id="89cab-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="89cab-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89cab-110">EXAMPLES</span></span>

### <span data-ttu-id="89cab-111">Beispiel 1: Update-Integrationslauf Zeit Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="89cab-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="89cab-112">Das Cmdlet aktualisiert die Beschreibung der Integrationslaufzeit mit dem Namen "Test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="89cab-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="89cab-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="89cab-113">PARAMETERS</span></span>

### <span data-ttu-id="89cab-114">-Authentifizierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="89cab-114">-AuthKey</span></span>
<span data-ttu-id="89cab-115">Der Authentifizierungsschlüssel der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="89cab-115">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89cab-116">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="89cab-116">-CatalogAdminCredential</span></span>
<span data-ttu-id="89cab-117">Die Anmeldeinformationen für den Katalogdaten Bank Administrator der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="89cab-117">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="89cab-118">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="89cab-118">-CatalogPricingTier</span></span>
<span data-ttu-id="89cab-119">Die Preisstufe der Katalogdatenbank der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="89cab-119">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="89cab-120">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="89cab-120">-CatalogServerEndpoint</span></span>
<span data-ttu-id="89cab-121">Der Katalogdatenbankserver-Endpunkt der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="89cab-121">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="89cab-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="89cab-122">-DataFactoryName</span></span>
<span data-ttu-id="89cab-123">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="89cab-123">The data factory name.</span></span>

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

### <span data-ttu-id="89cab-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89cab-124">-DefaultProfile</span></span>
<span data-ttu-id="89cab-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="89cab-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89cab-126">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89cab-126">-Description</span></span>
<span data-ttu-id="89cab-127">Die Beschreibung der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="89cab-127">The integration runtime description.</span></span>

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

### <span data-ttu-id="89cab-128">-Edition</span><span class="sxs-lookup"><span data-stu-id="89cab-128">-Edition</span></span>
<span data-ttu-id="89cab-129">Die Edition für die SSIS-Integrationslaufzeit, die Standard oder Enterprise sein kann, Standard ist Standard, wenn Sie nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="89cab-129">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89cab-130">-Force</span><span class="sxs-lookup"><span data-stu-id="89cab-130">-Force</span></span>
<span data-ttu-id="89cab-131">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="89cab-131">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="89cab-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="89cab-132">-InputObject</span></span>
<span data-ttu-id="89cab-133">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="89cab-133">The integration runtime object.</span></span>

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

### <span data-ttu-id="89cab-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="89cab-134">-LicenseType</span></span>
<span data-ttu-id="89cab-135">Der Lizenztyp, den Sie für die SSIS-IR auswählen möchten.</span><span class="sxs-lookup"><span data-stu-id="89cab-135">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="89cab-136">Es gibt zwei Typen: LicenseIncluded oder Grundpr..</span><span class="sxs-lookup"><span data-stu-id="89cab-136">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="89cab-137">Wenn Sie für die Azure Hybrid use Benefit (AHUB)-Preise qualifiziert sind, wählen Sie Grundpr. aus.</span><span class="sxs-lookup"><span data-stu-id="89cab-137">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="89cab-138">Wenn dies nicht der Fall ist, wählen Sie LicenseIncluded aus.</span><span class="sxs-lookup"><span data-stu-id="89cab-138">If not, please select LicenseIncluded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89cab-139">-Standort</span><span class="sxs-lookup"><span data-stu-id="89cab-139">-Location</span></span>
<span data-ttu-id="89cab-140">Der Speicherort der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="89cab-140">The integration runtime location.</span></span>

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

### <span data-ttu-id="89cab-141">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="89cab-141">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="89cab-142">Maximale parallele Ausführungsanzahl pro Knoten für eine verwaltete dedizierte Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="89cab-142">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="89cab-143">-Name</span><span class="sxs-lookup"><span data-stu-id="89cab-143">-Name</span></span>
<span data-ttu-id="89cab-144">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="89cab-144">The integration runtime name.</span></span>

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

### <span data-ttu-id="89cab-145">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="89cab-145">-NodeCount</span></span>
<span data-ttu-id="89cab-146">Die Anzahl der Zielknoten der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="89cab-146">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="89cab-147">-Knoten</span><span class="sxs-lookup"><span data-stu-id="89cab-147">-NodeSize</span></span>
<span data-ttu-id="89cab-148">Die Knoten Größe der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="89cab-148">The integration runtime node size.</span></span>

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

### <span data-ttu-id="89cab-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89cab-149">-ResourceGroupName</span></span>
<span data-ttu-id="89cab-150">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="89cab-150">The resource group name.</span></span>

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

### <span data-ttu-id="89cab-151">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="89cab-151">-ResourceId</span></span>
<span data-ttu-id="89cab-152">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="89cab-152">The Azure resource ID.</span></span>

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

### <span data-ttu-id="89cab-153">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="89cab-153">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="89cab-154">Der SAS-URI des Azure-BLOB-Containers, der das benutzerdefinierte Setupskript enthält.</span><span class="sxs-lookup"><span data-stu-id="89cab-154">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="89cab-155">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="89cab-155">-Subnet</span></span>
<span data-ttu-id="89cab-156">Der Name des Subnets in der VNet.</span><span class="sxs-lookup"><span data-stu-id="89cab-156">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="89cab-157">-Typ</span><span class="sxs-lookup"><span data-stu-id="89cab-157">-Type</span></span>
<span data-ttu-id="89cab-158">Der Typ der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="89cab-158">The integration runtime type.</span></span>

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

### <span data-ttu-id="89cab-159">-VNetId</span><span class="sxs-lookup"><span data-stu-id="89cab-159">-VNetId</span></span>
<span data-ttu-id="89cab-160">Die ID des VNet, dem die Integrationslaufzeit Beitritt.</span><span class="sxs-lookup"><span data-stu-id="89cab-160">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="89cab-161">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="89cab-161">-Confirm</span></span>
<span data-ttu-id="89cab-162">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="89cab-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89cab-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89cab-163">-WhatIf</span></span>
<span data-ttu-id="89cab-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="89cab-164">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="89cab-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89cab-165">CommonParameters</span></span>
<span data-ttu-id="89cab-166">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89cab-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89cab-167">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89cab-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89cab-168">Eingaben</span><span class="sxs-lookup"><span data-stu-id="89cab-168">INPUTS</span></span>

### <span data-ttu-id="89cab-169">System. String</span><span class="sxs-lookup"><span data-stu-id="89cab-169">System.String</span></span>
<span data-ttu-id="89cab-170">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="89cab-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="89cab-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="89cab-171">OUTPUTS</span></span>

### <span data-ttu-id="89cab-172">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="89cab-172">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="89cab-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="89cab-173">NOTES</span></span>

## <span data-ttu-id="89cab-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="89cab-174">RELATED LINKS</span></span>

[<span data-ttu-id="89cab-175">Satz-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="89cab-175">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
