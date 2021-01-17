---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
ms.openlocfilehash: 681cbc620a5c6067102dfe2a67f20dd9edc42046
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459187"
---
# <span data-ttu-id="9e51c-101">Set-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="9e51c-101">Set-AzTemplateSpec</span></span>

## <span data-ttu-id="9e51c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e51c-102">SYNOPSIS</span></span>
<span data-ttu-id="9e51c-103">Ändert eine Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="9e51c-103">Modifies a Template Spec.</span></span>

## <span data-ttu-id="9e51c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e51c-104">SYNTAX</span></span>

### <span data-ttu-id="9e51c-105">FromJsonStringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9e51c-105">FromJsonStringParameterSet (Default)</span></span>
```
Set-AzTemplateSpec [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e51c-106">UpdateByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e51c-106">UpdateByIdParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> [-Description <String>] [-DisplayName <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e51c-107">UpdateVersionByIdFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e51c-107">UpdateVersionByIdFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e51c-108">UpdateVersionByIdFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e51c-108">UpdateVersionByIdFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e51c-109">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e51c-109">UpdateByNameParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e51c-110">UpdateVersionByNameFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e51c-110">UpdateVersionByNameFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e51c-111">UpdateVersionByNameFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e51c-111">UpdateVersionByNameFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e51c-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e51c-112">DESCRIPTION</span></span>
<span data-ttu-id="9e51c-113">Ändert eine Templace-Spezifikation. Wenn die Vorlagenspezifikation mit dem angegebenen Namen und/oder einer bestimmten Version noch nicht vorhanden ist, wird sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="9e51c-113">Modifies a Templace Spec. If the Template Spec with the specified name and/or specific version does not already exist, it will be created.</span></span>

<span data-ttu-id="9e51c-114">Beim Ändern des ARM-Vorlageninhalts einer Vorlagenspezifikation kann der Inhalt entweder aus einer unformatierten JSON-Zeichenfolge (mit dem Parametersatz **"UpdateVersionByNameFromJsonParameterSet")** oder aus einer angegebenen "JSON"-Datei (mit dem Parametersatz **"UpdateVersionByNameFromJsonFileParameterSet")** stammen.</span><span class="sxs-lookup"><span data-stu-id="9e51c-114">When modifying a Template Spec version's ARM Template content, the content can either come from a raw JSON string (using **UpdateVersionByNameFromJsonParameterSet** parameter set) or from a specified JSON file (using **UpdateVersionByNameFromJsonFileParameterSet** parameter set).</span></span>

## <span data-ttu-id="9e51c-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9e51c-115">EXAMPLES</span></span>

### <span data-ttu-id="9e51c-116">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="9e51c-116">Example 1:</span></span>
```powershell
PS C:\> $templateJson = @"
{
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "resources": []
}
"@
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v1.0' -Location 'West US' -TemplateJson $templateJson
```

<span data-ttu-id="9e51c-117">Ändert Version "v1.0" eines Vorlagenspezifikationen namens "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="9e51c-117">Modifies version "v1.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="9e51c-118">Die angegebene Version $templateJson als Der Inhalt der ARM Version angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9e51c-118">The specified version will have $templateJson as the version's ARM Template content.</span></span> <span data-ttu-id="9e51c-119">Wenn die Stammvorlagenspezifikation und/oder -version noch nicht vorhanden ist, werden sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="9e51c-119">If the root Template Spec and/or version do not already exist they will be created.</span></span>


<span data-ttu-id="9e51c-120">**Hinweise:**</span><span class="sxs-lookup"><span data-stu-id="9e51c-120">**Notes:**</span></span> 

* <span data-ttu-id="9e51c-121">Die ARM Beispiel ist ein "No-Op"-Wert, da sie keine tatsächlichen Ressourcen enthält.</span><span class="sxs-lookup"><span data-stu-id="9e51c-121">The ARM Template in the example is a no-op as it contains no actual resources.</span></span>
* <span data-ttu-id="9e51c-122">Speicherort ist nur erforderlich, wenn die Vorlagenspezifikation noch nicht vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="9e51c-122">Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="9e51c-123">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="9e51c-123">Example 2:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="9e51c-124">Ändert Version "v2.0" eines Vorlagenspezifikationen namens "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="9e51c-124">Modifies version "v2.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="9e51c-125">Bei der angegebenen Version wird der Inhalt aus der lokalen Datei "myTemplateContent.js" als Der Inhalt der ARM Version angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9e51c-125">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span> <span data-ttu-id="9e51c-126">Wenn die Stammvorlagenspezifikation und/oder -version noch nicht vorhanden ist, werden sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="9e51c-126">If the root Template Spec and/or version do not already exist they will be created.</span></span>

<span data-ttu-id="9e51c-127">**Hinweis:** Speicherort ist nur erforderlich, wenn die Vorlagenspezifikation noch nicht vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="9e51c-127">**Note:** Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="9e51c-128">Beispiel 3:</span><span class="sxs-lookup"><span data-stu-id="9e51c-128">Example 3:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec'  -Location 'West US' -Description 'My updated Template Spec'
```

<span data-ttu-id="9e51c-129">Ändert die Beschreibung der Vorlagenspezifikation mit dem Namen "myTemplateSpec" in der Ressourcengruppe "myRG".</span><span class="sxs-lookup"><span data-stu-id="9e51c-129">Modifies the description of the Template Spec named "myTemplateSpec" in resource group "myRG".</span></span> <span data-ttu-id="9e51c-130">Wenn die Vorlagenspezifikation noch nicht vorhanden ist, wird sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="9e51c-130">If the Template Spec does not already exist it will be created.</span></span>

<span data-ttu-id="9e51c-131">**Hinweis:** Speicherort ist nur erforderlich, wenn die Vorlagenspezifikation noch nicht vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="9e51c-131">**Note:** Location is only required when the Template Spec does not already exist</span></span>

## <span data-ttu-id="9e51c-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e51c-132">PARAMETERS</span></span>

### <span data-ttu-id="9e51c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e51c-133">-DefaultProfile</span></span>
<span data-ttu-id="9e51c-134">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e51c-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e51c-135">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e51c-135">-Description</span></span>
<span data-ttu-id="9e51c-136">Die Beschreibung der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="9e51c-136">The description of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e51c-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9e51c-137">-DisplayName</span></span>
<span data-ttu-id="9e51c-138">Der Anzeigename der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="9e51c-138">The display name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e51c-139">-Location</span><span class="sxs-lookup"><span data-stu-id="9e51c-139">-Location</span></span>
<span data-ttu-id="9e51c-140">Der Speicherort der Vorlagenspezifikation. Nur erforderlich, wenn die Vorlagenspezifikation noch nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9e51c-140">The location of the template spec. Only required if the template spec does not already exist.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e51c-141">-Name</span><span class="sxs-lookup"><span data-stu-id="9e51c-141">-Name</span></span>
<span data-ttu-id="9e51c-142">Der Name der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="9e51c-142">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e51c-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e51c-143">-ResourceGroupName</span></span>
<span data-ttu-id="9e51c-144">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9e51c-144">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e51c-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e51c-145">-ResourceId</span></span>
<span data-ttu-id="9e51c-146">Die vollqualifizierte Ressourcen-ID der Vorlagenspezifikation. Beispiel: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="9e51c-146">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e51c-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="9e51c-147">-Tag</span></span>
<span data-ttu-id="9e51c-148">Hashtable von Tags für die Vorlagenspezifikation und/oder Version</span><span class="sxs-lookup"><span data-stu-id="9e51c-148">Hashtable of tags for the template spec and/or version</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e51c-149">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="9e51c-149">-TemplateFile</span></span>
<span data-ttu-id="9e51c-150">Der Dateipfad zur lokalen JSON-Datei der Azure-Ressourcen-Manager-Vorlage.</span><span class="sxs-lookup"><span data-stu-id="9e51c-150">The file path to the local Azure Resource Manager template JSON file.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByNameFromJsonFileParameterSet
Aliases: InputFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e51c-151">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="9e51c-151">-TemplateJson</span></span>
<span data-ttu-id="9e51c-152">Die Azure-Ressourcen-Manager-Vorlage JSON.</span><span class="sxs-lookup"><span data-stu-id="9e51c-152">The Azure Resource Manager template JSON.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e51c-153">-Version</span><span class="sxs-lookup"><span data-stu-id="9e51c-153">-Version</span></span>
<span data-ttu-id="9e51c-154">Die Version der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="9e51c-154">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e51c-155">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="9e51c-155">-VersionDescription</span></span>
<span data-ttu-id="9e51c-156">Die Beschreibung der Version.</span><span class="sxs-lookup"><span data-stu-id="9e51c-156">The description of the version.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e51c-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e51c-157">-Confirm</span></span>
<span data-ttu-id="9e51c-158">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e51c-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e51c-159">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9e51c-159">-WhatIf</span></span>
<span data-ttu-id="9e51c-160">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e51c-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e51c-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e51c-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e51c-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e51c-162">CommonParameters</span></span>
<span data-ttu-id="9e51c-163">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e51c-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e51c-164">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e51c-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e51c-165">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9e51c-165">INPUTS</span></span>

### <span data-ttu-id="9e51c-166">System.String</span><span class="sxs-lookup"><span data-stu-id="9e51c-166">System.String</span></span>

## <span data-ttu-id="9e51c-167">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9e51c-167">OUTPUTS</span></span>

### <span data-ttu-id="9e51c-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="9e51c-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="9e51c-169">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9e51c-169">NOTES</span></span>

## <span data-ttu-id="9e51c-170">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9e51c-170">RELATED LINKS</span></span>
