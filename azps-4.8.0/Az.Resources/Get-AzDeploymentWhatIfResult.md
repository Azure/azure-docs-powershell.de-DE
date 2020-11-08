---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
ms.openlocfilehash: 15dcc77a616037d6190fa11be34b8bc8f762aa59
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165009"
---
# <span data-ttu-id="c9248-101">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="c9248-101">Get-AzDeploymentWhatIfResult</span></span>

## <span data-ttu-id="c9248-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c9248-102">SYNOPSIS</span></span>
<span data-ttu-id="c9248-103">Ruft eine Arm-Vorlage What-If Ergebnis für eine Bereitstellung im Abonnement Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="c9248-103">Gets an ARM template What-If result for a deployment at subscription scope.</span></span> 

## <span data-ttu-id="c9248-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9248-104">SYNTAX</span></span>

### <span data-ttu-id="c9248-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="c9248-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9248-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c9248-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9248-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c9248-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9248-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c9248-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9248-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c9248-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9248-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c9248-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9248-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c9248-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9248-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c9248-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9248-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c9248-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9248-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c9248-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9248-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c9248-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9248-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c9248-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9248-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9248-117">DESCRIPTION</span></span>
<span data-ttu-id="c9248-118">Das Cmdlet " **Get-AzDeploymentWhatIfResult** " Ruft die Arm-Vorlage What-If Ergebnis für eine Vorlagenbereitstellung im aktuellen Abonnement Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="c9248-118">The **Get-AzDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the current subscription scope.</span></span> <span data-ttu-id="c9248-119">Sie gibt eine Liste der Änderungen zurück, die angibt, welche Ressourcen aktualisiert werden, wenn die Bereitstellung angewendet wird, ohne dass Änderungen an realen Ressourcen vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="c9248-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="c9248-120">Wenn Sie das Format für das Ergebnis der Rückgabe angeben möchten, verwenden Sie den Parameter *ResultFormat* .</span><span class="sxs-lookup"><span data-stu-id="c9248-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="c9248-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9248-121">EXAMPLES</span></span>

### <span data-ttu-id="c9248-122">Beispiel 1: Abrufen eines What-If Ergebnisses im Abonnement Bereich</span><span class="sxs-lookup"><span data-stu-id="c9248-122">Example 1: Get a What-If result at subscription scope</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="c9248-123">Dieser Befehl ruft mit einer benutzerdefinierten Vorlagendatei und einer Parameterdatei auf dem Datenträger ein What-If Ergebnis im aktuellen Abonnement Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="c9248-123">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="c9248-124">Der Befehl verwendet den *Location* -Parameter, um anzugeben, wo die Bereitstellungsdaten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c9248-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="c9248-125">Der Befehl verwendet den *Templatedatei* -Parameter, um eine Vorlagendatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c9248-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="c9248-126">Der Befehl gibt mithilfe des *TemplateParameterFile* -Parameters eine Vorlagenparameter Datei an.</span><span class="sxs-lookup"><span data-stu-id="c9248-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="c9248-127">Der Befehl legt mithilfe des *ResultFormat* -Parameters das What-If Ergebnis auf vollständige Ressourcen Nutzlasten ein.</span><span class="sxs-lookup"><span data-stu-id="c9248-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="c9248-128">Beispiel 2: Abrufen eines What-If Ergebnisses im Abonnement Bereich mit ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="c9248-128">Example 2: Get a What-If result at subscription scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="c9248-129">Dieser Befehl ruft mit einer benutzerdefinierten Vorlagendatei und einer Parameterdatei auf dem Datenträger ein What-If Ergebnis im aktuellen Abonnement Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="c9248-129">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="c9248-130">Der Befehl verwendet den *Location* -Parameter, um anzugeben, wo die Bereitstellungsdaten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c9248-130">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="c9248-131">Der Befehl verwendet den *Templatedatei* -Parameter, um eine Vorlagendatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c9248-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="c9248-132">Der Befehl gibt mithilfe des *TemplateParameterFile* -Parameters eine Vorlagenparameter Datei an.</span><span class="sxs-lookup"><span data-stu-id="c9248-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="c9248-133">Der Befehl verwendet den *ResultFormat* -Parameter, um das What-If Ergebnis so zu definieren, dass nur Ressourcen-IDs enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c9248-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="c9248-134">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9248-134">PARAMETERS</span></span>

### <span data-ttu-id="c9248-135">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c9248-135">-ApiVersion</span></span>
<span data-ttu-id="c9248-136">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c9248-136">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c9248-137">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c9248-137">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c9248-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9248-138">-DefaultProfile</span></span>
<span data-ttu-id="c9248-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c9248-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9248-140">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="c9248-140">-ExcludeChangeType</span></span>
<span data-ttu-id="c9248-141">Durch trennzeichengetrennte Liste der Ressourcen Änderungstypen, die von What-If Ergebnissen ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c9248-141">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="c9248-142">-Standort</span><span class="sxs-lookup"><span data-stu-id="c9248-142">-Location</span></span>
<span data-ttu-id="c9248-143">Der Speicherort, an dem Bereitstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c9248-143">The location to store deployment data.</span></span>

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

### <span data-ttu-id="c9248-144">-Name</span><span class="sxs-lookup"><span data-stu-id="c9248-144">-Name</span></span>
<span data-ttu-id="c9248-145">Der Name der Bereitstellung, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9248-145">The name of the deployment it's going to create.</span></span> <span data-ttu-id="c9248-146">Wenn nicht angegeben, wird standardmäßig der Name der Vorlagendatei verwendet, wenn eine Vorlagendatei bereitgestellt wird. Standardmäßig wird die aktuelle Uhrzeit verwendet, zu der ein Vorlagenobjekt bereitgestellt wird, beispielsweise "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="c9248-146">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="c9248-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="c9248-147">-Pre</span></span>
<span data-ttu-id="c9248-148">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="c9248-148">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c9248-149">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="c9248-149">-ResultFormat</span></span>
<span data-ttu-id="c9248-150">Das What-If Ergebnisformat.</span><span class="sxs-lookup"><span data-stu-id="c9248-150">The What-If result format.</span></span>

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

### <span data-ttu-id="c9248-151">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="c9248-151">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="c9248-152">Überspringt die dynamische PowerShell-Parameterverarbeitung, die überprüft, ob der angegebene Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9248-152">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="c9248-153">Mit dieser Prüfung wird der Benutzer aufgefordert, einen Wert für die fehlenden Parameter bereitzustellen, doch die Bereitstellung von-SkipTemplateParameterPrompt ignoriert diese Eingabeaufforderung und ist sofort fehlerhaft, wenn ein Parameter gefunden wurde, der in der Vorlage nicht gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9248-153">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="c9248-154">Für nicht interaktive Skripts kann-SkipTemplateParameterPrompt bereitgestellt werden, um eine bessere Fehlermeldung bereitzustellen, falls nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="c9248-154">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="c9248-155">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="c9248-155">-TemplateFile</span></span>
<span data-ttu-id="c9248-156">Lokaler Pfad zur Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="c9248-156">Local path to the template file.</span></span>

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

### <span data-ttu-id="c9248-157">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="c9248-157">-TemplateObject</span></span>
<span data-ttu-id="c9248-158">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="c9248-158">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="c9248-159">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="c9248-159">-TemplateParameterFile</span></span>
<span data-ttu-id="c9248-160">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="c9248-160">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="c9248-161">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="c9248-161">-TemplateParameterObject</span></span>
<span data-ttu-id="c9248-162">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="c9248-162">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="c9248-163">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="c9248-163">-TemplateParameterUri</span></span>
<span data-ttu-id="c9248-164">URI zur Vorlagenparameter Datei.</span><span class="sxs-lookup"><span data-stu-id="c9248-164">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="c9248-165">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="c9248-165">-TemplateUri</span></span>
<span data-ttu-id="c9248-166">URI zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="c9248-166">Uri to the template file.</span></span>

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

### <span data-ttu-id="c9248-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9248-167">CommonParameters</span></span>
<span data-ttu-id="c9248-168">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9248-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9248-169">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9248-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9248-170">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c9248-170">INPUTS</span></span>

### <span data-ttu-id="c9248-171">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c9248-171">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c9248-172">System. String</span><span class="sxs-lookup"><span data-stu-id="c9248-172">System.String</span></span>

## <span data-ttu-id="c9248-173">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c9248-173">OUTPUTS</span></span>

### <span data-ttu-id="c9248-174">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. Deployments. PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="c9248-174">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="c9248-175">Notizen</span><span class="sxs-lookup"><span data-stu-id="c9248-175">NOTES</span></span>

## <span data-ttu-id="c9248-176">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c9248-176">RELATED LINKS</span></span>
