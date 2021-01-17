---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
ms.openlocfilehash: 2d0eb49a46e0d6fbbe02d145e42195d059c5176f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459267"
---
# <span data-ttu-id="1de3f-101">New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="1de3f-101">New-AzTemplateSpec</span></span>

## <span data-ttu-id="1de3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1de3f-102">SYNOPSIS</span></span>
<span data-ttu-id="1de3f-103">Erstellt eine neue Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="1de3f-103">Creates a new Template Spec.</span></span>

## <span data-ttu-id="1de3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1de3f-104">SYNTAX</span></span>

### <span data-ttu-id="1de3f-105">FromJsonStringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1de3f-105">FromJsonStringParameterSet (Default)</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String>
 [-VersionDescription <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1de3f-106">FromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="1de3f-106">FromJsonFileParameterSet</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String>
 [-VersionDescription <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1de3f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1de3f-107">DESCRIPTION</span></span>
<span data-ttu-id="1de3f-108">Erstellt eine neue Version von Vorlagenspezifikationen mit dem angegebenen ARM Vorlageninhalt.</span><span class="sxs-lookup"><span data-stu-id="1de3f-108">Creates a new Template Spec version with the specified ARM Template content.</span></span> <span data-ttu-id="1de3f-109">Der Inhalt kann entweder aus einer unformatierte jSON-Zeichenfolge (mit dem **Parametersatz "FromJsonStringParameterSet")** oder aus einer angegebenen Datei (mit dem Parametersatz **"FromJsonFileParameterSet")** stammen.</span><span class="sxs-lookup"><span data-stu-id="1de3f-109">The content can either come from a raw JSON string (using **FromJsonStringParameterSet** parameter set) or from a specified JSON file (using **FromJsonFileParameterSet** parameter set).</span></span>  

<span data-ttu-id="1de3f-110">Wenn die Stammvorlagenspezifikation noch nicht vorhanden ist, wird sie zusammen mit der Version "Vorlagenspezifikation" erstellt.</span><span class="sxs-lookup"><span data-stu-id="1de3f-110">If the root Template Spec does not already exist it will be created along with the Template Spec version.</span></span> <span data-ttu-id="1de3f-111">Wenn bereits eine Vorlagenspezifikation mit dem angegebenen Namen vorhanden ist, wird sie aktualisiert, und die angegebene Version wird aktualisiert (alle anderen vorhandenen Versionen werden beibehalten).</span><span class="sxs-lookup"><span data-stu-id="1de3f-111">If a Template Spec already exists with the given name, it and the specified version will be updated (any other existing versions will be preserved).</span></span>

## <span data-ttu-id="1de3f-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1de3f-112">EXAMPLES</span></span>

### <span data-ttu-id="1de3f-113">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="1de3f-113">Example 1:</span></span>
```powershell
PS C:\> $templateJson = @"
{
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "resources": []
}
"@
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v1.0' -Location 'West US' -TemplateJson $templateJson
```

<span data-ttu-id="1de3f-114">Erstellt eine neue Version der Vorlagenspezifikation "v1.0" in einer Vorlagenspezifikation namens "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="1de3f-114">Creates a new Template Spec version "v1.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="1de3f-115">Die angegebene Version $templateJson als Der Inhalt der ARM Version angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1de3f-115">The specified version will have $templateJson as the version's ARM Template content.</span></span>

 <span data-ttu-id="1de3f-116">**Hinweis:** Die ARM Beispiel ist ein "No-Op"-Wert, da sie keine tatsächlichen Ressourcen enthält.</span><span class="sxs-lookup"><span data-stu-id="1de3f-116">**Note:** The ARM Template in the example is a no-op as it contains no actual resources.</span></span>

### <span data-ttu-id="1de3f-117">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="1de3f-117">Example 2:</span></span>
```powershell
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="1de3f-118">Erstellt eine neue Version der Vorlagenspezifikation "v2.0" in einer Vorlagenspezifikation namens "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="1de3f-118">Creates a new Template Spec version "v2.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="1de3f-119">Bei der angegebenen Version wird der Inhalt aus der lokalen Datei "myTemplateContent.js" als Der Inhalt der ARM Version angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1de3f-119">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span>

## <span data-ttu-id="1de3f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1de3f-120">PARAMETERS</span></span>

### <span data-ttu-id="1de3f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1de3f-121">-DefaultProfile</span></span>
<span data-ttu-id="1de3f-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1de3f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1de3f-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1de3f-123">-Description</span></span>
<span data-ttu-id="1de3f-124">Die Beschreibung der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="1de3f-124">The description of the template spec.</span></span>

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

### <span data-ttu-id="1de3f-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1de3f-125">-DisplayName</span></span>
<span data-ttu-id="1de3f-126">Der Anzeigename der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="1de3f-126">The display name of the template spec.</span></span>

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

### <span data-ttu-id="1de3f-127">-Force</span><span class="sxs-lookup"><span data-stu-id="1de3f-127">-Force</span></span>
<span data-ttu-id="1de3f-128">Fordern Sie beim Überschreiben einer vorhandenen Version keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="1de3f-128">Do not ask for confirmation when overwriting an existing version.</span></span>

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

### <span data-ttu-id="1de3f-129">-Location</span><span class="sxs-lookup"><span data-stu-id="1de3f-129">-Location</span></span>
<span data-ttu-id="1de3f-130">Der Speicherort der Vorlagenspezifikation. Nur erforderlich, wenn die Vorlagenspezifikation noch nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1de3f-130">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="1de3f-131">-Name</span><span class="sxs-lookup"><span data-stu-id="1de3f-131">-Name</span></span>
<span data-ttu-id="1de3f-132">Der Name der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="1de3f-132">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de3f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1de3f-133">-ResourceGroupName</span></span>
<span data-ttu-id="1de3f-134">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1de3f-134">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de3f-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="1de3f-135">-Tag</span></span>
<span data-ttu-id="1de3f-136">Hashtable von Tags für die ressource(n) der neuen Vorlagenspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="1de3f-136">Hashtable of tags for the new template spec resource(s).</span></span>

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

### <span data-ttu-id="1de3f-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="1de3f-137">-TemplateFile</span></span>
<span data-ttu-id="1de3f-138">Der Dateipfad zur lokalen JSON-Datei der Azure-Ressourcen-Manager-Vorlage.</span><span class="sxs-lookup"><span data-stu-id="1de3f-138">The file path to the local Azure Resource Manager template JSON file.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonFileParameterSet
Aliases: InputFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de3f-139">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="1de3f-139">-TemplateJson</span></span>
<span data-ttu-id="1de3f-140">Die Azure-Ressourcen-Manager-Vorlage JSON.</span><span class="sxs-lookup"><span data-stu-id="1de3f-140">The Azure Resource Manager template JSON.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de3f-141">-Version</span><span class="sxs-lookup"><span data-stu-id="1de3f-141">-Version</span></span>
<span data-ttu-id="1de3f-142">Die Version der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="1de3f-142">The version of the template spec.</span></span>

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

### <span data-ttu-id="1de3f-143">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="1de3f-143">-VersionDescription</span></span>
<span data-ttu-id="1de3f-144">Die Beschreibung der Version.</span><span class="sxs-lookup"><span data-stu-id="1de3f-144">The description of the version.</span></span>

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

### <span data-ttu-id="1de3f-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1de3f-145">-Confirm</span></span>
<span data-ttu-id="1de3f-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1de3f-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1de3f-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1de3f-147">-WhatIf</span></span>
<span data-ttu-id="1de3f-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1de3f-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1de3f-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1de3f-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1de3f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1de3f-150">CommonParameters</span></span>
<span data-ttu-id="1de3f-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1de3f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1de3f-152">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1de3f-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1de3f-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1de3f-153">INPUTS</span></span>

### <span data-ttu-id="1de3f-154">System.String</span><span class="sxs-lookup"><span data-stu-id="1de3f-154">System.String</span></span>

## <span data-ttu-id="1de3f-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1de3f-155">OUTPUTS</span></span>

### <span data-ttu-id="1de3f-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="1de3f-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="1de3f-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1de3f-157">NOTES</span></span>

## <span data-ttu-id="1de3f-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1de3f-158">RELATED LINKS</span></span>
