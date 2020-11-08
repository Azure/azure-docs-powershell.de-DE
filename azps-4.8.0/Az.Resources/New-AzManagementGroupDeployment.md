---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
ms.openlocfilehash: c15a7fca43568e63b8e7407b5c2048d03b9b6bc1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174211"
---
# <span data-ttu-id="186ff-101">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="186ff-101">New-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="186ff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="186ff-102">SYNOPSIS</span></span>
<span data-ttu-id="186ff-103">Erstellen einer Bereitstellung in einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="186ff-103">Create a deployment at a management group</span></span>

## <span data-ttu-id="186ff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="186ff-104">SYNTAX</span></span>

### <span data-ttu-id="186ff-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="186ff-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="186ff-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="186ff-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="186ff-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="186ff-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="186ff-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="186ff-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="186ff-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="186ff-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="186ff-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="186ff-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="186ff-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="186ff-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="186ff-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="186ff-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="186ff-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="186ff-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="186ff-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="186ff-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="186ff-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="186ff-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="186ff-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="186ff-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="186ff-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="186ff-117">DESCRIPTION</span></span>
<span data-ttu-id="186ff-118">Mit dem Cmdlet **New-AzManagementGroupDeployment** wird eine Bereitstellung in einer Verwaltungsgruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="186ff-118">The **New-AzManagementGroupDeployment** cmdlet adds a deployment at a management group.</span></span>

<span data-ttu-id="186ff-119">Wenn Sie eine Bereitstellung in einer Verwaltungsgruppe hinzufügen möchten, geben Sie die Verwaltungsgruppe, den Standort und eine Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="186ff-119">To add a deployment at a management group, specify the management group, location and a template.</span></span>
<span data-ttu-id="186ff-120">Der Speicherort weist Azure Resource Manager an, wo die Bereitstellungsdaten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="186ff-120">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="186ff-121">Bei der Vorlage handelt es sich um eine JSON-Zeichenfolge, die einzelne Ressourcen enthält, die bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="186ff-121">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="186ff-122">Die Vorlage enthält Parameterplatzhalter für erforderliche Ressourcen und konfigurierbare Eigenschaftswerte wie Namen und Größen.</span><span class="sxs-lookup"><span data-stu-id="186ff-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="186ff-123">Wenn Sie eine benutzerdefinierte Vorlage für die Bereitstellung verwenden möchten, geben Sie den Parameter " *Templatedatei* " oder " *TemplateUri* " an.</span><span class="sxs-lookup"><span data-stu-id="186ff-123">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="186ff-124">Jede Vorlage verfügt über Parameter für konfigurierbare Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="186ff-124">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="186ff-125">Wenn Sie Werte für die Vorlagenparameter angeben möchten, geben Sie den *TemplateParameterFile* -Parameter oder den *TemplateParameterObject* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="186ff-125">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="186ff-126">Alternativ können Sie die Vorlagenparameter verwenden, die dem Befehl dynamisch hinzugefügt werden, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="186ff-126">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="186ff-127">Wenn Sie dynamische Parameter verwenden möchten, geben Sie Sie an der Eingabeaufforderung ein, oder geben Sie ein Minuszeichen (-) ein, um einen Parameter anzugeben, und verwenden Sie die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="186ff-127">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="186ff-128">Vorlagenparameter Werte, die Sie an der Eingabeaufforderung eingeben, haben Vorrang vor Werten in einem Vorlagenparameter Objekt oder einer Datei.</span><span class="sxs-lookup"><span data-stu-id="186ff-128">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="186ff-129">Verwenden Sie zum Hinzufügen von Ressourcen zu einer Ressourcengruppe das **New-AzResourceGroupDeployment-** Objekt, das eine Bereitstellung in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="186ff-129">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="186ff-130">Verwenden Sie zum Hinzufügen von Ressourcen zu einem Abonnement das **New-AzSubscriptionDeployment-** Projekt, das eine Bereitstellung im Abonnement Bereich erstellt, in dem die Ressourcen auf Abonnementebene bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="186ff-130">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="186ff-131">Verwenden Sie zum Hinzufügen von Ressourcen im MANDANTENBEREICH das **New-AzTenantDeployment-** Projekt, das eine Bereitstellung im MANDANTENBEREICH erstellt.</span><span class="sxs-lookup"><span data-stu-id="186ff-131">To add resources at tenant scope, use the **New-AzTenantDeployment** which creates a deployment at tenant scope.</span></span>

## <span data-ttu-id="186ff-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="186ff-132">EXAMPLES</span></span>

### <span data-ttu-id="186ff-133">Beispiel 1: Verwenden einer benutzerdefinierten Vorlage und einer Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="186ff-133">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="186ff-134">Dieser Befehl erstellt eine neue Bereitstellung in der Verwaltungsgruppe "myMG" mithilfe einer benutzerdefinierten Vorlage und einer Vorlagendatei auf dem Datenträger mit dem Parameter für definierte Tags.</span><span class="sxs-lookup"><span data-stu-id="186ff-134">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="186ff-135">Der Befehl verwendet den *Templatedatei* -Parameter, um die Vorlage und den *TemplateParameterFile* -Parameter anzugeben, um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="186ff-135">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="186ff-136">Beispiel 2: Verwenden eines benutzerdefinierten Vorlagenobjekts und einer Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="186ff-136">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="186ff-137">Dieser Befehl erstellt eine neue Bereitstellung in der Verwaltungsgruppe "myMG", indem Sie eine benutzerdefinierte Vorlage und eine Vorlagendatei auf einem Datenträger verwenden, die in eine Arbeitsspeicher-Hashtable konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="186ff-137">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="186ff-138">Mit den ersten beiden Befehlen wird der Text für die Vorlagendatei auf dem Datenträger gelesen und in eine Arbeitsspeicher-Hashtable konvertiert.</span><span class="sxs-lookup"><span data-stu-id="186ff-138">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="186ff-139">Der letzte Befehl verwendet den *templateobject* -Parameter zum Angeben dieser Hashtable und des *TemplateParameterFile* -Parameters, um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="186ff-139">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="186ff-140">Parameter</span><span class="sxs-lookup"><span data-stu-id="186ff-140">PARAMETERS</span></span>

### <span data-ttu-id="186ff-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="186ff-141">-ApiVersion</span></span>
<span data-ttu-id="186ff-142">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="186ff-142">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="186ff-143">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="186ff-143">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="186ff-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="186ff-144">-AsJob</span></span>
<span data-ttu-id="186ff-145">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="186ff-145">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="186ff-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="186ff-146">-DefaultProfile</span></span>
<span data-ttu-id="186ff-147">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="186ff-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="186ff-148">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="186ff-148">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="186ff-149">Die Debug-Protokollebene der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="186ff-149">The deployment debug log level.</span></span>

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

### <span data-ttu-id="186ff-150">-Standort</span><span class="sxs-lookup"><span data-stu-id="186ff-150">-Location</span></span>
<span data-ttu-id="186ff-151">Der Speicherort, an dem Bereitstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="186ff-151">The location to store deployment data.</span></span>

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

### <span data-ttu-id="186ff-152">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="186ff-152">-ManagementGroupId</span></span>
<span data-ttu-id="186ff-153">Die Verwaltungsgruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="186ff-153">The management group ID.</span></span>

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

### <span data-ttu-id="186ff-154">-Name</span><span class="sxs-lookup"><span data-stu-id="186ff-154">-Name</span></span>
<span data-ttu-id="186ff-155">Der Name der Bereitstellung, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="186ff-155">The name of the deployment it's going to create.</span></span> <span data-ttu-id="186ff-156">Wenn nicht angegeben, wird standardmäßig der Name der Vorlagendatei verwendet, wenn eine Vorlagendatei bereitgestellt wird. Standardmäßig wird die aktuelle Uhrzeit verwendet, zu der ein Vorlagenobjekt bereitgestellt wird, beispielsweise "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="186ff-156">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="186ff-157">-Pre</span><span class="sxs-lookup"><span data-stu-id="186ff-157">-Pre</span></span>
<span data-ttu-id="186ff-158">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="186ff-158">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="186ff-159">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="186ff-159">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="186ff-160">Überspringt die dynamische PowerShell-Parameterverarbeitung, die überprüft, ob der angegebene Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="186ff-160">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="186ff-161">Mit dieser Prüfung wird der Benutzer aufgefordert, einen Wert für die fehlenden Parameter bereitzustellen, doch die Bereitstellung von-SkipTemplateParameterPrompt ignoriert diese Eingabeaufforderung und ist sofort fehlerhaft, wenn ein Parameter gefunden wurde, der in der Vorlage nicht gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="186ff-161">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="186ff-162">Für nicht interaktive Skripts kann-SkipTemplateParameterPrompt bereitgestellt werden, um eine bessere Fehlermeldung bereitzustellen, falls nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="186ff-162">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="186ff-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="186ff-163">-Tag</span></span>
<span data-ttu-id="186ff-164">Die Tags, die für die Bereitstellung bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="186ff-164">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="186ff-165">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="186ff-165">-TemplateFile</span></span>
<span data-ttu-id="186ff-166">Lokaler Pfad zur Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="186ff-166">Local path to the template file.</span></span>

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

### <span data-ttu-id="186ff-167">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="186ff-167">-TemplateObject</span></span>
<span data-ttu-id="186ff-168">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="186ff-168">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="186ff-169">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="186ff-169">-TemplateParameterFile</span></span>
<span data-ttu-id="186ff-170">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="186ff-170">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="186ff-171">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="186ff-171">-TemplateParameterObject</span></span>
<span data-ttu-id="186ff-172">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="186ff-172">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="186ff-173">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="186ff-173">-TemplateParameterUri</span></span>
<span data-ttu-id="186ff-174">URI zur Vorlagenparameter Datei.</span><span class="sxs-lookup"><span data-stu-id="186ff-174">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="186ff-175">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="186ff-175">-TemplateUri</span></span>
<span data-ttu-id="186ff-176">URI zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="186ff-176">Uri to the template file.</span></span>

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

### <span data-ttu-id="186ff-177">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="186ff-177">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="186ff-178">Durch Kommas getrennte Ressourcen Änderungstypen, die von What-If Ergebnissen ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="186ff-178">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="186ff-179">Anwendbar, wenn der-WhatIf-oder-Confirm-Schalter festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="186ff-179">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="186ff-180">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="186ff-180">-WhatIfResultFormat</span></span>
<span data-ttu-id="186ff-181">Das What-If Ergebnisformat.</span><span class="sxs-lookup"><span data-stu-id="186ff-181">The What-If result format.</span></span> <span data-ttu-id="186ff-182">Anwendbar, wenn der-WhatIf-oder-Confirm-Schalter festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="186ff-182">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="186ff-183">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="186ff-183">-Confirm</span></span>
<span data-ttu-id="186ff-184">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="186ff-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="186ff-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="186ff-185">-WhatIf</span></span>
<span data-ttu-id="186ff-186">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="186ff-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="186ff-187">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="186ff-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="186ff-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="186ff-188">CommonParameters</span></span>
<span data-ttu-id="186ff-189">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="186ff-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="186ff-190">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="186ff-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="186ff-191">Eingaben</span><span class="sxs-lookup"><span data-stu-id="186ff-191">INPUTS</span></span>

### <span data-ttu-id="186ff-192">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="186ff-192">System.Collections.Hashtable</span></span>

### <span data-ttu-id="186ff-193">System. String</span><span class="sxs-lookup"><span data-stu-id="186ff-193">System.String</span></span>

## <span data-ttu-id="186ff-194">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="186ff-194">OUTPUTS</span></span>

### <span data-ttu-id="186ff-195">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="186ff-195">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="186ff-196">Notizen</span><span class="sxs-lookup"><span data-stu-id="186ff-196">NOTES</span></span>

## <span data-ttu-id="186ff-197">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="186ff-197">RELATED LINKS</span></span>
