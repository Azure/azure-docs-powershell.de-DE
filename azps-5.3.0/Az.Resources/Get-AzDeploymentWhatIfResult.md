---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
ms.openlocfilehash: 0ad3df8e010beec777bd059bbef708774570792d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459479"
---
# <span data-ttu-id="904c4-101">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="904c4-101">Get-AzDeploymentWhatIfResult</span></span>

## <span data-ttu-id="904c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="904c4-102">SYNOPSIS</span></span>
<span data-ttu-id="904c4-103">Ruft eine ARM vorlagen What-If für eine Bereitstellung im Abonnementbereich ab.</span><span class="sxs-lookup"><span data-stu-id="904c4-103">Gets an ARM template What-If result for a deployment at subscription scope.</span></span> 

## <span data-ttu-id="904c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="904c4-104">SYNTAX</span></span>

### <span data-ttu-id="904c4-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="904c4-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="904c4-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="904c4-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="904c4-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="904c4-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="904c4-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="904c4-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="904c4-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="904c4-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="904c4-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="904c4-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="904c4-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="904c4-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="904c4-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="904c4-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="904c4-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="904c4-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="904c4-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="904c4-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="904c4-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="904c4-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="904c4-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="904c4-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="904c4-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="904c4-117">DESCRIPTION</span></span>
<span data-ttu-id="904c4-118">Das **Cmdlet "Get-AzDeploymentWhatIfResult"** ruft ARM Vorlage What-If Ergebnis für eine Vorlagenbereitstellung im aktuellen Abonnementbereich ab.</span><span class="sxs-lookup"><span data-stu-id="904c4-118">The **Get-AzDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the current subscription scope.</span></span> <span data-ttu-id="904c4-119">Es gibt eine Liste mit Änderungen zurück, die angibt, welche Ressourcen aktualisiert werden, wenn die Bereitstellung angewendet wird, ohne Änderungen an echten Ressourcen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="904c4-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="904c4-120">Verwenden Sie den Parameter *"ResultFormat",* um das Format für das zurückgebende Ergebnis anzugeben.</span><span class="sxs-lookup"><span data-stu-id="904c4-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="904c4-121">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="904c4-121">EXAMPLES</span></span>

### <span data-ttu-id="904c4-122">Beispiel 1: Erhalten What-If Ergebnis im Abonnementbereich</span><span class="sxs-lookup"><span data-stu-id="904c4-122">Example 1: Get a What-If result at subscription scope</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="904c4-123">Dieser Befehl ruft ein What-If im aktuellen Abonnementbereich ab, indem eine benutzerdefinierte Vorlagendatei und eine Parameterdatei auf dem Datenträger verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="904c4-123">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="904c4-124">Der Befehl verwendet den Parameter *"Location",* um anzugeben, wo die Bereitstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="904c4-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="904c4-125">Der Befehl verwendet den *Parameter "TemplateFile",* um eine Vorlagendatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="904c4-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="904c4-126">Der Befehl verwendet den *Parameter "TemplateParameterFile",* um eine Vorlagenparameterdatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="904c4-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="904c4-127">Der Befehl verwendet den *ResultFormat-Parameter,* um das What-If so zu ändern, dass vollständige Ressourcennutzlasten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="904c4-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="904c4-128">Beispiel 2: Erhalten eines What-If im Abonnementbereich mit "ResourceIdOnly"</span><span class="sxs-lookup"><span data-stu-id="904c4-128">Example 2: Get a What-If result at subscription scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="904c4-129">Dieser Befehl ruft ein What-If im aktuellen Abonnementbereich ab, indem eine benutzerdefinierte Vorlagendatei und eine Parameterdatei auf dem Datenträger verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="904c4-129">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="904c4-130">Der Befehl verwendet den Parameter *"Location",* um anzugeben, wo die Bereitstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="904c4-130">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="904c4-131">Der Befehl verwendet den *Parameter "TemplateFile",* um eine Vorlagendatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="904c4-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="904c4-132">Der Befehl verwendet den *Parameter "TemplateParameterFile",* um eine Vorlagenparameterdatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="904c4-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="904c4-133">Der Befehl verwendet den *Parameter "ResultFormat",* um das What-If nur Ressourcen-IDs zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="904c4-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="904c4-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="904c4-134">PARAMETERS</span></span>

### <span data-ttu-id="904c4-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="904c4-135">-DefaultProfile</span></span>
<span data-ttu-id="904c4-136">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="904c4-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="904c4-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="904c4-137">-ExcludeChangeType</span></span>
<span data-ttu-id="904c4-138">Durch Kommas getrennte Liste der Ressourcenänderungstypen, die aus den What-If ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="904c4-138">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="904c4-139">-Location</span><span class="sxs-lookup"><span data-stu-id="904c4-139">-Location</span></span>
<span data-ttu-id="904c4-140">Der Speicherort zum Speichern von Bereitstellungsdaten.</span><span class="sxs-lookup"><span data-stu-id="904c4-140">The location to store deployment data.</span></span>

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

### <span data-ttu-id="904c4-141">-Name</span><span class="sxs-lookup"><span data-stu-id="904c4-141">-Name</span></span>
<span data-ttu-id="904c4-142">Der Name der Bereitstellung, die erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="904c4-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="904c4-143">Wenn keine Angabe erfolgt, wird standardmäßig der Vorlagendateiname verwendet, wenn eine Vorlagendatei bereitgestellt wird. wird standardmäßig die aktuelle Uhrzeit verwendet, zu der ein Vorlagenobjekt bereitgestellt wird, z. B. "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="904c4-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="904c4-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="904c4-144">-Pre</span></span>
<span data-ttu-id="904c4-145">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="904c4-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="904c4-146">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="904c4-146">-ResultFormat</span></span>
<span data-ttu-id="904c4-147">Das What-If Ergebnisformat.</span><span class="sxs-lookup"><span data-stu-id="904c4-147">The What-If result format.</span></span>

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

### <span data-ttu-id="904c4-148">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="904c4-148">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="904c4-149">Überspringt die Verarbeitung dynamischer PowerShell-Parameter, die überprüft, ob der bereitgestellte Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="904c4-149">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="904c4-150">Bei dieser Überprüfung müsste der Benutzer einen Wert für die fehlenden Parameter angeben. Wenn jedoch "-SkipTemplateParameterPrompt" angegeben wird, wird diese Eingabeaufforderung und der Fehler sofort ignoriert, wenn ein Parameter nicht in der Vorlage gebunden wurde.</span><span class="sxs-lookup"><span data-stu-id="904c4-150">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="904c4-151">Bei nicht interaktiven Skripts kann "-SkipTemplateParameterPrompt" bereitgestellt werden, um eine bessere Fehlermeldung für den Fall zu liefern, dass nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="904c4-151">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="904c4-152">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="904c4-152">-TemplateFile</span></span>
<span data-ttu-id="904c4-153">Lokaler Pfad zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="904c4-153">Local path to the template file.</span></span>

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

### <span data-ttu-id="904c4-154">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="904c4-154">-TemplateObject</span></span>
<span data-ttu-id="904c4-155">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="904c4-155">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="904c4-156">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="904c4-156">-TemplateParameterFile</span></span>
<span data-ttu-id="904c4-157">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="904c4-157">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="904c4-158">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="904c4-158">-TemplateParameterObject</span></span>
<span data-ttu-id="904c4-159">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="904c4-159">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="904c4-160">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="904c4-160">-TemplateParameterUri</span></span>
<span data-ttu-id="904c4-161">URI der Vorlagenparameterdatei.</span><span class="sxs-lookup"><span data-stu-id="904c4-161">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="904c4-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="904c4-162">-TemplateUri</span></span>
<span data-ttu-id="904c4-163">URI der Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="904c4-163">Uri to the template file.</span></span>

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

### <span data-ttu-id="904c4-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="904c4-164">CommonParameters</span></span>
<span data-ttu-id="904c4-165">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="904c4-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="904c4-166">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="904c4-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="904c4-167">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="904c4-167">INPUTS</span></span>

### <span data-ttu-id="904c4-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="904c4-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="904c4-169">System.String</span><span class="sxs-lookup"><span data-stu-id="904c4-169">System.String</span></span>

## <span data-ttu-id="904c4-170">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="904c4-170">OUTPUTS</span></span>

### <span data-ttu-id="904c4-171">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="904c4-171">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="904c4-172">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="904c4-172">NOTES</span></span>

## <span data-ttu-id="904c4-173">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="904c4-173">RELATED LINKS</span></span>
