---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentWhatIfResult.md
ms.openlocfilehash: 8e25d83eda64bb9705829ff0a8b1dd40d6055953
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172062"
---
# <span data-ttu-id="2d940-101">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="2d940-101">Get-AzTenantDeploymentWhatIfResult</span></span>

## <span data-ttu-id="2d940-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d940-102">SYNOPSIS</span></span>
<span data-ttu-id="2d940-103">Ruft eine ARM vorlagen What-If für eine Bereitstellung im Mandantenbereich ab.</span><span class="sxs-lookup"><span data-stu-id="2d940-103">Gets an ARM template What-If result for a deployment at tenant scope.</span></span> 

## <span data-ttu-id="2d940-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d940-104">SYNTAX</span></span>

### <span data-ttu-id="2d940-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d940-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d940-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2d940-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d940-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2d940-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d940-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2d940-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d940-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2d940-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d940-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2d940-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d940-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2d940-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d940-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2d940-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d940-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2d940-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d940-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2d940-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d940-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2d940-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d940-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2d940-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d940-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d940-117">DESCRIPTION</span></span>
<span data-ttu-id="2d940-118">Das **Cmdlet "Get-AzTenantDeploymentWhatIfResult"** ruft das ARM-Vorlage-What-If für eine Vorlagenbereitstellung im angegebenen Mandantenbereich ab.</span><span class="sxs-lookup"><span data-stu-id="2d940-118">The **Get-AzTenantDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified tenant scope.</span></span> <span data-ttu-id="2d940-119">Es gibt eine Liste mit Änderungen zurück, die angibt, welche Ressourcen aktualisiert werden, wenn die Bereitstellung angewendet wird, ohne Änderungen an echten Ressourcen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="2d940-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="2d940-120">Verwenden Sie den Parameter *"ResultFormat",* um das Format für das zurückgebende Ergebnis anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2d940-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="2d940-121">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2d940-121">EXAMPLES</span></span>

### <span data-ttu-id="2d940-122">Beispiel 1: Erhalten What-If Ergebnis im Mandantenbereich</span><span class="sxs-lookup"><span data-stu-id="2d940-122">Example 1: Get a What-If result at tenant scope</span></span>
```powershell
PS C:\> Get-AzTenantDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="2d940-123">Dieser Befehl ruft ein What-If im Mandantenbereich ab, indem eine benutzerdefinierte Vorlagendatei und eine Parameterdatei auf dem Datenträger verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d940-123">This command gets a What-If result at tenant scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="2d940-124">Der Befehl verwendet den Parameter *"Location",* um anzugeben, wo die Bereitstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2d940-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="2d940-125">Der Befehl verwendet den *Parameter "TemplateFile",* um eine Vorlagendatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2d940-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="2d940-126">Der Befehl verwendet den *Parameter "TemplateParameterFile",* um eine Vorlagenparameterdatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2d940-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="2d940-127">Der Befehl verwendet den *ResultFormat-Parameter,* um das What-If so zu ändern, dass vollständige Ressourcennutzlasten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="2d940-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="2d940-128">Beispiel 2: Erhalten What-If Ergebnis im Mandantenbereich mit "ResourceIdOnly"</span><span class="sxs-lookup"><span data-stu-id="2d940-128">Example 2: Get a What-If result at tenant scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzTenantDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="2d940-129">Dieser Befehl ruft ein What-If im Mandantenbereich ab, indem eine benutzerdefinierte Vorlagendatei und eine Parameterdatei auf dem Datenträger verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d940-129">This command gets a What-If result at tenant scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="2d940-130">Der Befehl verwendet den Parameter *"Location",* um anzugeben, wo die Bereitstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2d940-130">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="2d940-131">Der Befehl verwendet den *Parameter "TemplateFile",* um eine Vorlagendatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2d940-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="2d940-132">Der Befehl verwendet den *Parameter "TemplateParameterFile",* um eine Vorlagenparameterdatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2d940-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="2d940-133">Der Befehl verwendet den *Parameter "ResultFormat",* um das What-If nur Ressourcen-IDs zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="2d940-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="2d940-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d940-134">PARAMETERS</span></span>

### <span data-ttu-id="2d940-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d940-135">-DefaultProfile</span></span>
<span data-ttu-id="2d940-136">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d940-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d940-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="2d940-137">-ExcludeChangeType</span></span>
<span data-ttu-id="2d940-138">Durch Kommas getrennte Liste der Ressourcenänderungstypen, die aus den What-If ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2d940-138">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="2d940-139">-Location</span><span class="sxs-lookup"><span data-stu-id="2d940-139">-Location</span></span>
<span data-ttu-id="2d940-140">Der Speicherort zum Speichern von Bereitstellungsdaten.</span><span class="sxs-lookup"><span data-stu-id="2d940-140">The location to store deployment data.</span></span>

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

### <span data-ttu-id="2d940-141">-Name</span><span class="sxs-lookup"><span data-stu-id="2d940-141">-Name</span></span>
<span data-ttu-id="2d940-142">Der Name der Bereitstellung, die erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2d940-142">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="2d940-143">Wenn keine Angabe erfolgt, wird standardmäßig der Vorlagendateiname verwendet, wenn eine Vorlagendatei bereitgestellt wird. wird standardmäßig die aktuelle Uhrzeit verwendet, zu der ein Vorlagenobjekt bereitgestellt wird, z. B. "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="2d940-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="2d940-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="2d940-144">-Pre</span></span>
<span data-ttu-id="2d940-145">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d940-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2d940-146">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="2d940-146">-ResultFormat</span></span>
<span data-ttu-id="2d940-147">Das What-If Ergebnisformat.</span><span class="sxs-lookup"><span data-stu-id="2d940-147">The What-If result format.</span></span>

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

### <span data-ttu-id="2d940-148">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="2d940-148">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="2d940-149">Überspringt die Verarbeitung dynamischer PowerShell-Parameter, die überprüft, ob der bereitgestellte Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d940-149">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="2d940-150">Bei dieser Überprüfung müsste der Benutzer einen Wert für die fehlenden Parameter angeben. Wenn jedoch "-SkipTemplateParameterPrompt" angegeben wird, wird diese Eingabeaufforderung und der Fehler sofort ignoriert, wenn ein Parameter nicht in der Vorlage gebunden wurde.</span><span class="sxs-lookup"><span data-stu-id="2d940-150">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="2d940-151">Bei nicht interaktiven Skripts kann "-SkipTemplateParameterPrompt" bereitgestellt werden, um eine bessere Fehlermeldung für den Fall zu liefern, dass nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="2d940-151">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="2d940-152">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="2d940-152">-TemplateFile</span></span>
<span data-ttu-id="2d940-153">Lokaler Pfad zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="2d940-153">Local path to the template file.</span></span>

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

### <span data-ttu-id="2d940-154">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="2d940-154">-TemplateObject</span></span>
<span data-ttu-id="2d940-155">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="2d940-155">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="2d940-156">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="2d940-156">-TemplateParameterFile</span></span>
<span data-ttu-id="2d940-157">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="2d940-157">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="2d940-158">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="2d940-158">-TemplateParameterObject</span></span>
<span data-ttu-id="2d940-159">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="2d940-159">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="2d940-160">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="2d940-160">-TemplateParameterUri</span></span>
<span data-ttu-id="2d940-161">URI der Vorlagenparameterdatei.</span><span class="sxs-lookup"><span data-stu-id="2d940-161">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="2d940-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="2d940-162">-TemplateUri</span></span>
<span data-ttu-id="2d940-163">URI der Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="2d940-163">Uri to the template file.</span></span>

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

### <span data-ttu-id="2d940-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d940-164">CommonParameters</span></span>
<span data-ttu-id="2d940-165">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d940-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d940-166">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d940-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d940-167">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2d940-167">INPUTS</span></span>

### <span data-ttu-id="2d940-168">System.String</span><span class="sxs-lookup"><span data-stu-id="2d940-168">System.String</span></span>

### <span data-ttu-id="2d940-169">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2d940-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2d940-170">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2d940-170">OUTPUTS</span></span>

### <span data-ttu-id="2d940-171">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="2d940-171">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="2d940-172">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2d940-172">NOTES</span></span>

## <span data-ttu-id="2d940-173">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2d940-173">RELATED LINKS</span></span>
