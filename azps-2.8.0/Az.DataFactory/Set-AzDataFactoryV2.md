---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 374263c26a3572e8d85e18d1795c27a761866a4a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651674"
---
# <span data-ttu-id="b49a6-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b49a6-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="b49a6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b49a6-102">SYNOPSIS</span></span>
<span data-ttu-id="b49a6-103">Erstellt eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b49a6-103">Creates a data factory.</span></span>

## <span data-ttu-id="b49a6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b49a6-104">SYNTAX</span></span>

### <span data-ttu-id="b49a6-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b49a6-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b49a6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b49a6-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b49a6-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="b49a6-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b49a6-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="b49a6-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b49a6-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="b49a6-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b49a6-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="b49a6-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b49a6-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b49a6-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b49a6-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="b49a6-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b49a6-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="b49a6-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b49a6-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b49a6-114">DESCRIPTION</span></span>
<span data-ttu-id="b49a6-115">Das Cmdlet " **Satz-AzDataFactoryV2** " erstellt eine Data Factory mit dem angegebenen Namen und Speicherort der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b49a6-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="b49a6-116">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:--Erstellen Sie eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b49a6-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="b49a6-117">--Erstellen Sie verknüpfte Dienste.</span><span class="sxs-lookup"><span data-stu-id="b49a6-117">-- Create linked services.</span></span>
<span data-ttu-id="b49a6-118">--Erstellen von Datasets.</span><span class="sxs-lookup"><span data-stu-id="b49a6-118">-- Create datasets.</span></span>
<span data-ttu-id="b49a6-119">--Erstellen Sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b49a6-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="b49a6-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b49a6-120">EXAMPLES</span></span>

### <span data-ttu-id="b49a6-121">Beispiel 1: Erstellen einer Data Factory</span><span class="sxs-lookup"><span data-stu-id="b49a6-121">Example 1: Create a data factory</span></span>
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

### <span data-ttu-id="b49a6-122">Beispiel 2: Erstellen einer Data Factory mit repoconfiguration-Details mithilfe eines vorhandenen Factory-Objekts</span><span class="sxs-lookup"><span data-stu-id="b49a6-122">Example 2: Create a data factory with repoconfiguration details using an existing factory object.</span></span>
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

<span data-ttu-id="b49a6-123">Mit diesem Befehl wird eine Data Factory mit dem Namen WikiADF in der Ressourcengruppe ADF in der westus-Position erstellt.</span><span class="sxs-lookup"><span data-stu-id="b49a6-123">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="b49a6-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="b49a6-124">PARAMETERS</span></span>

### <span data-ttu-id="b49a6-125">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="b49a6-125">-AccountName</span></span>
<span data-ttu-id="b49a6-126">Der Konto Name für die Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b49a6-126">The account name for repo configuration.</span></span>

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

### <span data-ttu-id="b49a6-127">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="b49a6-127">-CollaborationBranch</span></span>
<span data-ttu-id="b49a6-128">Der Zusammenarbeits Zweig für die Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b49a6-128">The collaboration branch for repo configuration.</span></span>

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

### <span data-ttu-id="b49a6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b49a6-129">-DefaultProfile</span></span>
<span data-ttu-id="b49a6-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b49a6-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b49a6-131">-Force</span><span class="sxs-lookup"><span data-stu-id="b49a6-131">-Force</span></span>
<span data-ttu-id="b49a6-132">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="b49a6-132">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b49a6-133">-Hostname</span><span class="sxs-lookup"><span data-stu-id="b49a6-133">-HostName</span></span>
<span data-ttu-id="b49a6-134">Der Hostname für die Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b49a6-134">The host name for repo configuration.</span></span>

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

### <span data-ttu-id="b49a6-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b49a6-135">-InputObject</span></span>
<span data-ttu-id="b49a6-136">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b49a6-136">The data factory object.</span></span>

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

### <span data-ttu-id="b49a6-137">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="b49a6-137">-LastCommitId</span></span>
<span data-ttu-id="b49a6-138">Die letzte Commit-ID für die Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b49a6-138">The last commit id for repo configuration.</span></span>

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

### <span data-ttu-id="b49a6-139">-Standort</span><span class="sxs-lookup"><span data-stu-id="b49a6-139">-Location</span></span>
<span data-ttu-id="b49a6-140">Die Data Factory wird in diesem Bereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="b49a6-140">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="b49a6-141">-Name</span><span class="sxs-lookup"><span data-stu-id="b49a6-141">-Name</span></span>
<span data-ttu-id="b49a6-142">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="b49a6-142">The data factory name.</span></span>

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

### <span data-ttu-id="b49a6-143">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="b49a6-143">-ProjectName</span></span>
<span data-ttu-id="b49a6-144">Der Projektname für die Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b49a6-144">The project name for repo configuration.</span></span>

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

### <span data-ttu-id="b49a6-145">-Repositoryname</span><span class="sxs-lookup"><span data-stu-id="b49a6-145">-RepositoryName</span></span>
<span data-ttu-id="b49a6-146">Der Repository-Name für die Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b49a6-146">The repository name for repo configuration.</span></span>

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

### <span data-ttu-id="b49a6-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b49a6-147">-ResourceGroupName</span></span>
<span data-ttu-id="b49a6-148">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b49a6-148">The resource group name.</span></span>

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

### <span data-ttu-id="b49a6-149">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b49a6-149">-ResourceId</span></span>
<span data-ttu-id="b49a6-150">Die Azure-Ressourcen-ID von V2 Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b49a6-150">The Azure resource ID of V2 data factory.</span></span>

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

### <span data-ttu-id="b49a6-151">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="b49a6-151">-RootFolder</span></span>
<span data-ttu-id="b49a6-152">Der Stammordner für die Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b49a6-152">The root folder for repo configuration.</span></span>

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

### <span data-ttu-id="b49a6-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="b49a6-153">-Tag</span></span>
<span data-ttu-id="b49a6-154">Die Tags der Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b49a6-154">The tags of the data factory.</span></span>

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

### <span data-ttu-id="b49a6-155">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="b49a6-155">-TenantId</span></span>
<span data-ttu-id="b49a6-156">Die Mandanten-ID für die Repo-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b49a6-156">The tenant id for repo configuration.</span></span>

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

### <span data-ttu-id="b49a6-157">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b49a6-157">-Confirm</span></span>
<span data-ttu-id="b49a6-158">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b49a6-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b49a6-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b49a6-159">-WhatIf</span></span>
<span data-ttu-id="b49a6-160">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b49a6-160">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b49a6-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b49a6-161">CommonParameters</span></span>
<span data-ttu-id="b49a6-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b49a6-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b49a6-163">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b49a6-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b49a6-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b49a6-164">INPUTS</span></span>

### <span data-ttu-id="b49a6-165">System. String</span><span class="sxs-lookup"><span data-stu-id="b49a6-165">System.String</span></span>

### <span data-ttu-id="b49a6-166">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b49a6-166">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b49a6-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b49a6-167">OUTPUTS</span></span>

### <span data-ttu-id="b49a6-168">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b49a6-168">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="b49a6-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="b49a6-169">NOTES</span></span>
<span data-ttu-id="b49a6-170">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="b49a6-170">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b49a6-171">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b49a6-171">RELATED LINKS</span></span>

[<span data-ttu-id="b49a6-172">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b49a6-172">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="b49a6-173">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b49a6-173">Remove-AzDataFactoryV2</span></span>]()
