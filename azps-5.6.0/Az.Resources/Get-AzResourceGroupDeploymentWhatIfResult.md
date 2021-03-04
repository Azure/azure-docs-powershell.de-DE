---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 1b45c08f2906f3b1bec827a7f870d2c901bbb2b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924515"
---
# <span data-ttu-id="2d735-101">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="2d735-101">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="2d735-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d735-102">SYNOPSIS</span></span>
<span data-ttu-id="2d735-103">Ruft eine Vorlage What-If ergebnis für eine Bereitstellung im Ressourcengruppenbereich ab.</span><span class="sxs-lookup"><span data-stu-id="2d735-103">Gets a template What-If result for a deployment at resource group scope.</span></span> 

## <span data-ttu-id="2d735-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d735-104">SYNTAX</span></span>

### <span data-ttu-id="2d735-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d735-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d735-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2d735-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d735-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2d735-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d735-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2d735-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d735-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2d735-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d735-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2d735-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d735-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2d735-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d735-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2d735-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d735-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2d735-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d735-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2d735-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d735-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2d735-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d735-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2d735-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d735-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d735-117">DESCRIPTION</span></span>
<span data-ttu-id="2d735-118">Das **Get-AzResourceGroupDeploymentWhatIfResult-Cmdlet** ruft das ARM-What-If-Ergebnis für eine Vorlagenbereitstellung im angegebenen Ressourcengruppenbereich ab.</span><span class="sxs-lookup"><span data-stu-id="2d735-118">The **Get-AzResourceGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified resource group scope.</span></span> <span data-ttu-id="2d735-119">Es gibt eine Liste mit Änderungen zurück, die angibt, welche Ressourcen aktualisiert werden, wenn die Bereitstellung angewendet wird, ohne Änderungen an echten Ressourcen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="2d735-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="2d735-120">Verwenden Sie den Parameter *ResultFormat,* um das Format für das zurückgebende Ergebnis anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2d735-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="2d735-121">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2d735-121">EXAMPLES</span></span>

### <span data-ttu-id="2d735-122">Beispiel 1: Erhalten eines What-If ergebnisses im Ressourcengruppenbereich</span><span class="sxs-lookup"><span data-stu-id="2d735-122">Example 1: Get a What-If result at resource group scope</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="2d735-123">Dieser Befehl ruft ein What-If des angegebenen Ressourcengruppenbereichs ab, indem eine benutzerdefinierte Vorlagendatei und eine Parameterdatei auf dem Datenträger verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d735-123">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="2d735-124">Der Befehl verwendet den *Parameter ResourceGroupName,* um eine Ressourcengruppe anzugeben, in der die Vorlage bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2d735-124">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="2d735-125">Der Befehl verwendet den *Parameter TemplateFile,* um eine Vorlagendatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2d735-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="2d735-126">Der Befehl verwendet den *Parameter TemplateParameterFile,* um eine Vorlagenparameterdatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2d735-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="2d735-127">Der Befehl verwendet den *Parameter ResultFormat,* um das What-If ergebnis so zu legen, dass vollständige Ressourcennutzlasten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="2d735-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="2d735-128">Beispiel 2: Erhalten eines What-If ergebnisses im Ressourcengruppenbereich mit ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="2d735-128">Example 2: Get a What-If result at resource group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="2d735-129">Dieser Befehl ruft ein What-If des angegebenen Ressourcengruppenbereichs ab, indem eine benutzerdefinierte Vorlagendatei und eine Parameterdatei auf dem Datenträger verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d735-129">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="2d735-130">Der Befehl verwendet den *Parameter ResourceGroupName,* um eine Ressourcengruppe anzugeben, in der die Vorlage bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2d735-130">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="2d735-131">Der Befehl verwendet den *Parameter TemplateFile,* um eine Vorlagendatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2d735-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="2d735-132">Der Befehl verwendet den *Parameter TemplateParameterFile,* um eine Vorlagenparameterdatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2d735-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="2d735-133">Der Befehl verwendet den *Parameter ResultFormat,* um das ergebnis What-If nur Ressourcen-IDs zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="2d735-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="2d735-134">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2d735-134">PARAMETERS</span></span>

### <span data-ttu-id="2d735-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d735-135">-DefaultProfile</span></span>
<span data-ttu-id="2d735-136">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d735-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d735-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="2d735-137">-ExcludeChangeType</span></span>
<span data-ttu-id="2d735-138">Durch Kommas getrennte Ressourcenänderungstypen, die aus den Ergebnissen What-If werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2d735-138">Comma-separated resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="2d735-139">-Modus</span><span class="sxs-lookup"><span data-stu-id="2d735-139">-Mode</span></span>
<span data-ttu-id="2d735-140">Der Bereitstellungsmodus.</span><span class="sxs-lookup"><span data-stu-id="2d735-140">The deployment mode.</span></span>

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

### <span data-ttu-id="2d735-141">-Name</span><span class="sxs-lookup"><span data-stu-id="2d735-141">-Name</span></span>
<span data-ttu-id="2d735-142">Der Name der Bereitstellung, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d735-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="2d735-143">Wenn nicht angegeben, wird standardmäßig der Vorlagendateiname verwendet, wenn eine Vorlagendatei bereitgestellt wird. ist standardmäßig auf die aktuelle Uhrzeit festgelegt, zu der ein Vorlagenobjekt bereitgestellt wird, z. B. "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="2d735-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="2d735-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="2d735-144">-Pre</span></span>
<span data-ttu-id="2d735-145">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d735-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2d735-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d735-146">-ResourceGroupName</span></span>
<span data-ttu-id="2d735-147">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2d735-147">The resource group name.</span></span>

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

### <span data-ttu-id="2d735-148">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="2d735-148">-ResultFormat</span></span>
<span data-ttu-id="2d735-149">Das What-If Ergebnisformat.</span><span class="sxs-lookup"><span data-stu-id="2d735-149">The What-If result format.</span></span>

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

### <span data-ttu-id="2d735-150">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="2d735-150">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="2d735-151">Überspringt die PowerShell-Dynamische Parameterverarbeitung, die überprüft, ob der bereitgestellte Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d735-151">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="2d735-152">Bei dieser Überprüfung wird der Benutzer aufgefordert, einen Wert für die fehlenden Parameter zur Verfügung zu stellen. Wenn jedoch -SkipTemplateParameterPrompt angegeben wird, werden diese Eingabeaufforderung und der Fehler sofort ignoriert, wenn festgestellt wurde, dass ein Parameter nicht in der Vorlage gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="2d735-152">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="2d735-153">Für nicht interaktive Skripts kann -SkipTemplateParameterPrompt bereitgestellt werden, um eine bessere Fehlermeldung für den Fall zu liefern, dass nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="2d735-153">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="2d735-154">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="2d735-154">-TemplateFile</span></span>
<span data-ttu-id="2d735-155">Lokaler Pfad zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="2d735-155">Local path to the template file.</span></span> <span data-ttu-id="2d735-156">Unterstützter Vorlagendateityp: json und bicep.</span><span class="sxs-lookup"><span data-stu-id="2d735-156">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="2d735-157">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="2d735-157">-TemplateObject</span></span>
<span data-ttu-id="2d735-158">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="2d735-158">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="2d735-159">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="2d735-159">-TemplateParameterFile</span></span>
<span data-ttu-id="2d735-160">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="2d735-160">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="2d735-161">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="2d735-161">-TemplateParameterObject</span></span>
<span data-ttu-id="2d735-162">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="2d735-162">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="2d735-163">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="2d735-163">-TemplateParameterUri</span></span>
<span data-ttu-id="2d735-164">URI für die Vorlagenparameterdatei.</span><span class="sxs-lookup"><span data-stu-id="2d735-164">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="2d735-165">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="2d735-165">-TemplateUri</span></span>
<span data-ttu-id="2d735-166">URI für die Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="2d735-166">Uri to the template file.</span></span>

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

### <span data-ttu-id="2d735-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d735-167">CommonParameters</span></span>
<span data-ttu-id="2d735-168">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d735-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d735-169">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d735-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d735-170">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2d735-170">INPUTS</span></span>

### <span data-ttu-id="2d735-171">System.String</span><span class="sxs-lookup"><span data-stu-id="2d735-171">System.String</span></span>

### <span data-ttu-id="2d735-172">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="2d735-172">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="2d735-173">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2d735-173">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2d735-174">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2d735-174">OUTPUTS</span></span>

### <span data-ttu-id="2d735-175">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="2d735-175">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="2d735-176">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2d735-176">NOTES</span></span>

## <span data-ttu-id="2d735-177">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2d735-177">RELATED LINKS</span></span>
