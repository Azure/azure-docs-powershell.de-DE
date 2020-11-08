---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: 7187994ca1e6e6ba9da3980be2e75b7b4ad1a877
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176298"
---
# <span data-ttu-id="858d8-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="858d8-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="858d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="858d8-102">SYNOPSIS</span></span>
<span data-ttu-id="858d8-103">Aktualisieren eines Artefakts in einer Blueprint-Definition</span><span class="sxs-lookup"><span data-stu-id="858d8-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="858d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="858d8-104">SYNTAX</span></span>

### <span data-ttu-id="858d8-105">UpdateTemplateArtifact (Standard)</span><span class="sxs-lookup"><span data-stu-id="858d8-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="858d8-106">UpdateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="858d8-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="858d8-107">UpdateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="858d8-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="858d8-108">UpdatePolicyAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="858d8-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="858d8-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="858d8-109">DESCRIPTION</span></span>
<span data-ttu-id="858d8-110">Aktualisieren eines Artefakts</span><span class="sxs-lookup"><span data-stu-id="858d8-110">Update an artifact.</span></span> <span data-ttu-id="858d8-111">Es gibt zwei Möglichkeiten zum Aktualisieren eines Artefakts: entweder über ein Artefakt JSON als Eingabedatei oder über die Bereitstellung von Inline Parametern für das Artefakt.</span><span class="sxs-lookup"><span data-stu-id="858d8-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="858d8-112">Während die JSON-Methode den Typ des zu bereitzustellenden Artefakts nicht erfordert, erfordert die Inline Parameter-Methode, dass der Benutzer den Typ des durch-type-Parameters des Artefakts bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="858d8-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="858d8-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="858d8-113">EXAMPLES</span></span>

### <span data-ttu-id="858d8-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="858d8-114">Example 1</span></span>
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

<span data-ttu-id="858d8-115">Aktualisieren Sie ein Artefakt über eine JSON-artefaktdatei.</span><span class="sxs-lookup"><span data-stu-id="858d8-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="858d8-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="858d8-116">Example 2</span></span>
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

<span data-ttu-id="858d8-117">Aktualisieren eines Artefakts über Inline Parameter</span><span class="sxs-lookup"><span data-stu-id="858d8-117">Update an artifact through inline parameters.</span></span>

### <span data-ttu-id="858d8-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="858d8-118">Example 3</span></span>
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

<span data-ttu-id="858d8-119">Aktualisieren Sie ein Artefakt über eine Arm-Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="858d8-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="858d8-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="858d8-120">PARAMETERS</span></span>

### <span data-ttu-id="858d8-121">-Artefaktdatei</span><span class="sxs-lookup"><span data-stu-id="858d8-121">-ArtifactFile</span></span>
<span data-ttu-id="858d8-122">Der Speicherort der artefaktdatei im JSON-Format auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="858d8-122">Location of the artifact file in JSON format on disk.</span></span>

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

### <span data-ttu-id="858d8-123">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="858d8-123">-Blueprint</span></span>
<span data-ttu-id="858d8-124">Blueprint-Objekt</span><span class="sxs-lookup"><span data-stu-id="858d8-124">Blueprint object.</span></span>

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

### <span data-ttu-id="858d8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="858d8-125">-DefaultProfile</span></span>
<span data-ttu-id="858d8-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="858d8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="858d8-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="858d8-127">-DependsOn</span></span>
<span data-ttu-id="858d8-128">Liste der Namen von Artefakten, die erstellt werden müssen, bevor das aktuelle Artefakt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="858d8-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

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

### <span data-ttu-id="858d8-129">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="858d8-129">-Description</span></span>
<span data-ttu-id="858d8-130">Beschreibung des Artefakts.</span><span class="sxs-lookup"><span data-stu-id="858d8-130">Description of the artifact.</span></span>

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

### <span data-ttu-id="858d8-131">-Name</span><span class="sxs-lookup"><span data-stu-id="858d8-131">-Name</span></span>
<span data-ttu-id="858d8-132">Name des Artefakts</span><span class="sxs-lookup"><span data-stu-id="858d8-132">Name of the artifact</span></span>

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

### <span data-ttu-id="858d8-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="858d8-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="858d8-134">Definitions-ID der Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="858d8-134">Definition Id of the policy definition.</span></span>

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

### <span data-ttu-id="858d8-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="858d8-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="858d8-136">Hashtable mit Parametern, die an das Richtlinien Definitions Artefakt übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="858d8-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

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

### <span data-ttu-id="858d8-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="858d8-137">-ResourceGroupName</span></span>
<span data-ttu-id="858d8-138">Der Name der Ressourcengruppe, unter der das Artefakt sein wird.</span><span class="sxs-lookup"><span data-stu-id="858d8-138">Name of the resource group the artifact is going to be under.</span></span>

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

### <span data-ttu-id="858d8-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="858d8-139">-RoleDefinitionId</span></span>
<span data-ttu-id="858d8-140">Liste der Rollendefinition</span><span class="sxs-lookup"><span data-stu-id="858d8-140">List of role definition</span></span>

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

### <span data-ttu-id="858d8-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="858d8-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="858d8-142">Liste der Prinzipal-IDs für Rollendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="858d8-142">List of role definition principal ids.</span></span>

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

### <span data-ttu-id="858d8-143">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="858d8-143">-TemplateFile</span></span>
<span data-ttu-id="858d8-144">Der Speicherort der Arm-Vorlagendatei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="858d8-144">Location of the ARM template file on disk.</span></span>

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

### <span data-ttu-id="858d8-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="858d8-145">-TemplateParameterFile</span></span>
<span data-ttu-id="858d8-146">Der Speicherort der Parameterdatei für Arm-Vorlagen auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="858d8-146">Location of the ARM template parameter file on disk.</span></span>

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

### <span data-ttu-id="858d8-147">-Typ</span><span class="sxs-lookup"><span data-stu-id="858d8-147">-Type</span></span>
<span data-ttu-id="858d8-148">Der Typ des Artefakts.</span><span class="sxs-lookup"><span data-stu-id="858d8-148">Type of the artifact.</span></span>
<span data-ttu-id="858d8-149">Es gibt 3 Unterstützte Typen: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="858d8-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

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

### <span data-ttu-id="858d8-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="858d8-150">-Confirm</span></span>
<span data-ttu-id="858d8-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="858d8-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="858d8-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="858d8-152">-WhatIf</span></span>
<span data-ttu-id="858d8-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="858d8-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="858d8-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="858d8-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="858d8-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="858d8-155">CommonParameters</span></span>
<span data-ttu-id="858d8-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="858d8-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="858d8-157">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="858d8-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="858d8-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="858d8-158">INPUTS</span></span>

### <span data-ttu-id="858d8-159">System. String</span><span class="sxs-lookup"><span data-stu-id="858d8-159">System.String</span></span>

### <span data-ttu-id="858d8-160">Microsoft. Azure. Commands. Blueprint. Models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="858d8-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="858d8-161">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="858d8-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="858d8-162">System. Collections. Generic. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="858d8-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="858d8-163">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="858d8-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="858d8-164">System. String []</span><span class="sxs-lookup"><span data-stu-id="858d8-164">System.String[]</span></span>

## <span data-ttu-id="858d8-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="858d8-165">OUTPUTS</span></span>

### <span data-ttu-id="858d8-166">Microsoft. Azure. Management. Blueprint. Models. Artefakt</span><span class="sxs-lookup"><span data-stu-id="858d8-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="858d8-167">Notizen</span><span class="sxs-lookup"><span data-stu-id="858d8-167">NOTES</span></span>

## <span data-ttu-id="858d8-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="858d8-168">RELATED LINKS</span></span>
