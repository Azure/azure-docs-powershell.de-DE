---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: d3b9fce538512fdb55328d6c2e846c955bcfbb5d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153657"
---
# <span data-ttu-id="4b7d8-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="4b7d8-101">New-AzDeployment</span></span>

## <span data-ttu-id="4b7d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b7d8-102">SYNOPSIS</span></span>
<span data-ttu-id="4b7d8-103">Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="4b7d8-103">Create a deployment</span></span>

## <span data-ttu-id="4b7d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b7d8-104">SYNTAX</span></span>

### <span data-ttu-id="4b7d8-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="4b7d8-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b7d8-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4b7d8-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b7d8-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4b7d8-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b7d8-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4b7d8-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b7d8-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4b7d8-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b7d8-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4b7d8-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b7d8-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4b7d8-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b7d8-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="4b7d8-112">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterFile <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b7d8-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4b7d8-113">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b7d8-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4b7d8-114">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b7d8-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4b7d8-115">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b7d8-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="4b7d8-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateParameterUri <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b7d8-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4b7d8-117">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b7d8-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4b7d8-118">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b7d8-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="4b7d8-119">ByTemplateSpecResourceId</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>]
 [-AsJob] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b7d8-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b7d8-120">DESCRIPTION</span></span>
<span data-ttu-id="4b7d8-121">Das **Cmdlet "New-AzDeployment"** fügt eine Bereitstellung zum aktuellen Abonnementbereich hinzu.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-121">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="4b7d8-122">Dazu gehören auch die Ressourcen, die für die Bereitstellung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-122">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="4b7d8-123">Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-123">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="4b7d8-124">Eine Ressource kann sich in einer Ressourcengruppe befinden, z. B. Datenbankserver, Datenbank, Website, virtueller Computer oder Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-124">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="4b7d8-125">Oder es kann sich um eine Ressource auf Abonnementebene wie Rollendefinition, Richtliniendefinition usw.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-125">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="4b7d8-126">Wenn Sie einer Ressourcengruppe Ressourcen hinzufügen möchten, verwenden Sie die **New-AzResourceGroupDeployment,** die eine Bereitstellung für eine Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-126">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="4b7d8-127">Das **Cmdlet "New-AzDeployment"** erstellt eine Bereitstellung im aktuellen Abonnementbereich, wodurch Ressourcen auf Abonnementebene bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-127">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="4b7d8-128">Wenn Sie eine Bereitstellung im Abonnement hinzufügen möchten, geben Sie den Speicherort und eine Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-128">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="4b7d8-129">Der Speicherort teilt dem Azure-Ressourcen-Manager mit, wo die Bereitstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-129">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="4b7d8-130">Die Vorlage ist eine JSON-Zeichenfolge, die einzelne ressourcen enthält, die bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-130">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="4b7d8-131">Die Vorlage enthält Parameterplatzhalter für erforderliche Ressourcen und konfigurierbare Eigenschaftswerte, z. B. Namen und Größen.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-131">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="4b7d8-132">Wenn Sie eine benutzerdefinierte Vorlage für die Bereitstellung verwenden möchten, geben Sie den *Parameter "TemplateFile"* oder *"TemplateUri"* an.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-132">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="4b7d8-133">Jede Vorlage enthält Parameter für konfigurierbare Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-133">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="4b7d8-134">Um Werte für die Vorlagenparameter anzugeben, geben Sie den *Parameter "TemplateParameterFile"* oder den Parameter *"TemplateParameterObject"* an.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-134">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="4b7d8-135">Alternativ können Sie die Vorlagenparameter verwenden, die dem Befehl dynamisch hinzugefügt werden, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-135">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="4b7d8-136">Wenn Sie dynamische Parameter verwenden möchten, geben Sie diese an der Eingabeaufforderung ein, oder geben Sie ein Minuszeichen (-) ein, um einen Parameter anzugeben, und verwenden Sie die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-136">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="4b7d8-137">Werte von Vorlagenparametern, die Sie an der Eingabeaufforderung eingeben, haben Vorrang vor Werten in einem Vorlagenparameterobjekt oder in einer Vorlagenparameterdatei.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-137">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="4b7d8-138">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4b7d8-138">EXAMPLES</span></span>

### <span data-ttu-id="4b7d8-139">Beispiel 1: Verwenden einer benutzerdefinierten Vorlage und Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="4b7d8-139">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="4b7d8-140">Dieser Befehl erstellt eine neue Bereitstellung im aktuellen Abonnementbereich mithilfe einer benutzerdefinierten Vorlage und einer Vorlagendatei auf dem Datenträger mit definierten Tagsparametern.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-140">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="4b7d8-141">Der Befehl verwendet den *Parameter "TemplateFile",* um die Vorlage anzugeben, und den *Parameter "TemplateParameterFile",* um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-141">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="4b7d8-142">Es verwendet den *Parameter "TemplateVersion",* um die Version der Vorlage anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-142">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="4b7d8-143">Beispiel 2: Bereitstellen einer Vorlage, die in einem nicht öffentlichen Speicherkonto gespeichert ist, mit einem URI und einem SAS-Token</span><span class="sxs-lookup"><span data-stu-id="4b7d8-143">Example 2: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```
<span data-ttu-id="4b7d8-144">Mit diesem Befehl wird mithilfe der Vorlage in TemplateUri eine neue Bereitstellung erstellt, die nicht öffentlich ist und für den Zugriff ein Tokenparameter erforderlich ist, der mit dem Parameter "QueryString" bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-144">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="4b7d8-145">Mit diesem Befehl wird effektiv über die URL auf die Vorlage https://example.com/example.json?foo zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-145">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="4b7d8-146">Dies kann verwendet werden, wenn Sie eine Vorlage in einem Speicherkonto verwenden möchten, indem Sie das SAS-Token als QueryString</span><span class="sxs-lookup"><span data-stu-id="4b7d8-146">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>

### <span data-ttu-id="4b7d8-147">Beispiel 3: Verwenden eines benutzerdefinierten Vorlagenobjekts und einer Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="4b7d8-147">Example 3: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="4b7d8-148">Mit diesem Befehl wird eine neue Bereitstellung im aktuellen Abonnementbereich erstellt, indem eine benutzerdefinierte Vorlage und eine Vorlagendatei auf dem Datenträger verwendet wird, die in eine Speicherhashtable konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-148">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="4b7d8-149">Die ersten beiden Befehle lesen den Text für die Vorlagendatei auf dem Datenträger und konvertieren sie in eine Speicherhashtable.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-149">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="4b7d8-150">Der letzte Befehl verwendet den *Parameter "TemplateObject",* um diese Hashtabelle anzugeben, und den *Parameter "TemplateParameterFile",* um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-150">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="4b7d8-151">Es verwendet den *Parameter "TemplateVersion",* um die Version der Vorlage anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-151">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="4b7d8-152">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b7d8-152">PARAMETERS</span></span>

### <span data-ttu-id="4b7d8-153">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b7d8-153">-AsJob</span></span>
<span data-ttu-id="4b7d8-154">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4b7d8-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b7d8-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b7d8-155">-DefaultProfile</span></span>
<span data-ttu-id="4b7d8-156">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-156">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b7d8-157">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="4b7d8-157">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="4b7d8-158">Die Protokollebene des Bereitstellungsdebuggers.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-158">The deployment debug log level.</span></span>

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

### <span data-ttu-id="4b7d8-159">-Location</span><span class="sxs-lookup"><span data-stu-id="4b7d8-159">-Location</span></span>
<span data-ttu-id="4b7d8-160">Der Speicherort zum Speichern von Bereitstellungsdaten.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-160">The location to store deployment data.</span></span>

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

### <span data-ttu-id="4b7d8-161">-Name</span><span class="sxs-lookup"><span data-stu-id="4b7d8-161">-Name</span></span>
<span data-ttu-id="4b7d8-162">Der Name der Bereitstellung, die erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-162">The name of the deployment it's going to create.</span></span> <span data-ttu-id="4b7d8-163">Wenn keine Angabe erfolgt, wird standardmäßig der Vorlagendateiname verwendet, wenn eine Vorlagendatei bereitgestellt wird. wird standardmäßig die aktuelle Uhrzeit verwendet, zu der ein Vorlagenobjekt bereitgestellt wird, z. B. "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="4b7d8-163">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="4b7d8-164">-Pre</span><span class="sxs-lookup"><span data-stu-id="4b7d8-164">-Pre</span></span>
<span data-ttu-id="4b7d8-165">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-165">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4b7d8-166">-QueryString</span><span class="sxs-lookup"><span data-stu-id="4b7d8-166">-QueryString</span></span>
<span data-ttu-id="4b7d8-167">Die Abfragezeichenfolge (z. B. ein SAS-Token), die mit dem "TemplateUri"-Parameter verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-167">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="4b7d8-168">Würde im Fall von verknüpften Vorlagen verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4b7d8-168">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="4b7d8-169">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="4b7d8-169">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="4b7d8-170">Überspringt die Verarbeitung dynamischer PowerShell-Parameter, die überprüft, ob der bereitgestellte Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-170">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="4b7d8-171">Bei dieser Überprüfung müsste der Benutzer einen Wert für die fehlenden Parameter angeben. Wenn jedoch "-SkipTemplateParameterPrompt" angegeben wird, wird diese Eingabeaufforderung und der Fehler sofort ignoriert, wenn ein Parameter nicht in der Vorlage gebunden wurde.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-171">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="4b7d8-172">Bei nicht interaktiven Skripts kann "-SkipTemplateParameterPrompt" bereitgestellt werden, um eine bessere Fehlermeldung für den Fall zu liefern, dass nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-172">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="4b7d8-173">-Tag</span><span class="sxs-lookup"><span data-stu-id="4b7d8-173">-Tag</span></span>
<span data-ttu-id="4b7d8-174">Die Tags, die für die Bereitstellung verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-174">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="4b7d8-175">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="4b7d8-175">-TemplateFile</span></span>
<span data-ttu-id="4b7d8-176">Lokaler Pfad zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-176">Local path to the template file.</span></span>

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

### <span data-ttu-id="4b7d8-177">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="4b7d8-177">-TemplateObject</span></span>
<span data-ttu-id="4b7d8-178">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-178">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="4b7d8-179">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="4b7d8-179">-TemplateParameterFile</span></span>
<span data-ttu-id="4b7d8-180">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-180">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="4b7d8-181">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="4b7d8-181">-TemplateParameterObject</span></span>
<span data-ttu-id="4b7d8-182">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-182">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="4b7d8-183">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="4b7d8-183">-TemplateParameterUri</span></span>
<span data-ttu-id="4b7d8-184">URI der Vorlagenparameterdatei.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-184">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="4b7d8-185">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="4b7d8-185">-TemplateSpecId</span></span>
<span data-ttu-id="4b7d8-186">Ressourcen-ID der bereitgestellten "templateSpec".</span><span class="sxs-lookup"><span data-stu-id="4b7d8-186">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="4b7d8-187">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="4b7d8-187">-TemplateUri</span></span>
<span data-ttu-id="4b7d8-188">URI der Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-188">Uri to the template file.</span></span>

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

### <span data-ttu-id="4b7d8-189">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="4b7d8-189">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="4b7d8-190">Durch Kommas getrennte Ressourcenänderungstypen, die aus den What-If werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-190">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="4b7d8-191">Anwendbar, wenn der Schalter "-WhatIf" oder "-Confirm" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-191">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="4b7d8-192">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="4b7d8-192">-WhatIfResultFormat</span></span>
<span data-ttu-id="4b7d8-193">Das What-If Ergebnisformat.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-193">The What-If result format.</span></span>

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

### <span data-ttu-id="4b7d8-194">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b7d8-194">-Confirm</span></span>
<span data-ttu-id="4b7d8-195">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b7d8-196">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4b7d8-196">-WhatIf</span></span>
<span data-ttu-id="4b7d8-197">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b7d8-198">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b7d8-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b7d8-199">CommonParameters</span></span>
<span data-ttu-id="4b7d8-200">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b7d8-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b7d8-201">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b7d8-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b7d8-202">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4b7d8-202">INPUTS</span></span>

### <span data-ttu-id="4b7d8-203">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4b7d8-203">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4b7d8-204">System.String</span><span class="sxs-lookup"><span data-stu-id="4b7d8-204">System.String</span></span>

## <span data-ttu-id="4b7d8-205">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4b7d8-205">OUTPUTS</span></span>

### <span data-ttu-id="4b7d8-206">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="4b7d8-206">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="4b7d8-207">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4b7d8-207">NOTES</span></span>

## <span data-ttu-id="4b7d8-208">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4b7d8-208">RELATED LINKS</span></span>
