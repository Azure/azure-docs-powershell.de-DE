---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
ms.openlocfilehash: da2a2bc6d7c35f6d7f092123dce08496f491655b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944758"
---
# <span data-ttu-id="b321e-101">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b321e-101">New-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="b321e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b321e-102">SYNOPSIS</span></span>
<span data-ttu-id="b321e-103">Erstellen einer Bereitstellung in einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="b321e-103">Create a deployment at a management group</span></span>

## <span data-ttu-id="b321e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b321e-104">SYNTAX</span></span>

### <span data-ttu-id="b321e-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="b321e-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b321e-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b321e-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b321e-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b321e-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b321e-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b321e-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b321e-109">ByTemplateSpecResourceIdAndParamsObject</span><span class="sxs-lookup"><span data-stu-id="b321e-109">ByTemplateSpecResourceIdAndParamsObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b321e-110">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b321e-110">ByTemplateObjectAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b321e-111">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b321e-111">ByTemplateFileAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b321e-112">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b321e-112">ByTemplateUriAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b321e-113">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="b321e-113">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b321e-114">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b321e-114">ByTemplateObjectAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b321e-115">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b321e-115">ByTemplateFileAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b321e-116">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b321e-116">ByTemplateUriAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b321e-117">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="b321e-117">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b321e-118">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b321e-118">ByTemplateObjectWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b321e-119">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b321e-119">ByTemplateUriWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b321e-120">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="b321e-120">ByTemplateSpecResourceId</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] [-QueryString <String>] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b321e-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b321e-121">DESCRIPTION</span></span>
<span data-ttu-id="b321e-122">Das **Cmdlet New-AzManagementGroupDeployment** fügt eine Bereitstellung bei einer Verwaltungsgruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="b321e-122">The **New-AzManagementGroupDeployment** cmdlet adds a deployment at a management group.</span></span>

<span data-ttu-id="b321e-123">Wenn Sie eine Bereitstellung in einer Verwaltungsgruppe hinzufügen möchten, geben Sie die Verwaltungsgruppe, den Standort und eine Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="b321e-123">To add a deployment at a management group, specify the management group, location and a template.</span></span>
<span data-ttu-id="b321e-124">Der Speicherort teilt Azure Resource Manager mit, wo die Bereitstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b321e-124">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="b321e-125">Die Vorlage ist eine JSON-Zeichenfolge, die einzelne ressourcen enthält, die bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b321e-125">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="b321e-126">Die Vorlage enthält Parameterplatzhalter für erforderliche Ressourcen und konfigurierbare Eigenschaftswerte, z. B. Namen und Größen.</span><span class="sxs-lookup"><span data-stu-id="b321e-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="b321e-127">Wenn Sie eine benutzerdefinierte Vorlage für die Bereitstellung verwenden möchten, geben Sie den *Parameter TemplateFile* oder *TemplateUri* an.</span><span class="sxs-lookup"><span data-stu-id="b321e-127">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="b321e-128">Jede Vorlage verfügt über Parameter für konfigurierbare Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b321e-128">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="b321e-129">Wenn Sie Werte für die Vorlagenparameter angeben möchten, geben Sie den *Parameter TemplateParameterFile* oder *den Parameter TemplateParameterObject* an.</span><span class="sxs-lookup"><span data-stu-id="b321e-129">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="b321e-130">Alternativ können Sie die Vorlagenparameter verwenden, die dem Befehl dynamisch hinzugefügt werden, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="b321e-130">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="b321e-131">Wenn Sie dynamische Parameter verwenden möchten, geben Sie sie an der Eingabeaufforderung ein, oder geben Sie ein Minuszeichen (-) ein, um einen Parameter anzugeben, und verwenden Sie die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="b321e-131">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="b321e-132">Vorlagenparameterwerte, die Sie an der Eingabeaufforderung eingeben, haben Vorrang vor Werten in einem Vorlagenparameterobjekt oder einer Datei.</span><span class="sxs-lookup"><span data-stu-id="b321e-132">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="b321e-133">Zum Hinzufügen von Ressourcen zu einer Ressourcengruppe verwenden Sie **die New-AzResourceGroupDeployment,** die eine Bereitstellung bei einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="b321e-133">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="b321e-134">Verwenden Sie zum Hinzufügen von Ressourcen zu einem Abonnement die **New-AzSubscriptionDeployment,** die eine Bereitstellung im Abonnementbereich erstellt, die Ressourcen auf Abonnementebene bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b321e-134">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="b321e-135">Zum Hinzufügen von Ressourcen im Mandantenbereich verwenden Sie **die New-AzTenantDeployment,** die eine Bereitstellung im Mandantenbereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="b321e-135">To add resources at tenant scope, use the **New-AzTenantDeployment** which creates a deployment at tenant scope.</span></span>

## <span data-ttu-id="b321e-136">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b321e-136">EXAMPLES</span></span>

### <span data-ttu-id="b321e-137">Beispiel 1: Verwenden einer benutzerdefinierten Vorlage und Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="b321e-137">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="b321e-138">Mit diesem Befehl wird eine neue Bereitstellung bei der Verwaltungsgruppe "myMG" mithilfe einer benutzerdefinierten Vorlage und einer Vorlagendatei auf dem Datenträger mit definierten Tagsparameter erstellt.</span><span class="sxs-lookup"><span data-stu-id="b321e-138">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="b321e-139">Der Befehl verwendet den *Parameter TemplateFile,* um die Vorlage und den *Parameter TemplateParameterFile* anzugeben, um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="b321e-139">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="b321e-140">Beispiel 2: Bereitstellen einer In einem nicht öffentlichen Speicherkonto gespeicherten Vorlage mithilfe eines URI- und SAS-Tokens</span><span class="sxs-lookup"><span data-stu-id="b321e-140">Example 2: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```

<span data-ttu-id="b321e-141">Mit diesem Befehl wird mithilfe der Vorlage in TemplateUri eine neue Bereitstellung erstellt, die nicht öffentlich ist und für den Zugriff ein Tokenparameter erforderlich ist, der mit dem Parameter QueryString bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b321e-141">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="b321e-142">Durch Ausführen dieses Befehls wird effektiv über die URL auf die Vorlage https://example.com/example.json?foo zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="b321e-142">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="b321e-143">Dies kann verwendet werden, wenn Sie eine Vorlage in einem Speicherkonto verwenden möchten, indem Sie das SAS-Token als QueryString bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b321e-143">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>

### <span data-ttu-id="b321e-144">Beispiel 3: Verwenden eines benutzerdefinierten Vorlagenobjekts und einer Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="b321e-144">Example 3: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="b321e-145">Mit diesem Befehl wird eine neue Bereitstellung bei der Verwaltungsgruppe "myMG" mithilfe einer benutzerdefinierten Vorlage und einer Vorlagendatei auf einem Datenträger erstellt, die in eine #A0 konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b321e-145">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="b321e-146">Die ersten beiden Befehle lesen den Text für die Vorlagendatei auf dem Datenträger und konvertieren sie in eine Hashtabelle im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="b321e-146">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="b321e-147">Der letzte Befehl verwendet den *Parameter TemplateObject,* um diese Hashtabelle und den *Parameter TemplateParameterFile* anzugeben, um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="b321e-147">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="b321e-148">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b321e-148">PARAMETERS</span></span>

### <span data-ttu-id="b321e-149">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b321e-149">-AsJob</span></span>
<span data-ttu-id="b321e-150">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b321e-150">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b321e-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b321e-151">-DefaultProfile</span></span>
<span data-ttu-id="b321e-152">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b321e-152">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b321e-153">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="b321e-153">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="b321e-154">Die Protokollebene des Bereitstellungsdebuggers.</span><span class="sxs-lookup"><span data-stu-id="b321e-154">The deployment debug log level.</span></span>

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

### <span data-ttu-id="b321e-155">-Location</span><span class="sxs-lookup"><span data-stu-id="b321e-155">-Location</span></span>
<span data-ttu-id="b321e-156">Der Speicherort zum Speichern von Bereitstellungsdaten.</span><span class="sxs-lookup"><span data-stu-id="b321e-156">The location to store deployment data.</span></span>

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

### <span data-ttu-id="b321e-157">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="b321e-157">-ManagementGroupId</span></span>
<span data-ttu-id="b321e-158">Die Id der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b321e-158">The management group ID.</span></span>

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

### <span data-ttu-id="b321e-159">-Name</span><span class="sxs-lookup"><span data-stu-id="b321e-159">-Name</span></span>
<span data-ttu-id="b321e-160">Der Name der Bereitstellung, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b321e-160">The name of the deployment it's going to create.</span></span> <span data-ttu-id="b321e-161">Wenn nicht angegeben, wird standardmäßig der Vorlagendateiname verwendet, wenn eine Vorlagendatei bereitgestellt wird. ist standardmäßig auf die aktuelle Uhrzeit festgelegt, zu der ein Vorlagenobjekt bereitgestellt wird, z. B. "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="b321e-161">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="b321e-162">-Pre</span><span class="sxs-lookup"><span data-stu-id="b321e-162">-Pre</span></span>
<span data-ttu-id="b321e-163">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b321e-163">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b321e-164">-QueryString</span><span class="sxs-lookup"><span data-stu-id="b321e-164">-QueryString</span></span>
<span data-ttu-id="b321e-165">Die Abfragezeichenfolge (z. B. ein SAS-Token), die mit dem Parameter TemplateUri verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b321e-165">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="b321e-166">Würde bei verknüpften Vorlagen verwendet</span><span class="sxs-lookup"><span data-stu-id="b321e-166">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="b321e-167">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="b321e-167">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="b321e-168">Überspringt die PowerShell-Dynamische Parameterverarbeitung, die überprüft, ob der bereitgestellte Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b321e-168">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="b321e-169">Bei dieser Überprüfung wird der Benutzer aufgefordert, einen Wert für die fehlenden Parameter zur Verfügung zu stellen. Wenn jedoch -SkipTemplateParameterPrompt angegeben wird, werden diese Eingabeaufforderung und der Fehler sofort ignoriert, wenn festgestellt wurde, dass ein Parameter nicht in der Vorlage gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="b321e-169">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="b321e-170">Für nicht interaktive Skripts kann -SkipTemplateParameterPrompt bereitgestellt werden, um eine bessere Fehlermeldung für den Fall zu liefern, dass nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="b321e-170">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="b321e-171">-Tag</span><span class="sxs-lookup"><span data-stu-id="b321e-171">-Tag</span></span>
<span data-ttu-id="b321e-172">Die Tags, die für die Bereitstellung zu setzen sind.</span><span class="sxs-lookup"><span data-stu-id="b321e-172">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="b321e-173">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="b321e-173">-TemplateFile</span></span>
<span data-ttu-id="b321e-174">Lokaler Pfad zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="b321e-174">Local path to the template file.</span></span> <span data-ttu-id="b321e-175">Unterstützter Vorlagendateityp: json und bicep.</span><span class="sxs-lookup"><span data-stu-id="b321e-175">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="b321e-176">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="b321e-176">-TemplateObject</span></span>
<span data-ttu-id="b321e-177">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="b321e-177">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="b321e-178">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="b321e-178">-TemplateParameterFile</span></span>
<span data-ttu-id="b321e-179">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="b321e-179">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="b321e-180">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="b321e-180">-TemplateParameterObject</span></span>
<span data-ttu-id="b321e-181">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="b321e-181">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="b321e-182">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="b321e-182">-TemplateParameterUri</span></span>
<span data-ttu-id="b321e-183">URI für die Vorlagenparameterdatei.</span><span class="sxs-lookup"><span data-stu-id="b321e-183">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="b321e-184">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="b321e-184">-TemplateSpecId</span></span>
<span data-ttu-id="b321e-185">Ressourcen-ID der zu bereitstellende TemplateSpec.</span><span class="sxs-lookup"><span data-stu-id="b321e-185">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="b321e-186">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="b321e-186">-TemplateUri</span></span>
<span data-ttu-id="b321e-187">URI für die Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="b321e-187">Uri to the template file.</span></span>

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

### <span data-ttu-id="b321e-188">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="b321e-188">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="b321e-189">Durch Kommas getrennte Ressourcenänderungstypen, die aus den Ergebnissen What-If werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b321e-189">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="b321e-190">Gilt, wenn der Schalter -WhatIf oder -Confirm festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b321e-190">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="b321e-191">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="b321e-191">-WhatIfResultFormat</span></span>
<span data-ttu-id="b321e-192">Das What-If Ergebnisformat.</span><span class="sxs-lookup"><span data-stu-id="b321e-192">The What-If result format.</span></span> <span data-ttu-id="b321e-193">Gilt, wenn der Schalter -WhatIf oder -Confirm festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b321e-193">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="b321e-194">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b321e-194">-Confirm</span></span>
<span data-ttu-id="b321e-195">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b321e-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b321e-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b321e-196">-WhatIf</span></span>
<span data-ttu-id="b321e-197">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b321e-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b321e-198">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b321e-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b321e-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b321e-199">CommonParameters</span></span>
<span data-ttu-id="b321e-200">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b321e-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b321e-201">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b321e-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b321e-202">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b321e-202">INPUTS</span></span>

### <span data-ttu-id="b321e-203">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b321e-203">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b321e-204">System.String</span><span class="sxs-lookup"><span data-stu-id="b321e-204">System.String</span></span>

## <span data-ttu-id="b321e-205">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b321e-205">OUTPUTS</span></span>

### <span data-ttu-id="b321e-206">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="b321e-206">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="b321e-207">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b321e-207">NOTES</span></span>

## <span data-ttu-id="b321e-208">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b321e-208">RELATED LINKS</span></span>
