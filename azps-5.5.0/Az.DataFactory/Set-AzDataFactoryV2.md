---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 5020ddeccc755ef52bf7410d61eb57b637d261bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162057"
---
# <span data-ttu-id="1529f-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1529f-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="1529f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1529f-102">SYNOPSIS</span></span>
<span data-ttu-id="1529f-103">Erstellt eine Daten factory.</span><span class="sxs-lookup"><span data-stu-id="1529f-103">Creates a data factory.</span></span>

## <span data-ttu-id="1529f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1529f-104">SYNTAX</span></span>

### <span data-ttu-id="1529f-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1529f-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1529f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1529f-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1529f-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="1529f-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1529f-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="1529f-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1529f-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="1529f-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1529f-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="1529f-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1529f-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1529f-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1529f-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="1529f-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1529f-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="1529f-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1529f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1529f-114">DESCRIPTION</span></span>
<span data-ttu-id="1529f-115">Das **Cmdlet "Set-AzDataFactoryV2"** erstellt eine Datenfactory mit dem angegebenen Ressourcengruppennamen und -ort.</span><span class="sxs-lookup"><span data-stu-id="1529f-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="1529f-116">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus: -- Erstellen Sie eine Daten factory.</span><span class="sxs-lookup"><span data-stu-id="1529f-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="1529f-117">- Verknüpfte Dienste erstellen.</span><span class="sxs-lookup"><span data-stu-id="1529f-117">-- Create linked services.</span></span>
<span data-ttu-id="1529f-118">– Erstellen sie Datasets.</span><span class="sxs-lookup"><span data-stu-id="1529f-118">-- Create datasets.</span></span>
<span data-ttu-id="1529f-119">– Erstellen Sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="1529f-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="1529f-120">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1529f-120">EXAMPLES</span></span>

### <span data-ttu-id="1529f-121">Beispiel 1: Erstellen einer Daten factory</span><span class="sxs-lookup"><span data-stu-id="1529f-121">Example 1: Create a data factory</span></span>
```
PS C:\> Set-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration :
```

### <span data-ttu-id="1529f-122">Beispiel 2: Erstellen einer Daten factory mit Repositorykonfigurationsdetails mithilfe eines vorhandenen Factoryobjekts.</span><span class="sxs-lookup"><span data-stu-id="1529f-122">Example 2: Create a data factory with repo configuration details using an existing factory object.</span></span>
```
PS C:\> Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" | Set-AzDataFactoryV2 -AccountName msdata -RepositoryName ADFRepo -CollaborationBranch master -RootFolder / -ProjectName "Azure Data Factory"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration : Microsoft.Azure.Management.DataFactory.Models.FactoryVSTSConfiguration
```

<span data-ttu-id="1529f-123">Mit diesem Befehl wird eine Daten factory namens WikiADF in der Ressourcengruppe namens ADF am Standort EastUS mit der Azure DevOps-Quellsteuerelementkonfiguration erstellt.</span><span class="sxs-lookup"><span data-stu-id="1529f-123">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with Azure DevOps source control configuration.</span></span>

### <span data-ttu-id="1529f-124">Beispiel 3: Erstellen einer Daten factory mit GitHub-Repository-Konfigurationsdetails mithilfe eines neuen Factoryobjekts.</span><span class="sxs-lookup"><span data-stu-id="1529f-124">Example 3: Create a data factory with GitHub repo configuration details using a new factory object.</span></span>
```
PS C:\> New-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location 'EastUS' -HostName 'https://github.com' -AccountName msdata -RepositoryName ADFRepo -CollaborationBranch master -RootFolder /

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration : Microsoft.Azure.Management.DataFactory.Models.FactoryGitHubConfiguration
```

<span data-ttu-id="1529f-125">Mit diesem Befehl wird eine Daten factory namens WikiADF in der Ressourcengruppe namens ADF an der Position "EastUS" mit der GitHub-Quellcodeverwaltungskonfiguration erstellt.</span><span class="sxs-lookup"><span data-stu-id="1529f-125">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with GitHub source control configuration..</span></span>

## <span data-ttu-id="1529f-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1529f-126">PARAMETERS</span></span>

### <span data-ttu-id="1529f-127">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1529f-127">-AccountName</span></span>
<span data-ttu-id="1529f-128">Der Kontoname für die Repositorykonfiguration.</span><span class="sxs-lookup"><span data-stu-id="1529f-128">The account name for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1529f-129">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="1529f-129">-CollaborationBranch</span></span>
<span data-ttu-id="1529f-130">Der Zweig für die Zusammenarbeit für repository-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1529f-130">The collaboration branch for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1529f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1529f-131">-DefaultProfile</span></span>
<span data-ttu-id="1529f-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1529f-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1529f-133">-Force</span><span class="sxs-lookup"><span data-stu-id="1529f-133">-Force</span></span>
<span data-ttu-id="1529f-134">Führt das Cmdlet ohne Bestätigungsaufforderung aus.</span><span class="sxs-lookup"><span data-stu-id="1529f-134">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="1529f-135">-GlobalParameterDefinition</span><span class="sxs-lookup"><span data-stu-id="1529f-135">-GlobalParameterDefinition</span></span>
<span data-ttu-id="1529f-136">Das Wörterbuch, das die globalen Parameter der Daten factory enthält.</span><span class="sxs-lookup"><span data-stu-id="1529f-136">The dictionary containing the global parameters of the data factory.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1529f-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="1529f-137">-HostName</span></span>
<span data-ttu-id="1529f-138">Der Hostname für die GitHub-Repositorykonfiguration.</span><span class="sxs-lookup"><span data-stu-id="1529f-138">The host name for GitHub repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1529f-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1529f-139">-InputObject</span></span>
<span data-ttu-id="1529f-140">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1529f-140">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1529f-141">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="1529f-141">-LastCommitId</span></span>
<span data-ttu-id="1529f-142">Die letzte Commit-ID für repository-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1529f-142">The last commit id for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1529f-143">-Location</span><span class="sxs-lookup"><span data-stu-id="1529f-143">-Location</span></span>
<span data-ttu-id="1529f-144">Die Daten factory wird in dieser Region erstellt.</span><span class="sxs-lookup"><span data-stu-id="1529f-144">The data factory is created in this region.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1529f-145">-Name</span><span class="sxs-lookup"><span data-stu-id="1529f-145">-Name</span></span>
<span data-ttu-id="1529f-146">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="1529f-146">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1529f-147">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="1529f-147">-ProjectName</span></span>
<span data-ttu-id="1529f-148">Der Projektname Azure DevOps für Repositorykonfiguration.</span><span class="sxs-lookup"><span data-stu-id="1529f-148">The project name Azure DevOps for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1529f-149">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="1529f-149">-RepositoryName</span></span>
<span data-ttu-id="1529f-150">Der Repositoryname für die Repositorykonfiguration.</span><span class="sxs-lookup"><span data-stu-id="1529f-150">The repository name for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1529f-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1529f-151">-ResourceGroupName</span></span>
<span data-ttu-id="1529f-152">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1529f-152">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1529f-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1529f-153">-ResourceId</span></span>
<span data-ttu-id="1529f-154">Die Azure-Ressourcen-ID der V2-Daten factory.</span><span class="sxs-lookup"><span data-stu-id="1529f-154">The Azure resource ID of V2 data factory.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig
Aliases: Id, DataFactoryId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1529f-155">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="1529f-155">-RootFolder</span></span>
<span data-ttu-id="1529f-156">Der Stammordner für die Repositorykonfiguration.</span><span class="sxs-lookup"><span data-stu-id="1529f-156">The root folder for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1529f-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="1529f-157">-Tag</span></span>
<span data-ttu-id="1529f-158">Die Tags der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="1529f-158">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFactoryName, ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1529f-159">-TenantId</span><span class="sxs-lookup"><span data-stu-id="1529f-159">-TenantId</span></span>
<span data-ttu-id="1529f-160">Die Mandanten-ID für Azure DevOps Repository-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1529f-160">The tenant id for Azure DevOps repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1529f-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1529f-161">-Confirm</span></span>
<span data-ttu-id="1529f-162">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1529f-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1529f-163">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1529f-163">-WhatIf</span></span>
<span data-ttu-id="1529f-164">Zeigt, was geschieht, wenn das Cmdlet ausgeführt, aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1529f-164">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="1529f-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1529f-165">CommonParameters</span></span>
<span data-ttu-id="1529f-166">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1529f-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1529f-167">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1529f-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1529f-168">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1529f-168">INPUTS</span></span>

### <span data-ttu-id="1529f-169">System.String</span><span class="sxs-lookup"><span data-stu-id="1529f-169">System.String</span></span>

### <span data-ttu-id="1529f-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1529f-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="1529f-171">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1529f-171">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1529f-172">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1529f-172">OUTPUTS</span></span>

### <span data-ttu-id="1529f-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1529f-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="1529f-174">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1529f-174">NOTES</span></span>
<span data-ttu-id="1529f-175">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="1529f-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1529f-176">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1529f-176">RELATED LINKS</span></span>

[<span data-ttu-id="1529f-177">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1529f-177">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="1529f-178">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1529f-178">Remove-AzDataFactoryV2</span></span>]()
