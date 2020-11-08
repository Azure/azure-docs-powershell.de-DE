---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
ms.openlocfilehash: aa011c7a858f08e3528fb2cdd7d67bcff37d76d3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165684"
---
# <span data-ttu-id="7c253-101">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="7c253-101">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="7c253-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7c253-102">SYNOPSIS</span></span>
<span data-ttu-id="7c253-103">Ruft eine Arm-Vorlage What-If Ergebnis für eine Bereitstellung im Bereich der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="7c253-103">Gets an ARM template What-If result for a deployment at resource group scope.</span></span> 

## <span data-ttu-id="7c253-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c253-104">SYNTAX</span></span>

### <span data-ttu-id="7c253-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="7c253-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c253-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7c253-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c253-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7c253-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c253-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7c253-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c253-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7c253-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c253-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7c253-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c253-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7c253-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c253-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7c253-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c253-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7c253-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c253-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7c253-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c253-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="7c253-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c253-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="7c253-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c253-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c253-117">DESCRIPTION</span></span>
<span data-ttu-id="7c253-118">Das Cmdlet " **Get-AzResourceGroupDeploymentWhatIfResult** " Ruft die Arm-Vorlage What-If Ergebnis für eine Vorlagenbereitstellung im angegebenen Ressourcengruppen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="7c253-118">The **Get-AzResourceGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified resource group scope.</span></span> <span data-ttu-id="7c253-119">Sie gibt eine Liste der Änderungen zurück, die angibt, welche Ressourcen aktualisiert werden, wenn die Bereitstellung angewendet wird, ohne dass Änderungen an realen Ressourcen vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="7c253-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="7c253-120">Wenn Sie das Format für das Ergebnis der Rückgabe angeben möchten, verwenden Sie den Parameter *ResultFormat* .</span><span class="sxs-lookup"><span data-stu-id="7c253-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="7c253-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c253-121">EXAMPLES</span></span>

### <span data-ttu-id="7c253-122">Beispiel 1: Abrufen eines What-If Ergebnisses im Ressourcengruppen Bereich</span><span class="sxs-lookup"><span data-stu-id="7c253-122">Example 1: Get a What-If result at resource group scope</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="7c253-123">Dieser Befehl ruft mit einer benutzerdefinierten Vorlagendatei und einer Parameterdatei auf dem Datenträger ein What-If Ergebnis am angegebenen Ressourcengruppen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="7c253-123">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="7c253-124">Der Befehl gibt mithilfe des *ResourceGroupName* -Parameters eine Ressourcengruppe an, in der die Vorlage bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7c253-124">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="7c253-125">Der Befehl verwendet den *Templatedatei* -Parameter, um eine Vorlagendatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7c253-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="7c253-126">Der Befehl gibt mithilfe des *TemplateParameterFile* -Parameters eine Vorlagenparameter Datei an.</span><span class="sxs-lookup"><span data-stu-id="7c253-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="7c253-127">Der Befehl legt mithilfe des *ResultFormat* -Parameters das What-If Ergebnis auf vollständige Ressourcen Nutzlasten ein.</span><span class="sxs-lookup"><span data-stu-id="7c253-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="7c253-128">Beispiel 2: Abrufen eines What-If Ergebnisses im Ressourcengruppen Bereich mit ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="7c253-128">Example 2: Get a What-If result at resource group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="7c253-129">Dieser Befehl ruft mit einer benutzerdefinierten Vorlagendatei und einer Parameterdatei auf dem Datenträger ein What-If Ergebnis am angegebenen Ressourcengruppen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="7c253-129">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="7c253-130">Der Befehl gibt mithilfe des *ResourceGroupName* -Parameters eine Ressourcengruppe an, in der die Vorlage bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7c253-130">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="7c253-131">Der Befehl verwendet den *Templatedatei* -Parameter, um eine Vorlagendatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7c253-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="7c253-132">Der Befehl gibt mithilfe des *TemplateParameterFile* -Parameters eine Vorlagenparameter Datei an.</span><span class="sxs-lookup"><span data-stu-id="7c253-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="7c253-133">Der Befehl verwendet den *ResultFormat* -Parameter, um das What-If Ergebnis so zu definieren, dass nur Ressourcen-IDs enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7c253-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="7c253-134">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c253-134">PARAMETERS</span></span>

### <span data-ttu-id="7c253-135">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7c253-135">-ApiVersion</span></span>
<span data-ttu-id="7c253-136">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7c253-136">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="7c253-137">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="7c253-137">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c253-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c253-138">-DefaultProfile</span></span>
<span data-ttu-id="7c253-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7c253-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c253-140">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="7c253-140">-ExcludeChangeType</span></span>
<span data-ttu-id="7c253-141">Durch Kommas getrennte Ressourcen Änderungstypen, die von What-If Ergebnissen ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="7c253-141">Comma-separated resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="7c253-142">-Modus</span><span class="sxs-lookup"><span data-stu-id="7c253-142">-Mode</span></span>
<span data-ttu-id="7c253-143">Der Bereitstellungsmodus.</span><span class="sxs-lookup"><span data-stu-id="7c253-143">The deployment mode.</span></span>

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

### <span data-ttu-id="7c253-144">-Name</span><span class="sxs-lookup"><span data-stu-id="7c253-144">-Name</span></span>
<span data-ttu-id="7c253-145">Der Name der Bereitstellung, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c253-145">The name of the deployment it's going to create.</span></span> <span data-ttu-id="7c253-146">Wenn nicht angegeben, wird standardmäßig der Name der Vorlagendatei verwendet, wenn eine Vorlagendatei bereitgestellt wird. Standardmäßig wird die aktuelle Uhrzeit verwendet, zu der ein Vorlagenobjekt bereitgestellt wird, beispielsweise "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="7c253-146">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="7c253-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="7c253-147">-Pre</span></span>
<span data-ttu-id="7c253-148">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="7c253-148">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7c253-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c253-149">-ResourceGroupName</span></span>
<span data-ttu-id="7c253-150">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7c253-150">The resource group name.</span></span>

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

### <span data-ttu-id="7c253-151">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="7c253-151">-ResultFormat</span></span>
<span data-ttu-id="7c253-152">Das What-If Ergebnisformat.</span><span class="sxs-lookup"><span data-stu-id="7c253-152">The What-If result format.</span></span>

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

### <span data-ttu-id="7c253-153">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="7c253-153">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="7c253-154">Überspringt die dynamische PowerShell-Parameterverarbeitung, die überprüft, ob der angegebene Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c253-154">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="7c253-155">Mit dieser Prüfung wird der Benutzer aufgefordert, einen Wert für die fehlenden Parameter bereitzustellen, doch die Bereitstellung von-SkipTemplateParameterPrompt ignoriert diese Eingabeaufforderung und ist sofort fehlerhaft, wenn ein Parameter gefunden wurde, der in der Vorlage nicht gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c253-155">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="7c253-156">Für nicht interaktive Skripts kann-SkipTemplateParameterPrompt bereitgestellt werden, um eine bessere Fehlermeldung bereitzustellen, falls nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="7c253-156">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="7c253-157">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="7c253-157">-TemplateFile</span></span>
<span data-ttu-id="7c253-158">Lokaler Pfad zur Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="7c253-158">Local path to the template file.</span></span>

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

### <span data-ttu-id="7c253-159">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="7c253-159">-TemplateObject</span></span>
<span data-ttu-id="7c253-160">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="7c253-160">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="7c253-161">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="7c253-161">-TemplateParameterFile</span></span>
<span data-ttu-id="7c253-162">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="7c253-162">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="7c253-163">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="7c253-163">-TemplateParameterObject</span></span>
<span data-ttu-id="7c253-164">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="7c253-164">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="7c253-165">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="7c253-165">-TemplateParameterUri</span></span>
<span data-ttu-id="7c253-166">URI zur Vorlagenparameter Datei.</span><span class="sxs-lookup"><span data-stu-id="7c253-166">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="7c253-167">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="7c253-167">-TemplateUri</span></span>
<span data-ttu-id="7c253-168">URI zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="7c253-168">Uri to the template file.</span></span>

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

### <span data-ttu-id="7c253-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c253-169">CommonParameters</span></span>
<span data-ttu-id="7c253-170">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c253-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c253-171">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c253-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c253-172">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7c253-172">INPUTS</span></span>

### <span data-ttu-id="7c253-173">System. String</span><span class="sxs-lookup"><span data-stu-id="7c253-173">System.String</span></span>

### <span data-ttu-id="7c253-174">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="7c253-174">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="7c253-175">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7c253-175">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7c253-176">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7c253-176">OUTPUTS</span></span>

### <span data-ttu-id="7c253-177">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. Deployments. PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="7c253-177">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="7c253-178">Notizen</span><span class="sxs-lookup"><span data-stu-id="7c253-178">NOTES</span></span>

## <span data-ttu-id="7c253-179">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7c253-179">RELATED LINKS</span></span>
