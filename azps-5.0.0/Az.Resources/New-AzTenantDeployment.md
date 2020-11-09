---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
ms.openlocfilehash: 8135dc4c4bdb6eb21761dbf5cb7ecea216a81593
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303351"
---
# <span data-ttu-id="65936-101">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="65936-101">New-AzTenantDeployment</span></span>

## <span data-ttu-id="65936-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65936-102">SYNOPSIS</span></span>
<span data-ttu-id="65936-103">Erstellen einer Bereitstellung im MANDANTENBEREICH</span><span class="sxs-lookup"><span data-stu-id="65936-103">Create a deployment at tenant scope</span></span>

## <span data-ttu-id="65936-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65936-104">SYNTAX</span></span>

### <span data-ttu-id="65936-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="65936-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65936-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="65936-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65936-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="65936-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65936-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="65936-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65936-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="65936-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65936-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="65936-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65936-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="65936-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65936-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="65936-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65936-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="65936-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65936-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="65936-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65936-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="65936-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65936-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="65936-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65936-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65936-117">DESCRIPTION</span></span>
<span data-ttu-id="65936-118">Mit dem Cmdlet **New-AzTenantDeployment** wird eine Bereitstellung im aktuellen MANDANTENBEREICH hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="65936-118">The **New-AzTenantDeployment** cmdlet adds a deployment at the current tenant scope.</span></span>

<span data-ttu-id="65936-119">Wenn Sie eine Bereitstellung im MANDANTENBEREICH hinzufügen möchten, geben Sie den Speicherort und eine Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="65936-119">To add a deployment at tenant scope, specify the location and a template.</span></span>
<span data-ttu-id="65936-120">Der Speicherort weist Azure Resource Manager an, wo die Bereitstellungsdaten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="65936-120">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="65936-121">Bei der Vorlage handelt es sich um eine JSON-Zeichenfolge, die einzelne Ressourcen enthält, die bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="65936-121">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="65936-122">Die Vorlage enthält Parameterplatzhalter für erforderliche Ressourcen und konfigurierbare Eigenschaftswerte wie Namen und Größen.</span><span class="sxs-lookup"><span data-stu-id="65936-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="65936-123">Wenn Sie eine benutzerdefinierte Vorlage für die Bereitstellung verwenden möchten, geben Sie den Parameter " *Templatedatei* " oder " *TemplateUri* " an.</span><span class="sxs-lookup"><span data-stu-id="65936-123">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="65936-124">Jede Vorlage verfügt über Parameter für konfigurierbare Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="65936-124">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="65936-125">Wenn Sie Werte für die Vorlagenparameter angeben möchten, geben Sie den *TemplateParameterFile* -Parameter oder den *TemplateParameterObject* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="65936-125">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="65936-126">Alternativ können Sie die Vorlagenparameter verwenden, die dem Befehl dynamisch hinzugefügt werden, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="65936-126">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="65936-127">Wenn Sie dynamische Parameter verwenden möchten, geben Sie Sie an der Eingabeaufforderung ein, oder geben Sie ein Minuszeichen (-) ein, um einen Parameter anzugeben, und verwenden Sie die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="65936-127">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="65936-128">Vorlagenparameter Werte, die Sie an der Eingabeaufforderung eingeben, haben Vorrang vor Werten in einem Vorlagenparameter Objekt oder einer Datei.</span><span class="sxs-lookup"><span data-stu-id="65936-128">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="65936-129">Verwenden Sie zum Hinzufügen von Ressourcen zu einer Ressourcengruppe das **New-AzResourceGroupDeployment-** Objekt, das eine Bereitstellung in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="65936-129">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="65936-130">Verwenden Sie zum Hinzufügen von Ressourcen zu einem Abonnement das **New-AzSubscriptionDeployment-** Projekt, das eine Bereitstellung im Abonnement Bereich erstellt, in dem die Ressourcen auf Abonnementebene bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="65936-130">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="65936-131">Wenn Sie Ressourcen in einer Verwaltungsgruppe hinzufügen möchten, verwenden Sie die **New-AzManagementGroupDeployment** , die eine Bereitstellung in einer Verwaltungsgruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="65936-131">To add resources at a management group, use the **New-AzManagementGroupDeployment** which creates a deployment at a management group.</span></span>

## <span data-ttu-id="65936-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65936-132">EXAMPLES</span></span>

### <span data-ttu-id="65936-133">Beispiel 1: Verwenden einer benutzerdefinierten Vorlage und einer Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="65936-133">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="65936-134">Dieser Befehl erstellt eine neue Bereitstellung im aktuellen MANDANTENBEREICH unter Verwendung einer benutzerdefinierten Vorlage und einer Vorlagendatei auf dem Datenträger mit dem Parameter für definierte Tags.</span><span class="sxs-lookup"><span data-stu-id="65936-134">This command creates a new deployment at the current tenant scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="65936-135">Der Befehl verwendet den *Templatedatei* -Parameter, um die Vorlage und den *TemplateParameterFile* -Parameter anzugeben, um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="65936-135">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="65936-136">Beispiel 2: Verwenden eines benutzerdefinierten Vorlagenobjekts und einer Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="65936-136">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="65936-137">Mit diesem Befehl wird eine neue Bereitstellung beim aktuellen Mandanten mithilfe einer benutzerdefinierten Vorlage und einer Vorlagendatei auf einem Datenträger erstellt, die in eine Arbeitsspeicher-Hashtable konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="65936-137">This command creates a new deployment at the current tenant by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="65936-138">Mit den ersten beiden Befehlen wird der Text für die Vorlagendatei auf dem Datenträger gelesen und in eine Arbeitsspeicher-Hashtable konvertiert.</span><span class="sxs-lookup"><span data-stu-id="65936-138">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="65936-139">Der letzte Befehl verwendet den *templateobject* -Parameter zum Angeben dieser Hashtable und des *TemplateParameterFile* -Parameters, um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="65936-139">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="65936-140">Parameter</span><span class="sxs-lookup"><span data-stu-id="65936-140">PARAMETERS</span></span>

### <span data-ttu-id="65936-141">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65936-141">-AsJob</span></span>
<span data-ttu-id="65936-142">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="65936-142">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65936-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65936-143">-DefaultProfile</span></span>
<span data-ttu-id="65936-144">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="65936-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65936-145">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="65936-145">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="65936-146">Die Debug-Protokollebene der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="65936-146">The deployment debug log level.</span></span>

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

### <span data-ttu-id="65936-147">-Standort</span><span class="sxs-lookup"><span data-stu-id="65936-147">-Location</span></span>
<span data-ttu-id="65936-148">Der Speicherort, an dem Bereitstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="65936-148">The location to store deployment data.</span></span>

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

### <span data-ttu-id="65936-149">-Name</span><span class="sxs-lookup"><span data-stu-id="65936-149">-Name</span></span>
<span data-ttu-id="65936-150">Der Name der Bereitstellung, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="65936-150">The name of the deployment it's going to create.</span></span> <span data-ttu-id="65936-151">Wenn nicht angegeben, wird standardmäßig der Name der Vorlagendatei verwendet, wenn eine Vorlagendatei bereitgestellt wird. Standardmäßig wird die aktuelle Uhrzeit verwendet, zu der ein Vorlagenobjekt bereitgestellt wird, beispielsweise "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="65936-151">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="65936-152">-Pre</span><span class="sxs-lookup"><span data-stu-id="65936-152">-Pre</span></span>
<span data-ttu-id="65936-153">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="65936-153">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="65936-154">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="65936-154">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="65936-155">Überspringt die dynamische PowerShell-Parameterverarbeitung, die überprüft, ob der angegebene Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="65936-155">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="65936-156">Mit dieser Prüfung wird der Benutzer aufgefordert, einen Wert für die fehlenden Parameter bereitzustellen, doch die Bereitstellung von-SkipTemplateParameterPrompt ignoriert diese Eingabeaufforderung und ist sofort fehlerhaft, wenn ein Parameter gefunden wurde, der in der Vorlage nicht gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="65936-156">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="65936-157">Für nicht interaktive Skripts kann-SkipTemplateParameterPrompt bereitgestellt werden, um eine bessere Fehlermeldung bereitzustellen, falls nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="65936-157">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="65936-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="65936-158">-Tag</span></span>
<span data-ttu-id="65936-159">Die Tags, die für die Bereitstellung bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="65936-159">The tags to put on the deployment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65936-160">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="65936-160">-TemplateFile</span></span>
<span data-ttu-id="65936-161">Lokaler Pfad zur Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="65936-161">Local path to the template file.</span></span>

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

### <span data-ttu-id="65936-162">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="65936-162">-TemplateObject</span></span>
<span data-ttu-id="65936-163">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="65936-163">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="65936-164">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="65936-164">-TemplateParameterFile</span></span>
<span data-ttu-id="65936-165">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="65936-165">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="65936-166">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="65936-166">-TemplateParameterObject</span></span>
<span data-ttu-id="65936-167">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="65936-167">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="65936-168">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="65936-168">-TemplateParameterUri</span></span>
<span data-ttu-id="65936-169">URI zur Vorlagenparameter Datei.</span><span class="sxs-lookup"><span data-stu-id="65936-169">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="65936-170">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="65936-170">-TemplateUri</span></span>
<span data-ttu-id="65936-171">URI zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="65936-171">Uri to the template file.</span></span>

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

### <span data-ttu-id="65936-172">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="65936-172">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="65936-173">Durch Kommas getrennte Ressourcen Änderungstypen, die von What-If Ergebnissen ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="65936-173">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="65936-174">Anwendbar, wenn der-WhatIf-oder-Confirm-Schalter festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="65936-174">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="65936-175">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="65936-175">-WhatIfResultFormat</span></span>
<span data-ttu-id="65936-176">Das What-If Ergebnisformat.</span><span class="sxs-lookup"><span data-stu-id="65936-176">The What-If result format.</span></span> <span data-ttu-id="65936-177">Anwendbar, wenn der-WhatIf-oder-Confirm-Schalter festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="65936-177">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="65936-178">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="65936-178">-Confirm</span></span>
<span data-ttu-id="65936-179">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="65936-179">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65936-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65936-180">-WhatIf</span></span>
<span data-ttu-id="65936-181">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65936-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65936-182">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="65936-182">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65936-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65936-183">CommonParameters</span></span>
<span data-ttu-id="65936-184">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65936-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65936-185">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65936-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65936-186">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65936-186">INPUTS</span></span>

### <span data-ttu-id="65936-187">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="65936-187">System.Collections.Hashtable</span></span>

### <span data-ttu-id="65936-188">System. String</span><span class="sxs-lookup"><span data-stu-id="65936-188">System.String</span></span>

## <span data-ttu-id="65936-189">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65936-189">OUTPUTS</span></span>

### <span data-ttu-id="65936-190">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="65936-190">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="65936-191">Notizen</span><span class="sxs-lookup"><span data-stu-id="65936-191">NOTES</span></span>

## <span data-ttu-id="65936-192">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65936-192">RELATED LINKS</span></span>
