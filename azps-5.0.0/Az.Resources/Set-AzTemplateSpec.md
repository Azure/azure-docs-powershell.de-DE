---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
ms.openlocfilehash: ff2911c1fd8e49e5057c13c086f68a2b3489ad2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177244"
---
# <span data-ttu-id="09490-101">Set-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="09490-101">Set-AzTemplateSpec</span></span>

## <span data-ttu-id="09490-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09490-102">SYNOPSIS</span></span>
<span data-ttu-id="09490-103">Ändert eine Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="09490-103">Modifies a Template Spec.</span></span>

## <span data-ttu-id="09490-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09490-104">SYNTAX</span></span>

### <span data-ttu-id="09490-105">FromJsonStringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="09490-105">FromJsonStringParameterSet (Default)</span></span>
```
Set-AzTemplateSpec [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="09490-106">UpdateByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09490-106">UpdateByIdParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> [-Description <String>] [-DisplayName <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09490-107">UpdateVersionByIdFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="09490-107">UpdateVersionByIdFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09490-108">UpdateVersionByIdFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="09490-108">UpdateVersionByIdFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09490-109">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="09490-109">UpdateByNameParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09490-110">UpdateVersionByNameFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="09490-110">UpdateVersionByNameFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09490-111">UpdateVersionByNameFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="09490-111">UpdateVersionByNameFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09490-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09490-112">DESCRIPTION</span></span>
<span data-ttu-id="09490-113">Ändert eine Templace-Spezifikation. Wenn die Vorlagenspezifikation mit dem angegebenen Namen und/oder der spezifischen Version noch nicht vorhanden ist, wird Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="09490-113">Modifies a Templace Spec. If the Template Spec with the specified name and/or specific version does not already exist, it will be created.</span></span>

<span data-ttu-id="09490-114">Wenn Sie den Arm-Vorlageninhalt einer Vorlage-Spezifikationsversion ändern, kann der Inhalt entweder aus einer unformatierten JSON-Zeichenfolge (mit **UpdateVersionByNameFromJsonParameterSet** -Parametersatz) oder aus einer angegebenen JSON-Datei (mit dem **UpdateVersionByNameFromJsonFileParameterSet** -Parametersatz) stammen.</span><span class="sxs-lookup"><span data-stu-id="09490-114">When modifying a Template Spec version's ARM Template content, the content can either come from a raw JSON string (using **UpdateVersionByNameFromJsonParameterSet** parameter set) or from a specified JSON file (using **UpdateVersionByNameFromJsonFileParameterSet** parameter set).</span></span>

## <span data-ttu-id="09490-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09490-115">EXAMPLES</span></span>

### <span data-ttu-id="09490-116">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="09490-116">Example 1:</span></span>
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

<span data-ttu-id="09490-117">Ändert die Version "v 1.0" einer Vorlagenspezifikation mit dem Namen "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="09490-117">Modifies version "v1.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="09490-118">Die angegebene Version hat $templateJson als Arm-Vorlageninhalt der Version.</span><span class="sxs-lookup"><span data-stu-id="09490-118">The specified version will have $templateJson as the version's ARM Template content.</span></span> <span data-ttu-id="09490-119">Wenn die Stamm Vorlagenspezifikation und/oder-Version noch nicht vorhanden ist, werden Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="09490-119">If the root Template Spec and/or version do not already exist they will be created.</span></span>


<span data-ttu-id="09490-120">**Notizen**</span><span class="sxs-lookup"><span data-stu-id="09490-120">**Notes:**</span></span> 

* <span data-ttu-id="09490-121">Bei der Arm-Vorlage im Beispiel handelt es sich um eine No-op-Datei, da Sie keine tatsächlichen Ressourcen enthält.</span><span class="sxs-lookup"><span data-stu-id="09490-121">The ARM Template in the example is a no-op as it contains no actual resources.</span></span>
* <span data-ttu-id="09490-122">Der Speicherort ist nur erforderlich, wenn die Vorlagenspezifikation nicht bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="09490-122">Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="09490-123">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="09490-123">Example 2:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="09490-124">Ändert die Version "v 2.0" einer Vorlagenspezifikation mit dem Namen "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="09490-124">Modifies version "v2.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="09490-125">In der angegebenen Version ist der Inhalt der lokalen Datei "myTemplateContent.jsauf" als Inhalt der Arm-Vorlage der Version enthalten.</span><span class="sxs-lookup"><span data-stu-id="09490-125">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span> <span data-ttu-id="09490-126">Wenn die Stamm Vorlagenspezifikation und/oder-Version noch nicht vorhanden ist, werden Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="09490-126">If the root Template Spec and/or version do not already exist they will be created.</span></span>

<span data-ttu-id="09490-127">**Hinweis:** Der Speicherort ist nur erforderlich, wenn die Vorlagenspezifikation nicht bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="09490-127">**Note:** Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="09490-128">Beispiel 3:</span><span class="sxs-lookup"><span data-stu-id="09490-128">Example 3:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec'  -Location 'West US' -Description 'My updated Template Spec'
```

<span data-ttu-id="09490-129">Ändert die Beschreibung der Vorlagenspezifikation mit dem Namen "myTemplateSpec" in der Ressourcengruppe "myRG".</span><span class="sxs-lookup"><span data-stu-id="09490-129">Modifies the description of the Template Spec named "myTemplateSpec" in resource group "myRG".</span></span> <span data-ttu-id="09490-130">Wenn die Vorlagenspezifikation nicht bereits vorhanden ist, wird Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="09490-130">If the Template Spec does not already exist it will be created.</span></span>

<span data-ttu-id="09490-131">**Hinweis:** Der Speicherort ist nur erforderlich, wenn die Vorlagenspezifikation nicht bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="09490-131">**Note:** Location is only required when the Template Spec does not already exist</span></span>

## <span data-ttu-id="09490-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="09490-132">PARAMETERS</span></span>

### <span data-ttu-id="09490-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09490-133">-DefaultProfile</span></span>
<span data-ttu-id="09490-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="09490-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09490-135">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09490-135">-Description</span></span>
<span data-ttu-id="09490-136">Die Beschreibung der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="09490-136">The description of the template spec.</span></span>

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

### <span data-ttu-id="09490-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="09490-137">-DisplayName</span></span>
<span data-ttu-id="09490-138">Der Anzeigename der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="09490-138">The display name of the template spec.</span></span>

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

### <span data-ttu-id="09490-139">-Standort</span><span class="sxs-lookup"><span data-stu-id="09490-139">-Location</span></span>
<span data-ttu-id="09490-140">Der Speicherort der Vorlagenspezifikation. Nur erforderlich, wenn die Vorlagenspezifikation noch nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="09490-140">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="09490-141">-Name</span><span class="sxs-lookup"><span data-stu-id="09490-141">-Name</span></span>
<span data-ttu-id="09490-142">Der Name der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="09490-142">The name of the template spec.</span></span>

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

### <span data-ttu-id="09490-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09490-143">-ResourceGroupName</span></span>
<span data-ttu-id="09490-144">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="09490-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="09490-145">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="09490-145">-ResourceId</span></span>
<span data-ttu-id="09490-146">Die vollqualifizierte Ressourcen-ID der Vorlagenspezifikation. Beispiel:/Subscriptions/{subId}/resourceGroups/{rgName}/Providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="09490-146">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="09490-147">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="09490-147">-TemplateFile</span></span>
<span data-ttu-id="09490-148">Der Dateipfad zu der JSON-Datei für die lokale Azure Resource Manager-Vorlage.</span><span class="sxs-lookup"><span data-stu-id="09490-148">The file path to the local Azure Resource Manager template JSON file.</span></span>

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

### <span data-ttu-id="09490-149">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="09490-149">-TemplateJson</span></span>
<span data-ttu-id="09490-150">Die Azure Resource Manager-Vorlage JSON.</span><span class="sxs-lookup"><span data-stu-id="09490-150">The Azure Resource Manager template JSON.</span></span>

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

### <span data-ttu-id="09490-151">-Version</span><span class="sxs-lookup"><span data-stu-id="09490-151">-Version</span></span>
<span data-ttu-id="09490-152">Die Version der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="09490-152">The version of the template spec.</span></span>

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

### <span data-ttu-id="09490-153">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="09490-153">-VersionDescription</span></span>
<span data-ttu-id="09490-154">Die Beschreibung der Version.</span><span class="sxs-lookup"><span data-stu-id="09490-154">The description of the version.</span></span>

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

### <span data-ttu-id="09490-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="09490-155">-Confirm</span></span>
<span data-ttu-id="09490-156">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="09490-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09490-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09490-157">-WhatIf</span></span>
<span data-ttu-id="09490-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09490-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09490-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="09490-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09490-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09490-160">CommonParameters</span></span>
<span data-ttu-id="09490-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09490-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09490-162">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09490-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09490-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09490-163">INPUTS</span></span>

### <span data-ttu-id="09490-164">System. String</span><span class="sxs-lookup"><span data-stu-id="09490-164">System.String</span></span>

## <span data-ttu-id="09490-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09490-165">OUTPUTS</span></span>

### <span data-ttu-id="09490-166">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="09490-166">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="09490-167">Notizen</span><span class="sxs-lookup"><span data-stu-id="09490-167">NOTES</span></span>

## <span data-ttu-id="09490-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09490-168">RELATED LINKS</span></span>
