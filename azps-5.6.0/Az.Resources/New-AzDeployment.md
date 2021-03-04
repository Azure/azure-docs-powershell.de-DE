---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: 42f68065fb5a1785d0f9a243d0165bc72125743d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919155"
---
# <span data-ttu-id="122ff-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="122ff-101">New-AzDeployment</span></span>

## <span data-ttu-id="122ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="122ff-102">SYNOPSIS</span></span>
<span data-ttu-id="122ff-103">Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="122ff-103">Create a deployment</span></span>

## <span data-ttu-id="122ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="122ff-104">SYNTAX</span></span>

### <span data-ttu-id="122ff-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="122ff-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="122ff-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="122ff-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="122ff-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="122ff-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="122ff-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="122ff-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="122ff-109">ByTemplateSpecResourceIdAndParamsObject</span><span class="sxs-lookup"><span data-stu-id="122ff-109">ByTemplateSpecResourceIdAndParamsObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="122ff-110">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="122ff-110">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="122ff-111">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="122ff-111">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="122ff-112">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="122ff-112">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="122ff-113">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="122ff-113">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="122ff-114">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="122ff-114">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="122ff-115">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="122ff-115">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="122ff-116">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="122ff-116">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="122ff-117">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="122ff-117">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="122ff-118">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="122ff-118">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="122ff-119">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="122ff-119">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="122ff-120">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="122ff-120">ByTemplateSpecResourceId</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="122ff-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="122ff-121">DESCRIPTION</span></span>
<span data-ttu-id="122ff-122">Das **Cmdlet New-AzDeployment** fügt eine Bereitstellung im aktuellen Abonnementbereich hinzu.</span><span class="sxs-lookup"><span data-stu-id="122ff-122">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="122ff-123">Dies schließt die Ressourcen ein, die für die Bereitstellung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="122ff-123">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="122ff-124">Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität.</span><span class="sxs-lookup"><span data-stu-id="122ff-124">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="122ff-125">Eine Ressource kann in einer Ressourcengruppe leben, z. B. Datenbankserver, Datenbank, Website, virtueller Computer oder Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="122ff-125">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="122ff-126">Oder es kann sich um eine Ressource auf Abonnementebene wie Rollendefinition, Richtliniendefinition usw. geben.</span><span class="sxs-lookup"><span data-stu-id="122ff-126">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="122ff-127">Zum Hinzufügen von Ressourcen zu einer Ressourcengruppe verwenden Sie **die New-AzResourceGroupDeployment,** die eine Bereitstellung bei einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="122ff-127">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="122ff-128">Das **Cmdlet "New-AzDeployment"** erstellt eine Bereitstellung im aktuellen Abonnementbereich, wodurch Ressourcen auf Abonnementebene bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="122ff-128">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="122ff-129">Wenn Sie eine Bereitstellung im Abonnement hinzufügen möchten, geben Sie den Speicherort und eine Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="122ff-129">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="122ff-130">Der Speicherort teilt Azure Resource Manager mit, wo die Bereitstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="122ff-130">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="122ff-131">Die Vorlage ist eine JSON-Zeichenfolge, die einzelne ressourcen enthält, die bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="122ff-131">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="122ff-132">Die Vorlage enthält Parameterplatzhalter für erforderliche Ressourcen und konfigurierbare Eigenschaftswerte, z. B. Namen und Größen.</span><span class="sxs-lookup"><span data-stu-id="122ff-132">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="122ff-133">Wenn Sie eine benutzerdefinierte Vorlage für die Bereitstellung verwenden möchten, geben Sie den *Parameter TemplateFile* oder *TemplateUri* an.</span><span class="sxs-lookup"><span data-stu-id="122ff-133">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="122ff-134">Jede Vorlage verfügt über Parameter für konfigurierbare Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="122ff-134">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="122ff-135">Wenn Sie Werte für die Vorlagenparameter angeben möchten, geben Sie den *Parameter TemplateParameterFile* oder *den Parameter TemplateParameterObject* an.</span><span class="sxs-lookup"><span data-stu-id="122ff-135">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="122ff-136">Alternativ können Sie die Vorlagenparameter verwenden, die dem Befehl dynamisch hinzugefügt werden, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="122ff-136">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="122ff-137">Wenn Sie dynamische Parameter verwenden möchten, geben Sie sie an der Eingabeaufforderung ein, oder geben Sie ein Minuszeichen (-) ein, um einen Parameter anzugeben, und verwenden Sie die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="122ff-137">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="122ff-138">Vorlagenparameterwerte, die Sie an der Eingabeaufforderung eingeben, haben Vorrang vor Werten in einem Vorlagenparameterobjekt oder einer Datei.</span><span class="sxs-lookup"><span data-stu-id="122ff-138">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="122ff-139">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="122ff-139">EXAMPLES</span></span>

### <span data-ttu-id="122ff-140">Beispiel 1: Verwenden einer benutzerdefinierten Vorlage und Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="122ff-140">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="122ff-141">Mit diesem Befehl wird eine neue Bereitstellung im aktuellen Abonnementbereich mithilfe einer benutzerdefinierten Vorlage und einer Vorlagendatei auf dem Datenträger mit dem Parameter für definierte Tags erstellt.</span><span class="sxs-lookup"><span data-stu-id="122ff-141">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="122ff-142">Der Befehl verwendet den *Parameter TemplateFile,* um die Vorlage und den *Parameter TemplateParameterFile* anzugeben, um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="122ff-142">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="122ff-143">Sie verwendet den *Parameter TemplateVersion,* um die Version der Vorlage anzugeben.</span><span class="sxs-lookup"><span data-stu-id="122ff-143">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="122ff-144">Beispiel 2: Bereitstellen einer In einem nicht öffentlichen Speicherkonto gespeicherten Vorlage mithilfe eines URI- und SAS-Tokens</span><span class="sxs-lookup"><span data-stu-id="122ff-144">Example 2: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```

<span data-ttu-id="122ff-145">Mit diesem Befehl wird mithilfe der Vorlage in TemplateUri eine neue Bereitstellung erstellt, die nicht öffentlich ist und für den Zugriff ein Tokenparameter erforderlich ist, der mit dem Parameter QueryString bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="122ff-145">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="122ff-146">Durch Ausführen dieses Befehls wird effektiv über die URL auf die Vorlage https://example.com/example.json?foo zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="122ff-146">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="122ff-147">Dies kann verwendet werden, wenn Sie eine Vorlage in einem Speicherkonto verwenden möchten, indem Sie das SAS-Token als QueryString bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="122ff-147">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>

### <span data-ttu-id="122ff-148">Beispiel 3: Verwenden eines benutzerdefinierten Vorlagenobjekts und einer Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="122ff-148">Example 3: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="122ff-149">Mit diesem Befehl wird eine neue Bereitstellung im aktuellen Abonnementbereich mithilfe einer benutzerdefinierten Vorlage und einer Vorlagendatei auf dem Datenträger erstellt, die in eine #A0 im Arbeitsspeicher konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="122ff-149">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="122ff-150">Die ersten beiden Befehle lesen den Text für die Vorlagendatei auf dem Datenträger und konvertieren sie in eine Hashtabelle im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="122ff-150">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="122ff-151">Der letzte Befehl verwendet den *Parameter TemplateObject,* um diese Hashtabelle und den *Parameter TemplateParameterFile* anzugeben, um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="122ff-151">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="122ff-152">Sie verwendet den *Parameter TemplateVersion,* um die Version der Vorlage anzugeben.</span><span class="sxs-lookup"><span data-stu-id="122ff-152">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="122ff-153">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="122ff-153">PARAMETERS</span></span>

### <span data-ttu-id="122ff-154">-AsJob</span><span class="sxs-lookup"><span data-stu-id="122ff-154">-AsJob</span></span>
<span data-ttu-id="122ff-155">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="122ff-155">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="122ff-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="122ff-156">-DefaultProfile</span></span>
<span data-ttu-id="122ff-157">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="122ff-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="122ff-158">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="122ff-158">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="122ff-159">Die Protokollebene des Bereitstellungsdebuggers.</span><span class="sxs-lookup"><span data-stu-id="122ff-159">The deployment debug log level.</span></span>

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

### <span data-ttu-id="122ff-160">-Location</span><span class="sxs-lookup"><span data-stu-id="122ff-160">-Location</span></span>
<span data-ttu-id="122ff-161">Der Speicherort zum Speichern von Bereitstellungsdaten.</span><span class="sxs-lookup"><span data-stu-id="122ff-161">The location to store deployment data.</span></span>

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

### <span data-ttu-id="122ff-162">-Name</span><span class="sxs-lookup"><span data-stu-id="122ff-162">-Name</span></span>
<span data-ttu-id="122ff-163">Der Name der Bereitstellung, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="122ff-163">The name of the deployment it's going to create.</span></span> <span data-ttu-id="122ff-164">Wenn nicht angegeben, wird standardmäßig der Vorlagendateiname verwendet, wenn eine Vorlagendatei bereitgestellt wird. ist standardmäßig auf die aktuelle Uhrzeit festgelegt, zu der ein Vorlagenobjekt bereitgestellt wird, z. B. "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="122ff-164">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="122ff-165">-Pre</span><span class="sxs-lookup"><span data-stu-id="122ff-165">-Pre</span></span>
<span data-ttu-id="122ff-166">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="122ff-166">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="122ff-167">-QueryString</span><span class="sxs-lookup"><span data-stu-id="122ff-167">-QueryString</span></span>
<span data-ttu-id="122ff-168">Die Abfragezeichenfolge (z. B. ein SAS-Token), die mit dem Parameter TemplateUri verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="122ff-168">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="122ff-169">Würde bei verknüpften Vorlagen verwendet</span><span class="sxs-lookup"><span data-stu-id="122ff-169">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="122ff-170">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="122ff-170">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="122ff-171">Überspringt die PowerShell-Dynamische Parameterverarbeitung, die überprüft, ob der bereitgestellte Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="122ff-171">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="122ff-172">Bei dieser Überprüfung wird der Benutzer aufgefordert, einen Wert für die fehlenden Parameter zur Verfügung zu stellen. Wenn jedoch -SkipTemplateParameterPrompt angegeben wird, werden diese Eingabeaufforderung und der Fehler sofort ignoriert, wenn festgestellt wurde, dass ein Parameter nicht in der Vorlage gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="122ff-172">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="122ff-173">Für nicht interaktive Skripts kann -SkipTemplateParameterPrompt bereitgestellt werden, um eine bessere Fehlermeldung für den Fall zu liefern, dass nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="122ff-173">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="122ff-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="122ff-174">-Tag</span></span>
<span data-ttu-id="122ff-175">Die Tags, die für die Bereitstellung zu setzen sind.</span><span class="sxs-lookup"><span data-stu-id="122ff-175">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="122ff-176">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="122ff-176">-TemplateFile</span></span>
<span data-ttu-id="122ff-177">Lokaler Pfad zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="122ff-177">Local path to the template file.</span></span> <span data-ttu-id="122ff-178">Unterstützter Vorlagendateityp: json und bicep.</span><span class="sxs-lookup"><span data-stu-id="122ff-178">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="122ff-179">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="122ff-179">-TemplateObject</span></span>
<span data-ttu-id="122ff-180">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="122ff-180">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="122ff-181">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="122ff-181">-TemplateParameterFile</span></span>
<span data-ttu-id="122ff-182">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="122ff-182">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="122ff-183">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="122ff-183">-TemplateParameterObject</span></span>
<span data-ttu-id="122ff-184">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="122ff-184">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="122ff-185">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="122ff-185">-TemplateParameterUri</span></span>
<span data-ttu-id="122ff-186">URI für die Vorlagenparameterdatei.</span><span class="sxs-lookup"><span data-stu-id="122ff-186">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="122ff-187">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="122ff-187">-TemplateSpecId</span></span>
<span data-ttu-id="122ff-188">Ressourcen-ID der zu bereitstellende TemplateSpec.</span><span class="sxs-lookup"><span data-stu-id="122ff-188">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="122ff-189">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="122ff-189">-TemplateUri</span></span>
<span data-ttu-id="122ff-190">URI für die Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="122ff-190">Uri to the template file.</span></span>

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

### <span data-ttu-id="122ff-191">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="122ff-191">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="122ff-192">Durch Kommas getrennte Ressourcenänderungstypen, die aus den Ergebnissen What-If werden sollen.</span><span class="sxs-lookup"><span data-stu-id="122ff-192">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="122ff-193">Gilt, wenn der Schalter -WhatIf oder -Confirm festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="122ff-193">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="122ff-194">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="122ff-194">-WhatIfResultFormat</span></span>
<span data-ttu-id="122ff-195">Das What-If Ergebnisformat.</span><span class="sxs-lookup"><span data-stu-id="122ff-195">The What-If result format.</span></span>

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

### <span data-ttu-id="122ff-196">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="122ff-196">-Confirm</span></span>
<span data-ttu-id="122ff-197">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="122ff-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="122ff-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="122ff-198">-WhatIf</span></span>
<span data-ttu-id="122ff-199">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="122ff-199">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="122ff-200">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="122ff-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="122ff-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="122ff-201">CommonParameters</span></span>
<span data-ttu-id="122ff-202">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="122ff-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="122ff-203">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="122ff-203">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="122ff-204">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="122ff-204">INPUTS</span></span>

### <span data-ttu-id="122ff-205">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="122ff-205">System.Collections.Hashtable</span></span>

### <span data-ttu-id="122ff-206">System.String</span><span class="sxs-lookup"><span data-stu-id="122ff-206">System.String</span></span>

## <span data-ttu-id="122ff-207">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="122ff-207">OUTPUTS</span></span>

### <span data-ttu-id="122ff-208">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="122ff-208">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="122ff-209">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="122ff-209">NOTES</span></span>

## <span data-ttu-id="122ff-210">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="122ff-210">RELATED LINKS</span></span>
