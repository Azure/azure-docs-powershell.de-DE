---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 3e704885c4ce2df0aee2a9b890f768983f93d7bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153633"
---
# <span data-ttu-id="052e2-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="052e2-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="052e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="052e2-102">SYNOPSIS</span></span>
<span data-ttu-id="052e2-103">Fügt einer Ressourcengruppe eine Azure-Bereitstellung hinzu.</span><span class="sxs-lookup"><span data-stu-id="052e2-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="052e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="052e2-104">SYNTAX</span></span>

### <span data-ttu-id="052e2-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="052e2-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="052e2-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="052e2-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="052e2-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="052e2-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="052e2-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="052e2-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="052e2-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="052e2-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="052e2-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="052e2-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="052e2-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="052e2-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="052e2-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="052e2-112">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="052e2-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="052e2-113">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="052e2-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="052e2-114">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="052e2-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="052e2-115">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="052e2-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="052e2-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="052e2-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="052e2-117">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="052e2-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="052e2-118">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="052e2-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="052e2-119">ByTemplateSpecResourceId</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="052e2-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="052e2-120">DESCRIPTION</span></span>
<span data-ttu-id="052e2-121">Das **Cmdlet "New-AzResourceGroupDeployment"** fügt einer vorhandenen Ressourcengruppe eine Bereitstellung hinzu.</span><span class="sxs-lookup"><span data-stu-id="052e2-121">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="052e2-122">Dazu gehören auch die Ressourcen, die für die Bereitstellung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="052e2-122">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="052e2-123">Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität, z. B. ein Datenbankserver, eine Datenbank, eine Website, ein virtueller Computer oder ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="052e2-123">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="052e2-124">Eine Azure-Ressourcengruppe ist eine Sammlung von Azure-Ressourcen, die als Einheit bereitgestellt werden, z. B. die Website, der Datenbankserver und Datenbanken, die für eine Finanzwebsite erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="052e2-124">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="052e2-125">Eine Ressourcengruppenbereitstellung verwendet eine Vorlage zum Hinzufügen von Ressourcen zu einer Ressourcengruppe und veröffentlicht diese so, dass sie in Azure verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="052e2-125">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="052e2-126">Wenn Sie einer Ressourcengruppe Ressourcen hinzufügen möchten, ohne eine Vorlage zu verwenden, verwenden Sie New-AzResource-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="052e2-126">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="052e2-127">Um eine Ressourcengruppenbereitstellung hinzuzufügen, geben Sie den Namen einer vorhandenen Ressourcengruppe und eine Ressourcengruppenvorlage an.</span><span class="sxs-lookup"><span data-stu-id="052e2-127">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="052e2-128">Eine Ressourcengruppenvorlage ist eine JSON-Zeichenfolge, die eine Ressourcengruppe für einen komplexen cloudbasierten Dienst darstellt, z. B. ein Webportal.</span><span class="sxs-lookup"><span data-stu-id="052e2-128">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="052e2-129">Die Vorlage enthält Parameterplatzhalter für erforderliche Ressourcen und konfigurierbare Eigenschaftswerte, z. B. Namen und Größen.</span><span class="sxs-lookup"><span data-stu-id="052e2-129">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="052e2-130">Sie finden viele Vorlagen im Azure-Vorlagenkatalog, oder Sie können eigene Vorlagen erstellen.</span><span class="sxs-lookup"><span data-stu-id="052e2-130">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="052e2-131">Wenn Sie eine benutzerdefinierte Vorlage zum Erstellen einer Ressourcengruppe verwenden möchten, geben Sie den *Parameter "TemplateFile"* oder *"TemplateUri"* an.</span><span class="sxs-lookup"><span data-stu-id="052e2-131">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="052e2-132">Jede Vorlage enthält Parameter für konfigurierbare Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="052e2-132">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="052e2-133">Um Werte für die Vorlagenparameter anzugeben, geben Sie den *Parameter "TemplateParameterFile"* oder den Parameter *"TemplateParameterObject"* an.</span><span class="sxs-lookup"><span data-stu-id="052e2-133">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="052e2-134">Alternativ können Sie die Vorlagenparameter verwenden, die dem Befehl dynamisch hinzugefügt werden, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="052e2-134">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="052e2-135">Wenn Sie dynamische Parameter verwenden möchten, geben Sie diese an der Eingabeaufforderung ein, oder geben Sie ein Minuszeichen (-) ein, um einen Parameter anzugeben, und verwenden Sie die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="052e2-135">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="052e2-136">Werte von Vorlagenparametern, die Sie an der Eingabeaufforderung eingeben, haben Vorrang vor Werten in einem Vorlagenparameterobjekt oder in einer Vorlagenparameterdatei.</span><span class="sxs-lookup"><span data-stu-id="052e2-136">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="052e2-137">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="052e2-137">EXAMPLES</span></span>

### <span data-ttu-id="052e2-138">Beispiel 1: Verwenden einer benutzerdefinierten Vorlage und Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="052e2-138">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="052e2-139">Dieser Befehl erstellt eine neue Bereitstellung mithilfe einer benutzerdefinierten Vorlage und einer Vorlagendatei auf dem Datenträger mit definierten Tagsparametern.</span><span class="sxs-lookup"><span data-stu-id="052e2-139">This command creates a new deployment by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="052e2-140">Der Befehl verwendet den *Parameter "TemplateFile",* um die Vorlage anzugeben, und den *Parameter "TemplateParameterFile",* um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="052e2-140">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="052e2-141">Beispiel 2: Verwenden eines benutzerdefinierten Vorlagenobjekts und einer Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="052e2-141">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="052e2-142">Dieser Befehl erstellt eine neue Bereitstellung mithilfe einer benutzerdefinierten Datei und einer Vorlagendatei auf dem Datenträger, die in eine Speicherhashtable konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="052e2-142">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="052e2-143">Die ersten beiden Befehle lesen den Text für die Vorlagendatei auf dem Datenträger und konvertieren sie in eine Speicherhashtable.</span><span class="sxs-lookup"><span data-stu-id="052e2-143">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="052e2-144">Der letzte Befehl verwendet den *Parameter "TemplateObject",* um die Hashtabelle und den *Parameter "TemplateParameterFile"* anzugeben, um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="052e2-144">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="052e2-145">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="052e2-145">Example 3</span></span>

<span data-ttu-id="052e2-146">Fügt einer Ressourcengruppe eine Azure-Bereitstellung hinzu.</span><span class="sxs-lookup"><span data-stu-id="052e2-146">Adds an Azure deployment to a resource group.</span></span> <span data-ttu-id="052e2-147">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="052e2-147">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzResourceGroupDeployment -DeploymentDebugLogLevel RequestContent -Name mynewstorageaccount -ResourceGroupName 'ContosoEngineering' -TemplateFile 'D:\Azure\Templates\EngineeringSite.json' -TemplateParameterObject <Hashtable>
```

### <span data-ttu-id="052e2-148">Beispiel 4: Bereitstellen einer Vorlage, die in einem nicht öffentlichen Speicherkonto gespeichert ist, mithilfe eines URI- und SAS-Tokens</span><span class="sxs-lookup"><span data-stu-id="052e2-148">Example 4: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "RGName" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```
<span data-ttu-id="052e2-149">Mit diesem Befehl wird mithilfe der Vorlage in TemplateUri eine neue Bereitstellung erstellt, die nicht öffentlich ist und für den Zugriff ein Tokenparameter erforderlich ist, der mit dem Parameter "QueryString" bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="052e2-149">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="052e2-150">Mit diesem Befehl wird effektiv über die URL auf die Vorlage https://example.com/example.json?foo zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="052e2-150">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="052e2-151">Dies kann verwendet werden, wenn Sie eine Vorlage in einem Speicherkonto verwenden möchten, indem Sie das SAS-Token als QueryString</span><span class="sxs-lookup"><span data-stu-id="052e2-151">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>
## <span data-ttu-id="052e2-152">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="052e2-152">PARAMETERS</span></span>

### <span data-ttu-id="052e2-153">-AsJob</span><span class="sxs-lookup"><span data-stu-id="052e2-153">-AsJob</span></span>
<span data-ttu-id="052e2-154">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="052e2-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="052e2-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="052e2-155">-DefaultProfile</span></span>
<span data-ttu-id="052e2-156">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="052e2-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="052e2-157">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="052e2-157">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="052e2-158">Gibt eine Debugprotokollebene an.</span><span class="sxs-lookup"><span data-stu-id="052e2-158">Specifies a debug log level.</span></span>
<span data-ttu-id="052e2-159">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="052e2-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="052e2-160">RequestContent</span><span class="sxs-lookup"><span data-stu-id="052e2-160">RequestContent</span></span>
- <span data-ttu-id="052e2-161">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="052e2-161">ResponseContent</span></span>
- <span data-ttu-id="052e2-162">Alle</span><span class="sxs-lookup"><span data-stu-id="052e2-162">All</span></span>
- <span data-ttu-id="052e2-163">Keine</span><span class="sxs-lookup"><span data-stu-id="052e2-163">None</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RequestContent, ResponseContent, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="052e2-164">-Force</span><span class="sxs-lookup"><span data-stu-id="052e2-164">-Force</span></span>
<span data-ttu-id="052e2-165">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="052e2-165">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="052e2-166">-Mode</span><span class="sxs-lookup"><span data-stu-id="052e2-166">-Mode</span></span>
<span data-ttu-id="052e2-167">Gibt den Bereitstellungsmodus an.</span><span class="sxs-lookup"><span data-stu-id="052e2-167">Specifies the deployment mode.</span></span> <span data-ttu-id="052e2-168">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="052e2-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="052e2-169">Abgeschlossen: Im vollständigen Modus löscht der Ressourcen-Manager Ressourcen, die in der Ressourcengruppe vorhanden, aber nicht in der Vorlage angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="052e2-169">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="052e2-170">Inkrementell: Im inkrementellen Modus belässt der Ressourcen-Manager unveränderte Ressourcen, die in der Ressourcengruppe vorhanden, aber nicht in der Vorlage angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="052e2-170">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="052e2-171">-Name</span><span class="sxs-lookup"><span data-stu-id="052e2-171">-Name</span></span>
<span data-ttu-id="052e2-172">Der Name der Bereitstellung, die erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="052e2-172">The name of the deployment it's going to create.</span></span> <span data-ttu-id="052e2-173">Wenn keine Angabe erfolgt, wird standardmäßig der Vorlagendateiname verwendet, wenn eine Vorlagendatei bereitgestellt wird. wird standardmäßig die aktuelle Uhrzeit verwendet, zu der ein Vorlagenobjekt bereitgestellt wird, z. B. "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="052e2-173">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="052e2-174">-Pre</span><span class="sxs-lookup"><span data-stu-id="052e2-174">-Pre</span></span>
<span data-ttu-id="052e2-175">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="052e2-175">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="052e2-176">-QueryString</span><span class="sxs-lookup"><span data-stu-id="052e2-176">-QueryString</span></span>
<span data-ttu-id="052e2-177">Die Abfragezeichenfolge (z. B. ein SAS-Token), die mit dem "TemplateUri"-Parameter verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="052e2-177">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="052e2-178">Würde im Fall von verknüpften Vorlagen verwendet werden</span><span class="sxs-lookup"><span data-stu-id="052e2-178">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="052e2-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="052e2-179">-ResourceGroupName</span></span>
<span data-ttu-id="052e2-180">Gibt den Namen der Ressourcengruppe an, die bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="052e2-180">Specifies the name of the resource group to deploy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="052e2-181">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="052e2-181">-RollBackDeploymentName</span></span>
<span data-ttu-id="052e2-182">Ein Rollback zur erfolgreichen Bereitstellung unter dem angegebenen Namen in der Ressourcengruppe sollte nicht verwendet werden, wenn "-RollbackToLastDeployment" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="052e2-182">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="052e2-183">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="052e2-183">-RollbackToLastDeployment</span></span>
<span data-ttu-id="052e2-184">Ein Rollback zur letzten erfolgreichen Bereitstellung in der Ressourcengruppe sollte nicht vorhanden sein, wenn "-RollBackDeploymentName" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="052e2-184">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="052e2-185">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="052e2-185">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="052e2-186">Überspringt die Verarbeitung dynamischer PowerShell-Parameter, die überprüft, ob der bereitgestellte Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="052e2-186">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="052e2-187">Bei dieser Überprüfung müsste der Benutzer einen Wert für die fehlenden Parameter angeben. Wenn jedoch "-SkipTemplateParameterPrompt" angegeben wird, wird diese Eingabeaufforderung und der Fehler sofort ignoriert, wenn ein Parameter nicht in der Vorlage gebunden wurde.</span><span class="sxs-lookup"><span data-stu-id="052e2-187">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="052e2-188">Bei nicht interaktiven Skripts kann "-SkipTemplateParameterPrompt" bereitgestellt werden, um eine bessere Fehlermeldung für den Fall zu liefern, dass nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="052e2-188">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="052e2-189">-Tag</span><span class="sxs-lookup"><span data-stu-id="052e2-189">-Tag</span></span>
<span data-ttu-id="052e2-190">Die Tags, die für die Bereitstellung verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="052e2-190">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="052e2-191">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="052e2-191">-TemplateFile</span></span>
<span data-ttu-id="052e2-192">Gibt den vollständigen Pfad einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="052e2-192">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="052e2-193">Dabei kann es sich um eine benutzerdefinierte Vorlage oder eine Katalogvorlage handelt, die als JSON-Datei gespeichert wird, z. B. eine, die mit dem **Cmdlet Save-AzResourceGroupGalleryTemplate** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="052e2-193">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="052e2-194">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="052e2-194">-TemplateObject</span></span>
<span data-ttu-id="052e2-195">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="052e2-195">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="052e2-196">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="052e2-196">-TemplateParameterFile</span></span>
<span data-ttu-id="052e2-197">Gibt den vollständigen Pfad einer JSON-Datei an, die die Namen und Werte der Vorlagenparameter enthält.</span><span class="sxs-lookup"><span data-stu-id="052e2-197">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="052e2-198">Wenn eine Vorlage Parameter enthält, müssen Sie die Parameterwerte mit dem Parameter *"TemplateParameterFile"* oder dem Parameter *"TemplateParameterObject"* angeben.</span><span class="sxs-lookup"><span data-stu-id="052e2-198">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="052e2-199">Vorlagenparameter werden dynamisch zum Befehl hinzugefügt, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="052e2-199">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="052e2-200">Um die dynamischen Parameter zu verwenden, geben Sie ein Minuszeichen (-) ein, um einen Parameternamen anzugeben, und verwenden Sie dann die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="052e2-200">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="052e2-201">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="052e2-201">-TemplateParameterObject</span></span>
<span data-ttu-id="052e2-202">Gibt eine Hashtabelle mit Vorlagenparameternamen und -werten an.</span><span class="sxs-lookup"><span data-stu-id="052e2-202">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="052e2-203">Wenn Sie Hilfe zu Hashtabellen in Windows PowerShell, geben Sie " `Get-Help about_Hash_Tables` ein.</span><span class="sxs-lookup"><span data-stu-id="052e2-203">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="052e2-204">Wenn eine Vorlage Parameter enthält, müssen Sie Parameterwerte angeben.</span><span class="sxs-lookup"><span data-stu-id="052e2-204">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="052e2-205">Vorlagenparameter werden dynamisch zum Befehl hinzugefügt, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="052e2-205">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="052e2-206">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="052e2-206">-TemplateParameterUri</span></span>
<span data-ttu-id="052e2-207">Gibt den URI einer Vorlagenparameterdatei an.</span><span class="sxs-lookup"><span data-stu-id="052e2-207">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="052e2-208">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="052e2-208">-TemplateSpecId</span></span>
<span data-ttu-id="052e2-209">Ressourcen-ID der bereitgestellten "templateSpec".</span><span class="sxs-lookup"><span data-stu-id="052e2-209">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="052e2-210">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="052e2-210">-TemplateUri</span></span>
<span data-ttu-id="052e2-211">Gibt den URI einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="052e2-211">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="052e2-212">Bei dieser Datei kann es sich um eine benutzerdefinierte Vorlage oder eine Katalogvorlage handelt, die als JSON-Datei gespeichert wird, z. B. mithilfe von **Save-AzResourceGroupGalleryTemplate.**</span><span class="sxs-lookup"><span data-stu-id="052e2-212">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="052e2-213">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="052e2-213">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="052e2-214">Durch Kommas getrennte Ressourcenänderungstypen, die aus den What-If werden sollen.</span><span class="sxs-lookup"><span data-stu-id="052e2-214">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="052e2-215">Anwendbar, wenn der Schalter "-WhatIf" oder "-Confirm" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="052e2-215">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="052e2-216">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="052e2-216">-WhatIfResultFormat</span></span>
<span data-ttu-id="052e2-217">Das What-If Ergebnisformat.</span><span class="sxs-lookup"><span data-stu-id="052e2-217">The What-If result format.</span></span>

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

### <span data-ttu-id="052e2-218">-Confirm</span><span class="sxs-lookup"><span data-stu-id="052e2-218">-Confirm</span></span>
<span data-ttu-id="052e2-219">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="052e2-219">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="052e2-220">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="052e2-220">-WhatIf</span></span>
<span data-ttu-id="052e2-221">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="052e2-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="052e2-222">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="052e2-222">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="052e2-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="052e2-223">CommonParameters</span></span>
<span data-ttu-id="052e2-224">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="052e2-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="052e2-225">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="052e2-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="052e2-226">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="052e2-226">INPUTS</span></span>

### <span data-ttu-id="052e2-227">System.String</span><span class="sxs-lookup"><span data-stu-id="052e2-227">System.String</span></span>

### <span data-ttu-id="052e2-228">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="052e2-228">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="052e2-229">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="052e2-229">System.Collections.Hashtable</span></span>

## <span data-ttu-id="052e2-230">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="052e2-230">OUTPUTS</span></span>

### <span data-ttu-id="052e2-231">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="052e2-231">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="052e2-232">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="052e2-232">NOTES</span></span>

## <span data-ttu-id="052e2-233">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="052e2-233">RELATED LINKS</span></span>

[<span data-ttu-id="052e2-234">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="052e2-234">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="052e2-235">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="052e2-235">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="052e2-236">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="052e2-236">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="052e2-237">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="052e2-237">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="052e2-238">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="052e2-238">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="052e2-239">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="052e2-239">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)