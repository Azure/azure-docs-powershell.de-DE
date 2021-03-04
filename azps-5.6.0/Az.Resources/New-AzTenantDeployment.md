---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
ms.openlocfilehash: 029e1342caeac078d98418cfc508051b04dd816f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943517"
---
# <span data-ttu-id="1943d-101">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="1943d-101">New-AzTenantDeployment</span></span>

## <span data-ttu-id="1943d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1943d-102">SYNOPSIS</span></span>
<span data-ttu-id="1943d-103">Erstellen einer Bereitstellung im Mandantenbereich</span><span class="sxs-lookup"><span data-stu-id="1943d-103">Create a deployment at tenant scope</span></span>

## <span data-ttu-id="1943d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1943d-104">SYNTAX</span></span>

### <span data-ttu-id="1943d-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="1943d-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1943d-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1943d-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1943d-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1943d-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1943d-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1943d-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1943d-109">ByTemplateSpecResourceIdAndParamsObject</span><span class="sxs-lookup"><span data-stu-id="1943d-109">ByTemplateSpecResourceIdAndParamsObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1943d-110">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1943d-110">ByTemplateObjectAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1943d-111">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1943d-111">ByTemplateFileAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1943d-112">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1943d-112">ByTemplateUriAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1943d-113">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="1943d-113">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1943d-114">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1943d-114">ByTemplateObjectAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1943d-115">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1943d-115">ByTemplateFileAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1943d-116">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1943d-116">ByTemplateUriAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1943d-117">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="1943d-117">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1943d-118">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="1943d-118">ByTemplateObjectWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1943d-119">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="1943d-119">ByTemplateUriWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1943d-120">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="1943d-120">ByTemplateSpecResourceId</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1943d-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1943d-121">DESCRIPTION</span></span>
<span data-ttu-id="1943d-122">Das **Cmdlet New-AzTenantDeployment** fügt eine Bereitstellung im aktuellen Mandantenbereich hinzu.</span><span class="sxs-lookup"><span data-stu-id="1943d-122">The **New-AzTenantDeployment** cmdlet adds a deployment at the current tenant scope.</span></span>

<span data-ttu-id="1943d-123">Wenn Sie eine Bereitstellung im Mandantenbereich hinzufügen möchten, geben Sie den Speicherort und eine Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="1943d-123">To add a deployment at tenant scope, specify the location and a template.</span></span>
<span data-ttu-id="1943d-124">Der Speicherort teilt Azure Resource Manager mit, wo die Bereitstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1943d-124">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="1943d-125">Die Vorlage ist eine JSON-Zeichenfolge, die einzelne ressourcen enthält, die bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1943d-125">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="1943d-126">Die Vorlage enthält Parameterplatzhalter für erforderliche Ressourcen und konfigurierbare Eigenschaftswerte, z. B. Namen und Größen.</span><span class="sxs-lookup"><span data-stu-id="1943d-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="1943d-127">Wenn Sie eine benutzerdefinierte Vorlage für die Bereitstellung verwenden möchten, geben Sie den *Parameter TemplateFile* oder *TemplateUri* an.</span><span class="sxs-lookup"><span data-stu-id="1943d-127">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="1943d-128">Jede Vorlage verfügt über Parameter für konfigurierbare Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1943d-128">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="1943d-129">Wenn Sie Werte für die Vorlagenparameter angeben möchten, geben Sie den *Parameter TemplateParameterFile* oder *den Parameter TemplateParameterObject* an.</span><span class="sxs-lookup"><span data-stu-id="1943d-129">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="1943d-130">Alternativ können Sie die Vorlagenparameter verwenden, die dem Befehl dynamisch hinzugefügt werden, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="1943d-130">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="1943d-131">Wenn Sie dynamische Parameter verwenden möchten, geben Sie sie an der Eingabeaufforderung ein, oder geben Sie ein Minuszeichen (-) ein, um einen Parameter anzugeben, und verwenden Sie die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="1943d-131">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="1943d-132">Vorlagenparameterwerte, die Sie an der Eingabeaufforderung eingeben, haben Vorrang vor Werten in einem Vorlagenparameterobjekt oder einer Datei.</span><span class="sxs-lookup"><span data-stu-id="1943d-132">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="1943d-133">Zum Hinzufügen von Ressourcen zu einer Ressourcengruppe verwenden Sie **die New-AzResourceGroupDeployment,** die eine Bereitstellung bei einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="1943d-133">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="1943d-134">Verwenden Sie zum Hinzufügen von Ressourcen zu einem Abonnement die **New-AzSubscriptionDeployment,** die eine Bereitstellung im Abonnementbereich erstellt, die Ressourcen auf Abonnementebene bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="1943d-134">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="1943d-135">Zum Hinzufügen von Ressourcen in einer Verwaltungsgruppe verwenden Sie **die New-AzManagementGroupDeployment,** die eine Bereitstellung bei einer Verwaltungsgruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="1943d-135">To add resources at a management group, use the **New-AzManagementGroupDeployment** which creates a deployment at a management group.</span></span>

## <span data-ttu-id="1943d-136">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1943d-136">EXAMPLES</span></span>

### <span data-ttu-id="1943d-137">Beispiel 1: Verwenden einer benutzerdefinierten Vorlage und Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="1943d-137">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="1943d-138">Mit diesem Befehl wird eine neue Bereitstellung im aktuellen Mandantenbereich mithilfe einer benutzerdefinierten Vorlage und einer Vorlagendatei auf dem Datenträger mit dem Parameter für definierte Tags erstellt.</span><span class="sxs-lookup"><span data-stu-id="1943d-138">This command creates a new deployment at the current tenant scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="1943d-139">Der Befehl verwendet den *Parameter TemplateFile,* um die Vorlage und den *Parameter TemplateParameterFile* anzugeben, um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="1943d-139">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="1943d-140">Beispiel 2: Verwenden eines benutzerdefinierten Vorlagenobjekts und einer Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="1943d-140">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="1943d-141">Mit diesem Befehl wird eine neue Bereitstellung beim aktuellen Mandanten mithilfe einer benutzerdefinierten Vorlage und einer Vorlagendatei auf einem Datenträger erstellt, die in eine #A0 im Arbeitsspeicher konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1943d-141">This command creates a new deployment at the current tenant by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="1943d-142">Die ersten beiden Befehle lesen den Text für die Vorlagendatei auf dem Datenträger und konvertieren sie in eine Hashtabelle im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1943d-142">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="1943d-143">Der letzte Befehl verwendet den *Parameter TemplateObject,* um diese Hashtabelle und den *Parameter TemplateParameterFile* anzugeben, um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="1943d-143">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="1943d-144">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1943d-144">PARAMETERS</span></span>

### <span data-ttu-id="1943d-145">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1943d-145">-AsJob</span></span>
<span data-ttu-id="1943d-146">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1943d-146">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1943d-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1943d-147">-DefaultProfile</span></span>
<span data-ttu-id="1943d-148">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1943d-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1943d-149">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="1943d-149">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="1943d-150">Die Protokollebene des Bereitstellungsdebuggers.</span><span class="sxs-lookup"><span data-stu-id="1943d-150">The deployment debug log level.</span></span>

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

### <span data-ttu-id="1943d-151">-Location</span><span class="sxs-lookup"><span data-stu-id="1943d-151">-Location</span></span>
<span data-ttu-id="1943d-152">Der Speicherort zum Speichern von Bereitstellungsdaten.</span><span class="sxs-lookup"><span data-stu-id="1943d-152">The location to store deployment data.</span></span>

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

### <span data-ttu-id="1943d-153">-Name</span><span class="sxs-lookup"><span data-stu-id="1943d-153">-Name</span></span>
<span data-ttu-id="1943d-154">Der Name der Bereitstellung, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1943d-154">The name of the deployment it's going to create.</span></span> <span data-ttu-id="1943d-155">Wenn nicht angegeben, wird standardmäßig der Vorlagendateiname verwendet, wenn eine Vorlagendatei bereitgestellt wird. ist standardmäßig auf die aktuelle Uhrzeit festgelegt, zu der ein Vorlagenobjekt bereitgestellt wird, z. B. "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="1943d-155">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="1943d-156">-Pre</span><span class="sxs-lookup"><span data-stu-id="1943d-156">-Pre</span></span>
<span data-ttu-id="1943d-157">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1943d-157">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1943d-158">-QueryString</span><span class="sxs-lookup"><span data-stu-id="1943d-158">-QueryString</span></span>
<span data-ttu-id="1943d-159">Die Abfragezeichenfolge (z. B. ein SAS-Token), die mit dem Parameter TemplateUri verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1943d-159">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="1943d-160">Würde bei verknüpften Vorlagen verwendet</span><span class="sxs-lookup"><span data-stu-id="1943d-160">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="1943d-161">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="1943d-161">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="1943d-162">Überspringt die PowerShell-Dynamische Parameterverarbeitung, die überprüft, ob der bereitgestellte Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1943d-162">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="1943d-163">Bei dieser Überprüfung wird der Benutzer aufgefordert, einen Wert für die fehlenden Parameter zur Verfügung zu stellen. Wenn jedoch -SkipTemplateParameterPrompt angegeben wird, werden diese Eingabeaufforderung und der Fehler sofort ignoriert, wenn festgestellt wurde, dass ein Parameter nicht in der Vorlage gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="1943d-163">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="1943d-164">Für nicht interaktive Skripts kann -SkipTemplateParameterPrompt bereitgestellt werden, um eine bessere Fehlermeldung für den Fall zu liefern, dass nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="1943d-164">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="1943d-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="1943d-165">-Tag</span></span>
<span data-ttu-id="1943d-166">Die Tags, die für die Bereitstellung zu setzen sind.</span><span class="sxs-lookup"><span data-stu-id="1943d-166">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="1943d-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="1943d-167">-TemplateFile</span></span>
<span data-ttu-id="1943d-168">Lokaler Pfad zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="1943d-168">Local path to the template file.</span></span> <span data-ttu-id="1943d-169">Unterstützter Vorlagendateityp: json und bicep.</span><span class="sxs-lookup"><span data-stu-id="1943d-169">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="1943d-170">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="1943d-170">-TemplateObject</span></span>
<span data-ttu-id="1943d-171">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="1943d-171">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="1943d-172">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="1943d-172">-TemplateParameterFile</span></span>
<span data-ttu-id="1943d-173">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="1943d-173">A file that has the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile, ByTemplateSpecResourceIdAndParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1943d-174">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="1943d-174">-TemplateParameterObject</span></span>
<span data-ttu-id="1943d-175">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="1943d-175">A hash table which represents the parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject, ByTemplateSpecResourceIdAndParamsObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1943d-176">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="1943d-176">-TemplateParameterUri</span></span>
<span data-ttu-id="1943d-177">URI für die Vorlagenparameterdatei.</span><span class="sxs-lookup"><span data-stu-id="1943d-177">Uri to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri, ByTemplateSpecResourceIdAndParamsUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1943d-178">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="1943d-178">-TemplateSpecId</span></span>
<span data-ttu-id="1943d-179">Ressourcen-ID der zu bereitstellende TemplateSpec.</span><span class="sxs-lookup"><span data-stu-id="1943d-179">Resource ID of the templateSpec to be deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateSpecResourceIdAndParamsObject, ByTemplateSpecResourceIdAndParams, ByTemplateSpecResourceIdAndParamsUri, ByTemplateSpecResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1943d-180">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="1943d-180">-TemplateUri</span></span>
<span data-ttu-id="1943d-181">URI für die Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="1943d-181">Uri to the template file.</span></span>

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

### <span data-ttu-id="1943d-182">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="1943d-182">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="1943d-183">Durch Kommas getrennte Ressourcenänderungstypen, die aus den Ergebnissen What-If werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1943d-183">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="1943d-184">Gilt, wenn der Schalter -WhatIf oder -Confirm festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1943d-184">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="1943d-185">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="1943d-185">-WhatIfResultFormat</span></span>
<span data-ttu-id="1943d-186">Das What-If Ergebnisformat.</span><span class="sxs-lookup"><span data-stu-id="1943d-186">The What-If result format.</span></span> <span data-ttu-id="1943d-187">Gilt, wenn der Schalter -WhatIf oder -Confirm festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1943d-187">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="1943d-188">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1943d-188">-Confirm</span></span>
<span data-ttu-id="1943d-189">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1943d-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1943d-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1943d-190">-WhatIf</span></span>
<span data-ttu-id="1943d-191">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1943d-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1943d-192">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1943d-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1943d-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1943d-193">CommonParameters</span></span>
<span data-ttu-id="1943d-194">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1943d-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1943d-195">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1943d-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1943d-196">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1943d-196">INPUTS</span></span>

### <span data-ttu-id="1943d-197">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1943d-197">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1943d-198">System.String</span><span class="sxs-lookup"><span data-stu-id="1943d-198">System.String</span></span>

## <span data-ttu-id="1943d-199">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1943d-199">OUTPUTS</span></span>

### <span data-ttu-id="1943d-200">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="1943d-200">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="1943d-201">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1943d-201">NOTES</span></span>

## <span data-ttu-id="1943d-202">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1943d-202">RELATED LINKS</span></span>
