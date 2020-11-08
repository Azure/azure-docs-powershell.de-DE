---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 39b652f1e6096f74da8d23baee10cd5b2ce54b6d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174430"
---
# <span data-ttu-id="72fec-101">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="72fec-101">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="72fec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72fec-102">SYNOPSIS</span></span>
<span data-ttu-id="72fec-103">Ruft eine Arm-Vorlage What-If Ergebnis für eine Bereitstellung im Bereich der Verwaltungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="72fec-103">Gets an ARM template What-If result for a deployment at management group scope.</span></span> 

## <span data-ttu-id="72fec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72fec-104">SYNTAX</span></span>

### <span data-ttu-id="72fec-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="72fec-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="72fec-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="72fec-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72fec-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="72fec-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72fec-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="72fec-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72fec-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="72fec-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72fec-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="72fec-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72fec-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="72fec-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72fec-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="72fec-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72fec-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="72fec-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72fec-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="72fec-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72fec-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="72fec-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="72fec-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="72fec-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72fec-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72fec-117">DESCRIPTION</span></span>
<span data-ttu-id="72fec-118">Das Cmdlet " **Get-AzManagementGroupDeploymentWhatIfResult** " Ruft die Arm-Vorlage What-If Ergebnis für eine Vorlagenbereitstellung im angegebenen Verwaltungsgruppen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="72fec-118">The **Get-AzManagementGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified management group scope.</span></span> <span data-ttu-id="72fec-119">Sie gibt eine Liste der Änderungen zurück, die angibt, welche Ressourcen aktualisiert werden, wenn die Bereitstellung angewendet wird, ohne dass Änderungen an realen Ressourcen vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="72fec-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="72fec-120">Wenn Sie das Format für das Ergebnis der Rückgabe angeben möchten, verwenden Sie den Parameter *ResultFormat* .</span><span class="sxs-lookup"><span data-stu-id="72fec-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="72fec-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72fec-121">EXAMPLES</span></span>

### <span data-ttu-id="72fec-122">Beispiel 1: Abrufen eines What-If Ergebnisses im Verwaltungsgruppen Bereich</span><span class="sxs-lookup"><span data-stu-id="72fec-122">Example 1: Get a What-If result at management group scope</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="72fec-123">Mit diesem Befehl wird ein What-If Ergebnis im Verwaltungsgruppen Bereich unter Verwendung einer benutzerdefinierten Vorlagendatei und einer Parameterdatei auf dem Datenträger abgerufen.</span><span class="sxs-lookup"><span data-stu-id="72fec-123">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="72fec-124">Der Befehl verwendet den *Location* -Parameter, um anzugeben, wo die Bereitstellungsdaten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="72fec-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="72fec-125">Der Befehl gibt mithilfe des *ManagementGroupId* -Parameters die Verwaltungsgruppe an, in der die Vorlage bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="72fec-125">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="72fec-126">Der Befehl verwendet den *Templatedatei* -Parameter, um eine Vorlagendatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="72fec-126">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="72fec-127">Der Befehl gibt mithilfe des *TemplateParameterFile* -Parameters eine Vorlagenparameter Datei an.</span><span class="sxs-lookup"><span data-stu-id="72fec-127">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="72fec-128">Der Befehl legt mithilfe des *ResultFormat* -Parameters das What-If Ergebnis auf vollständige Ressourcen Nutzlasten ein.</span><span class="sxs-lookup"><span data-stu-id="72fec-128">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="72fec-129">Beispiel 2: Abrufen eines What-If Ergebnisses im Verwaltungsgruppen Bereich mit ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="72fec-129">Example 2: Get a What-If result at management group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="72fec-130">Mit diesem Befehl wird ein What-If Ergebnis im Verwaltungsgruppen Bereich unter Verwendung einer benutzerdefinierten Vorlagendatei und einer Parameterdatei auf dem Datenträger abgerufen.</span><span class="sxs-lookup"><span data-stu-id="72fec-130">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="72fec-131">Der Befehl verwendet den *Location* -Parameter, um anzugeben, wo die Bereitstellungsdaten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="72fec-131">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="72fec-132">Der Befehl gibt mithilfe des *ManagementGroupId* -Parameters die Verwaltungsgruppe an, in der die Vorlage bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="72fec-132">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="72fec-133">Der Befehl verwendet den *Templatedatei* -Parameter, um eine Vorlagendatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="72fec-133">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="72fec-134">Der Befehl gibt mithilfe des *TemplateParameterFile* -Parameters eine Vorlagenparameter Datei an.</span><span class="sxs-lookup"><span data-stu-id="72fec-134">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="72fec-135">Der Befehl verwendet den *ResultFormat* -Parameter, um das What-If Ergebnis so zu definieren, dass nur Ressourcen-IDs enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="72fec-135">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="72fec-136">Parameter</span><span class="sxs-lookup"><span data-stu-id="72fec-136">PARAMETERS</span></span>

### <span data-ttu-id="72fec-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="72fec-137">-ApiVersion</span></span>
<span data-ttu-id="72fec-138">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="72fec-138">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="72fec-139">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="72fec-139">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="72fec-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72fec-140">-DefaultProfile</span></span>
<span data-ttu-id="72fec-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="72fec-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72fec-142">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="72fec-142">-ExcludeChangeType</span></span>
<span data-ttu-id="72fec-143">Durch trennzeichengetrennte Liste der Ressourcen Änderungstypen, die von What-If Ergebnissen ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="72fec-143">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="72fec-144">-Standort</span><span class="sxs-lookup"><span data-stu-id="72fec-144">-Location</span></span>
<span data-ttu-id="72fec-145">Der Speicherort, an dem Bereitstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="72fec-145">The location to store deployment data.</span></span>

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

### <span data-ttu-id="72fec-146">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="72fec-146">-ManagementGroupId</span></span>
<span data-ttu-id="72fec-147">Die Verwaltungsgruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="72fec-147">The management group ID.</span></span>

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

### <span data-ttu-id="72fec-148">-Name</span><span class="sxs-lookup"><span data-stu-id="72fec-148">-Name</span></span>
<span data-ttu-id="72fec-149">Der Name der Bereitstellung, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="72fec-149">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="72fec-150">Wenn nicht angegeben, wird standardmäßig der Name der Vorlagendatei verwendet, wenn eine Vorlagendatei bereitgestellt wird. Standardmäßig wird die aktuelle Uhrzeit verwendet, zu der ein Vorlagenobjekt bereitgestellt wird, beispielsweise "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="72fec-150">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="72fec-151">-Pre</span><span class="sxs-lookup"><span data-stu-id="72fec-151">-Pre</span></span>
<span data-ttu-id="72fec-152">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="72fec-152">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="72fec-153">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="72fec-153">-ResultFormat</span></span>
<span data-ttu-id="72fec-154">Das What-If Ergebnisformat.</span><span class="sxs-lookup"><span data-stu-id="72fec-154">The What-If result format.</span></span>

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

### <span data-ttu-id="72fec-155">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="72fec-155">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="72fec-156">Überspringt die dynamische PowerShell-Parameterverarbeitung, die überprüft, ob der angegebene Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72fec-156">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="72fec-157">Mit dieser Prüfung wird der Benutzer aufgefordert, einen Wert für die fehlenden Parameter bereitzustellen, doch die Bereitstellung von-SkipTemplateParameterPrompt ignoriert diese Eingabeaufforderung und ist sofort fehlerhaft, wenn ein Parameter gefunden wurde, der in der Vorlage nicht gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="72fec-157">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="72fec-158">Für nicht interaktive Skripts kann-SkipTemplateParameterPrompt bereitgestellt werden, um eine bessere Fehlermeldung bereitzustellen, falls nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="72fec-158">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="72fec-159">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="72fec-159">-TemplateFile</span></span>
<span data-ttu-id="72fec-160">Lokaler Pfad zur Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="72fec-160">Local path to the template file.</span></span>

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

### <span data-ttu-id="72fec-161">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="72fec-161">-TemplateObject</span></span>
<span data-ttu-id="72fec-162">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="72fec-162">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="72fec-163">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="72fec-163">-TemplateParameterFile</span></span>
<span data-ttu-id="72fec-164">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="72fec-164">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="72fec-165">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="72fec-165">-TemplateParameterObject</span></span>
<span data-ttu-id="72fec-166">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="72fec-166">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="72fec-167">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="72fec-167">-TemplateParameterUri</span></span>
<span data-ttu-id="72fec-168">URI zur Vorlagenparameter Datei.</span><span class="sxs-lookup"><span data-stu-id="72fec-168">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="72fec-169">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="72fec-169">-TemplateUri</span></span>
<span data-ttu-id="72fec-170">URI zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="72fec-170">Uri to the template file.</span></span>

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

### <span data-ttu-id="72fec-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72fec-171">CommonParameters</span></span>
<span data-ttu-id="72fec-172">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72fec-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72fec-173">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72fec-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72fec-174">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72fec-174">INPUTS</span></span>

### <span data-ttu-id="72fec-175">System. String</span><span class="sxs-lookup"><span data-stu-id="72fec-175">System.String</span></span>

### <span data-ttu-id="72fec-176">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="72fec-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="72fec-177">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72fec-177">OUTPUTS</span></span>

### <span data-ttu-id="72fec-178">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. Deployments. PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="72fec-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="72fec-179">Notizen</span><span class="sxs-lookup"><span data-stu-id="72fec-179">NOTES</span></span>

## <span data-ttu-id="72fec-180">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72fec-180">RELATED LINKS</span></span>
