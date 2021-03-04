---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 3403900fafae1615f8253b4d5671e497a1d507f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931691"
---
# <span data-ttu-id="a8c6f-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a8c6f-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="a8c6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8c6f-102">SYNOPSIS</span></span>
<span data-ttu-id="a8c6f-103">Fügt einer Ressourcengruppe eine Azure-Bereitstellung hinzu.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="a8c6f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a8c6f-104">SYNTAX</span></span>

### <span data-ttu-id="a8c6f-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="a8c6f-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8c6f-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a8c6f-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8c6f-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a8c6f-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8c6f-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="a8c6f-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8c6f-109">ByTemplateSpecResourceIdAndParamsObject</span><span class="sxs-lookup"><span data-stu-id="a8c6f-109">ByTemplateSpecResourceIdAndParamsObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8c6f-110">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a8c6f-110">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8c6f-111">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a8c6f-111">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8c6f-112">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="a8c6f-112">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8c6f-113">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="a8c6f-113">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8c6f-114">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a8c6f-114">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8c6f-115">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a8c6f-115">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8c6f-116">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="a8c6f-116">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8c6f-117">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="a8c6f-117">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8c6f-118">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="a8c6f-118">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8c6f-119">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="a8c6f-119">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8c6f-120">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="a8c6f-120">ByTemplateSpecResourceId</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8c6f-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a8c6f-121">DESCRIPTION</span></span>
<span data-ttu-id="a8c6f-122">Das **Cmdlet New-AzResourceGroupDeployment** fügt einer vorhandenen Ressourcengruppe eine Bereitstellung hinzu.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-122">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="a8c6f-123">Dies schließt die Ressourcen ein, die für die Bereitstellung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-123">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="a8c6f-124">Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität, z. B. ein Datenbankserver, eine Datenbank, eine Website, ein virtueller Computer oder ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-124">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="a8c6f-125">Eine Azure-Ressourcengruppe ist eine Sammlung von Azure-Ressourcen, die als Einheit bereitgestellt werden, z. B. die Website, der Datenbankserver und Datenbanken, die für eine Finanzwebsite erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-125">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="a8c6f-126">Eine Ressourcengruppenbereitstellung verwendet eine Vorlage zum Hinzufügen von Ressourcen zu einer Ressourcengruppe und veröffentlicht sie so, dass sie in Azure verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-126">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="a8c6f-127">Wenn Sie einer Ressourcengruppe Ressourcen hinzufügen möchten, ohne eine Vorlage zu verwenden, verwenden Sie das New-AzResource Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-127">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="a8c6f-128">Wenn Sie eine Ressourcengruppenbereitstellung hinzufügen möchten, geben Sie den Namen einer vorhandenen Ressourcengruppe und einer Ressourcengruppenvorlage an.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-128">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="a8c6f-129">Eine Ressourcengruppenvorlage ist eine JSON-Zeichenfolge, die eine Ressourcengruppe für einen komplexen cloudbasierten Dienst darstellt, z. B. ein Webportal.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-129">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="a8c6f-130">Die Vorlage enthält Parameterplatzhalter für erforderliche Ressourcen und konfigurierbare Eigenschaftswerte, z. B. Namen und Größen.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-130">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="a8c6f-131">Sie finden viele Vorlagen im Azure-Vorlagenkatalog, oder Sie können eigene Vorlagen erstellen.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-131">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="a8c6f-132">Wenn Sie eine benutzerdefinierte Vorlage zum Erstellen einer Ressourcengruppe verwenden möchten, geben Sie den *Parameter TemplateFile* oder *TemplateUri* an.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-132">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="a8c6f-133">Jede Vorlage verfügt über Parameter für konfigurierbare Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-133">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="a8c6f-134">Wenn Sie Werte für die Vorlagenparameter angeben möchten, geben Sie den *Parameter TemplateParameterFile* oder *den Parameter TemplateParameterObject* an.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-134">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="a8c6f-135">Alternativ können Sie die Vorlagenparameter verwenden, die dem Befehl dynamisch hinzugefügt werden, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-135">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="a8c6f-136">Wenn Sie dynamische Parameter verwenden möchten, geben Sie sie an der Eingabeaufforderung ein, oder geben Sie ein Minuszeichen (-) ein, um einen Parameter anzugeben, und verwenden Sie die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-136">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="a8c6f-137">Vorlagenparameterwerte, die Sie an der Eingabeaufforderung eingeben, haben Vorrang vor Werten in einem Vorlagenparameterobjekt oder einer Datei.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-137">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="a8c6f-138">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a8c6f-138">EXAMPLES</span></span>

### <span data-ttu-id="a8c6f-139">Beispiel 1: Verwenden einer benutzerdefinierten Vorlage und Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="a8c6f-139">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="a8c6f-140">Mit diesem Befehl wird eine neue Bereitstellung mithilfe einer benutzerdefinierten Vorlage und einer Vorlagendatei auf dem Datenträger mit definierten Tagsparametern erstellt.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-140">This command creates a new deployment by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="a8c6f-141">Der Befehl verwendet den *Parameter TemplateFile,* um die Vorlage und den *Parameter TemplateParameterFile* anzugeben, um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-141">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="a8c6f-142">Beispiel 2: Verwenden eines benutzerdefinierten Vorlagenobjekts und einer Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="a8c6f-142">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="a8c6f-143">Mit diesem Befehl wird eine neue Bereitstellung mithilfe einer benutzerdefinierten und einer Vorlagendatei auf einem Datenträger erstellt, die in eine In-Memory-Hashtable konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-143">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="a8c6f-144">Die ersten beiden Befehle lesen den Text für die Vorlagendatei auf dem Datenträger und konvertieren sie in eine Hashtabelle im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-144">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="a8c6f-145">Der letzte Befehl verwendet den *Parameter TemplateObject,* um die Hashtabelle und den *Parameter TemplateParameterFile* anzugeben, um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-145">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="a8c6f-146">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a8c6f-146">Example 3</span></span>

<span data-ttu-id="a8c6f-147">Fügt einer Ressourcengruppe eine Azure-Bereitstellung hinzu.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-147">Adds an Azure deployment to a resource group.</span></span> <span data-ttu-id="a8c6f-148">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="a8c6f-148">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzResourceGroupDeployment -DeploymentDebugLogLevel RequestContent -Name mynewstorageaccount -ResourceGroupName 'ContosoEngineering' -TemplateFile 'D:\Azure\Templates\EngineeringSite.json' -TemplateParameterObject <Hashtable>
```

### <span data-ttu-id="a8c6f-149">Beispiel 4: Bereitstellen einer In einem nicht öffentlichen Speicherkonto gespeicherten Vorlage mithilfe eines URI- und SAS-Tokens</span><span class="sxs-lookup"><span data-stu-id="a8c6f-149">Example 4: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "RGName" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```

<span data-ttu-id="a8c6f-150">Mit diesem Befehl wird mithilfe der Vorlage in TemplateUri eine neue Bereitstellung erstellt, die nicht öffentlich ist und für den Zugriff ein Tokenparameter erforderlich ist, der mit dem Parameter QueryString bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-150">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="a8c6f-151">Durch Ausführen dieses Befehls wird effektiv über die URL auf die Vorlage https://example.com/example.json?foo zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-151">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="a8c6f-152">Dies kann verwendet werden, wenn Sie eine Vorlage in einem Speicherkonto verwenden möchten, indem Sie das SAS-Token als QueryString bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-152">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>

## <span data-ttu-id="a8c6f-153">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a8c6f-153">PARAMETERS</span></span>

### <span data-ttu-id="a8c6f-154">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8c6f-154">-AsJob</span></span>
<span data-ttu-id="a8c6f-155">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a8c6f-155">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8c6f-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8c6f-156">-DefaultProfile</span></span>
<span data-ttu-id="a8c6f-157">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a8c6f-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8c6f-158">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="a8c6f-158">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="a8c6f-159">Gibt eine Debugprotokollebene an.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-159">Specifies a debug log level.</span></span>
<span data-ttu-id="a8c6f-160">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="a8c6f-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a8c6f-161">RequestContent</span><span class="sxs-lookup"><span data-stu-id="a8c6f-161">RequestContent</span></span>
- <span data-ttu-id="a8c6f-162">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="a8c6f-162">ResponseContent</span></span>
- <span data-ttu-id="a8c6f-163">Alle</span><span class="sxs-lookup"><span data-stu-id="a8c6f-163">All</span></span>
- <span data-ttu-id="a8c6f-164">Keine</span><span class="sxs-lookup"><span data-stu-id="a8c6f-164">None</span></span>

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

### <span data-ttu-id="a8c6f-165">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="a8c6f-165">-Force</span></span>
<span data-ttu-id="a8c6f-166">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-166">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a8c6f-167">-Modus</span><span class="sxs-lookup"><span data-stu-id="a8c6f-167">-Mode</span></span>
<span data-ttu-id="a8c6f-168">Gibt den Bereitstellungsmodus an.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-168">Specifies the deployment mode.</span></span> <span data-ttu-id="a8c6f-169">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="a8c6f-169">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a8c6f-170">Abgeschlossen: Im vollständigen Modus löscht Ressourcenmanager Ressourcen, die in der Ressourcengruppe vorhanden, aber nicht in der Vorlage angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-170">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="a8c6f-171">Inkrementell: Im inkrementellen Modus belässt Ressourcen-Manager unveränderte Ressourcen, die in der Ressourcengruppe vorhanden, aber nicht in der Vorlage angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-171">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

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

### <span data-ttu-id="a8c6f-172">-Name</span><span class="sxs-lookup"><span data-stu-id="a8c6f-172">-Name</span></span>
<span data-ttu-id="a8c6f-173">Der Name der Bereitstellung, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-173">The name of the deployment it's going to create.</span></span> <span data-ttu-id="a8c6f-174">Wenn nicht angegeben, wird standardmäßig der Vorlagendateiname verwendet, wenn eine Vorlagendatei bereitgestellt wird. ist standardmäßig auf die aktuelle Uhrzeit festgelegt, zu der ein Vorlagenobjekt bereitgestellt wird, z. B. "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="a8c6f-174">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="a8c6f-175">-Pre</span><span class="sxs-lookup"><span data-stu-id="a8c6f-175">-Pre</span></span>
<span data-ttu-id="a8c6f-176">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-176">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a8c6f-177">-QueryString</span><span class="sxs-lookup"><span data-stu-id="a8c6f-177">-QueryString</span></span>
<span data-ttu-id="a8c6f-178">Die Abfragezeichenfolge (z. B. ein SAS-Token), die mit dem Parameter TemplateUri verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-178">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="a8c6f-179">Würde bei verknüpften Vorlagen verwendet</span><span class="sxs-lookup"><span data-stu-id="a8c6f-179">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="a8c6f-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8c6f-180">-ResourceGroupName</span></span>
<span data-ttu-id="a8c6f-181">Gibt den Namen der Ressourcengruppe an, die bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-181">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="a8c6f-182">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="a8c6f-182">-RollBackDeploymentName</span></span>
<span data-ttu-id="a8c6f-183">Ein Rollback auf die erfolgreiche Bereitstellung mit dem angegebenen Namen in der Ressourcengruppe sollte nicht verwendet werden, wenn -RollbackToLastDeployment verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-183">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="a8c6f-184">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="a8c6f-184">-RollbackToLastDeployment</span></span>
<span data-ttu-id="a8c6f-185">Ein Rollback zur letzten erfolgreichen Bereitstellung in der Ressourcengruppe sollte nicht vorhanden sein, wenn -RollBackDeploymentName verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-185">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="a8c6f-186">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="a8c6f-186">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="a8c6f-187">Überspringt die PowerShell-Dynamische Parameterverarbeitung, die überprüft, ob der bereitgestellte Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-187">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="a8c6f-188">Bei dieser Überprüfung wird der Benutzer aufgefordert, einen Wert für die fehlenden Parameter zur Verfügung zu stellen. Wenn jedoch -SkipTemplateParameterPrompt angegeben wird, werden diese Eingabeaufforderung und der Fehler sofort ignoriert, wenn festgestellt wurde, dass ein Parameter nicht in der Vorlage gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-188">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="a8c6f-189">Für nicht interaktive Skripts kann -SkipTemplateParameterPrompt bereitgestellt werden, um eine bessere Fehlermeldung für den Fall zu liefern, dass nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-189">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="a8c6f-190">-Tag</span><span class="sxs-lookup"><span data-stu-id="a8c6f-190">-Tag</span></span>
<span data-ttu-id="a8c6f-191">Die Tags, die für die Bereitstellung zu setzen sind.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-191">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="a8c6f-192">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="a8c6f-192">-TemplateFile</span></span>
<span data-ttu-id="a8c6f-193">Gibt den vollständigen Pfad einer Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-193">Specifies the full path of a template file.</span></span> <span data-ttu-id="a8c6f-194">Unterstützter Vorlagendateityp: json und bicep.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-194">Supported template file type: json and bicep.</span></span>
<span data-ttu-id="a8c6f-195">Dies kann eine benutzerdefinierte Vorlage oder eine Katalogvorlage sein, die als JSON-Datei gespeichert wird, z. B. eine, die mit dem **Cmdlet Save-AzResourceGroupGalleryTemplate** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-195">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="a8c6f-196">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="a8c6f-196">-TemplateObject</span></span>
<span data-ttu-id="a8c6f-197">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-197">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="a8c6f-198">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="a8c6f-198">-TemplateParameterFile</span></span>
<span data-ttu-id="a8c6f-199">Gibt den vollständigen Pfad einer JSON-Datei an, der die Namen und Werte der Vorlagenparameter enthält.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-199">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="a8c6f-200">Wenn eine Vorlage Parameter enthält, müssen Sie die Parameterwerte mit dem *Parameter TemplateParameterFile* oder dem *Parameter TemplateParameterObject* angeben.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-200">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="a8c6f-201">Vorlagenparameter werden dem Befehl dynamisch hinzugefügt, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-201">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="a8c6f-202">Wenn Sie die dynamischen Parameter verwenden möchten, geben Sie ein Minuszeichen (-) ein, um einen Parameternamen anzugeben, und verwenden Sie dann die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-202">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="a8c6f-203">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="a8c6f-203">-TemplateParameterObject</span></span>
<span data-ttu-id="a8c6f-204">Gibt eine Hashtabelle mit Vorlagenparameternamen und -werten an.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-204">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="a8c6f-205">Wenn Sie Hilfe zu #A0 in Windows PowerShell, geben Sie `Get-Help about_Hash_Tables` ein.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-205">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="a8c6f-206">Wenn eine Vorlage Parameter enthält, müssen Sie Parameterwerte angeben.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-206">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="a8c6f-207">Vorlagenparameter werden dem Befehl dynamisch hinzugefügt, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-207">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="a8c6f-208">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="a8c6f-208">-TemplateParameterUri</span></span>
<span data-ttu-id="a8c6f-209">Gibt den URI einer Vorlagenparameterdatei an.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-209">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="a8c6f-210">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="a8c6f-210">-TemplateSpecId</span></span>
<span data-ttu-id="a8c6f-211">Ressourcen-ID der zu bereitstellende TemplateSpec.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-211">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="a8c6f-212">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="a8c6f-212">-TemplateUri</span></span>
<span data-ttu-id="a8c6f-213">Gibt den URI einer Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-213">Specifies the URI of a template file.</span></span>
<span data-ttu-id="a8c6f-214">Diese Datei kann eine benutzerdefinierte Vorlage oder eine Katalogvorlage sein, die als JSON-Datei gespeichert wird, z. B. mithilfe von **Save-AzResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-214">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="a8c6f-215">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="a8c6f-215">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="a8c6f-216">Durch Kommas getrennte Ressourcenänderungstypen, die aus den Ergebnissen What-If werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-216">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="a8c6f-217">Gilt, wenn der Schalter -WhatIf oder -Confirm festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-217">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="a8c6f-218">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="a8c6f-218">-WhatIfResultFormat</span></span>
<span data-ttu-id="a8c6f-219">Das What-If Ergebnisformat.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-219">The What-If result format.</span></span>

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

### <span data-ttu-id="a8c6f-220">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a8c6f-220">-Confirm</span></span>
<span data-ttu-id="a8c6f-221">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-221">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8c6f-222">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8c6f-222">-WhatIf</span></span>
<span data-ttu-id="a8c6f-223">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-223">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8c6f-224">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-224">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8c6f-225">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8c6f-225">CommonParameters</span></span>
<span data-ttu-id="a8c6f-226">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8c6f-226">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8c6f-227">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8c6f-227">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8c6f-228">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a8c6f-228">INPUTS</span></span>

### <span data-ttu-id="a8c6f-229">System.String</span><span class="sxs-lookup"><span data-stu-id="a8c6f-229">System.String</span></span>

### <span data-ttu-id="a8c6f-230">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="a8c6f-230">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="a8c6f-231">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a8c6f-231">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a8c6f-232">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a8c6f-232">OUTPUTS</span></span>

### <span data-ttu-id="a8c6f-233">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a8c6f-233">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="a8c6f-234">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a8c6f-234">NOTES</span></span>

## <span data-ttu-id="a8c6f-235">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a8c6f-235">RELATED LINKS</span></span>

[<span data-ttu-id="a8c6f-236">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a8c6f-236">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="a8c6f-237">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="a8c6f-237">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="a8c6f-238">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a8c6f-238">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="a8c6f-239">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a8c6f-239">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="a8c6f-240">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a8c6f-240">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="a8c6f-241">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a8c6f-241">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)