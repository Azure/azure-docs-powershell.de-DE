---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: 6bd05fc372afc6ef04c943906de8b3eb99cc0aa5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652332"
---
# <span data-ttu-id="7ae64-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="7ae64-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="7ae64-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ae64-102">SYNOPSIS</span></span>
<span data-ttu-id="7ae64-103">Aktualisieren eines Artefakts in einer Blueprint-Definition</span><span class="sxs-lookup"><span data-stu-id="7ae64-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="7ae64-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ae64-104">SYNTAX</span></span>


### <span data-ttu-id="7ae64-105">UpdateTemplateArtifact (Standard)</span><span class="sxs-lookup"><span data-stu-id="7ae64-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ae64-106">UpdateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="7ae64-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ae64-107">UpdateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="7ae64-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ae64-108">UpdatePolicyAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="7ae64-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ae64-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ae64-109">DESCRIPTION</span></span>
<span data-ttu-id="7ae64-110">Aktualisieren eines Artefakts</span><span class="sxs-lookup"><span data-stu-id="7ae64-110">Update an artifact.</span></span> <span data-ttu-id="7ae64-111">Es gibt zwei Möglichkeiten zum Aktualisieren eines Artefakts: entweder über ein Artefakt JSON als Eingabedatei oder über die Bereitstellung von Inline Parametern für das Artefakt.</span><span class="sxs-lookup"><span data-stu-id="7ae64-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="7ae64-112">Während die JSON-Methode den Typ des zu bereitzustellenden Artefakts nicht erfordert, erfordert die Inline Parameter-Methode, dass der Benutzer den Typ des durch-type-Parameters des Artefakts bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="7ae64-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="7ae64-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ae64-113">EXAMPLES</span></span>

### <span data-ttu-id="7ae64-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7ae64-114">Example 1</span></span>
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

<span data-ttu-id="7ae64-115">Aktualisieren Sie ein Artefakt über eine JSON-artefaktdatei.</span><span class="sxs-lookup"><span data-stu-id="7ae64-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="7ae64-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7ae64-116">Example 2</span></span>
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

<span data-ttu-id="7ae64-117">Aktualisieren eines Artefakts über Inline Parameter</span><span class="sxs-lookup"><span data-stu-id="7ae64-117">Update an artifact through inline parameters.</span></span>


### <span data-ttu-id="7ae64-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="7ae64-118">Example 3</span></span>
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

<span data-ttu-id="7ae64-119">Aktualisieren Sie ein Artefakt über eine Arm-Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="7ae64-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="7ae64-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ae64-120">PARAMETERS</span></span>

### <span data-ttu-id="7ae64-121">-Artefaktdatei</span><span class="sxs-lookup"><span data-stu-id="7ae64-121">-ArtifactFile</span></span>
<span data-ttu-id="7ae64-122">Der Speicherort der artefaktdatei im JSON-Format auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="7ae64-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae64-123">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="7ae64-123">-Blueprint</span></span>
<span data-ttu-id="7ae64-124">Blueprint-Objekt</span><span class="sxs-lookup"><span data-stu-id="7ae64-124">Blueprint object.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: UpdateTemplateArtifact, ArtifactsByBlueprint, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSBlueprintBase
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae64-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ae64-125">-DefaultProfile</span></span>
<span data-ttu-id="7ae64-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7ae64-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae64-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="7ae64-127">-DependsOn</span></span>
<span data-ttu-id="7ae64-128">Liste der Namen von Artefakten, die erstellt werden müssen, bevor das aktuelle Artefakt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7ae64-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae64-129">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ae64-129">-Description</span></span>
<span data-ttu-id="7ae64-130">Beschreibung des Artefakts.</span><span class="sxs-lookup"><span data-stu-id="7ae64-130">Description of the artifact.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae64-131">-Name</span><span class="sxs-lookup"><span data-stu-id="7ae64-131">-Name</span></span>
<span data-ttu-id="7ae64-132">Name des Artefakts</span><span class="sxs-lookup"><span data-stu-id="7ae64-132">Name of the artifact</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateArtifactByInputFile, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ArtifactsByBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae64-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="7ae64-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="7ae64-134">Definitions-ID der Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="7ae64-134">Definition Id of the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae64-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="7ae64-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="7ae64-136">Hashtable mit Parametern, die an das Richtlinien Definitions Artefakt übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7ae64-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae64-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ae64-137">-ResourceGroupName</span></span>
<span data-ttu-id="7ae64-138">Der Name der Ressourcengruppe, unter der das Artefakt sein wird.</span><span class="sxs-lookup"><span data-stu-id="7ae64-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae64-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="7ae64-139">-RoleDefinitionId</span></span>
<span data-ttu-id="7ae64-140">Liste der Rollendefinition</span><span class="sxs-lookup"><span data-stu-id="7ae64-140">List of role definition</span></span>

```yaml
Type: String
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae64-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="7ae64-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="7ae64-142">Liste der Prinzipal-IDs für Rollendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7ae64-142">List of role definition principal ids.</span></span>

```yaml
Type: String[]
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae64-143">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="7ae64-143">-TemplateFile</span></span>
<span data-ttu-id="7ae64-144">Der Speicherort der Arm-Vorlagendatei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="7ae64-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae64-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="7ae64-145">-TemplateParameterFile</span></span>
<span data-ttu-id="7ae64-146">Der Speicherort der Parameterdatei für Arm-Vorlagen auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="7ae64-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae64-147">-Typ</span><span class="sxs-lookup"><span data-stu-id="7ae64-147">-Type</span></span>
<span data-ttu-id="7ae64-148">Der Typ des Artefakts.</span><span class="sxs-lookup"><span data-stu-id="7ae64-148">Type of the artifact.</span></span>
<span data-ttu-id="7ae64-149">Es gibt 3 Unterstützte Typen: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="7ae64-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: PSArtifactKind
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae64-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ae64-150">CommonParameters</span></span>
<span data-ttu-id="7ae64-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ae64-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7ae64-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ae64-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ae64-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ae64-153">INPUTS</span></span>

### <span data-ttu-id="7ae64-154">System. String</span><span class="sxs-lookup"><span data-stu-id="7ae64-154">System.String</span></span>

### <span data-ttu-id="7ae64-155">Microsoft. Azure. Commands. Blueprint. Models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="7ae64-155">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="7ae64-156">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="7ae64-156">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="7ae64-157">System. Collections. Generic. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7ae64-157">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7ae64-158">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7ae64-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7ae64-159">System. String []</span><span class="sxs-lookup"><span data-stu-id="7ae64-159">System.String[]</span></span>

## <span data-ttu-id="7ae64-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ae64-160">OUTPUTS</span></span>

### <span data-ttu-id="7ae64-161">Microsoft. Azure. Management. Blueprint. Models. Artefakt</span><span class="sxs-lookup"><span data-stu-id="7ae64-161">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="7ae64-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ae64-162">NOTES</span></span>

## <span data-ttu-id="7ae64-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ae64-163">RELATED LINKS</span></span>
