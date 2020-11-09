---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
ms.openlocfilehash: df199c25a210a4975eccf96f9f7aa7e6c219689c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301174"
---
# <span data-ttu-id="b0abb-101">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="b0abb-101">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="b0abb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b0abb-102">SYNOPSIS</span></span>
<span data-ttu-id="b0abb-103">Ruft eine Arm-Vorlage What-If Ergebnis für eine Bereitstellung im Bereich der Verwaltungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="b0abb-103">Gets an ARM template What-If result for a deployment at management group scope.</span></span> 

## <span data-ttu-id="b0abb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0abb-104">SYNTAX</span></span>

### <span data-ttu-id="b0abb-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="b0abb-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0abb-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b0abb-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0abb-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b0abb-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0abb-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b0abb-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0abb-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b0abb-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0abb-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b0abb-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0abb-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b0abb-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0abb-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b0abb-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0abb-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b0abb-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0abb-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b0abb-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0abb-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b0abb-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0abb-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b0abb-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0abb-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0abb-117">DESCRIPTION</span></span>
<span data-ttu-id="b0abb-118">Das Cmdlet " **Get-AzManagementGroupDeploymentWhatIfResult** " Ruft die Arm-Vorlage What-If Ergebnis für eine Vorlagenbereitstellung im angegebenen Verwaltungsgruppen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="b0abb-118">The **Get-AzManagementGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified management group scope.</span></span> <span data-ttu-id="b0abb-119">Sie gibt eine Liste der Änderungen zurück, die angibt, welche Ressourcen aktualisiert werden, wenn die Bereitstellung angewendet wird, ohne dass Änderungen an realen Ressourcen vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="b0abb-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="b0abb-120">Wenn Sie das Format für das Ergebnis der Rückgabe angeben möchten, verwenden Sie den Parameter *ResultFormat* .</span><span class="sxs-lookup"><span data-stu-id="b0abb-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="b0abb-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0abb-121">EXAMPLES</span></span>

### <span data-ttu-id="b0abb-122">Beispiel 1: Abrufen eines What-If Ergebnisses im Verwaltungsgruppen Bereich</span><span class="sxs-lookup"><span data-stu-id="b0abb-122">Example 1: Get a What-If result at management group scope</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="b0abb-123">Mit diesem Befehl wird ein What-If Ergebnis im Verwaltungsgruppen Bereich unter Verwendung einer benutzerdefinierten Vorlagendatei und einer Parameterdatei auf dem Datenträger abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b0abb-123">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="b0abb-124">Der Befehl verwendet den *Location* -Parameter, um anzugeben, wo die Bereitstellungsdaten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b0abb-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="b0abb-125">Der Befehl gibt mithilfe des *ManagementGroupId* -Parameters die Verwaltungsgruppe an, in der die Vorlage bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b0abb-125">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="b0abb-126">Der Befehl verwendet den *Templatedatei* -Parameter, um eine Vorlagendatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b0abb-126">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="b0abb-127">Der Befehl gibt mithilfe des *TemplateParameterFile* -Parameters eine Vorlagenparameter Datei an.</span><span class="sxs-lookup"><span data-stu-id="b0abb-127">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="b0abb-128">Der Befehl legt mithilfe des *ResultFormat* -Parameters das What-If Ergebnis auf vollständige Ressourcen Nutzlasten ein.</span><span class="sxs-lookup"><span data-stu-id="b0abb-128">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="b0abb-129">Beispiel 2: Abrufen eines What-If Ergebnisses im Verwaltungsgruppen Bereich mit ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="b0abb-129">Example 2: Get a What-If result at management group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="b0abb-130">Mit diesem Befehl wird ein What-If Ergebnis im Verwaltungsgruppen Bereich unter Verwendung einer benutzerdefinierten Vorlagendatei und einer Parameterdatei auf dem Datenträger abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b0abb-130">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="b0abb-131">Der Befehl verwendet den *Location* -Parameter, um anzugeben, wo die Bereitstellungsdaten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b0abb-131">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="b0abb-132">Der Befehl gibt mithilfe des *ManagementGroupId* -Parameters die Verwaltungsgruppe an, in der die Vorlage bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b0abb-132">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="b0abb-133">Der Befehl verwendet den *Templatedatei* -Parameter, um eine Vorlagendatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b0abb-133">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="b0abb-134">Der Befehl gibt mithilfe des *TemplateParameterFile* -Parameters eine Vorlagenparameter Datei an.</span><span class="sxs-lookup"><span data-stu-id="b0abb-134">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="b0abb-135">Der Befehl verwendet den *ResultFormat* -Parameter, um das What-If Ergebnis so zu definieren, dass nur Ressourcen-IDs enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b0abb-135">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="b0abb-136">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0abb-136">PARAMETERS</span></span>

### <span data-ttu-id="b0abb-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0abb-137">-DefaultProfile</span></span>
<span data-ttu-id="b0abb-138">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b0abb-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0abb-139">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="b0abb-139">-ExcludeChangeType</span></span>
<span data-ttu-id="b0abb-140">Durch trennzeichengetrennte Liste der Ressourcen Änderungstypen, die von What-If Ergebnissen ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b0abb-140">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="b0abb-141">-Standort</span><span class="sxs-lookup"><span data-stu-id="b0abb-141">-Location</span></span>
<span data-ttu-id="b0abb-142">Der Speicherort, an dem Bereitstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b0abb-142">The location to store deployment data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0abb-143">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="b0abb-143">-ManagementGroupId</span></span>
<span data-ttu-id="b0abb-144">Die Verwaltungsgruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="b0abb-144">The management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0abb-145">-Name</span><span class="sxs-lookup"><span data-stu-id="b0abb-145">-Name</span></span>
<span data-ttu-id="b0abb-146">Der Name der Bereitstellung, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0abb-146">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="b0abb-147">Wenn nicht angegeben, wird standardmäßig der Name der Vorlagendatei verwendet, wenn eine Vorlagendatei bereitgestellt wird. Standardmäßig wird die aktuelle Uhrzeit verwendet, zu der ein Vorlagenobjekt bereitgestellt wird, beispielsweise "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="b0abb-147">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0abb-148">-Pre</span><span class="sxs-lookup"><span data-stu-id="b0abb-148">-Pre</span></span>
<span data-ttu-id="b0abb-149">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="b0abb-149">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b0abb-150">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="b0abb-150">-ResultFormat</span></span>
<span data-ttu-id="b0abb-151">Das What-If Ergebnisformat.</span><span class="sxs-lookup"><span data-stu-id="b0abb-151">The What-If result format.</span></span>

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

### <span data-ttu-id="b0abb-152">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="b0abb-152">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="b0abb-153">Überspringt die dynamische PowerShell-Parameterverarbeitung, die überprüft, ob der angegebene Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b0abb-153">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="b0abb-154">Mit dieser Prüfung wird der Benutzer aufgefordert, einen Wert für die fehlenden Parameter bereitzustellen, doch die Bereitstellung von-SkipTemplateParameterPrompt ignoriert diese Eingabeaufforderung und ist sofort fehlerhaft, wenn ein Parameter gefunden wurde, der in der Vorlage nicht gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0abb-154">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="b0abb-155">Für nicht interaktive Skripts kann-SkipTemplateParameterPrompt bereitgestellt werden, um eine bessere Fehlermeldung bereitzustellen, falls nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="b0abb-155">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="b0abb-156">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="b0abb-156">-TemplateFile</span></span>
<span data-ttu-id="b0abb-157">Lokaler Pfad zur Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="b0abb-157">Local path to the template file.</span></span>

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

### <span data-ttu-id="b0abb-158">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="b0abb-158">-TemplateObject</span></span>
<span data-ttu-id="b0abb-159">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="b0abb-159">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="b0abb-160">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="b0abb-160">-TemplateParameterFile</span></span>
<span data-ttu-id="b0abb-161">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="b0abb-161">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="b0abb-162">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="b0abb-162">-TemplateParameterObject</span></span>
<span data-ttu-id="b0abb-163">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="b0abb-163">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="b0abb-164">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="b0abb-164">-TemplateParameterUri</span></span>
<span data-ttu-id="b0abb-165">URI zur Vorlagenparameter Datei.</span><span class="sxs-lookup"><span data-stu-id="b0abb-165">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="b0abb-166">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="b0abb-166">-TemplateUri</span></span>
<span data-ttu-id="b0abb-167">URI zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="b0abb-167">Uri to the template file.</span></span>

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

### <span data-ttu-id="b0abb-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0abb-168">CommonParameters</span></span>
<span data-ttu-id="b0abb-169">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0abb-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0abb-170">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0abb-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0abb-171">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b0abb-171">INPUTS</span></span>

### <span data-ttu-id="b0abb-172">System. String</span><span class="sxs-lookup"><span data-stu-id="b0abb-172">System.String</span></span>

### <span data-ttu-id="b0abb-173">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b0abb-173">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b0abb-174">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b0abb-174">OUTPUTS</span></span>

### <span data-ttu-id="b0abb-175">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. Deployments. PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="b0abb-175">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="b0abb-176">Notizen</span><span class="sxs-lookup"><span data-stu-id="b0abb-176">NOTES</span></span>

## <span data-ttu-id="b0abb-177">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b0abb-177">RELATED LINKS</span></span>
