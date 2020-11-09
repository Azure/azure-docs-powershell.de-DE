---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 5020ddeccc755ef52bf7410d61eb57b637d261bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298263"
---
# <span data-ttu-id="dd1c9-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="dd1c9-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="dd1c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd1c9-102">SYNOPSIS</span></span>
<span data-ttu-id="dd1c9-103">Erstellt eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-103">Creates a data factory.</span></span>

## <span data-ttu-id="dd1c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd1c9-104">SYNTAX</span></span>

### <span data-ttu-id="dd1c9-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="dd1c9-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd1c9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dd1c9-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd1c9-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="dd1c9-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd1c9-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="dd1c9-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd1c9-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="dd1c9-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd1c9-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="dd1c9-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd1c9-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dd1c9-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd1c9-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="dd1c9-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd1c9-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="dd1c9-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd1c9-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd1c9-114">DESCRIPTION</span></span>
<span data-ttu-id="dd1c9-115">Das Cmdlet " **Satz-AzDataFactoryV2** " erstellt eine Data Factory mit dem angegebenen Namen und Speicherort der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="dd1c9-116">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:--Erstellen Sie eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="dd1c9-117">--Erstellen Sie verknüpfte Dienste.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-117">-- Create linked services.</span></span>
<span data-ttu-id="dd1c9-118">--Erstellen von Datasets.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-118">-- Create datasets.</span></span>
<span data-ttu-id="dd1c9-119">--Erstellen Sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="dd1c9-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd1c9-120">EXAMPLES</span></span>

### <span data-ttu-id="dd1c9-121">Beispiel 1: Erstellen einer Data Factory</span><span class="sxs-lookup"><span data-stu-id="dd1c9-121">Example 1: Create a data factory</span></span>
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

### <span data-ttu-id="dd1c9-122">Beispiel 2: Erstellen einer Data Factory mit Repo-Konfigurationsdetails mithilfe eines vorhandenen Factory-Objekts</span><span class="sxs-lookup"><span data-stu-id="dd1c9-122">Example 2: Create a data factory with repo configuration details using an existing factory object.</span></span>
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

<span data-ttu-id="dd1c9-123">Mit diesem Befehl wird eine Data Factory mit dem Namen WikiADF in der Ressourcengruppe ADF in der eastus-Position mit Azure DevOps-Quell Code Verwaltungskonfiguration erstellt.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-123">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with Azure DevOps source control configuration.</span></span>

### <span data-ttu-id="dd1c9-124">Beispiel 3: Erstellen einer Data Factory mit GitHub-Repo-Konfigurationsdetails mithilfe eines neuen Factory-Objekts</span><span class="sxs-lookup"><span data-stu-id="dd1c9-124">Example 3: Create a data factory with GitHub repo configuration details using a new factory object.</span></span>
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

<span data-ttu-id="dd1c9-125">Mit diesem Befehl wird eine Data Factory mit dem Namen WikiADF in der Ressourcengruppe ADF in der eastus-Position mit GitHub-Quellcodeverwaltungs-Konfiguration erstellt.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-125">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with GitHub source control configuration..</span></span>

## <span data-ttu-id="dd1c9-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd1c9-126">PARAMETERS</span></span>

### <span data-ttu-id="dd1c9-127">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="dd1c9-127">-AccountName</span></span>
<span data-ttu-id="dd1c9-128">Der Konto Name für die Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-128">The account name for repo configuration.</span></span>

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

### <span data-ttu-id="dd1c9-129">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="dd1c9-129">-CollaborationBranch</span></span>
<span data-ttu-id="dd1c9-130">Der Zusammenarbeits Zweig für die Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-130">The collaboration branch for repo configuration.</span></span>

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

### <span data-ttu-id="dd1c9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd1c9-131">-DefaultProfile</span></span>
<span data-ttu-id="dd1c9-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd1c9-133">-Force</span><span class="sxs-lookup"><span data-stu-id="dd1c9-133">-Force</span></span>
<span data-ttu-id="dd1c9-134">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-134">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="dd1c9-135">-GlobalParameterDefinition</span><span class="sxs-lookup"><span data-stu-id="dd1c9-135">-GlobalParameterDefinition</span></span>
<span data-ttu-id="dd1c9-136">Das Wörterbuch, das die globalen Parameter der Data Factory enthält.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-136">The dictionary containing the global parameters of the data factory.</span></span>

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

### <span data-ttu-id="dd1c9-137">-Hostname</span><span class="sxs-lookup"><span data-stu-id="dd1c9-137">-HostName</span></span>
<span data-ttu-id="dd1c9-138">Der Hostname für die GitHub-Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-138">The host name for GitHub repo configuration.</span></span>

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

### <span data-ttu-id="dd1c9-139">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dd1c9-139">-InputObject</span></span>
<span data-ttu-id="dd1c9-140">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-140">The data factory object.</span></span>

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

### <span data-ttu-id="dd1c9-141">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="dd1c9-141">-LastCommitId</span></span>
<span data-ttu-id="dd1c9-142">Die letzte Commit-ID für die Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-142">The last commit id for repo configuration.</span></span>

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

### <span data-ttu-id="dd1c9-143">-Standort</span><span class="sxs-lookup"><span data-stu-id="dd1c9-143">-Location</span></span>
<span data-ttu-id="dd1c9-144">Die Data Factory wird in diesem Bereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-144">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="dd1c9-145">-Name</span><span class="sxs-lookup"><span data-stu-id="dd1c9-145">-Name</span></span>
<span data-ttu-id="dd1c9-146">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-146">The data factory name.</span></span>

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

### <span data-ttu-id="dd1c9-147">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="dd1c9-147">-ProjectName</span></span>
<span data-ttu-id="dd1c9-148">Der Projektname Azure DevOps für die Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-148">The project name Azure DevOps for repo configuration.</span></span>

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

### <span data-ttu-id="dd1c9-149">-Repositoryname</span><span class="sxs-lookup"><span data-stu-id="dd1c9-149">-RepositoryName</span></span>
<span data-ttu-id="dd1c9-150">Der Repository-Name für die Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-150">The repository name for repo configuration.</span></span>

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

### <span data-ttu-id="dd1c9-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd1c9-151">-ResourceGroupName</span></span>
<span data-ttu-id="dd1c9-152">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-152">The resource group name.</span></span>

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

### <span data-ttu-id="dd1c9-153">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="dd1c9-153">-ResourceId</span></span>
<span data-ttu-id="dd1c9-154">Die Azure-Ressourcen-ID von V2 Data Factory.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-154">The Azure resource ID of V2 data factory.</span></span>

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

### <span data-ttu-id="dd1c9-155">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="dd1c9-155">-RootFolder</span></span>
<span data-ttu-id="dd1c9-156">Der Stammordner für die Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-156">The root folder for repo configuration.</span></span>

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

### <span data-ttu-id="dd1c9-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="dd1c9-157">-Tag</span></span>
<span data-ttu-id="dd1c9-158">Die Tags der Data Factory.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-158">The tags of the data factory.</span></span>

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

### <span data-ttu-id="dd1c9-159">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="dd1c9-159">-TenantId</span></span>
<span data-ttu-id="dd1c9-160">Die Mandanten-ID für Azure DevOps Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-160">The tenant id for Azure DevOps repo configuration.</span></span>

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

### <span data-ttu-id="dd1c9-161">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dd1c9-161">-Confirm</span></span>
<span data-ttu-id="dd1c9-162">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd1c9-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd1c9-163">-WhatIf</span></span>
<span data-ttu-id="dd1c9-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-164">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="dd1c9-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd1c9-165">CommonParameters</span></span>
<span data-ttu-id="dd1c9-166">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd1c9-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd1c9-167">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd1c9-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd1c9-168">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd1c9-168">INPUTS</span></span>

### <span data-ttu-id="dd1c9-169">System. String</span><span class="sxs-lookup"><span data-stu-id="dd1c9-169">System.String</span></span>

### <span data-ttu-id="dd1c9-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="dd1c9-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="dd1c9-171">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dd1c9-171">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dd1c9-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd1c9-172">OUTPUTS</span></span>

### <span data-ttu-id="dd1c9-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="dd1c9-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="dd1c9-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd1c9-174">NOTES</span></span>
<span data-ttu-id="dd1c9-175">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="dd1c9-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="dd1c9-176">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd1c9-176">RELATED LINKS</span></span>

[<span data-ttu-id="dd1c9-177">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="dd1c9-177">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="dd1c9-178">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="dd1c9-178">Remove-AzDataFactoryV2</span></span>]()
