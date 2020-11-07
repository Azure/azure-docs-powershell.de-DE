---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: d8541285cb8cef0565a06715910ff5b8cc8cc392
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845156"
---
# <span data-ttu-id="1b4ba-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="1b4ba-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="1b4ba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1b4ba-102">SYNOPSIS</span></span>
<span data-ttu-id="1b4ba-103">Abrufen von Artefakten aus einer Blueprint-Definition</span><span class="sxs-lookup"><span data-stu-id="1b4ba-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="1b4ba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b4ba-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b4ba-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b4ba-105">DESCRIPTION</span></span>
<span data-ttu-id="1b4ba-106">Abrufen von Artefakten aus einer Blueprint-Definition</span><span class="sxs-lookup"><span data-stu-id="1b4ba-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="1b4ba-107">Wenn keine Blueprint-Definitionsversion angegeben ist, wird die Entwurfsversion abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1b4ba-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="1b4ba-108">In dem Fall, in dem es keine Entwurfsversion gibt, wird die neueste veröffentlichte Blueprint-Definition zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1b4ba-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="1b4ba-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1b4ba-109">EXAMPLES</span></span>

### <span data-ttu-id="1b4ba-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1b4ba-110">Example 1</span></span>
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

<span data-ttu-id="1b4ba-111">Abrufen von Artefakten aus einer Blueprint-Definition..</span><span class="sxs-lookup"><span data-stu-id="1b4ba-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="1b4ba-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b4ba-112">PARAMETERS</span></span>

### <span data-ttu-id="1b4ba-113">-Artefaktdatei</span><span class="sxs-lookup"><span data-stu-id="1b4ba-113">-ArtifactFile</span></span>
<span data-ttu-id="1b4ba-114">Der Speicherort der artefaktdatei im JSON-Format auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="1b4ba-114">Location of the artifact file in JSON format on disk.</span></span>

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

### <span data-ttu-id="1b4ba-115">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="1b4ba-115">-Blueprint</span></span>
<span data-ttu-id="1b4ba-116">Blueprint-Objekt</span><span class="sxs-lookup"><span data-stu-id="1b4ba-116">Blueprint object.</span></span>

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

### <span data-ttu-id="1b4ba-117">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="1b4ba-117">-BlueprintVersion</span></span>
<span data-ttu-id="1b4ba-118">Die Version des Blueprints, aus der die Artefakte abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1b4ba-118">Version of the blueprint to get the artifacts from.</span></span>

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

### <span data-ttu-id="1b4ba-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b4ba-119">-DefaultProfile</span></span>
<span data-ttu-id="1b4ba-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1b4ba-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b4ba-121">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="1b4ba-121">-DependsOn</span></span>
<span data-ttu-id="1b4ba-122">Liste der Namen von Artefakten, die erstellt werden müssen, bevor das aktuelle Artefakt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1b4ba-122">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

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

### <span data-ttu-id="1b4ba-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b4ba-123">-Description</span></span>
<span data-ttu-id="1b4ba-124">Beschreibung des Artefakts.</span><span class="sxs-lookup"><span data-stu-id="1b4ba-124">Description of the artifact.</span></span>

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

### <span data-ttu-id="1b4ba-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1b4ba-125">-Name</span></span>
<span data-ttu-id="1b4ba-126">Name des Artefakts</span><span class="sxs-lookup"><span data-stu-id="1b4ba-126">Name of the artifact</span></span>

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

### <span data-ttu-id="1b4ba-127">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="1b4ba-127">-PolicyDefinitionId</span></span>
<span data-ttu-id="1b4ba-128">Definitions-ID der Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="1b4ba-128">Definition Id of the policy definition.</span></span>

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

### <span data-ttu-id="1b4ba-129">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="1b4ba-129">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="1b4ba-130">Hashtable mit Parametern, die an das Richtlinien Definitions Artefakt übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1b4ba-130">Hashtable of parameters to pass to the policy definition artifact.</span></span>

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

### <span data-ttu-id="1b4ba-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b4ba-131">-ResourceGroupName</span></span>
<span data-ttu-id="1b4ba-132">Der Name der Ressourcengruppe, unter der das Artefakt sein wird.</span><span class="sxs-lookup"><span data-stu-id="1b4ba-132">Name of the resource group the artifact is going to be under.</span></span>

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

### <span data-ttu-id="1b4ba-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="1b4ba-133">-RoleDefinitionId</span></span>
<span data-ttu-id="1b4ba-134">Liste der Rollendefinition</span><span class="sxs-lookup"><span data-stu-id="1b4ba-134">List of role definition</span></span>

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

### <span data-ttu-id="1b4ba-135">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="1b4ba-135">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="1b4ba-136">Liste der Prinzipal-IDs für Rollendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1b4ba-136">List of role definition principal ids.</span></span>

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

### <span data-ttu-id="1b4ba-137">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="1b4ba-137">-TemplateFile</span></span>
<span data-ttu-id="1b4ba-138">Der Speicherort der Arm-Vorlagendatei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="1b4ba-138">Location of the ARM template file on disk.</span></span>

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

### <span data-ttu-id="1b4ba-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="1b4ba-139">-TemplateParameterFile</span></span>
<span data-ttu-id="1b4ba-140">Der Speicherort der Parameterdatei für Arm-Vorlagen auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="1b4ba-140">Location of the ARM template parameter file on disk.</span></span>

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

### <span data-ttu-id="1b4ba-141">-Typ</span><span class="sxs-lookup"><span data-stu-id="1b4ba-141">-Type</span></span>
<span data-ttu-id="1b4ba-142">Der Typ des Artefakts.</span><span class="sxs-lookup"><span data-stu-id="1b4ba-142">Type of the artifact.</span></span>
<span data-ttu-id="1b4ba-143">Es gibt 3 Unterstützte Typen: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="1b4ba-143">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

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

### <span data-ttu-id="1b4ba-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1b4ba-144">-Confirm</span></span>
<span data-ttu-id="1b4ba-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1b4ba-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b4ba-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b4ba-146">-WhatIf</span></span>
<span data-ttu-id="1b4ba-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b4ba-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b4ba-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b4ba-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b4ba-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b4ba-149">CommonParameters</span></span>
<span data-ttu-id="1b4ba-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b4ba-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1b4ba-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b4ba-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b4ba-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1b4ba-152">INPUTS</span></span>

### <span data-ttu-id="1b4ba-153">System. String</span><span class="sxs-lookup"><span data-stu-id="1b4ba-153">System.String</span></span>

### <span data-ttu-id="1b4ba-154">Microsoft. Azure. Commands. Blueprint. Models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="1b4ba-154">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="1b4ba-155">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="1b4ba-155">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="1b4ba-156">System. Collections. Generic. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1b4ba-156">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="1b4ba-157">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1b4ba-157">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1b4ba-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="1b4ba-158">System.String[]</span></span>

## <span data-ttu-id="1b4ba-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1b4ba-159">OUTPUTS</span></span>

### <span data-ttu-id="1b4ba-160">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="1b4ba-160">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="1b4ba-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="1b4ba-161">NOTES</span></span>

## <span data-ttu-id="1b4ba-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1b4ba-162">RELATED LINKS</span></span>
