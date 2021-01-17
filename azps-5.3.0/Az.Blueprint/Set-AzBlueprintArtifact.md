---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: 7187994ca1e6e6ba9da3980be2e75b7b4ad1a877
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471039"
---
# <span data-ttu-id="4152c-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="4152c-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="4152c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4152c-102">SYNOPSIS</span></span>
<span data-ttu-id="4152c-103">Aktualisieren Sie ein Artefakt in einer Entwurfsdefinition.</span><span class="sxs-lookup"><span data-stu-id="4152c-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="4152c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4152c-104">SYNTAX</span></span>

### <span data-ttu-id="4152c-105">UpdateTemplateArtifact (Standard)</span><span class="sxs-lookup"><span data-stu-id="4152c-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4152c-106">UpdateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="4152c-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4152c-107">UpdateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="4152c-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4152c-108">UpdatePolicyAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="4152c-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4152c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4152c-109">DESCRIPTION</span></span>
<span data-ttu-id="4152c-110">Aktualisieren sie ein Artefakt.</span><span class="sxs-lookup"><span data-stu-id="4152c-110">Update an artifact.</span></span> <span data-ttu-id="4152c-111">Es gibt zwei Möglichkeiten zum Aktualisieren eines Artefakts: entweder über ein Artefakt-JSON als Eingabedatei oder durch Bereitstellen von Inlineparametern für das Artefakt.</span><span class="sxs-lookup"><span data-stu-id="4152c-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="4152c-112">Während für die JSON-Methode kein Typ des Artefakts erforderlich ist, um inlineparametermethode bereitgestellt zu werden, muss der Benutzer den Typ des Artefakts über den Parameter "-Type" bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4152c-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="4152c-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4152c-113">EXAMPLES</span></span>

### <span data-ttu-id="4152c-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4152c-114">Example 1</span></span>
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

<span data-ttu-id="4152c-115">Aktualisieren Sie ein Artefakt mithilfe einer Artefakt-JSON-Datei.</span><span class="sxs-lookup"><span data-stu-id="4152c-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="4152c-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4152c-116">Example 2</span></span>
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

<span data-ttu-id="4152c-117">Aktualisieren Sie ein Artefakt mithilfe von Inlineparametern.</span><span class="sxs-lookup"><span data-stu-id="4152c-117">Update an artifact through inline parameters.</span></span>

### <span data-ttu-id="4152c-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4152c-118">Example 3</span></span>
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

<span data-ttu-id="4152c-119">Aktualisieren Sie ein Artefakt mithilfe ARM Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="4152c-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="4152c-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4152c-120">PARAMETERS</span></span>

### <span data-ttu-id="4152c-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="4152c-121">-ArtifactFile</span></span>
<span data-ttu-id="4152c-122">Speicherort der Artefaktdatei im JSON-Format auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="4152c-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4152c-123">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="4152c-123">-Blueprint</span></span>
<span data-ttu-id="4152c-124">"Blueprint"-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4152c-124">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4152c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4152c-125">-DefaultProfile</span></span>
<span data-ttu-id="4152c-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4152c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4152c-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="4152c-127">-DependsOn</span></span>
<span data-ttu-id="4152c-128">Liste der Namen von Artefakten, die erstellt werden müssen, bevor das aktuelle Artefakt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4152c-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4152c-129">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4152c-129">-Description</span></span>
<span data-ttu-id="4152c-130">Beschreibung des Artefakts.</span><span class="sxs-lookup"><span data-stu-id="4152c-130">Description of the artifact.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4152c-131">-Name</span><span class="sxs-lookup"><span data-stu-id="4152c-131">-Name</span></span>
<span data-ttu-id="4152c-132">Name des Artefakts</span><span class="sxs-lookup"><span data-stu-id="4152c-132">Name of the artifact</span></span>

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

### <span data-ttu-id="4152c-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="4152c-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="4152c-134">Definitions-ID der Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="4152c-134">Definition Id of the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4152c-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="4152c-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="4152c-136">Hashtable der Parameter, die an das Richtliniendefinitionsartefakt übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="4152c-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4152c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4152c-137">-ResourceGroupName</span></span>
<span data-ttu-id="4152c-138">Der Name der Ressourcengruppe, unter der sich das Artefakt befindet.</span><span class="sxs-lookup"><span data-stu-id="4152c-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4152c-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="4152c-139">-RoleDefinitionId</span></span>
<span data-ttu-id="4152c-140">Liste der Rollendefinition</span><span class="sxs-lookup"><span data-stu-id="4152c-140">List of role definition</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4152c-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="4152c-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="4152c-142">Liste der Rollendefinitions-Prinzipal-IDs.</span><span class="sxs-lookup"><span data-stu-id="4152c-142">List of role definition principal ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4152c-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="4152c-143">-TemplateFile</span></span>
<span data-ttu-id="4152c-144">Speicherort der ARM Vorlagendatei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="4152c-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4152c-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="4152c-145">-TemplateParameterFile</span></span>
<span data-ttu-id="4152c-146">Speicherort der ARM Vorlagenparameterdatei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="4152c-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4152c-147">-Type</span><span class="sxs-lookup"><span data-stu-id="4152c-147">-Type</span></span>
<span data-ttu-id="4152c-148">Typ des Artefakts.</span><span class="sxs-lookup"><span data-stu-id="4152c-148">Type of the artifact.</span></span>
<span data-ttu-id="4152c-149">Es werden drei Typen unterstützt: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="4152c-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4152c-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4152c-150">-Confirm</span></span>
<span data-ttu-id="4152c-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4152c-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4152c-152">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4152c-152">-WhatIf</span></span>
<span data-ttu-id="4152c-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4152c-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4152c-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4152c-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4152c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4152c-155">CommonParameters</span></span>
<span data-ttu-id="4152c-156">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4152c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4152c-157">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4152c-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4152c-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4152c-158">INPUTS</span></span>

### <span data-ttu-id="4152c-159">System.String</span><span class="sxs-lookup"><span data-stu-id="4152c-159">System.String</span></span>

### <span data-ttu-id="4152c-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="4152c-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="4152c-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="4152c-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="4152c-162">System.Collections.Generic.List'1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4152c-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="4152c-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4152c-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4152c-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4152c-164">System.String[]</span></span>

## <span data-ttu-id="4152c-165">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4152c-165">OUTPUTS</span></span>

### <span data-ttu-id="4152c-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span><span class="sxs-lookup"><span data-stu-id="4152c-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="4152c-167">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4152c-167">NOTES</span></span>

## <span data-ttu-id="4152c-168">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4152c-168">RELATED LINKS</span></span>
