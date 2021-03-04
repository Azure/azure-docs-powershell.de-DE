---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagementgroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 981d9e771a988a4166f542854959b38e140d2061
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928539"
---
# <span data-ttu-id="966ef-101">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="966ef-101">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="966ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="966ef-102">SYNOPSIS</span></span>
<span data-ttu-id="966ef-103">Ruft eine Vorlage What-If Ergebnis für eine Bereitstellung im Bereich der Verwaltungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="966ef-103">Gets a template What-If result for a deployment at management group scope.</span></span> 

## <span data-ttu-id="966ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="966ef-104">SYNTAX</span></span>

### <span data-ttu-id="966ef-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="966ef-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="966ef-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="966ef-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="966ef-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="966ef-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="966ef-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="966ef-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="966ef-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="966ef-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="966ef-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="966ef-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="966ef-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="966ef-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="966ef-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="966ef-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="966ef-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="966ef-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="966ef-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="966ef-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="966ef-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="966ef-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="966ef-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="966ef-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="966ef-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="966ef-117">DESCRIPTION</span></span>
<span data-ttu-id="966ef-118">Das **Get-AzManagementGroupDeploymentWhatIfResult-Cmdlet** ruft das ARM-Vorlagen-What-If für eine Vorlagenbereitstellung im angegebenen Verwaltungsgruppenbereich ab.</span><span class="sxs-lookup"><span data-stu-id="966ef-118">The **Get-AzManagementGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified management group scope.</span></span> <span data-ttu-id="966ef-119">Es gibt eine Liste mit Änderungen zurück, die angibt, welche Ressourcen aktualisiert werden, wenn die Bereitstellung angewendet wird, ohne Änderungen an echten Ressourcen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="966ef-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="966ef-120">Verwenden Sie den Parameter *ResultFormat,* um das Format für das zurückgebende Ergebnis anzugeben.</span><span class="sxs-lookup"><span data-stu-id="966ef-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="966ef-121">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="966ef-121">EXAMPLES</span></span>

### <span data-ttu-id="966ef-122">Beispiel 1: Erhalten eines What-If ergebnisses im Bereich der Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="966ef-122">Example 1: Get a What-If result at management group scope</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="966ef-123">Dieser Befehl ruft ein What-If ergebnis im Verwaltungsgruppenbereich ab, indem eine benutzerdefinierte Vorlagendatei und eine Parameterdatei auf dem Datenträger verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="966ef-123">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="966ef-124">Der Befehl verwendet den *Parameter Ort,* um anzugeben, wo die Bereitstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="966ef-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="966ef-125">Der Befehl verwendet den *Parameter ManagementGroupId,* um die Verwaltungsgruppe anzugeben, in der die Vorlage bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="966ef-125">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="966ef-126">Der Befehl verwendet den *Parameter TemplateFile,* um eine Vorlagendatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="966ef-126">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="966ef-127">Der Befehl verwendet den *Parameter TemplateParameterFile,* um eine Vorlagenparameterdatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="966ef-127">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="966ef-128">Der Befehl verwendet den *Parameter ResultFormat,* um das What-If ergebnis so zu legen, dass vollständige Ressourcennutzlasten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="966ef-128">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="966ef-129">Beispiel 2: Erzielen eines What-If ergebnisses im Verwaltungsgruppenbereich mit ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="966ef-129">Example 2: Get a What-If result at management group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="966ef-130">Dieser Befehl ruft ein What-If ergebnis im Verwaltungsgruppenbereich ab, indem eine benutzerdefinierte Vorlagendatei und eine Parameterdatei auf dem Datenträger verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="966ef-130">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="966ef-131">Der Befehl verwendet den *Parameter Ort,* um anzugeben, wo die Bereitstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="966ef-131">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="966ef-132">Der Befehl verwendet den *Parameter ManagementGroupId,* um die Verwaltungsgruppe anzugeben, in der die Vorlage bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="966ef-132">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="966ef-133">Der Befehl verwendet den *Parameter TemplateFile,* um eine Vorlagendatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="966ef-133">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="966ef-134">Der Befehl verwendet den *Parameter TemplateParameterFile,* um eine Vorlagenparameterdatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="966ef-134">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="966ef-135">Der Befehl verwendet den *Parameter ResultFormat,* um das ergebnis What-If nur Ressourcen-IDs zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="966ef-135">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="966ef-136">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="966ef-136">PARAMETERS</span></span>

### <span data-ttu-id="966ef-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="966ef-137">-DefaultProfile</span></span>
<span data-ttu-id="966ef-138">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="966ef-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="966ef-139">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="966ef-139">-ExcludeChangeType</span></span>
<span data-ttu-id="966ef-140">Durch Kommas getrennte Liste der Ressourcenänderungstypen, die aus den Ergebnissen What-If werden sollen.</span><span class="sxs-lookup"><span data-stu-id="966ef-140">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="966ef-141">-Location</span><span class="sxs-lookup"><span data-stu-id="966ef-141">-Location</span></span>
<span data-ttu-id="966ef-142">Der Speicherort zum Speichern von Bereitstellungsdaten.</span><span class="sxs-lookup"><span data-stu-id="966ef-142">The location to store deployment data.</span></span>

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

### <span data-ttu-id="966ef-143">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="966ef-143">-ManagementGroupId</span></span>
<span data-ttu-id="966ef-144">Die Id der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="966ef-144">The management group ID.</span></span>

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

### <span data-ttu-id="966ef-145">-Name</span><span class="sxs-lookup"><span data-stu-id="966ef-145">-Name</span></span>
<span data-ttu-id="966ef-146">Der Name der Bereitstellung, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="966ef-146">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="966ef-147">Wenn nicht angegeben, wird standardmäßig der Vorlagendateiname verwendet, wenn eine Vorlagendatei bereitgestellt wird. ist standardmäßig auf die aktuelle Uhrzeit festgelegt, zu der ein Vorlagenobjekt bereitgestellt wird, z. B. "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="966ef-147">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="966ef-148">-Pre</span><span class="sxs-lookup"><span data-stu-id="966ef-148">-Pre</span></span>
<span data-ttu-id="966ef-149">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="966ef-149">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="966ef-150">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="966ef-150">-ResultFormat</span></span>
<span data-ttu-id="966ef-151">Das What-If Ergebnisformat.</span><span class="sxs-lookup"><span data-stu-id="966ef-151">The What-If result format.</span></span>

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

### <span data-ttu-id="966ef-152">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="966ef-152">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="966ef-153">Überspringt die PowerShell-Dynamische Parameterverarbeitung, die überprüft, ob der bereitgestellte Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="966ef-153">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="966ef-154">Bei dieser Überprüfung wird der Benutzer aufgefordert, einen Wert für die fehlenden Parameter zur Verfügung zu stellen. Wenn jedoch -SkipTemplateParameterPrompt angegeben wird, werden diese Eingabeaufforderung und der Fehler sofort ignoriert, wenn festgestellt wurde, dass ein Parameter nicht in der Vorlage gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="966ef-154">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="966ef-155">Für nicht interaktive Skripts kann -SkipTemplateParameterPrompt bereitgestellt werden, um eine bessere Fehlermeldung für den Fall zu liefern, dass nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="966ef-155">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="966ef-156">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="966ef-156">-TemplateFile</span></span>
<span data-ttu-id="966ef-157">Lokaler Pfad zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="966ef-157">Local path to the template file.</span></span> <span data-ttu-id="966ef-158">Unterstützter Vorlagendateityp: json und bicep.</span><span class="sxs-lookup"><span data-stu-id="966ef-158">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="966ef-159">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="966ef-159">-TemplateObject</span></span>
<span data-ttu-id="966ef-160">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="966ef-160">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="966ef-161">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="966ef-161">-TemplateParameterFile</span></span>
<span data-ttu-id="966ef-162">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="966ef-162">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="966ef-163">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="966ef-163">-TemplateParameterObject</span></span>
<span data-ttu-id="966ef-164">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="966ef-164">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="966ef-165">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="966ef-165">-TemplateParameterUri</span></span>
<span data-ttu-id="966ef-166">URI für die Vorlagenparameterdatei.</span><span class="sxs-lookup"><span data-stu-id="966ef-166">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="966ef-167">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="966ef-167">-TemplateUri</span></span>
<span data-ttu-id="966ef-168">URI für die Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="966ef-168">Uri to the template file.</span></span>

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

### <span data-ttu-id="966ef-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="966ef-169">CommonParameters</span></span>
<span data-ttu-id="966ef-170">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="966ef-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="966ef-171">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="966ef-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="966ef-172">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="966ef-172">INPUTS</span></span>

### <span data-ttu-id="966ef-173">System.String</span><span class="sxs-lookup"><span data-stu-id="966ef-173">System.String</span></span>

### <span data-ttu-id="966ef-174">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="966ef-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="966ef-175">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="966ef-175">OUTPUTS</span></span>

### <span data-ttu-id="966ef-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="966ef-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="966ef-177">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="966ef-177">NOTES</span></span>

## <span data-ttu-id="966ef-178">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="966ef-178">RELATED LINKS</span></span>
