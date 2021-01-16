---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 09b0a1a6691b4c3d491d15d226fb8260fb7ae00e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298120"
---
# <span data-ttu-id="7d7f8-101">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="7d7f8-101">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="7d7f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d7f8-102">SYNOPSIS</span></span>
<span data-ttu-id="7d7f8-103">Ruft eine ARM vorlagen What-If für eine Bereitstellung im Bereich "Ressourcengruppe" ab.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-103">Gets an ARM template What-If result for a deployment at resource group scope.</span></span> 

## <span data-ttu-id="7d7f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d7f8-104">SYNTAX</span></span>

### <span data-ttu-id="7d7f8-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="7d7f8-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d7f8-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7d7f8-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d7f8-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7d7f8-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d7f8-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7d7f8-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d7f8-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7d7f8-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d7f8-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7d7f8-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d7f8-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7d7f8-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d7f8-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7d7f8-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d7f8-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7d7f8-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d7f8-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7d7f8-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d7f8-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="7d7f8-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d7f8-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="7d7f8-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d7f8-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d7f8-117">DESCRIPTION</span></span>
<span data-ttu-id="7d7f8-118">Das **Cmdlet "Get-AzResourceGroupDeploymentWhatIfResult"** ruft das ARM-What-If-Ergebnis für eine Vorlagenbereitstellung im angegebenen Ressourcengruppenbereich ab.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-118">The **Get-AzResourceGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified resource group scope.</span></span> <span data-ttu-id="7d7f8-119">Es gibt eine Liste mit Änderungen zurück, die angibt, welche Ressourcen aktualisiert werden, wenn die Bereitstellung angewendet wird, ohne Änderungen an echten Ressourcen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="7d7f8-120">Verwenden Sie den Parameter *"ResultFormat",* um das Format für das zurückgebende Ergebnis anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="7d7f8-121">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7d7f8-121">EXAMPLES</span></span>

### <span data-ttu-id="7d7f8-122">Beispiel 1: Erhalten eines What-If Ergebnisses im Bereich "Ressourcengruppe"</span><span class="sxs-lookup"><span data-stu-id="7d7f8-122">Example 1: Get a What-If result at resource group scope</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="7d7f8-123">Dieser Befehl ruft ein What-If ergebnis im angegebenen Ressourcengruppenbereich ab, indem eine benutzerdefinierte Vorlagendatei und eine Parameterdatei auf dem Datenträger verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-123">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="7d7f8-124">Der Befehl verwendet den *Parameter "ResourceGroupName",* um eine Ressourcengruppe anzugeben, in der die Vorlage bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-124">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="7d7f8-125">Der Befehl verwendet den *Parameter "TemplateFile",* um eine Vorlagendatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="7d7f8-126">Der Befehl verwendet den *Parameter "TemplateParameterFile",* um eine Vorlagenparameterdatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="7d7f8-127">Der Befehl verwendet den *ResultFormat-Parameter,* um das What-If so zu ändern, dass vollständige Ressourcennutzlasten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="7d7f8-128">Beispiel 2: Erhalten eines What-If Ergebnisses im Ressourcengruppenbereich mit "ResourceIdOnly"</span><span class="sxs-lookup"><span data-stu-id="7d7f8-128">Example 2: Get a What-If result at resource group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="7d7f8-129">Dieser Befehl ruft ein What-If ergebnis im angegebenen Ressourcengruppenbereich ab, indem eine benutzerdefinierte Vorlagendatei und eine Parameterdatei auf dem Datenträger verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-129">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="7d7f8-130">Der Befehl verwendet den *Parameter "ResourceGroupName",* um eine Ressourcengruppe anzugeben, in der die Vorlage bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-130">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="7d7f8-131">Der Befehl verwendet den *Parameter "TemplateFile",* um eine Vorlagendatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="7d7f8-132">Der Befehl verwendet den *Parameter "TemplateParameterFile",* um eine Vorlagenparameterdatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="7d7f8-133">Der Befehl verwendet den *Parameter "ResultFormat",* um das What-If nur Ressourcen-IDs zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="7d7f8-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d7f8-134">PARAMETERS</span></span>

### <span data-ttu-id="7d7f8-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d7f8-135">-DefaultProfile</span></span>
<span data-ttu-id="7d7f8-136">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d7f8-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="7d7f8-137">-ExcludeChangeType</span></span>
<span data-ttu-id="7d7f8-138">Durch Kommas getrennte Ressourcenänderungstypen, die aus den What-If werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-138">Comma-separated resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="7d7f8-139">-Mode</span><span class="sxs-lookup"><span data-stu-id="7d7f8-139">-Mode</span></span>
<span data-ttu-id="7d7f8-140">Der Bereitstellungsmodus.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-140">The deployment mode.</span></span>

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

### <span data-ttu-id="7d7f8-141">-Name</span><span class="sxs-lookup"><span data-stu-id="7d7f8-141">-Name</span></span>
<span data-ttu-id="7d7f8-142">Der Name der Bereitstellung, die erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="7d7f8-143">Wenn keine Angabe erfolgt, wird standardmäßig der Vorlagendateiname verwendet, wenn eine Vorlagendatei bereitgestellt wird. wird standardmäßig die aktuelle Uhrzeit verwendet, zu der ein Vorlagenobjekt bereitgestellt wird, z. B. "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="7d7f8-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="7d7f8-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="7d7f8-144">-Pre</span></span>
<span data-ttu-id="7d7f8-145">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7d7f8-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d7f8-146">-ResourceGroupName</span></span>
<span data-ttu-id="7d7f8-147">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-147">The resource group name.</span></span>

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

### <span data-ttu-id="7d7f8-148">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="7d7f8-148">-ResultFormat</span></span>
<span data-ttu-id="7d7f8-149">Das What-If Ergebnisformat.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-149">The What-If result format.</span></span>

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

### <span data-ttu-id="7d7f8-150">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="7d7f8-150">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="7d7f8-151">Überspringt die Verarbeitung dynamischer PowerShell-Parameter, die überprüft, ob der bereitgestellte Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-151">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="7d7f8-152">Bei dieser Überprüfung müsste der Benutzer einen Wert für die fehlenden Parameter angeben. Wenn jedoch "-SkipTemplateParameterPrompt" angegeben wird, wird diese Eingabeaufforderung und der Fehler sofort ignoriert, wenn ein Parameter nicht in der Vorlage gebunden wurde.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-152">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="7d7f8-153">Bei nicht interaktiven Skripts kann "-SkipTemplateParameterPrompt" bereitgestellt werden, um eine bessere Fehlermeldung für den Fall zu liefern, dass nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-153">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="7d7f8-154">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="7d7f8-154">-TemplateFile</span></span>
<span data-ttu-id="7d7f8-155">Lokaler Pfad zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-155">Local path to the template file.</span></span>

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

### <span data-ttu-id="7d7f8-156">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="7d7f8-156">-TemplateObject</span></span>
<span data-ttu-id="7d7f8-157">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-157">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="7d7f8-158">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="7d7f8-158">-TemplateParameterFile</span></span>
<span data-ttu-id="7d7f8-159">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-159">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="7d7f8-160">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="7d7f8-160">-TemplateParameterObject</span></span>
<span data-ttu-id="7d7f8-161">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-161">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="7d7f8-162">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="7d7f8-162">-TemplateParameterUri</span></span>
<span data-ttu-id="7d7f8-163">URI der Vorlagenparameterdatei.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-163">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="7d7f8-164">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="7d7f8-164">-TemplateUri</span></span>
<span data-ttu-id="7d7f8-165">URI der Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-165">Uri to the template file.</span></span>

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

### <span data-ttu-id="7d7f8-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d7f8-166">CommonParameters</span></span>
<span data-ttu-id="7d7f8-167">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d7f8-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d7f8-168">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d7f8-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d7f8-169">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7d7f8-169">INPUTS</span></span>

### <span data-ttu-id="7d7f8-170">System.String</span><span class="sxs-lookup"><span data-stu-id="7d7f8-170">System.String</span></span>

### <span data-ttu-id="7d7f8-171">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="7d7f8-171">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="7d7f8-172">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7d7f8-172">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7d7f8-173">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7d7f8-173">OUTPUTS</span></span>

### <span data-ttu-id="7d7f8-174">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="7d7f8-174">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="7d7f8-175">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7d7f8-175">NOTES</span></span>

## <span data-ttu-id="7d7f8-176">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7d7f8-176">RELATED LINKS</span></span>
