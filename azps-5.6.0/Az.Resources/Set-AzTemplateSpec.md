---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/set-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
ms.openlocfilehash: 48a700f29a80b03df0fd4fc2d858dcb1c1c57f76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933704"
---
# <span data-ttu-id="858fc-101">Set-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="858fc-101">Set-AzTemplateSpec</span></span>

## <span data-ttu-id="858fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="858fc-102">SYNOPSIS</span></span>
<span data-ttu-id="858fc-103">Ändert eine Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="858fc-103">Modifies a Template Spec.</span></span>

## <span data-ttu-id="858fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="858fc-104">SYNTAX</span></span>

### <span data-ttu-id="858fc-105">FromJsonStringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="858fc-105">FromJsonStringParameterSet (Default)</span></span>
```
Set-AzTemplateSpec [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="858fc-106">UpdateByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="858fc-106">UpdateByIdParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> [-Description <String>] [-DisplayName <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="858fc-107">UpdateVersionByIdFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="858fc-107">UpdateVersionByIdFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="858fc-108">UpdateVersionByIdFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="858fc-108">UpdateVersionByIdFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="858fc-109">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="858fc-109">UpdateByNameParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="858fc-110">UpdateVersionByNameFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="858fc-110">UpdateVersionByNameFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="858fc-111">UpdateVersionByNameFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="858fc-111">UpdateVersionByNameFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="858fc-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="858fc-112">DESCRIPTION</span></span>
<span data-ttu-id="858fc-113">Ändert eine Templace-Spezifikation. Wenn die Vorlagenspezifikation mit dem angegebenen Namen und/oder einer bestimmten Version noch nicht vorhanden ist, wird sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="858fc-113">Modifies a Templace Spec. If the Template Spec with the specified name and/or specific version does not already exist, it will be created.</span></span>

<span data-ttu-id="858fc-114">Beim Ändern des ARM-Vorlageninhalts einer Vorlagenspezifikationsversion kann der Inhalt entweder aus einer unformatierten JSON-Zeichenfolge (mithilfe des Parametersets **UpdateVersionByNameFromJsonParameterSet)** oder aus einer angegebenen JSON-Datei (mit **updateVersionByNameFromJsonFileParameterSet-Parametersatz)** stammen.</span><span class="sxs-lookup"><span data-stu-id="858fc-114">When modifying a Template Spec version's ARM Template content, the content can either come from a raw JSON string (using **UpdateVersionByNameFromJsonParameterSet** parameter set) or from a specified JSON file (using **UpdateVersionByNameFromJsonFileParameterSet** parameter set).</span></span>

## <span data-ttu-id="858fc-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="858fc-115">EXAMPLES</span></span>

### <span data-ttu-id="858fc-116">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="858fc-116">Example 1:</span></span>
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

<span data-ttu-id="858fc-117">Ändert Version "v1.0" einer Vorlagenspezifikation mit dem Namen "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="858fc-117">Modifies version "v1.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="858fc-118">Die angegebene Version enthält $templateJson als Inhalt der ARM Vorlage.</span><span class="sxs-lookup"><span data-stu-id="858fc-118">The specified version will have $templateJson as the version's ARM Template content.</span></span> <span data-ttu-id="858fc-119">Wenn die Stammvorlagenspezifikation und/oder -version noch nicht vorhanden ist, werden sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="858fc-119">If the root Template Spec and/or version do not already exist they will be created.</span></span>


<span data-ttu-id="858fc-120">**Hinweise:**</span><span class="sxs-lookup"><span data-stu-id="858fc-120">**Notes:**</span></span> 

* <span data-ttu-id="858fc-121">Die ARM-Vorlage im Beispiel ist ein No-Op, da sie keine tatsächlichen Ressourcen enthält.</span><span class="sxs-lookup"><span data-stu-id="858fc-121">The ARM Template in the example is a no-op as it contains no actual resources.</span></span>
* <span data-ttu-id="858fc-122">Speicherort ist nur erforderlich, wenn die Vorlagenspezifikation noch nicht vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="858fc-122">Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="858fc-123">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="858fc-123">Example 2:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="858fc-124">Ändert Version "v2.0" einer Vorlagenspezifikation mit dem Namen "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="858fc-124">Modifies version "v2.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="858fc-125">Die angegebene Version enthält den Inhalt aus der lokalen Datei "myTemplateContent.jsein" als Inhalt der ARM Vorlage.</span><span class="sxs-lookup"><span data-stu-id="858fc-125">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span> <span data-ttu-id="858fc-126">Wenn die Stammvorlagenspezifikation und/oder -version noch nicht vorhanden ist, werden sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="858fc-126">If the root Template Spec and/or version do not already exist they will be created.</span></span>

<span data-ttu-id="858fc-127">**Hinweis:** Speicherort ist nur erforderlich, wenn die Vorlagenspezifikation noch nicht vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="858fc-127">**Note:** Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="858fc-128">Beispiel 3:</span><span class="sxs-lookup"><span data-stu-id="858fc-128">Example 3:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec'  -Location 'West US' -Description 'My updated Template Spec'
```

<span data-ttu-id="858fc-129">Ändert die Beschreibung der Vorlagenspezifikation mit dem Namen "myTemplateSpec" in der Ressourcengruppe "myRG".</span><span class="sxs-lookup"><span data-stu-id="858fc-129">Modifies the description of the Template Spec named "myTemplateSpec" in resource group "myRG".</span></span> <span data-ttu-id="858fc-130">Wenn die Vorlagenspezifikation noch nicht vorhanden ist, wird sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="858fc-130">If the Template Spec does not already exist it will be created.</span></span>

<span data-ttu-id="858fc-131">**Hinweis:** Speicherort ist nur erforderlich, wenn die Vorlagenspezifikation noch nicht vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="858fc-131">**Note:** Location is only required when the Template Spec does not already exist</span></span>

## <span data-ttu-id="858fc-132">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="858fc-132">PARAMETERS</span></span>

### <span data-ttu-id="858fc-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="858fc-133">-DefaultProfile</span></span>
<span data-ttu-id="858fc-134">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="858fc-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="858fc-135">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="858fc-135">-Description</span></span>
<span data-ttu-id="858fc-136">Die Beschreibung der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="858fc-136">The description of the template spec.</span></span>

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

### <span data-ttu-id="858fc-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="858fc-137">-DisplayName</span></span>
<span data-ttu-id="858fc-138">Der Anzeigename der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="858fc-138">The display name of the template spec.</span></span>

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

### <span data-ttu-id="858fc-139">-Location</span><span class="sxs-lookup"><span data-stu-id="858fc-139">-Location</span></span>
<span data-ttu-id="858fc-140">Der Speicherort der Vorlagenspezifikation. Nur erforderlich, wenn die Vorlagenspezifikation noch nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="858fc-140">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="858fc-141">-Name</span><span class="sxs-lookup"><span data-stu-id="858fc-141">-Name</span></span>
<span data-ttu-id="858fc-142">Der Name der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="858fc-142">The name of the template spec.</span></span>

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

### <span data-ttu-id="858fc-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="858fc-143">-ResourceGroupName</span></span>
<span data-ttu-id="858fc-144">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="858fc-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="858fc-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="858fc-145">-ResourceId</span></span>
<span data-ttu-id="858fc-146">Die vollqualifizierte Ressourcen-ID der Vorlagenspezifikation. Beispiel: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="858fc-146">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="858fc-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="858fc-147">-Tag</span></span>
<span data-ttu-id="858fc-148">Hashtable von Tags für die Vorlagenspezifikation und/oder -version</span><span class="sxs-lookup"><span data-stu-id="858fc-148">Hashtable of tags for the template spec and/or version</span></span>

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

### <span data-ttu-id="858fc-149">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="858fc-149">-TemplateFile</span></span>
<span data-ttu-id="858fc-150">Der Dateipfad zur lokalen Azure Resource Manager-Vorlagen-JSON-Datei.</span><span class="sxs-lookup"><span data-stu-id="858fc-150">The file path to the local Azure Resource Manager template JSON file.</span></span>

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

### <span data-ttu-id="858fc-151">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="858fc-151">-TemplateJson</span></span>
<span data-ttu-id="858fc-152">Die Azure Resource Manager-Vorlage JSON.</span><span class="sxs-lookup"><span data-stu-id="858fc-152">The Azure Resource Manager template JSON.</span></span>

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

### <span data-ttu-id="858fc-153">-Version</span><span class="sxs-lookup"><span data-stu-id="858fc-153">-Version</span></span>
<span data-ttu-id="858fc-154">Die Version der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="858fc-154">The version of the template spec.</span></span>

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

### <span data-ttu-id="858fc-155">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="858fc-155">-VersionDescription</span></span>
<span data-ttu-id="858fc-156">Die Beschreibung der Version.</span><span class="sxs-lookup"><span data-stu-id="858fc-156">The description of the version.</span></span>

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

### <span data-ttu-id="858fc-157">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="858fc-157">-Confirm</span></span>
<span data-ttu-id="858fc-158">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="858fc-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="858fc-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="858fc-159">-WhatIf</span></span>
<span data-ttu-id="858fc-160">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="858fc-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="858fc-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="858fc-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="858fc-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="858fc-162">CommonParameters</span></span>
<span data-ttu-id="858fc-163">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="858fc-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="858fc-164">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="858fc-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="858fc-165">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="858fc-165">INPUTS</span></span>

### <span data-ttu-id="858fc-166">System.String</span><span class="sxs-lookup"><span data-stu-id="858fc-166">System.String</span></span>

## <span data-ttu-id="858fc-167">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="858fc-167">OUTPUTS</span></span>

### <span data-ttu-id="858fc-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="858fc-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="858fc-169">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="858fc-169">NOTES</span></span>

## <span data-ttu-id="858fc-170">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="858fc-170">RELATED LINKS</span></span>
