---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
ms.openlocfilehash: a04c19df84626fd08968e1950074306dfd7cf1ab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358013"
---
# <span data-ttu-id="1456c-101">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1456c-101">New-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="1456c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1456c-102">SYNOPSIS</span></span>
<span data-ttu-id="1456c-103">Erstellen einer Bereitstellung in einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="1456c-103">Create a deployment at a management group</span></span>

## <span data-ttu-id="1456c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1456c-104">SYNTAX</span></span>

### <span data-ttu-id="1456c-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="1456c-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1456c-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1456c-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1456c-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1456c-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1456c-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1456c-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1456c-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1456c-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1456c-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1456c-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1456c-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1456c-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1456c-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1456c-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1456c-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1456c-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1456c-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1456c-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1456c-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="1456c-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1456c-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="1456c-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1456c-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1456c-117">DESCRIPTION</span></span>
<span data-ttu-id="1456c-118">Das **Cmdlet "New-AzManagementGroupDeployment"** fügt einer Verwaltungsgruppe eine Bereitstellung hinzu.</span><span class="sxs-lookup"><span data-stu-id="1456c-118">The **New-AzManagementGroupDeployment** cmdlet adds a deployment at a management group.</span></span>

<span data-ttu-id="1456c-119">Wenn Sie eine Bereitstellung bei einer Verwaltungsgruppe hinzufügen möchten, geben Sie die Verwaltungsgruppe, den Standort und eine Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="1456c-119">To add a deployment at a management group, specify the management group, location and a template.</span></span>
<span data-ttu-id="1456c-120">Der Speicherort teilt dem Azure-Ressourcen-Manager mit, wo die Bereitstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1456c-120">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="1456c-121">Die Vorlage ist eine JSON-Zeichenfolge, die einzelne Ressourcen enthält, die bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1456c-121">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="1456c-122">Die Vorlage enthält Parameterplatzhalter für erforderliche Ressourcen und konfigurierbare Eigenschaftswerte, z. B. Namen und Größen.</span><span class="sxs-lookup"><span data-stu-id="1456c-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="1456c-123">Wenn Sie eine benutzerdefinierte Vorlage für die Bereitstellung verwenden möchten, geben Sie den *Parameter "TemplateFile"* oder *"TemplateUri"* an.</span><span class="sxs-lookup"><span data-stu-id="1456c-123">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="1456c-124">Jede Vorlage enthält Parameter für konfigurierbare Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1456c-124">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="1456c-125">Um Werte für die Vorlagenparameter anzugeben, geben Sie den *Parameter "TemplateParameterFile"* oder den Parameter *"TemplateParameterObject"* an.</span><span class="sxs-lookup"><span data-stu-id="1456c-125">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="1456c-126">Alternativ können Sie die Vorlagenparameter verwenden, die dem Befehl dynamisch hinzugefügt werden, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="1456c-126">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="1456c-127">Wenn Sie dynamische Parameter verwenden möchten, geben Sie diese an der Eingabeaufforderung ein, oder geben Sie ein Minuszeichen (-) ein, um einen Parameter anzugeben, und verwenden Sie die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="1456c-127">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="1456c-128">Werte von Vorlagenparametern, die Sie an der Eingabeaufforderung eingeben, haben Vorrang vor Werten in einem Vorlagenparameterobjekt oder in einer Vorlagenparameterdatei.</span><span class="sxs-lookup"><span data-stu-id="1456c-128">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="1456c-129">Wenn Sie einer Ressourcengruppe Ressourcen hinzufügen möchten, verwenden Sie die **New-AzResourceGroupDeployment,** die eine Bereitstellung für eine Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="1456c-129">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="1456c-130">Verwenden Sie zum Hinzufügen von Ressourcen zu einem Abonnement die **"New-AzSubscriptionDeployment",** die eine Bereitstellung im Abonnementbereich erstellt, die Ressourcen auf Abonnementebene bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="1456c-130">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="1456c-131">Um Ressourcen im Mandantenbereich hinzuzufügen, verwenden Sie die **Neue-AzTenantDeployment,** die eine Bereitstellung im Mandantenbereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="1456c-131">To add resources at tenant scope, use the **New-AzTenantDeployment** which creates a deployment at tenant scope.</span></span>

## <span data-ttu-id="1456c-132">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1456c-132">EXAMPLES</span></span>

### <span data-ttu-id="1456c-133">Beispiel 1: Verwenden einer benutzerdefinierten Vorlage und Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="1456c-133">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="1456c-134">Mit diesem Befehl wird eine neue Bereitstellung bei der Verwaltungsgruppe "myMG" erstellt, indem eine benutzerdefinierte Vorlage und eine Vorlagendatei auf dem Datenträger mit definierten Tagsparametern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1456c-134">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="1456c-135">Der Befehl verwendet den *Parameter "TemplateFile",* um die Vorlage anzugeben, und den *Parameter "TemplateParameterFile",* um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="1456c-135">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="1456c-136">Beispiel 2: Verwenden eines benutzerdefinierten Vorlagenobjekts und einer Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="1456c-136">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="1456c-137">Mit diesem Befehl wird eine neue Bereitstellung bei der Verwaltungsgruppe "myMG" erstellt, indem eine benutzerdefinierte Vorlage und eine Vorlagendatei auf dem Datenträger verwendet wird, die in eine Speicherhashtable konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1456c-137">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="1456c-138">Die ersten beiden Befehle lesen den Text für die Vorlagendatei auf dem Datenträger und konvertieren sie in eine Speicherhashtable.</span><span class="sxs-lookup"><span data-stu-id="1456c-138">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="1456c-139">Der letzte Befehl verwendet den *Parameter "TemplateObject",* um diese Hashtabelle anzugeben, und den *Parameter "TemplateParameterFile",* um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="1456c-139">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="1456c-140">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1456c-140">PARAMETERS</span></span>

### <span data-ttu-id="1456c-141">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1456c-141">-AsJob</span></span>
<span data-ttu-id="1456c-142">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1456c-142">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1456c-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1456c-143">-DefaultProfile</span></span>
<span data-ttu-id="1456c-144">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1456c-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1456c-145">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="1456c-145">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="1456c-146">Die Protokollebene des Bereitstellungsdebuggers.</span><span class="sxs-lookup"><span data-stu-id="1456c-146">The deployment debug log level.</span></span>

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

### <span data-ttu-id="1456c-147">-Location</span><span class="sxs-lookup"><span data-stu-id="1456c-147">-Location</span></span>
<span data-ttu-id="1456c-148">Der Speicherort zum Speichern von Bereitstellungsdaten.</span><span class="sxs-lookup"><span data-stu-id="1456c-148">The location to store deployment data.</span></span>

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

### <span data-ttu-id="1456c-149">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="1456c-149">-ManagementGroupId</span></span>
<span data-ttu-id="1456c-150">Die ID der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="1456c-150">The management group ID.</span></span>

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

### <span data-ttu-id="1456c-151">-Name</span><span class="sxs-lookup"><span data-stu-id="1456c-151">-Name</span></span>
<span data-ttu-id="1456c-152">Der Name der Bereitstellung, die erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1456c-152">The name of the deployment it's going to create.</span></span> <span data-ttu-id="1456c-153">Wenn keine Angabe erfolgt, wird standardmäßig der Vorlagendateiname verwendet, wenn eine Vorlagendatei bereitgestellt wird. wird standardmäßig die aktuelle Uhrzeit verwendet, zu der ein Vorlagenobjekt bereitgestellt wird, z. B. "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="1456c-153">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="1456c-154">-Pre</span><span class="sxs-lookup"><span data-stu-id="1456c-154">-Pre</span></span>
<span data-ttu-id="1456c-155">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1456c-155">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1456c-156">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="1456c-156">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="1456c-157">Überspringt die Verarbeitung dynamischer PowerShell-Parameter, die überprüft, ob der bereitgestellte Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1456c-157">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="1456c-158">Bei dieser Überprüfung müsste der Benutzer einen Wert für die fehlenden Parameter angeben. Wenn jedoch "-SkipTemplateParameterPrompt" angegeben wird, wird diese Eingabeaufforderung und der Fehler sofort ignoriert, wenn ein Parameter nicht in der Vorlage gebunden wurde.</span><span class="sxs-lookup"><span data-stu-id="1456c-158">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="1456c-159">Bei nicht interaktiven Skripts kann "-SkipTemplateParameterPrompt" bereitgestellt werden, um eine bessere Fehlermeldung für den Fall zu liefern, dass nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="1456c-159">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="1456c-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="1456c-160">-Tag</span></span>
<span data-ttu-id="1456c-161">Die Tags, die für die Bereitstellung verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1456c-161">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="1456c-162">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="1456c-162">-TemplateFile</span></span>
<span data-ttu-id="1456c-163">Lokaler Pfad zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="1456c-163">Local path to the template file.</span></span>

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

### <span data-ttu-id="1456c-164">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="1456c-164">-TemplateObject</span></span>
<span data-ttu-id="1456c-165">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="1456c-165">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="1456c-166">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="1456c-166">-TemplateParameterFile</span></span>
<span data-ttu-id="1456c-167">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="1456c-167">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="1456c-168">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="1456c-168">-TemplateParameterObject</span></span>
<span data-ttu-id="1456c-169">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="1456c-169">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="1456c-170">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="1456c-170">-TemplateParameterUri</span></span>
<span data-ttu-id="1456c-171">URI der Vorlagenparameterdatei.</span><span class="sxs-lookup"><span data-stu-id="1456c-171">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="1456c-172">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="1456c-172">-TemplateUri</span></span>
<span data-ttu-id="1456c-173">URI der Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="1456c-173">Uri to the template file.</span></span>

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

### <span data-ttu-id="1456c-174">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="1456c-174">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="1456c-175">Durch Kommas getrennte Ressourcenänderungstypen, die aus den What-If werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1456c-175">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="1456c-176">Anwendbar, wenn der Schalter "-WhatIf" oder "-Confirm" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1456c-176">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="1456c-177">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="1456c-177">-WhatIfResultFormat</span></span>
<span data-ttu-id="1456c-178">Das What-If Ergebnisformat.</span><span class="sxs-lookup"><span data-stu-id="1456c-178">The What-If result format.</span></span> <span data-ttu-id="1456c-179">Anwendbar, wenn der Schalter "-WhatIf" oder "-Confirm" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1456c-179">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="1456c-180">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1456c-180">-Confirm</span></span>
<span data-ttu-id="1456c-181">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1456c-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1456c-182">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1456c-182">-WhatIf</span></span>
<span data-ttu-id="1456c-183">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1456c-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1456c-184">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1456c-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1456c-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1456c-185">CommonParameters</span></span>
<span data-ttu-id="1456c-186">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1456c-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1456c-187">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1456c-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1456c-188">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1456c-188">INPUTS</span></span>

### <span data-ttu-id="1456c-189">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1456c-189">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1456c-190">System.String</span><span class="sxs-lookup"><span data-stu-id="1456c-190">System.String</span></span>

## <span data-ttu-id="1456c-191">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1456c-191">OUTPUTS</span></span>

### <span data-ttu-id="1456c-192">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="1456c-192">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="1456c-193">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1456c-193">NOTES</span></span>

## <span data-ttu-id="1456c-194">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1456c-194">RELATED LINKS</span></span>
