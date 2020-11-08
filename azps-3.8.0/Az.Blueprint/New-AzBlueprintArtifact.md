---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
ms.openlocfilehash: 5ee859811ce791f57fc8c4fa08d2584b28bef1dc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995698"
---
# <span data-ttu-id="1623f-101">New-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="1623f-101">New-AzBlueprintArtifact</span></span>

## <span data-ttu-id="1623f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1623f-102">SYNOPSIS</span></span>
<span data-ttu-id="1623f-103">Erstellen Sie ein neues Artefakt, und speichern Sie es in einer Blueprint-Definition.</span><span class="sxs-lookup"><span data-stu-id="1623f-103">Create a new artifact and save it within a blueprint definition.</span></span>

## <span data-ttu-id="1623f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1623f-104">SYNTAX</span></span>

### <span data-ttu-id="1623f-105">CreateTemplateArtifact (Standard)</span><span class="sxs-lookup"><span data-stu-id="1623f-105">CreateTemplateArtifact (Default)</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1623f-106">CreateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="1623f-106">CreateArtifactByInputFile</span></span>
```
New-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1623f-107">CreateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="1623f-107">CreateRoleAssignmentArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1623f-108">CreatePolicyArtifact</span><span class="sxs-lookup"><span data-stu-id="1623f-108">CreatePolicyArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1623f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1623f-109">DESCRIPTION</span></span>
<span data-ttu-id="1623f-110">Erstellen Sie ein neues Artefakt.</span><span class="sxs-lookup"><span data-stu-id="1623f-110">Create a new artifact.</span></span> <span data-ttu-id="1623f-111">Es gibt zwei Möglichkeiten zum Erstellen eines Artefakts: entweder über ein Artefakt JSON als Eingabedatei oder durch die Bereitstellung von Inline Parametern für das Artefakt.</span><span class="sxs-lookup"><span data-stu-id="1623f-111">There are two ways to create an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="1623f-112">Während die JSON-Methode den Typ des zu bereitzustellenden Artefakts nicht erfordert, erfordert die Inline Parameter-Methode, dass der Benutzer den Typ des durch-type-Parameters des Artefakts bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="1623f-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="1623f-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1623f-113">EXAMPLES</span></span>

### <span data-ttu-id="1623f-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1623f-114">Example 1</span></span>
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

<span data-ttu-id="1623f-115">Erstellen Sie ein neues Artefakt über eine JSON-artefaktdatei.</span><span class="sxs-lookup"><span data-stu-id="1623f-115">Create a new artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="1623f-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1623f-116">Example 2</span></span>
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

<span data-ttu-id="1623f-117">Erstellen Sie ein neues Artefakt über Inline Parameter.</span><span class="sxs-lookup"><span data-stu-id="1623f-117">Create a new artifact through inline parameters.</span></span>


### <span data-ttu-id="1623f-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="1623f-118">Example 3</span></span>
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

<span data-ttu-id="1623f-119">Erstellen Sie ein neues Artefakt über eine Arm-Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="1623f-119">Create a new artifact through an ARM template file.</span></span>

## <span data-ttu-id="1623f-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="1623f-120">PARAMETERS</span></span>

### <span data-ttu-id="1623f-121">-Artefaktdatei</span><span class="sxs-lookup"><span data-stu-id="1623f-121">-ArtifactFile</span></span>
<span data-ttu-id="1623f-122">Der Speicherort der artefaktdatei im JSON-Format auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="1623f-122">Location of the artifact file in JSON format on disk.</span></span>

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

### <span data-ttu-id="1623f-123">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="1623f-123">-Blueprint</span></span>
<span data-ttu-id="1623f-124">Blueprint-Objekt</span><span class="sxs-lookup"><span data-stu-id="1623f-124">Blueprint object.</span></span>

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

### <span data-ttu-id="1623f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1623f-125">-DefaultProfile</span></span>
<span data-ttu-id="1623f-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1623f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1623f-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="1623f-127">-DependsOn</span></span>
<span data-ttu-id="1623f-128">Liste der Namen von Artefakten, die erstellt werden müssen, bevor das aktuelle Artefakt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1623f-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

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

### <span data-ttu-id="1623f-129">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1623f-129">-Description</span></span>
<span data-ttu-id="1623f-130">Beschreibung des Artefakts.</span><span class="sxs-lookup"><span data-stu-id="1623f-130">Description of the artifact.</span></span>

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

### <span data-ttu-id="1623f-131">-Name</span><span class="sxs-lookup"><span data-stu-id="1623f-131">-Name</span></span>
<span data-ttu-id="1623f-132">Name des Artefakts</span><span class="sxs-lookup"><span data-stu-id="1623f-132">Name of the artifact</span></span>

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

### <span data-ttu-id="1623f-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="1623f-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="1623f-134">Definitions-ID der Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="1623f-134">Definition Id of the policy definition.</span></span>

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

### <span data-ttu-id="1623f-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="1623f-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="1623f-136">Hashtable mit Parametern, die an das Richtlinien Definitions Artefakt übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1623f-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

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

### <span data-ttu-id="1623f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1623f-137">-ResourceGroupName</span></span>
<span data-ttu-id="1623f-138">Der Name der Ressourcengruppe, unter der das Artefakt sein wird.</span><span class="sxs-lookup"><span data-stu-id="1623f-138">Name of the resource group the artifact is going to be under.</span></span>

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

### <span data-ttu-id="1623f-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="1623f-139">-RoleDefinitionId</span></span>
<span data-ttu-id="1623f-140">Liste der Rollendefinition</span><span class="sxs-lookup"><span data-stu-id="1623f-140">List of role definition</span></span>

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

### <span data-ttu-id="1623f-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="1623f-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="1623f-142">Liste der Prinzipal-IDs für Rollendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1623f-142">List of role definition principal ids.</span></span>

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

### <span data-ttu-id="1623f-143">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="1623f-143">-TemplateFile</span></span>
<span data-ttu-id="1623f-144">Der Speicherort der Arm-Vorlagendatei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="1623f-144">Location of the ARM template file on disk.</span></span>

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

### <span data-ttu-id="1623f-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="1623f-145">-TemplateParameterFile</span></span>
<span data-ttu-id="1623f-146">Der Speicherort der Parameterdatei für Arm-Vorlagen auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="1623f-146">Location of the ARM template parameter file on disk.</span></span>

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

### <span data-ttu-id="1623f-147">-Typ</span><span class="sxs-lookup"><span data-stu-id="1623f-147">-Type</span></span>
<span data-ttu-id="1623f-148">Der Typ des Artefakts.</span><span class="sxs-lookup"><span data-stu-id="1623f-148">Type of the artifact.</span></span>
<span data-ttu-id="1623f-149">Es gibt 3 Unterstützte Typen: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="1623f-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

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

### <span data-ttu-id="1623f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1623f-150">CommonParameters</span></span>
<span data-ttu-id="1623f-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1623f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1623f-152">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1623f-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1623f-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1623f-153">INPUTS</span></span>

### <span data-ttu-id="1623f-154">System. String</span><span class="sxs-lookup"><span data-stu-id="1623f-154">System.String</span></span>

### <span data-ttu-id="1623f-155">Microsoft. Azure. Commands. Blueprint. Models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="1623f-155">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="1623f-156">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="1623f-156">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="1623f-157">System. Collections. Generic. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1623f-157">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="1623f-158">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1623f-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1623f-159">System. String []</span><span class="sxs-lookup"><span data-stu-id="1623f-159">System.String[]</span></span>

## <span data-ttu-id="1623f-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1623f-160">OUTPUTS</span></span>

### <span data-ttu-id="1623f-161">Microsoft. Azure. Management. Blueprint. Models. Artefakt</span><span class="sxs-lookup"><span data-stu-id="1623f-161">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="1623f-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="1623f-162">NOTES</span></span>

## <span data-ttu-id="1623f-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1623f-163">RELATED LINKS</span></span>
