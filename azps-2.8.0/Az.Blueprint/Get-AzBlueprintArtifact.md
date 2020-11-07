---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: 94a0ff1d4e16748b769f51303fb397da7e029026
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652350"
---
# <span data-ttu-id="c739d-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="c739d-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="c739d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c739d-102">SYNOPSIS</span></span>
<span data-ttu-id="c739d-103">Abrufen von Artefakten aus einer Blueprint-Definition</span><span class="sxs-lookup"><span data-stu-id="c739d-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="c739d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c739d-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c739d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c739d-105">DESCRIPTION</span></span>
<span data-ttu-id="c739d-106">Abrufen von Artefakten aus einer Blueprint-Definition</span><span class="sxs-lookup"><span data-stu-id="c739d-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="c739d-107">Wenn keine Blueprint-Definitionsversion angegeben ist, wird die Entwurfsversion abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c739d-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="c739d-108">In dem Fall, in dem es keine Entwurfsversion gibt, wird die neueste veröffentlichte Blueprint-Definition zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c739d-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="c739d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c739d-109">EXAMPLES</span></span>

### <span data-ttu-id="c739d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c739d-110">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Get-AzBlueprintArtifact -Blueprint $bp 

DisplayName        : Audit use of classic virtual machines
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1d84d5fb-01f6-4d12-ba4f-4a26081d403d
Parameters         : {[effect, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : SimpleBlueprintRG
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/3ab44511-0228-4275-9641-7e93e6f34178
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 3ab44511-0228-4275-9641-7e93e6f34178

DisplayName        : Enforce tag and its value
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1e30110a-5ceb-460c-a204-c1c3969c6d62
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/0e1593da-47d5-4b75-800c-9a797dd23192
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 0e1593da-47d5-4b75-800c-9a797dd23192

```

<span data-ttu-id="c739d-111">Abrufen von Artefakten aus einer Blueprint-Definition..</span><span class="sxs-lookup"><span data-stu-id="c739d-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="c739d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c739d-112">PARAMETERS</span></span>

### <span data-ttu-id="c739d-113">-Artefaktdatei</span><span class="sxs-lookup"><span data-stu-id="c739d-113">-ArtifactFile</span></span>
<span data-ttu-id="c739d-114">Der Speicherort der artefaktdatei im JSON-Format auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="c739d-114">Location of the artifact file in JSON format on disk.</span></span>

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

### <span data-ttu-id="c739d-115">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="c739d-115">-Blueprint</span></span>
<span data-ttu-id="c739d-116">Blueprint-Objekt</span><span class="sxs-lookup"><span data-stu-id="c739d-116">Blueprint object.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: ArtifactsByBlueprint, UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
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

### <span data-ttu-id="c739d-117">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="c739d-117">-BlueprintVersion</span></span>
<span data-ttu-id="c739d-118">Die Version des Blueprints, aus der die Artefakte abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c739d-118">Version of the blueprint to get the artifacts from.</span></span>

```yaml
Type: String
Parameter Sets: ArtifactsByBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c739d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c739d-119">-DefaultProfile</span></span>
<span data-ttu-id="c739d-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c739d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c739d-121">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="c739d-121">-DependsOn</span></span>
<span data-ttu-id="c739d-122">Liste der Namen von Artefakten, die erstellt werden müssen, bevor das aktuelle Artefakt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c739d-122">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

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

### <span data-ttu-id="c739d-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c739d-123">-Description</span></span>
<span data-ttu-id="c739d-124">Beschreibung des Artefakts.</span><span class="sxs-lookup"><span data-stu-id="c739d-124">Description of the artifact.</span></span>

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

### <span data-ttu-id="c739d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c739d-125">-Name</span></span>
<span data-ttu-id="c739d-126">Name des Artefakts</span><span class="sxs-lookup"><span data-stu-id="c739d-126">Name of the artifact</span></span>

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

```yaml
Type: String
Parameter Sets: CreateArtifactByInputFile, UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c739d-127">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="c739d-127">-PolicyDefinitionId</span></span>
<span data-ttu-id="c739d-128">Definitions-ID der Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="c739d-128">Definition Id of the policy definition.</span></span>

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

### <span data-ttu-id="c739d-129">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="c739d-129">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="c739d-130">Hashtable mit Parametern, die an das Richtlinien Definitions Artefakt übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c739d-130">Hashtable of parameters to pass to the policy definition artifact.</span></span>

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

### <span data-ttu-id="c739d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c739d-131">-ResourceGroupName</span></span>
<span data-ttu-id="c739d-132">Der Name der Ressourcengruppe, unter der das Artefakt sein wird.</span><span class="sxs-lookup"><span data-stu-id="c739d-132">Name of the resource group the artifact is going to be under.</span></span>

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

### <span data-ttu-id="c739d-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="c739d-133">-RoleDefinitionId</span></span>
<span data-ttu-id="c739d-134">Liste der Rollendefinition</span><span class="sxs-lookup"><span data-stu-id="c739d-134">List of role definition</span></span>

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

### <span data-ttu-id="c739d-135">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="c739d-135">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="c739d-136">Liste der Prinzipal-IDs für Rollendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c739d-136">List of role definition principal ids.</span></span>

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

### <span data-ttu-id="c739d-137">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="c739d-137">-TemplateFile</span></span>
<span data-ttu-id="c739d-138">Der Speicherort der Arm-Vorlagendatei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="c739d-138">Location of the ARM template file on disk.</span></span>

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

### <span data-ttu-id="c739d-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="c739d-139">-TemplateParameterFile</span></span>
<span data-ttu-id="c739d-140">Der Speicherort der Parameterdatei für Arm-Vorlagen auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="c739d-140">Location of the ARM template parameter file on disk.</span></span>

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

### <span data-ttu-id="c739d-141">-Typ</span><span class="sxs-lookup"><span data-stu-id="c739d-141">-Type</span></span>
<span data-ttu-id="c739d-142">Der Typ des Artefakts.</span><span class="sxs-lookup"><span data-stu-id="c739d-142">Type of the artifact.</span></span>
<span data-ttu-id="c739d-143">Es gibt 3 Unterstützte Typen: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="c739d-143">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

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

### <span data-ttu-id="c739d-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c739d-144">-Confirm</span></span>
<span data-ttu-id="c739d-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c739d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c739d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c739d-146">-WhatIf</span></span>
<span data-ttu-id="c739d-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c739d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c739d-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c739d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c739d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c739d-149">CommonParameters</span></span>
<span data-ttu-id="c739d-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c739d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c739d-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c739d-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c739d-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c739d-152">INPUTS</span></span>

### <span data-ttu-id="c739d-153">System. String</span><span class="sxs-lookup"><span data-stu-id="c739d-153">System.String</span></span>

### <span data-ttu-id="c739d-154">Microsoft. Azure. Commands. Blueprint. Models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="c739d-154">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="c739d-155">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="c739d-155">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="c739d-156">System. Collections. Generic. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c739d-156">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="c739d-157">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c739d-157">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c739d-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="c739d-158">System.String[]</span></span>

## <span data-ttu-id="c739d-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c739d-159">OUTPUTS</span></span>

### <span data-ttu-id="c739d-160">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="c739d-160">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="c739d-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="c739d-161">NOTES</span></span>

## <span data-ttu-id="c739d-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c739d-162">RELATED LINKS</span></span>
