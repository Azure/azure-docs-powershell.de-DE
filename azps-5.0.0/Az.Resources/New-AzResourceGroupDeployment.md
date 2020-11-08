---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 916e2fea0e88a1409bc2586ab8b2e80b11ec1a70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177246"
---
# <span data-ttu-id="5b8f4-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5b8f4-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="5b8f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b8f4-102">SYNOPSIS</span></span>
<span data-ttu-id="5b8f4-103">Fügt eine Azure-Bereitstellung zu einer Ressourcengruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="5b8f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b8f4-104">SYNTAX</span></span>

### <span data-ttu-id="5b8f4-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="5b8f4-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b8f4-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="5b8f4-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b8f4-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="5b8f4-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b8f4-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="5b8f4-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b8f4-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="5b8f4-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b8f4-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="5b8f4-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b8f4-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="5b8f4-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b8f4-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="5b8f4-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b8f4-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="5b8f4-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b8f4-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="5b8f4-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b8f4-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="5b8f4-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b8f4-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="5b8f4-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b8f4-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b8f4-117">DESCRIPTION</span></span>
<span data-ttu-id="5b8f4-118">Mit dem Cmdlet **New-AzResourceGroupDeployment** wird eine Bereitstellung zu einer vorhandenen Ressourcengruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-118">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="5b8f4-119">Dazu gehören die Ressourcen, die für die Bereitstellung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-119">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="5b8f4-120">Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität, beispielsweise ein Datenbankserver, eine Datenbank, eine Website, einen virtuellen Computer oder ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-120">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="5b8f4-121">Eine Azure-Ressourcengruppe ist eine Sammlung von Azure-Ressourcen, die als Einheit bereitgestellt werden, beispielsweise die Website, den Datenbankserver und Datenbanken, die für eine Finanzwebsite erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-121">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="5b8f4-122">Eine Ressourcengruppen Bereitstellung verwendet eine Vorlage zum Hinzufügen von Ressourcen zu einer Ressourcengruppe und veröffentlicht diese, damit Sie in Azure verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-122">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="5b8f4-123">Verwenden Sie das New-AzResource-Cmdlet, um einer Ressourcengruppe Ressourcen hinzuzufügen, ohne eine Vorlage zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-123">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="5b8f4-124">Wenn Sie eine Ressourcengruppen Bereitstellung hinzufügen möchten, geben Sie den Namen einer vorhandenen Ressourcengruppe und einer Ressourcengruppen Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-124">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="5b8f4-125">Eine Ressourcengruppen Vorlage ist eine JSON-Zeichenfolge, die eine Ressourcengruppe für einen komplexen cloudbasierten Dienst, beispielsweise ein Webportal, darstellt.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-125">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="5b8f4-126">Die Vorlage enthält Parameterplatzhalter für erforderliche Ressourcen und konfigurierbare Eigenschaftswerte wie Namen und Größen.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="5b8f4-127">Sie können viele Vorlagen im Azure-Vorlagenkatalog finden, oder Sie können eigene Vorlagen erstellen.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-127">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="5b8f4-128">Wenn Sie eine benutzerdefinierte Vorlage zum Erstellen einer Ressourcengruppe verwenden möchten, geben Sie den Parameter " *Templatedatei* " oder " *TemplateUri* " an.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-128">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="5b8f4-129">Jede Vorlage verfügt über Parameter für konfigurierbare Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-129">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="5b8f4-130">Wenn Sie Werte für die Vorlagenparameter angeben möchten, geben Sie den *TemplateParameterFile* -Parameter oder den *TemplateParameterObject* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-130">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="5b8f4-131">Alternativ können Sie die Vorlagenparameter verwenden, die dem Befehl dynamisch hinzugefügt werden, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-131">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="5b8f4-132">Wenn Sie dynamische Parameter verwenden möchten, geben Sie Sie an der Eingabeaufforderung ein, oder geben Sie ein Minuszeichen (-) ein, um einen Parameter anzugeben, und verwenden Sie die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-132">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="5b8f4-133">Vorlagenparameter Werte, die Sie an der Eingabeaufforderung eingeben, haben Vorrang vor Werten in einem Vorlagenparameter Objekt oder einer Datei.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-133">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="5b8f4-134">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b8f4-134">EXAMPLES</span></span>

### <span data-ttu-id="5b8f4-135">Beispiel 1: Verwenden einer benutzerdefinierten Vorlage und einer Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="5b8f4-135">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="5b8f4-136">Dieser Befehl erstellt eine neue Bereitstellung mithilfe einer benutzerdefinierten Vorlage und einer Vorlagendatei auf dem Datenträger mit dem Parameter für definierte Tags.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-136">This command creates a new deployment by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="5b8f4-137">Der Befehl verwendet den *Templatedatei* -Parameter, um die Vorlage und den *TemplateParameterFile* -Parameter anzugeben, um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-137">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="5b8f4-138">Beispiel 2: Verwenden eines benutzerdefinierten Vorlagenobjekts und einer Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="5b8f4-138">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="5b8f4-139">Dieser Befehl erstellt eine neue Bereitstellung unter Verwendung einer benutzerdefinierten und einer Vorlagendatei auf einem Datenträger, die in eine Arbeitsspeicher-Hashtable konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-139">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="5b8f4-140">Mit den ersten beiden Befehlen wird der Text für die Vorlagendatei auf dem Datenträger gelesen und in eine Arbeitsspeicher-Hashtable konvertiert.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-140">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="5b8f4-141">Der letzte Befehl verwendet den *templateobject* -Parameter zum Angeben der Hashtable und des *TemplateParameterFile* -Parameters, um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-141">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="5b8f4-142">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5b8f4-142">Example 3</span></span>

<span data-ttu-id="5b8f4-143">Fügt eine Azure-Bereitstellung zu einer Ressourcengruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-143">Adds an Azure deployment to a resource group.</span></span> <span data-ttu-id="5b8f4-144">automatisch</span><span class="sxs-lookup"><span data-stu-id="5b8f4-144">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzResourceGroupDeployment -DeploymentDebugLogLevel RequestContent -Name mynewstorageaccount -ResourceGroupName 'ContosoEngineering' -TemplateFile 'D:\Azure\Templates\EngineeringSite.json' -TemplateParameterObject <Hashtable>
```

## <span data-ttu-id="5b8f4-145">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b8f4-145">PARAMETERS</span></span>

### <span data-ttu-id="5b8f4-146">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b8f4-146">-AsJob</span></span>
<span data-ttu-id="5b8f4-147">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5b8f4-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b8f4-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b8f4-148">-DefaultProfile</span></span>
<span data-ttu-id="5b8f4-149">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5b8f4-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b8f4-150">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="5b8f4-150">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="5b8f4-151">Gibt eine Debug-Protokollebene an.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-151">Specifies a debug log level.</span></span>
<span data-ttu-id="5b8f4-152">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5b8f4-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5b8f4-153">RequestContent</span><span class="sxs-lookup"><span data-stu-id="5b8f4-153">RequestContent</span></span>
- <span data-ttu-id="5b8f4-154">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="5b8f4-154">ResponseContent</span></span>
- <span data-ttu-id="5b8f4-155">Alle</span><span class="sxs-lookup"><span data-stu-id="5b8f4-155">All</span></span>
- <span data-ttu-id="5b8f4-156">Keine</span><span class="sxs-lookup"><span data-stu-id="5b8f4-156">None</span></span>

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

### <span data-ttu-id="5b8f4-157">-Force</span><span class="sxs-lookup"><span data-stu-id="5b8f4-157">-Force</span></span>
<span data-ttu-id="5b8f4-158">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-158">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5b8f4-159">-Modus</span><span class="sxs-lookup"><span data-stu-id="5b8f4-159">-Mode</span></span>
<span data-ttu-id="5b8f4-160">Gibt den Bereitstellungsmodus an.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-160">Specifies the deployment mode.</span></span> <span data-ttu-id="5b8f4-161">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5b8f4-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5b8f4-162">Abgeschlossen: im vollständigen Modus löscht der Ressourcen-Manager Ressourcen, die in der Ressourcengruppe vorhanden sind, aber nicht in der Vorlage angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-162">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="5b8f4-163">Inkrementell: im inkrementellen Modus hinterlässt der Ressourcen-Manager unveränderte Ressourcen, die in der Ressourcengruppe vorhanden sind, aber nicht in der Vorlage angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-163">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

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

### <span data-ttu-id="5b8f4-164">-Name</span><span class="sxs-lookup"><span data-stu-id="5b8f4-164">-Name</span></span>
<span data-ttu-id="5b8f4-165">Der Name der Bereitstellung, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-165">The name of the deployment it's going to create.</span></span> <span data-ttu-id="5b8f4-166">Wenn nicht angegeben, wird standardmäßig der Name der Vorlagendatei verwendet, wenn eine Vorlagendatei bereitgestellt wird. Standardmäßig wird die aktuelle Uhrzeit verwendet, zu der ein Vorlagenobjekt bereitgestellt wird, beispielsweise "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="5b8f4-166">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="5b8f4-167">-Pre</span><span class="sxs-lookup"><span data-stu-id="5b8f4-167">-Pre</span></span>
<span data-ttu-id="5b8f4-168">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-168">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5b8f4-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b8f4-169">-ResourceGroupName</span></span>
<span data-ttu-id="5b8f4-170">Gibt den Namen der Ressourcengruppe an, die bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-170">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="5b8f4-171">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="5b8f4-171">-RollBackDeploymentName</span></span>
<span data-ttu-id="5b8f4-172">Rollback zur erfolgreichen Bereitstellung mit dem angegebenen Namen in der Ressourcengruppe sollte nicht verwendet werden, wenn-RollbackToLastDeployment verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-172">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="5b8f4-173">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="5b8f4-173">-RollbackToLastDeployment</span></span>
<span data-ttu-id="5b8f4-174">Rollback zur letzten erfolgreichen Bereitstellung in der Ressourcengruppe sollte nicht vorhanden sein, wenn-RollBackDeploymentName verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-174">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="5b8f4-175">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="5b8f4-175">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="5b8f4-176">Überspringt die dynamische PowerShell-Parameterverarbeitung, die überprüft, ob der angegebene Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-176">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="5b8f4-177">Mit dieser Prüfung wird der Benutzer aufgefordert, einen Wert für die fehlenden Parameter bereitzustellen, doch die Bereitstellung von-SkipTemplateParameterPrompt ignoriert diese Eingabeaufforderung und ist sofort fehlerhaft, wenn ein Parameter gefunden wurde, der in der Vorlage nicht gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-177">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="5b8f4-178">Für nicht interaktive Skripts kann-SkipTemplateParameterPrompt bereitgestellt werden, um eine bessere Fehlermeldung bereitzustellen, falls nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-178">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="5b8f4-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="5b8f4-179">-Tag</span></span>
<span data-ttu-id="5b8f4-180">Die Tags, die für die Bereitstellung bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-180">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="5b8f4-181">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="5b8f4-181">-TemplateFile</span></span>
<span data-ttu-id="5b8f4-182">Gibt den vollständigen Pfad einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-182">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="5b8f4-183">Hierbei kann es sich um eine benutzerdefinierte Vorlage oder eine Katalogvorlage handeln, die als JSON-Datei gespeichert wird, beispielsweise eine mit dem Cmdlet **Save-AzResourceGroupGalleryTemplate** erstellte.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-183">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="5b8f4-184">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="5b8f4-184">-TemplateObject</span></span>
<span data-ttu-id="5b8f4-185">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-185">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="5b8f4-186">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="5b8f4-186">-TemplateParameterFile</span></span>
<span data-ttu-id="5b8f4-187">Gibt den vollständigen Pfad einer JSON-Datei an, die die Namen und Werte der Vorlagenparameter enthält.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-187">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="5b8f4-188">Wenn eine Vorlage über Parameter verfügt, müssen Sie die Parameterwerte mit dem *TemplateParameterFile* -Parameter oder dem *TemplateParameterObject* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-188">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="5b8f4-189">Vorlagenparameter werden dem Befehl dynamisch hinzugefügt, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-189">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="5b8f4-190">Wenn Sie die dynamischen Parameter verwenden möchten, geben Sie ein Minuszeichen (-) ein, um einen Parameternamen anzugeben, und verwenden Sie dann die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-190">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="5b8f4-191">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="5b8f4-191">-TemplateParameterObject</span></span>
<span data-ttu-id="5b8f4-192">Gibt eine Hashtabelle mit Vorlagenparameter Namen und-Werten an.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-192">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="5b8f4-193">Wenn Sie Hilfe zu Hashtabellen in Windows PowerShell benötigen, geben Sie `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="5b8f4-193">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="5b8f4-194">Wenn eine Vorlage über Parameter verfügt, müssen Sie Parameterwerte angeben.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-194">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="5b8f4-195">Vorlagenparameter werden dem Befehl dynamisch hinzugefügt, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-195">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="5b8f4-196">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="5b8f4-196">-TemplateParameterUri</span></span>
<span data-ttu-id="5b8f4-197">Gibt den URI einer Vorlagenparameter Datei an.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-197">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="5b8f4-198">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="5b8f4-198">-TemplateUri</span></span>
<span data-ttu-id="5b8f4-199">Gibt den URI einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-199">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="5b8f4-200">Diese Datei kann eine benutzerdefinierte Vorlage oder eine Katalogvorlage sein, die als JSON-Datei gespeichert wird, beispielsweise mithilfe von **Save-AzResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-200">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="5b8f4-201">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="5b8f4-201">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="5b8f4-202">Durch Kommas getrennte Ressourcen Änderungstypen, die von What-If Ergebnissen ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-202">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="5b8f4-203">Anwendbar, wenn der-WhatIf-oder-Confirm-Schalter festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-203">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="5b8f4-204">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="5b8f4-204">-WhatIfResultFormat</span></span>
<span data-ttu-id="5b8f4-205">Das What-If Ergebnisformat.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-205">The What-If result format.</span></span>

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

### <span data-ttu-id="5b8f4-206">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5b8f4-206">-Confirm</span></span>
<span data-ttu-id="5b8f4-207">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-207">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b8f4-208">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b8f4-208">-WhatIf</span></span>
<span data-ttu-id="5b8f4-209">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-209">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b8f4-210">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-210">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b8f4-211">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b8f4-211">CommonParameters</span></span>
<span data-ttu-id="5b8f4-212">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b8f4-212">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b8f4-213">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b8f4-213">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b8f4-214">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b8f4-214">INPUTS</span></span>

### <span data-ttu-id="5b8f4-215">System. String</span><span class="sxs-lookup"><span data-stu-id="5b8f4-215">System.String</span></span>

### <span data-ttu-id="5b8f4-216">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="5b8f4-216">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="5b8f4-217">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5b8f4-217">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5b8f4-218">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b8f4-218">OUTPUTS</span></span>

### <span data-ttu-id="5b8f4-219">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5b8f4-219">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="5b8f4-220">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b8f4-220">NOTES</span></span>

## <span data-ttu-id="5b8f4-221">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b8f4-221">RELATED LINKS</span></span>

[<span data-ttu-id="5b8f4-222">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5b8f4-222">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="5b8f4-223">Neu – AzResource</span><span class="sxs-lookup"><span data-stu-id="5b8f4-223">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="5b8f4-224">Neu – AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5b8f4-224">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="5b8f4-225">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5b8f4-225">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="5b8f4-226">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5b8f4-226">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="5b8f4-227">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5b8f4-227">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)