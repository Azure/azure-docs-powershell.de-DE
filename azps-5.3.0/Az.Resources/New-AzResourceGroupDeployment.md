---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 916e2fea0e88a1409bc2586ab8b2e80b11ec1a70
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459295"
---
# <span data-ttu-id="d9ec1-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d9ec1-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="d9ec1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9ec1-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ec1-103">Fügt einer Ressourcengruppe eine Azure-Bereitstellung hinzu.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="d9ec1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9ec1-104">SYNTAX</span></span>

### <span data-ttu-id="d9ec1-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="d9ec1-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ec1-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d9ec1-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ec1-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d9ec1-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ec1-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d9ec1-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ec1-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d9ec1-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ec1-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d9ec1-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ec1-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d9ec1-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ec1-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d9ec1-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ec1-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d9ec1-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ec1-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d9ec1-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ec1-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="d9ec1-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ec1-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="d9ec1-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9ec1-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9ec1-117">DESCRIPTION</span></span>
<span data-ttu-id="d9ec1-118">Das **Cmdlet "New-AzResourceGroupDeployment"** fügt einer vorhandenen Ressourcengruppe eine Bereitstellung hinzu.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-118">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="d9ec1-119">Dazu gehören auch die Ressourcen, die für die Bereitstellung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-119">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="d9ec1-120">Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität, z. B. ein Datenbankserver, eine Datenbank, eine Website, ein virtueller Computer oder ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-120">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="d9ec1-121">Eine Azure-Ressourcengruppe ist eine Sammlung von Azure-Ressourcen, die als Einheit bereitgestellt werden, z. B. die Website, der Datenbankserver und Datenbanken, die für eine Finanzwebsite erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-121">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="d9ec1-122">Eine Ressourcengruppenbereitstellung verwendet eine Vorlage zum Hinzufügen von Ressourcen zu einer Ressourcengruppe und veröffentlicht diese so, dass sie in Azure verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-122">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="d9ec1-123">Wenn Sie einer Ressourcengruppe Ressourcen hinzufügen möchten, ohne eine Vorlage zu verwenden, verwenden Sie New-AzResource-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-123">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="d9ec1-124">Um eine Ressourcengruppenbereitstellung hinzuzufügen, geben Sie den Namen einer vorhandenen Ressourcengruppe und eine Ressourcengruppenvorlage an.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-124">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="d9ec1-125">Eine Ressourcengruppenvorlage ist eine JSON-Zeichenfolge, die eine Ressourcengruppe für einen komplexen cloudbasierten Dienst darstellt, z. B. ein Webportal.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-125">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="d9ec1-126">Die Vorlage enthält Parameterplatzhalter für erforderliche Ressourcen und konfigurierbare Eigenschaftswerte, z. B. Namen und Größen.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="d9ec1-127">Sie finden viele Vorlagen im Azure-Vorlagenkatalog, oder Sie können eigene Vorlagen erstellen.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-127">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="d9ec1-128">Wenn Sie eine benutzerdefinierte Vorlage zum Erstellen einer Ressourcengruppe verwenden möchten, geben Sie den *Parameter "TemplateFile"* oder *"TemplateUri"* an.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-128">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="d9ec1-129">Jede Vorlage enthält Parameter für konfigurierbare Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-129">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="d9ec1-130">Um Werte für die Vorlagenparameter anzugeben, geben Sie den *Parameter "TemplateParameterFile"* oder den Parameter *"TemplateParameterObject"* an.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-130">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="d9ec1-131">Alternativ können Sie die Vorlagenparameter verwenden, die dem Befehl dynamisch hinzugefügt werden, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-131">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="d9ec1-132">Wenn Sie dynamische Parameter verwenden möchten, geben Sie diese an der Eingabeaufforderung ein, oder geben Sie ein Minuszeichen (-) ein, um einen Parameter anzugeben, und verwenden Sie die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-132">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="d9ec1-133">Werte von Vorlagenparametern, die Sie an der Eingabeaufforderung eingeben, haben Vorrang vor Werten in einem Vorlagenparameterobjekt oder in einer Vorlagenparameterdatei.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-133">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="d9ec1-134">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d9ec1-134">EXAMPLES</span></span>

### <span data-ttu-id="d9ec1-135">Beispiel 1: Verwenden einer benutzerdefinierten Vorlage und Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="d9ec1-135">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="d9ec1-136">Dieser Befehl erstellt eine neue Bereitstellung mithilfe einer benutzerdefinierten Vorlage und einer Vorlagendatei auf dem Datenträger mit definierten Tagsparametern.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-136">This command creates a new deployment by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="d9ec1-137">Der Befehl verwendet den *Parameter "TemplateFile",* um die Vorlage anzugeben, und den *Parameter "TemplateParameterFile",* um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-137">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="d9ec1-138">Beispiel 2: Verwenden eines benutzerdefinierten Vorlagenobjekts und einer Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="d9ec1-138">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="d9ec1-139">Mit diesem Befehl wird eine neue Bereitstellung mithilfe einer benutzerdefinierten Datei und einer Vorlagendatei auf dem Datenträger erstellt, die in eine Speicherhashtable konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-139">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="d9ec1-140">Die ersten beiden Befehle lesen den Text für die Vorlagendatei auf dem Datenträger und konvertieren sie in eine Speicherhashtable.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-140">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="d9ec1-141">Der letzte Befehl verwendet den *Parameter "TemplateObject",* um die Hashtabelle und den *Parameter "TemplateParameterFile"* anzugeben, um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-141">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="d9ec1-142">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d9ec1-142">Example 3</span></span>

<span data-ttu-id="d9ec1-143">Fügt einer Ressourcengruppe eine Azure-Bereitstellung hinzu.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-143">Adds an Azure deployment to a resource group.</span></span> <span data-ttu-id="d9ec1-144">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="d9ec1-144">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzResourceGroupDeployment -DeploymentDebugLogLevel RequestContent -Name mynewstorageaccount -ResourceGroupName 'ContosoEngineering' -TemplateFile 'D:\Azure\Templates\EngineeringSite.json' -TemplateParameterObject <Hashtable>
```

## <span data-ttu-id="d9ec1-145">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9ec1-145">PARAMETERS</span></span>

### <span data-ttu-id="d9ec1-146">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9ec1-146">-AsJob</span></span>
<span data-ttu-id="d9ec1-147">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d9ec1-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9ec1-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ec1-148">-DefaultProfile</span></span>
<span data-ttu-id="d9ec1-149">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d9ec1-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9ec1-150">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="d9ec1-150">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="d9ec1-151">Gibt eine Debugprotokollebene an.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-151">Specifies a debug log level.</span></span>
<span data-ttu-id="d9ec1-152">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="d9ec1-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d9ec1-153">RequestContent</span><span class="sxs-lookup"><span data-stu-id="d9ec1-153">RequestContent</span></span>
- <span data-ttu-id="d9ec1-154">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="d9ec1-154">ResponseContent</span></span>
- <span data-ttu-id="d9ec1-155">Alle</span><span class="sxs-lookup"><span data-stu-id="d9ec1-155">All</span></span>
- <span data-ttu-id="d9ec1-156">Keine</span><span class="sxs-lookup"><span data-stu-id="d9ec1-156">None</span></span>

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

### <span data-ttu-id="d9ec1-157">-Force</span><span class="sxs-lookup"><span data-stu-id="d9ec1-157">-Force</span></span>
<span data-ttu-id="d9ec1-158">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-158">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d9ec1-159">-Mode</span><span class="sxs-lookup"><span data-stu-id="d9ec1-159">-Mode</span></span>
<span data-ttu-id="d9ec1-160">Gibt den Bereitstellungsmodus an.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-160">Specifies the deployment mode.</span></span> <span data-ttu-id="d9ec1-161">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="d9ec1-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d9ec1-162">Abgeschlossen: Im vollständigen Modus löscht der Ressourcen-Manager Ressourcen, die in der Ressourcengruppe vorhanden, aber nicht in der Vorlage angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-162">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="d9ec1-163">Inkrementell: Im inkrementellen Modus belässt der Ressourcen-Manager unveränderte Ressourcen, die in der Ressourcengruppe vorhanden, aber nicht in der Vorlage angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-163">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

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

### <span data-ttu-id="d9ec1-164">-Name</span><span class="sxs-lookup"><span data-stu-id="d9ec1-164">-Name</span></span>
<span data-ttu-id="d9ec1-165">Der Name der Bereitstellung, die erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-165">The name of the deployment it's going to create.</span></span> <span data-ttu-id="d9ec1-166">Wenn keine Angabe erfolgt, wird standardmäßig der Vorlagendateiname verwendet, wenn eine Vorlagendatei bereitgestellt wird. wird standardmäßig die aktuelle Uhrzeit verwendet, zu der ein Vorlagenobjekt bereitgestellt wird, z. B. "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="d9ec1-166">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="d9ec1-167">-Pre</span><span class="sxs-lookup"><span data-stu-id="d9ec1-167">-Pre</span></span>
<span data-ttu-id="d9ec1-168">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-168">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d9ec1-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9ec1-169">-ResourceGroupName</span></span>
<span data-ttu-id="d9ec1-170">Gibt den Namen der Ressourcengruppe an, die bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-170">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="d9ec1-171">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="d9ec1-171">-RollBackDeploymentName</span></span>
<span data-ttu-id="d9ec1-172">Ein Rollback zur erfolgreichen Bereitstellung unter dem angegebenen Namen in der Ressourcengruppe sollte nicht verwendet werden, wenn "-RollbackToLastDeployment" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-172">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="d9ec1-173">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="d9ec1-173">-RollbackToLastDeployment</span></span>
<span data-ttu-id="d9ec1-174">Ein Rollback zur letzten erfolgreichen Bereitstellung in der Ressourcengruppe sollte nicht vorhanden sein, wenn "-RollBackDeploymentName" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-174">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="d9ec1-175">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="d9ec1-175">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="d9ec1-176">Überspringt die Verarbeitung dynamischer PowerShell-Parameter, die überprüft, ob der bereitgestellte Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-176">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="d9ec1-177">Bei dieser Überprüfung müsste der Benutzer einen Wert für die fehlenden Parameter angeben. Wenn jedoch "-SkipTemplateParameterPrompt" angegeben wird, wird diese Eingabeaufforderung und der Fehler sofort ignoriert, wenn ein Parameter nicht in der Vorlage gebunden wurde.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-177">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="d9ec1-178">Bei nicht interaktiven Skripts kann "-SkipTemplateParameterPrompt" bereitgestellt werden, um eine bessere Fehlermeldung für den Fall zu liefern, dass nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-178">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="d9ec1-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="d9ec1-179">-Tag</span></span>
<span data-ttu-id="d9ec1-180">Die Tags, die für die Bereitstellung verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-180">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="d9ec1-181">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="d9ec1-181">-TemplateFile</span></span>
<span data-ttu-id="d9ec1-182">Gibt den vollständigen Pfad einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-182">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="d9ec1-183">Dabei kann es sich um eine benutzerdefinierte Vorlage oder eine Katalogvorlage handelt, die als JSON-Datei gespeichert wird, z. B. eine, die mit dem **Cmdlet Save-AzResourceGroupGalleryTemplate** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-183">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="d9ec1-184">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="d9ec1-184">-TemplateObject</span></span>
<span data-ttu-id="d9ec1-185">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-185">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="d9ec1-186">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="d9ec1-186">-TemplateParameterFile</span></span>
<span data-ttu-id="d9ec1-187">Gibt den vollständigen Pfad einer JSON-Datei an, die die Namen und Werte der Vorlagenparameter enthält.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-187">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="d9ec1-188">Wenn eine Vorlage Parameter enthält, müssen Sie die Parameterwerte mit dem Parameter *"TemplateParameterFile"* oder dem Parameter *"TemplateParameterObject"* angeben.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-188">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="d9ec1-189">Vorlagenparameter werden dynamisch zum Befehl hinzugefügt, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-189">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="d9ec1-190">Um die dynamischen Parameter zu verwenden, geben Sie ein Minuszeichen (-) ein, um einen Parameternamen anzugeben, und verwenden Sie dann die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-190">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="d9ec1-191">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="d9ec1-191">-TemplateParameterObject</span></span>
<span data-ttu-id="d9ec1-192">Gibt eine Hashtabelle mit Vorlagenparameternamen und -werten an.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-192">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="d9ec1-193">Wenn Sie Hilfe zu Hashtabellen in Windows PowerShell, geben Sie `Get-Help about_Hash_Tables` " ein.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-193">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="d9ec1-194">Wenn eine Vorlage Parameter enthält, müssen Sie Parameterwerte angeben.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-194">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="d9ec1-195">Vorlagenparameter werden dynamisch zum Befehl hinzugefügt, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-195">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="d9ec1-196">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="d9ec1-196">-TemplateParameterUri</span></span>
<span data-ttu-id="d9ec1-197">Gibt den URI einer Vorlagenparameterdatei an.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-197">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="d9ec1-198">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="d9ec1-198">-TemplateUri</span></span>
<span data-ttu-id="d9ec1-199">Gibt den URI einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-199">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="d9ec1-200">Bei dieser Datei kann es sich um eine benutzerdefinierte Vorlage oder eine Katalogvorlage handelt, die als JSON-Datei gespeichert wird, z. B. mithilfe von **Save-AzResourceGroupGalleryTemplate.**</span><span class="sxs-lookup"><span data-stu-id="d9ec1-200">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="d9ec1-201">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="d9ec1-201">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="d9ec1-202">Durch Kommas getrennte Ressourcenänderungstypen, die aus den What-If werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-202">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="d9ec1-203">Anwendbar, wenn der Schalter "-WhatIf" oder "-Confirm" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-203">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="d9ec1-204">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="d9ec1-204">-WhatIfResultFormat</span></span>
<span data-ttu-id="d9ec1-205">Das What-If Ergebnisformat.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-205">The What-If result format.</span></span>

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

### <span data-ttu-id="d9ec1-206">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9ec1-206">-Confirm</span></span>
<span data-ttu-id="d9ec1-207">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-207">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9ec1-208">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d9ec1-208">-WhatIf</span></span>
<span data-ttu-id="d9ec1-209">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-209">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9ec1-210">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-210">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9ec1-211">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ec1-211">CommonParameters</span></span>
<span data-ttu-id="d9ec1-212">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9ec1-212">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ec1-213">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9ec1-213">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ec1-214">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d9ec1-214">INPUTS</span></span>

### <span data-ttu-id="d9ec1-215">System.String</span><span class="sxs-lookup"><span data-stu-id="d9ec1-215">System.String</span></span>

### <span data-ttu-id="d9ec1-216">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="d9ec1-216">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="d9ec1-217">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d9ec1-217">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d9ec1-218">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d9ec1-218">OUTPUTS</span></span>

### <span data-ttu-id="d9ec1-219">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d9ec1-219">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="d9ec1-220">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d9ec1-220">NOTES</span></span>

## <span data-ttu-id="d9ec1-221">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d9ec1-221">RELATED LINKS</span></span>

[<span data-ttu-id="d9ec1-222">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d9ec1-222">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="d9ec1-223">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="d9ec1-223">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="d9ec1-224">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d9ec1-224">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="d9ec1-225">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d9ec1-225">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="d9ec1-226">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d9ec1-226">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="d9ec1-227">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d9ec1-227">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)