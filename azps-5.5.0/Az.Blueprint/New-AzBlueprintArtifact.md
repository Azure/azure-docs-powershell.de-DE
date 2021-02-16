---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
ms.openlocfilehash: 7a6910e18b966c49ee6c766f06fddc88f903914f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168140"
---
# <span data-ttu-id="95e3d-101">New-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="95e3d-101">New-AzBlueprintArtifact</span></span>

## <span data-ttu-id="95e3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95e3d-102">SYNOPSIS</span></span>
<span data-ttu-id="95e3d-103">Erstellen Sie ein neues Artefakt, und speichern Sie es in einer Blaupausendefinition.</span><span class="sxs-lookup"><span data-stu-id="95e3d-103">Create a new artifact and save it within a blueprint definition.</span></span>

## <span data-ttu-id="95e3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95e3d-104">SYNTAX</span></span>

### <span data-ttu-id="95e3d-105">CreateTemplateArtifact (Standard)</span><span class="sxs-lookup"><span data-stu-id="95e3d-105">CreateTemplateArtifact (Default)</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95e3d-106">CreateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="95e3d-106">CreateArtifactByInputFile</span></span>
```
New-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95e3d-107">CreateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="95e3d-107">CreateRoleAssignmentArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95e3d-108">CreatePolicyArtifact</span><span class="sxs-lookup"><span data-stu-id="95e3d-108">CreatePolicyArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95e3d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95e3d-109">DESCRIPTION</span></span>
<span data-ttu-id="95e3d-110">Erstellen Sie ein neues Artefakt.</span><span class="sxs-lookup"><span data-stu-id="95e3d-110">Create a new artifact.</span></span> <span data-ttu-id="95e3d-111">Es gibt zwei Möglichkeiten zum Erstellen eines Artefakts: entweder über ein Artefakt-JSON als Eingabedatei oder durch Bereitstellen von Inlineparametern für das Artefakt.</span><span class="sxs-lookup"><span data-stu-id="95e3d-111">There are two ways to create an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="95e3d-112">Während für die JSON-Methode kein Typ des Artefakts erforderlich ist, um inlineparametermethode bereitgestellt zu werden, muss der Benutzer den Typ des Artefakts über den Parameter "-Type" bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="95e3d-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="95e3d-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="95e3d-113">EXAMPLES</span></span>

### <span data-ttu-id="95e3d-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="95e3d-114">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Name PolicyStorage -Blueprint $bp -ArtifactFile C:\PolicyAssignmentStorageTag.json

DisplayName        :
Description        : Apply storage tag and the parameter also used by the template to resource groups
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/AppNetwork/artifacts/PolicyAssignmentStorageTag
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : PolicyAssignmentStorageTag
```

<span data-ttu-id="95e3d-115">Erstellen Sie ein neues Artefakt mithilfe einer Artefakt-JSON-Datei.</span><span class="sxs-lookup"><span data-stu-id="95e3d-115">Create a new artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="95e3d-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="95e3d-116">Example 2</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Type PolicyAssignmentArtifact -Name "ApplyTag-RG" -Blueprint $bp -PolicyDefinitionId "/providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71" -PolicyDefinitionParameter @{tagName="[parameters('tagName')]"; tagValue="[parameters('tagValue')]"} -ResourceGroupName storageRG

DisplayName        : ApplyTag-RG
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71
Parameters         : {[tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagName,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : storageRG
Id                 : /subscriptions/28cbf98f-381d-4425-9ac4-cf342dab9753/providers/Microsoft.Blueprint/blueprints/AppNetwork/
                     artifacts/ApplyTag-RG
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : ApplyTag-RG
```

<span data-ttu-id="95e3d-117">Erstellen Sie ein neues Artefakt mithilfe von Inlineparametern.</span><span class="sxs-lookup"><span data-stu-id="95e3d-117">Create a new artifact through inline parameters.</span></span>

### <span data-ttu-id="95e3d-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="95e3d-118">Example 3</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Type TemplateArtifact -Name storage-account -Blueprint $bp -TemplateFile C:\StorageAccountArmTemplate.json -ResourceGroup "storageRG" -TemplateParameterFile C:\Workspace\BlueprintTemplates\RestTemplatesSomeInline\StorageAccountParameters.json

DisplayName   : storage-account
Description   :
DependsOn     :
Template      : {$schema, contentVersion, parameters, variables...}
Parameters    : {}
ResourceGroup : storageRG
Id            : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/AppNetwork/artifacts/storage-account
Type          : Microsoft.Blueprint/blueprints/artifacts
Name          : storage-account
```

<span data-ttu-id="95e3d-119">Erstellen Sie ein neues Artefakt mithilfe einer ARM Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="95e3d-119">Create a new artifact through an ARM template file.</span></span>

## <span data-ttu-id="95e3d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95e3d-120">PARAMETERS</span></span>

### <span data-ttu-id="95e3d-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="95e3d-121">-ArtifactFile</span></span>
<span data-ttu-id="95e3d-122">Speicherort der Artefaktdatei im JSON-Format auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="95e3d-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95e3d-123">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="95e3d-123">-Blueprint</span></span>
<span data-ttu-id="95e3d-124">"Blueprint"-Objekt.</span><span class="sxs-lookup"><span data-stu-id="95e3d-124">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95e3d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95e3d-125">-DefaultProfile</span></span>
<span data-ttu-id="95e3d-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95e3d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95e3d-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="95e3d-127">-DependsOn</span></span>
<span data-ttu-id="95e3d-128">Liste der Namen von Artefakten, die erstellt werden müssen, bevor das aktuelle Artefakt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="95e3d-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95e3d-129">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95e3d-129">-Description</span></span>
<span data-ttu-id="95e3d-130">Beschreibung des Artefakts.</span><span class="sxs-lookup"><span data-stu-id="95e3d-130">Description of the artifact.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95e3d-131">-Name</span><span class="sxs-lookup"><span data-stu-id="95e3d-131">-Name</span></span>
<span data-ttu-id="95e3d-132">Name des Artefakts</span><span class="sxs-lookup"><span data-stu-id="95e3d-132">Name of the artifact</span></span>

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

### <span data-ttu-id="95e3d-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="95e3d-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="95e3d-134">Definitions-ID der Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="95e3d-134">Definition Id of the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95e3d-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="95e3d-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="95e3d-136">Hashtable der Parameter, die an das Richtliniendefinitionsartefakt übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="95e3d-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95e3d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95e3d-137">-ResourceGroupName</span></span>
<span data-ttu-id="95e3d-138">Der Name der Ressourcengruppe, unter der sich das Artefakt befindet.</span><span class="sxs-lookup"><span data-stu-id="95e3d-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95e3d-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="95e3d-139">-RoleDefinitionId</span></span>
<span data-ttu-id="95e3d-140">Liste der Rollendefinition</span><span class="sxs-lookup"><span data-stu-id="95e3d-140">List of role definition</span></span>

```yaml
Type: System.String
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95e3d-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="95e3d-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="95e3d-142">Liste der Prinzipal-IDs für Rollendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="95e3d-142">List of role definition principal ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95e3d-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="95e3d-143">-TemplateFile</span></span>
<span data-ttu-id="95e3d-144">Speicherort der ARM Vorlagendatei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="95e3d-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95e3d-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="95e3d-145">-TemplateParameterFile</span></span>
<span data-ttu-id="95e3d-146">Speicherort der ARM Vorlagenparameterdatei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="95e3d-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95e3d-147">-Type</span><span class="sxs-lookup"><span data-stu-id="95e3d-147">-Type</span></span>
<span data-ttu-id="95e3d-148">Typ des Artefakts.</span><span class="sxs-lookup"><span data-stu-id="95e3d-148">Type of the artifact.</span></span>
<span data-ttu-id="95e3d-149">Es werden drei Typen unterstützt: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="95e3d-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95e3d-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95e3d-150">-Confirm</span></span>
<span data-ttu-id="95e3d-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="95e3d-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95e3d-152">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="95e3d-152">-WhatIf</span></span>
<span data-ttu-id="95e3d-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95e3d-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95e3d-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95e3d-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95e3d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95e3d-155">CommonParameters</span></span>
<span data-ttu-id="95e3d-156">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95e3d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95e3d-157">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95e3d-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95e3d-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="95e3d-158">INPUTS</span></span>

### <span data-ttu-id="95e3d-159">System.String</span><span class="sxs-lookup"><span data-stu-id="95e3d-159">System.String</span></span>

### <span data-ttu-id="95e3d-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="95e3d-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="95e3d-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="95e3d-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="95e3d-162">System.Collections.Generic.List'1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="95e3d-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="95e3d-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="95e3d-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="95e3d-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="95e3d-164">System.String[]</span></span>

## <span data-ttu-id="95e3d-165">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="95e3d-165">OUTPUTS</span></span>

### <span data-ttu-id="95e3d-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span><span class="sxs-lookup"><span data-stu-id="95e3d-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="95e3d-167">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="95e3d-167">NOTES</span></span>

## <span data-ttu-id="95e3d-168">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="95e3d-168">RELATED LINKS</span></span>
