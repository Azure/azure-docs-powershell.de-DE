---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 219e5b18a04332d2ee840fb41b92aa9d282a1792
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847160"
---
# <span data-ttu-id="a5e96-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a5e96-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="a5e96-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5e96-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e96-103">Erstellt eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a5e96-103">Creates a data factory.</span></span>

## <span data-ttu-id="a5e96-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5e96-104">SYNTAX</span></span>

### <span data-ttu-id="a5e96-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a5e96-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5e96-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a5e96-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5e96-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="a5e96-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5e96-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="a5e96-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5e96-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="a5e96-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5e96-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="a5e96-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5e96-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a5e96-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5e96-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="a5e96-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5e96-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="a5e96-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5e96-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5e96-114">DESCRIPTION</span></span>
<span data-ttu-id="a5e96-115">Das Cmdlet " **Satz-AzDataFactoryV2** " erstellt eine Data Factory mit dem angegebenen Namen und Speicherort der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a5e96-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="a5e96-116">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:--Erstellen Sie eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a5e96-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="a5e96-117">--Erstellen Sie verknüpfte Dienste.</span><span class="sxs-lookup"><span data-stu-id="a5e96-117">-- Create linked services.</span></span>
<span data-ttu-id="a5e96-118">--Erstellen von Datasets.</span><span class="sxs-lookup"><span data-stu-id="a5e96-118">-- Create datasets.</span></span>
<span data-ttu-id="a5e96-119">--Erstellen Sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a5e96-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="a5e96-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5e96-120">EXAMPLES</span></span>

### <span data-ttu-id="a5e96-121">Beispiel 1: Erstellen einer Data Factory</span><span class="sxs-lookup"><span data-stu-id="a5e96-121">Example 1: Create a data factory</span></span>
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

### <span data-ttu-id="a5e96-122">Beispiel 2: Erstellen einer Data Factory mit Repo-Konfigurationsdetails mithilfe eines vorhandenen Factory-Objekts</span><span class="sxs-lookup"><span data-stu-id="a5e96-122">Example 2: Create a data factory with repo configuration details using an existing factory object.</span></span>
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

<span data-ttu-id="a5e96-123">Mit diesem Befehl wird eine Data Factory mit dem Namen WikiADF in der Ressourcengruppe ADF in der eastus-Position mit Azure DevOps-Quell Code Verwaltungskonfiguration erstellt.</span><span class="sxs-lookup"><span data-stu-id="a5e96-123">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with Azure DevOps source control configuration.</span></span>

### <span data-ttu-id="a5e96-124">Beispiel 3: Erstellen einer Data Factory mit GitHub-Repo-Konfigurationsdetails mithilfe eines neuen Factory-Objekts</span><span class="sxs-lookup"><span data-stu-id="a5e96-124">Example 3: Create a data factory with GitHub repo configuration details using a new factory object.</span></span>
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

<span data-ttu-id="a5e96-125">Mit diesem Befehl wird eine Data Factory mit dem Namen WikiADF in der Ressourcengruppe ADF in der eastus-Position mit GitHub-Quellcodeverwaltungs-Konfiguration erstellt.</span><span class="sxs-lookup"><span data-stu-id="a5e96-125">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with GitHub source control configuration..</span></span>

## <span data-ttu-id="a5e96-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5e96-126">PARAMETERS</span></span>

### <span data-ttu-id="a5e96-127">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="a5e96-127">-AccountName</span></span>
<span data-ttu-id="a5e96-128">Der Konto Name für die Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a5e96-128">The account name for repo configuration.</span></span>

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

### <span data-ttu-id="a5e96-129">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="a5e96-129">-CollaborationBranch</span></span>
<span data-ttu-id="a5e96-130">Der Zusammenarbeits Zweig für die Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a5e96-130">The collaboration branch for repo configuration.</span></span>

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

### <span data-ttu-id="a5e96-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e96-131">-DefaultProfile</span></span>
<span data-ttu-id="a5e96-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a5e96-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5e96-133">-Force</span><span class="sxs-lookup"><span data-stu-id="a5e96-133">-Force</span></span>
<span data-ttu-id="a5e96-134">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="a5e96-134">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a5e96-135">-Hostname</span><span class="sxs-lookup"><span data-stu-id="a5e96-135">-HostName</span></span>
<span data-ttu-id="a5e96-136">Der Hostname für die GitHub-Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a5e96-136">The host name for GitHub repo configuration.</span></span>

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

### <span data-ttu-id="a5e96-137">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a5e96-137">-InputObject</span></span>
<span data-ttu-id="a5e96-138">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a5e96-138">The data factory object.</span></span>

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

### <span data-ttu-id="a5e96-139">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="a5e96-139">-LastCommitId</span></span>
<span data-ttu-id="a5e96-140">Die letzte Commit-ID für die Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a5e96-140">The last commit id for repo configuration.</span></span>

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

### <span data-ttu-id="a5e96-141">-Standort</span><span class="sxs-lookup"><span data-stu-id="a5e96-141">-Location</span></span>
<span data-ttu-id="a5e96-142">Die Data Factory wird in diesem Bereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="a5e96-142">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="a5e96-143">-Name</span><span class="sxs-lookup"><span data-stu-id="a5e96-143">-Name</span></span>
<span data-ttu-id="a5e96-144">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="a5e96-144">The data factory name.</span></span>

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

### <span data-ttu-id="a5e96-145">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="a5e96-145">-ProjectName</span></span>
<span data-ttu-id="a5e96-146">Der Projektname Azure DevOps für die Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a5e96-146">The project name Azure DevOps for repo configuration.</span></span>

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

### <span data-ttu-id="a5e96-147">-Repositoryname</span><span class="sxs-lookup"><span data-stu-id="a5e96-147">-RepositoryName</span></span>
<span data-ttu-id="a5e96-148">Der Repository-Name für die Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a5e96-148">The repository name for repo configuration.</span></span>

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

### <span data-ttu-id="a5e96-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5e96-149">-ResourceGroupName</span></span>
<span data-ttu-id="a5e96-150">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a5e96-150">The resource group name.</span></span>

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

### <span data-ttu-id="a5e96-151">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a5e96-151">-ResourceId</span></span>
<span data-ttu-id="a5e96-152">Die Azure-Ressourcen-ID von V2 Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a5e96-152">The Azure resource ID of V2 data factory.</span></span>

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

### <span data-ttu-id="a5e96-153">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="a5e96-153">-RootFolder</span></span>
<span data-ttu-id="a5e96-154">Der Stammordner für die Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a5e96-154">The root folder for repo configuration.</span></span>

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

### <span data-ttu-id="a5e96-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="a5e96-155">-Tag</span></span>
<span data-ttu-id="a5e96-156">Die Tags der Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a5e96-156">The tags of the data factory.</span></span>

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

### <span data-ttu-id="a5e96-157">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="a5e96-157">-TenantId</span></span>
<span data-ttu-id="a5e96-158">Die Mandanten-ID für Azure DevOps Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a5e96-158">The tenant id for Azure DevOps repo configuration.</span></span>

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

### <span data-ttu-id="a5e96-159">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a5e96-159">-Confirm</span></span>
<span data-ttu-id="a5e96-160">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5e96-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5e96-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5e96-161">-WhatIf</span></span>
<span data-ttu-id="a5e96-162">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a5e96-162">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="a5e96-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e96-163">CommonParameters</span></span>
<span data-ttu-id="a5e96-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5e96-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e96-165">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5e96-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e96-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5e96-166">INPUTS</span></span>

### <span data-ttu-id="a5e96-167">System. String</span><span class="sxs-lookup"><span data-stu-id="a5e96-167">System.String</span></span>

### <span data-ttu-id="a5e96-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a5e96-168">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a5e96-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5e96-169">OUTPUTS</span></span>

### <span data-ttu-id="a5e96-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a5e96-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="a5e96-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5e96-171">NOTES</span></span>
<span data-ttu-id="a5e96-172">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="a5e96-172">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a5e96-173">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5e96-173">RELATED LINKS</span></span>

[<span data-ttu-id="a5e96-174">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a5e96-174">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="a5e96-175">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a5e96-175">Remove-AzDataFactoryV2</span></span>]()
