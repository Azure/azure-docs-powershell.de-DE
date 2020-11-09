---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 09b0a1a6691b4c3d491d15d226fb8260fb7ae00e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301108"
---
# <span data-ttu-id="6e512-101">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="6e512-101">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="6e512-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6e512-102">SYNOPSIS</span></span>
<span data-ttu-id="6e512-103">Ruft eine Arm-Vorlage What-If Ergebnis für eine Bereitstellung im Bereich der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="6e512-103">Gets an ARM template What-If result for a deployment at resource group scope.</span></span> 

## <span data-ttu-id="6e512-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e512-104">SYNTAX</span></span>

### <span data-ttu-id="6e512-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="6e512-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e512-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="6e512-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e512-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="6e512-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e512-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="6e512-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e512-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="6e512-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e512-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="6e512-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e512-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="6e512-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e512-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="6e512-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e512-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="6e512-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e512-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="6e512-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e512-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="6e512-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e512-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="6e512-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e512-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e512-117">DESCRIPTION</span></span>
<span data-ttu-id="6e512-118">Das Cmdlet " **Get-AzResourceGroupDeploymentWhatIfResult** " Ruft die Arm-Vorlage What-If Ergebnis für eine Vorlagenbereitstellung im angegebenen Ressourcengruppen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="6e512-118">The **Get-AzResourceGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified resource group scope.</span></span> <span data-ttu-id="6e512-119">Sie gibt eine Liste der Änderungen zurück, die angibt, welche Ressourcen aktualisiert werden, wenn die Bereitstellung angewendet wird, ohne dass Änderungen an realen Ressourcen vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="6e512-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="6e512-120">Wenn Sie das Format für das Ergebnis der Rückgabe angeben möchten, verwenden Sie den Parameter *ResultFormat* .</span><span class="sxs-lookup"><span data-stu-id="6e512-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="6e512-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e512-121">EXAMPLES</span></span>

### <span data-ttu-id="6e512-122">Beispiel 1: Abrufen eines What-If Ergebnisses im Ressourcengruppen Bereich</span><span class="sxs-lookup"><span data-stu-id="6e512-122">Example 1: Get a What-If result at resource group scope</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="6e512-123">Dieser Befehl ruft mit einer benutzerdefinierten Vorlagendatei und einer Parameterdatei auf dem Datenträger ein What-If Ergebnis am angegebenen Ressourcengruppen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="6e512-123">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="6e512-124">Der Befehl gibt mithilfe des *ResourceGroupName* -Parameters eine Ressourcengruppe an, in der die Vorlage bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6e512-124">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="6e512-125">Der Befehl verwendet den *Templatedatei* -Parameter, um eine Vorlagendatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6e512-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="6e512-126">Der Befehl gibt mithilfe des *TemplateParameterFile* -Parameters eine Vorlagenparameter Datei an.</span><span class="sxs-lookup"><span data-stu-id="6e512-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="6e512-127">Der Befehl legt mithilfe des *ResultFormat* -Parameters das What-If Ergebnis auf vollständige Ressourcen Nutzlasten ein.</span><span class="sxs-lookup"><span data-stu-id="6e512-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="6e512-128">Beispiel 2: Abrufen eines What-If Ergebnisses im Ressourcengruppen Bereich mit ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="6e512-128">Example 2: Get a What-If result at resource group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="6e512-129">Dieser Befehl ruft mit einer benutzerdefinierten Vorlagendatei und einer Parameterdatei auf dem Datenträger ein What-If Ergebnis am angegebenen Ressourcengruppen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="6e512-129">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="6e512-130">Der Befehl gibt mithilfe des *ResourceGroupName* -Parameters eine Ressourcengruppe an, in der die Vorlage bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6e512-130">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="6e512-131">Der Befehl verwendet den *Templatedatei* -Parameter, um eine Vorlagendatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6e512-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="6e512-132">Der Befehl gibt mithilfe des *TemplateParameterFile* -Parameters eine Vorlagenparameter Datei an.</span><span class="sxs-lookup"><span data-stu-id="6e512-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="6e512-133">Der Befehl verwendet den *ResultFormat* -Parameter, um das What-If Ergebnis so zu definieren, dass nur Ressourcen-IDs enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6e512-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="6e512-134">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e512-134">PARAMETERS</span></span>

### <span data-ttu-id="6e512-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e512-135">-DefaultProfile</span></span>
<span data-ttu-id="6e512-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6e512-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e512-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="6e512-137">-ExcludeChangeType</span></span>
<span data-ttu-id="6e512-138">Durch Kommas getrennte Ressourcen Änderungstypen, die von What-If Ergebnissen ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="6e512-138">Comma-separated resource change types to be excluded from What-If results.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e512-139">-Modus</span><span class="sxs-lookup"><span data-stu-id="6e512-139">-Mode</span></span>
<span data-ttu-id="6e512-140">Der Bereitstellungsmodus.</span><span class="sxs-lookup"><span data-stu-id="6e512-140">The deployment mode.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e512-141">-Name</span><span class="sxs-lookup"><span data-stu-id="6e512-141">-Name</span></span>
<span data-ttu-id="6e512-142">Der Name der Bereitstellung, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e512-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="6e512-143">Wenn nicht angegeben, wird standardmäßig der Name der Vorlagendatei verwendet, wenn eine Vorlagendatei bereitgestellt wird. Standardmäßig wird die aktuelle Uhrzeit verwendet, zu der ein Vorlagenobjekt bereitgestellt wird, beispielsweise "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="6e512-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e512-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="6e512-144">-Pre</span></span>
<span data-ttu-id="6e512-145">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="6e512-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6e512-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e512-146">-ResourceGroupName</span></span>
<span data-ttu-id="6e512-147">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6e512-147">The resource group name.</span></span>

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

### <span data-ttu-id="6e512-148">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="6e512-148">-ResultFormat</span></span>
<span data-ttu-id="6e512-149">Das What-If Ergebnisformat.</span><span class="sxs-lookup"><span data-stu-id="6e512-149">The What-If result format.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.WhatIfResultFormat
Parameter Sets: (All)
Aliases:
Accepted values: ResourceIdOnly, FullResourcePayloads

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e512-150">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="6e512-150">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="6e512-151">Überspringt die dynamische PowerShell-Parameterverarbeitung, die überprüft, ob der angegebene Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6e512-151">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="6e512-152">Mit dieser Prüfung wird der Benutzer aufgefordert, einen Wert für die fehlenden Parameter bereitzustellen, doch die Bereitstellung von-SkipTemplateParameterPrompt ignoriert diese Eingabeaufforderung und ist sofort fehlerhaft, wenn ein Parameter gefunden wurde, der in der Vorlage nicht gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e512-152">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="6e512-153">Für nicht interaktive Skripts kann-SkipTemplateParameterPrompt bereitgestellt werden, um eine bessere Fehlermeldung bereitzustellen, falls nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="6e512-153">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="6e512-154">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="6e512-154">-TemplateFile</span></span>
<span data-ttu-id="6e512-155">Lokaler Pfad zur Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="6e512-155">Local path to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e512-156">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="6e512-156">-TemplateObject</span></span>
<span data-ttu-id="6e512-157">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="6e512-157">A hash table which represents the template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e512-158">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="6e512-158">-TemplateParameterFile</span></span>
<span data-ttu-id="6e512-159">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="6e512-159">A file that has the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e512-160">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="6e512-160">-TemplateParameterObject</span></span>
<span data-ttu-id="6e512-161">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="6e512-161">A hash table which represents the parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e512-162">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="6e512-162">-TemplateParameterUri</span></span>
<span data-ttu-id="6e512-163">URI zur Vorlagenparameter Datei.</span><span class="sxs-lookup"><span data-stu-id="6e512-163">Uri to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e512-164">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="6e512-164">-TemplateUri</span></span>
<span data-ttu-id="6e512-165">URI zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="6e512-165">Uri to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e512-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e512-166">CommonParameters</span></span>
<span data-ttu-id="6e512-167">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e512-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e512-168">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e512-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e512-169">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6e512-169">INPUTS</span></span>

### <span data-ttu-id="6e512-170">System. String</span><span class="sxs-lookup"><span data-stu-id="6e512-170">System.String</span></span>

### <span data-ttu-id="6e512-171">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="6e512-171">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="6e512-172">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6e512-172">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6e512-173">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6e512-173">OUTPUTS</span></span>

### <span data-ttu-id="6e512-174">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. Deployments. PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="6e512-174">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="6e512-175">Notizen</span><span class="sxs-lookup"><span data-stu-id="6e512-175">NOTES</span></span>

## <span data-ttu-id="6e512-176">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6e512-176">RELATED LINKS</span></span>
