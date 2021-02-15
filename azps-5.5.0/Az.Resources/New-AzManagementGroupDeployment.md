---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
ms.openlocfilehash: 95aa46354fb0ea1f2a1883fe7d319acfda220526
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174401"
---
# <span data-ttu-id="433ba-101">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="433ba-101">New-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="433ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="433ba-102">SYNOPSIS</span></span>
<span data-ttu-id="433ba-103">Erstellen einer Bereitstellung in einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="433ba-103">Create a deployment at a management group</span></span>

## <span data-ttu-id="433ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="433ba-104">SYNTAX</span></span>

### <span data-ttu-id="433ba-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="433ba-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="433ba-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="433ba-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="433ba-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="433ba-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="433ba-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="433ba-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="433ba-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="433ba-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="433ba-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="433ba-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="433ba-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="433ba-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="433ba-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="433ba-112">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="433ba-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="433ba-113">ByTemplateObjectAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="433ba-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="433ba-114">ByTemplateFileAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="433ba-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="433ba-115">ByTemplateUriAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="433ba-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="433ba-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="433ba-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="433ba-117">ByTemplateObjectWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="433ba-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="433ba-118">ByTemplateUriWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="433ba-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="433ba-119">ByTemplateSpecResourceId</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="433ba-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="433ba-120">DESCRIPTION</span></span>
<span data-ttu-id="433ba-121">Das **Cmdlet "New-AzManagementGroupDeployment"** fügt einer Verwaltungsgruppe eine Bereitstellung hinzu.</span><span class="sxs-lookup"><span data-stu-id="433ba-121">The **New-AzManagementGroupDeployment** cmdlet adds a deployment at a management group.</span></span>

<span data-ttu-id="433ba-122">Wenn Sie eine Bereitstellung für eine Verwaltungsgruppe hinzufügen möchten, geben Sie die Verwaltungsgruppe, den Standort und eine Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="433ba-122">To add a deployment at a management group, specify the management group, location and a template.</span></span>
<span data-ttu-id="433ba-123">Der Speicherort teilt dem Azure-Ressourcen-Manager mit, wo die Bereitstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="433ba-123">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="433ba-124">Die Vorlage ist eine JSON-Zeichenfolge, die einzelne ressourcen enthält, die bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="433ba-124">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="433ba-125">Die Vorlage enthält Parameterplatzhalter für erforderliche Ressourcen und konfigurierbare Eigenschaftswerte, z. B. Namen und Größen.</span><span class="sxs-lookup"><span data-stu-id="433ba-125">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="433ba-126">Wenn Sie eine benutzerdefinierte Vorlage für die Bereitstellung verwenden möchten, geben Sie den *Parameter "TemplateFile"* oder *"TemplateUri"* an.</span><span class="sxs-lookup"><span data-stu-id="433ba-126">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="433ba-127">Jede Vorlage enthält Parameter für konfigurierbare Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="433ba-127">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="433ba-128">Um Werte für die Vorlagenparameter anzugeben, geben Sie den *Parameter "TemplateParameterFile"* oder den Parameter *"TemplateParameterObject"* an.</span><span class="sxs-lookup"><span data-stu-id="433ba-128">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="433ba-129">Alternativ können Sie die Vorlagenparameter verwenden, die dem Befehl dynamisch hinzugefügt werden, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="433ba-129">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="433ba-130">Wenn Sie dynamische Parameter verwenden möchten, geben Sie diese an der Eingabeaufforderung ein, oder geben Sie ein Minuszeichen (-) ein, um einen Parameter anzugeben, und verwenden Sie die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="433ba-130">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="433ba-131">Werte von Vorlagenparametern, die Sie an der Eingabeaufforderung eingeben, haben Vorrang vor Werten in einem Vorlagenparameterobjekt oder in einer Vorlagenparameterdatei.</span><span class="sxs-lookup"><span data-stu-id="433ba-131">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="433ba-132">Wenn Sie einer Ressourcengruppe Ressourcen hinzufügen möchten, verwenden Sie die **New-AzResourceGroupDeployment,** die eine Bereitstellung für eine Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="433ba-132">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="433ba-133">Verwenden Sie zum Hinzufügen von Ressourcen zu einem Abonnement die **"New-AzSubscriptionDeployment",** die eine Bereitstellung im Abonnementbereich erstellt, wodurch Ressourcen auf Abonnementebene bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="433ba-133">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="433ba-134">Um Ressourcen im Mandantenbereich hinzuzufügen, verwenden Sie die **Neue-AzTenantDeployment,** die eine Bereitstellung im Mandantenbereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="433ba-134">To add resources at tenant scope, use the **New-AzTenantDeployment** which creates a deployment at tenant scope.</span></span>

## <span data-ttu-id="433ba-135">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="433ba-135">EXAMPLES</span></span>

### <span data-ttu-id="433ba-136">Beispiel 1: Verwenden einer benutzerdefinierten Vorlage und Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="433ba-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="433ba-137">Mit diesem Befehl wird eine neue Bereitstellung bei der Verwaltungsgruppe "myMG" erstellt, indem eine benutzerdefinierte Vorlage und eine Vorlagendatei auf dem Datenträger mit definierten Tagsparametern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="433ba-137">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="433ba-138">Der Befehl verwendet den *Parameter "TemplateFile",* um die Vorlage anzugeben, und den *Parameter "TemplateParameterFile",* um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="433ba-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="433ba-139">Beispiel 2: Bereitstellen einer Vorlage, die in einem nicht öffentlichen Speicherkonto gespeichert ist, mit einem URI und einem SAS-Token</span><span class="sxs-lookup"><span data-stu-id="433ba-139">Example 2: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```
<span data-ttu-id="433ba-140">Mit diesem Befehl wird mithilfe der Vorlage in TemplateUri eine neue Bereitstellung erstellt, die nicht öffentlich ist und für den Zugriff ein Tokenparameter erforderlich ist, der mit dem Parameter "QueryString" bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="433ba-140">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="433ba-141">Mit diesem Befehl wird effektiv über die URL auf die Vorlage https://example.com/example.json?foo zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="433ba-141">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="433ba-142">Dies kann verwendet werden, wenn Sie eine Vorlage in einem Speicherkonto verwenden möchten, indem Sie das SAS-Token als QueryString</span><span class="sxs-lookup"><span data-stu-id="433ba-142">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>

### <span data-ttu-id="433ba-143">Beispiel 3: Verwenden eines benutzerdefinierten Vorlagenobjekts und einer Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="433ba-143">Example 3: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="433ba-144">Mit diesem Befehl wird eine neue Bereitstellung bei der Verwaltungsgruppe "myMG" erstellt, indem eine benutzerdefinierte Vorlage und eine Vorlagendatei auf dem Datenträger verwendet wird, die in eine Speicherhashtable konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="433ba-144">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="433ba-145">Die ersten beiden Befehle lesen den Text für die Vorlagendatei auf dem Datenträger und konvertieren sie in eine Speicherhashtable.</span><span class="sxs-lookup"><span data-stu-id="433ba-145">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="433ba-146">Der letzte Befehl verwendet den *Parameter "TemplateObject",* um diese Hashtabelle anzugeben, und den *Parameter "TemplateParameterFile",* um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="433ba-146">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="433ba-147">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="433ba-147">PARAMETERS</span></span>

### <span data-ttu-id="433ba-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="433ba-148">-AsJob</span></span>
<span data-ttu-id="433ba-149">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="433ba-149">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="433ba-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="433ba-150">-DefaultProfile</span></span>
<span data-ttu-id="433ba-151">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="433ba-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="433ba-152">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="433ba-152">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="433ba-153">Die Protokollebene des Bereitstellungsdebuggers.</span><span class="sxs-lookup"><span data-stu-id="433ba-153">The deployment debug log level.</span></span>

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

### <span data-ttu-id="433ba-154">-Location</span><span class="sxs-lookup"><span data-stu-id="433ba-154">-Location</span></span>
<span data-ttu-id="433ba-155">Der Speicherort zum Speichern von Bereitstellungsdaten.</span><span class="sxs-lookup"><span data-stu-id="433ba-155">The location to store deployment data.</span></span>

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

### <span data-ttu-id="433ba-156">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="433ba-156">-ManagementGroupId</span></span>
<span data-ttu-id="433ba-157">Die ID der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="433ba-157">The management group ID.</span></span>

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

### <span data-ttu-id="433ba-158">-Name</span><span class="sxs-lookup"><span data-stu-id="433ba-158">-Name</span></span>
<span data-ttu-id="433ba-159">Der Name der Bereitstellung, die erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="433ba-159">The name of the deployment it's going to create.</span></span> <span data-ttu-id="433ba-160">Wenn keine Angabe erfolgt, wird standardmäßig der Vorlagendateiname verwendet, wenn eine Vorlagendatei bereitgestellt wird. wird standardmäßig die aktuelle Uhrzeit verwendet, zu der ein Vorlagenobjekt bereitgestellt wird, z. B. "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="433ba-160">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="433ba-161">-Pre</span><span class="sxs-lookup"><span data-stu-id="433ba-161">-Pre</span></span>
<span data-ttu-id="433ba-162">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="433ba-162">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="433ba-163">-QueryString</span><span class="sxs-lookup"><span data-stu-id="433ba-163">-QueryString</span></span>
<span data-ttu-id="433ba-164">Die Abfragezeichenfolge (z. B. ein SAS-Token), die mit dem "TemplateUri"-Parameter verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="433ba-164">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="433ba-165">Würde im Fall von verknüpften Vorlagen verwendet werden</span><span class="sxs-lookup"><span data-stu-id="433ba-165">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="433ba-166">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="433ba-166">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="433ba-167">Überspringt die Verarbeitung dynamischer PowerShell-Parameter, die überprüft, ob der bereitgestellte Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="433ba-167">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="433ba-168">Bei dieser Überprüfung müsste der Benutzer einen Wert für die fehlenden Parameter angeben. Wenn jedoch "-SkipTemplateParameterPrompt" angegeben wird, wird diese Eingabeaufforderung und der Fehler sofort ignoriert, wenn ein Parameter nicht in der Vorlage gebunden wurde.</span><span class="sxs-lookup"><span data-stu-id="433ba-168">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="433ba-169">Bei nicht interaktiven Skripts kann "-SkipTemplateParameterPrompt" bereitgestellt werden, um eine bessere Fehlermeldung für den Fall zu liefern, dass nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="433ba-169">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="433ba-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="433ba-170">-Tag</span></span>
<span data-ttu-id="433ba-171">Die Tags, die für die Bereitstellung verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="433ba-171">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="433ba-172">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="433ba-172">-TemplateFile</span></span>
<span data-ttu-id="433ba-173">Lokaler Pfad zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="433ba-173">Local path to the template file.</span></span>

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

### <span data-ttu-id="433ba-174">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="433ba-174">-TemplateObject</span></span>
<span data-ttu-id="433ba-175">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="433ba-175">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="433ba-176">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="433ba-176">-TemplateParameterFile</span></span>
<span data-ttu-id="433ba-177">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="433ba-177">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="433ba-178">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="433ba-178">-TemplateParameterObject</span></span>
<span data-ttu-id="433ba-179">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="433ba-179">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="433ba-180">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="433ba-180">-TemplateParameterUri</span></span>
<span data-ttu-id="433ba-181">URI der Vorlagenparameterdatei.</span><span class="sxs-lookup"><span data-stu-id="433ba-181">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="433ba-182">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="433ba-182">-TemplateSpecId</span></span>
<span data-ttu-id="433ba-183">Ressourcen-ID der bereitgestellten "templateSpec".</span><span class="sxs-lookup"><span data-stu-id="433ba-183">Resource ID of the templateSpec to be deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateSpecResourceIdAndParams, ByTemplateSpecResourceIdAndParamsUri, ByTemplateSpecResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="433ba-184">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="433ba-184">-TemplateUri</span></span>
<span data-ttu-id="433ba-185">URI der Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="433ba-185">Uri to the template file.</span></span>

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

### <span data-ttu-id="433ba-186">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="433ba-186">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="433ba-187">Durch Kommas getrennte Ressourcenänderungstypen, die aus den What-If werden sollen.</span><span class="sxs-lookup"><span data-stu-id="433ba-187">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="433ba-188">Anwendbar, wenn der Schalter "-WhatIf" oder "-Confirm" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="433ba-188">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="433ba-189">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="433ba-189">-WhatIfResultFormat</span></span>
<span data-ttu-id="433ba-190">Das What-If Ergebnisformat.</span><span class="sxs-lookup"><span data-stu-id="433ba-190">The What-If result format.</span></span> <span data-ttu-id="433ba-191">Anwendbar, wenn der Schalter "-WhatIf" oder "-Confirm" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="433ba-191">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="433ba-192">-Confirm</span><span class="sxs-lookup"><span data-stu-id="433ba-192">-Confirm</span></span>
<span data-ttu-id="433ba-193">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="433ba-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="433ba-194">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="433ba-194">-WhatIf</span></span>
<span data-ttu-id="433ba-195">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="433ba-195">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="433ba-196">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="433ba-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="433ba-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="433ba-197">CommonParameters</span></span>
<span data-ttu-id="433ba-198">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="433ba-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="433ba-199">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="433ba-199">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="433ba-200">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="433ba-200">INPUTS</span></span>

### <span data-ttu-id="433ba-201">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="433ba-201">System.Collections.Hashtable</span></span>

### <span data-ttu-id="433ba-202">System.String</span><span class="sxs-lookup"><span data-stu-id="433ba-202">System.String</span></span>

## <span data-ttu-id="433ba-203">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="433ba-203">OUTPUTS</span></span>

### <span data-ttu-id="433ba-204">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="433ba-204">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="433ba-205">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="433ba-205">NOTES</span></span>

## <span data-ttu-id="433ba-206">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="433ba-206">RELATED LINKS</span></span>
