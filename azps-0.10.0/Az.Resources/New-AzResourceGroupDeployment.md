---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 35741c908e57e96fd4d9709ff350ac885f41181d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843327"
---
# <span data-ttu-id="b8559-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b8559-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="b8559-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b8559-102">SYNOPSIS</span></span>
<span data-ttu-id="b8559-103">Fügt eine Azure-Bereitstellung zu einer Ressourcengruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="b8559-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="b8559-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8559-104">SYNTAX</span></span>

### <span data-ttu-id="b8559-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="b8559-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8559-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b8559-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8559-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b8559-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8559-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b8559-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8559-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b8559-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8559-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b8559-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8559-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b8559-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8559-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b8559-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8559-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b8559-113">DESCRIPTION</span></span>
<span data-ttu-id="b8559-114">Mit dem Cmdlet **New-AzResourceGroupDeployment** wird eine Bereitstellung zu einer vorhandenen Ressourcengruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b8559-114">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="b8559-115">Dazu gehören die Ressourcen, die für die Bereitstellung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b8559-115">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="b8559-116">Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität, beispielsweise ein Datenbankserver, eine Datenbank, eine Website, einen virtuellen Computer oder ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="b8559-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="b8559-117">Eine Azure-Ressourcengruppe ist eine Sammlung von Azure-Ressourcen, die als Einheit bereitgestellt werden, beispielsweise die Website, den Datenbankserver und Datenbanken, die für eine Finanzwebsite erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b8559-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="b8559-118">Eine Ressourcengruppen Bereitstellung verwendet eine Vorlage zum Hinzufügen von Ressourcen zu einer Ressourcengruppe und veröffentlicht diese, damit Sie in Azure verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b8559-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="b8559-119">Verwenden Sie das New-AzResource-Cmdlet, um einer Ressourcengruppe Ressourcen hinzuzufügen, ohne eine Vorlage zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8559-119">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="b8559-120">Wenn Sie eine Ressourcengruppen Bereitstellung hinzufügen möchten, geben Sie den Namen einer vorhandenen Ressourcengruppe und einer Ressourcengruppen Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="b8559-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="b8559-121">Eine Ressourcengruppen Vorlage ist eine JSON-Zeichenfolge, die eine Ressourcengruppe für einen komplexen cloudbasierten Dienst, beispielsweise ein Webportal, darstellt.</span><span class="sxs-lookup"><span data-stu-id="b8559-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="b8559-122">Die Vorlage enthält Parameterplatzhalter für erforderliche Ressourcen und konfigurierbare Eigenschaftswerte wie Namen und Größen.</span><span class="sxs-lookup"><span data-stu-id="b8559-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="b8559-123">Sie können viele Vorlagen im Azure-Vorlagenkatalog finden, oder Sie können eigene Vorlagen erstellen.</span><span class="sxs-lookup"><span data-stu-id="b8559-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="b8559-124">Sie können das Cmdlet **Get-AzResourceGroupGalleryTemplate** verwenden, um eine Vorlage im Katalog zu finden.</span><span class="sxs-lookup"><span data-stu-id="b8559-124">You can use the **Get-AzResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>
<span data-ttu-id="b8559-125">Wenn Sie eine benutzerdefinierte Vorlage zum Erstellen einer Ressourcengruppe verwenden möchten, geben Sie den Parameter " *Templatedatei* " oder " *TemplateUri* " an.</span><span class="sxs-lookup"><span data-stu-id="b8559-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="b8559-126">Jede Vorlage verfügt über Parameter für konfigurierbare Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b8559-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="b8559-127">Wenn Sie Werte für die Vorlagenparameter angeben möchten, geben Sie den *TemplateParameterFile* -Parameter oder den *TemplateParameterObject* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="b8559-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="b8559-128">Alternativ können Sie die Vorlagenparameter verwenden, die dem Befehl dynamisch hinzugefügt werden, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="b8559-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="b8559-129">Wenn Sie dynamische Parameter verwenden möchten, geben Sie Sie an der Eingabeaufforderung ein, oder geben Sie ein Minuszeichen (-) ein, um einen Parameter anzugeben, und verwenden Sie die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="b8559-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="b8559-130">Vorlagenparameter Werte, die Sie an der Eingabeaufforderung eingeben, haben Vorrang vor Werten in einem Vorlagenparameter Objekt oder einer Datei.</span><span class="sxs-lookup"><span data-stu-id="b8559-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="b8559-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b8559-131">EXAMPLES</span></span>

### <span data-ttu-id="b8559-132">Beispiel 1: Verwenden einer benutzerdefinierten Vorlage und einer Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="b8559-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="b8559-133">Dieser Befehl erstellt eine neue Bereitstellung mithilfe einer benutzerdefinierten Vorlage und einer Vorlagendatei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="b8559-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="b8559-134">Der Befehl verwendet den *Templatedatei* -Parameter, um die Vorlage und den *TemplateParameterFile* -Parameter anzugeben, um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="b8559-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="b8559-135">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8559-135">PARAMETERS</span></span>

### <span data-ttu-id="b8559-136">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b8559-136">-ApiVersion</span></span>
<span data-ttu-id="b8559-137">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b8559-137">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b8559-138">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="b8559-138">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="b8559-139">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8559-139">-AsJob</span></span>
<span data-ttu-id="b8559-140">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b8559-140">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8559-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8559-141">-DefaultProfile</span></span>
<span data-ttu-id="b8559-142">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b8559-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8559-143">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="b8559-143">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="b8559-144">Gibt eine Debug-Protokollebene an.</span><span class="sxs-lookup"><span data-stu-id="b8559-144">Specifies a debug log level.</span></span>
<span data-ttu-id="b8559-145">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b8559-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b8559-146">RequestContent</span><span class="sxs-lookup"><span data-stu-id="b8559-146">RequestContent</span></span>
- <span data-ttu-id="b8559-147">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="b8559-147">ResponseContent</span></span>
- <span data-ttu-id="b8559-148">Alle</span><span class="sxs-lookup"><span data-stu-id="b8559-148">All</span></span>
- <span data-ttu-id="b8559-149">Keine</span><span class="sxs-lookup"><span data-stu-id="b8559-149">None</span></span>

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

### <span data-ttu-id="b8559-150">-Force</span><span class="sxs-lookup"><span data-stu-id="b8559-150">-Force</span></span>
<span data-ttu-id="b8559-151">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="b8559-151">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b8559-152">-Modus</span><span class="sxs-lookup"><span data-stu-id="b8559-152">-Mode</span></span>
<span data-ttu-id="b8559-153">Gibt den Bereitstellungsmodus an.</span><span class="sxs-lookup"><span data-stu-id="b8559-153">Specifies the deployment mode.</span></span> <span data-ttu-id="b8559-154">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b8559-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b8559-155">Komplette</span><span class="sxs-lookup"><span data-stu-id="b8559-155">Complete</span></span>
- <span data-ttu-id="b8559-156">Inkrementell im vollständigen Modus löscht der Ressourcen-Manager Ressourcen, die in der Ressourcengruppe vorhanden sind, aber nicht in der Vorlage angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b8559-156">Incremental In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> <span data-ttu-id="b8559-157">Im inkrementellen Modus hinterlässt der Ressourcen-Manager unveränderte Ressourcen, die in der Ressourcengruppe vorhanden sind, aber nicht in der Vorlage angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b8559-157">In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8559-158">-Name</span><span class="sxs-lookup"><span data-stu-id="b8559-158">-Name</span></span>
<span data-ttu-id="b8559-159">Gibt den Namen der zu erstellende Ressourcengruppen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="b8559-159">Specifies the name of the resource group deployment to create.</span></span>

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

### <span data-ttu-id="b8559-160">-Pre</span><span class="sxs-lookup"><span data-stu-id="b8559-160">-Pre</span></span>
<span data-ttu-id="b8559-161">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b8559-161">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b8559-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8559-162">-ResourceGroupName</span></span>
<span data-ttu-id="b8559-163">Gibt den Namen der Ressourcengruppe an, die bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8559-163">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="b8559-164">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="b8559-164">-RollBackDeploymentName</span></span>
<span data-ttu-id="b8559-165">Rollback zur erfolgreichen Bereitstellung mit dem angegebenen Namen in der Ressourcengruppe sollte nicht verwendet werden, wenn-RollbackToLastDeployment verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8559-165">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="b8559-166">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="b8559-166">-RollbackToLastDeployment</span></span>
<span data-ttu-id="b8559-167">Rollback zur letzten erfolgreichen Bereitstellung in der Ressourcengruppe sollte nicht vorhanden sein, wenn-RollBackDeploymentName verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8559-167">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="b8559-168">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="b8559-168">-TemplateFile</span></span>
<span data-ttu-id="b8559-169">Gibt den vollständigen Pfad einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="b8559-169">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="b8559-170">Hierbei kann es sich um eine benutzerdefinierte Vorlage oder eine Katalogvorlage handeln, die als JSON-Datei gespeichert wird, beispielsweise eine mit dem Cmdlet **Save-AzResourceGroupGalleryTemplate** erstellte.</span><span class="sxs-lookup"><span data-stu-id="b8559-170">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="b8559-171">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="b8559-171">-TemplateParameterFile</span></span>
<span data-ttu-id="b8559-172">Gibt den vollständigen Pfad einer JSON-Datei an, die die Namen und Werte der Vorlagenparameter enthält.</span><span class="sxs-lookup"><span data-stu-id="b8559-172">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="b8559-173">Wenn eine Vorlage über Parameter verfügt, müssen Sie die Parameterwerte mit dem *TemplateParameterFile* -Parameter oder dem *TemplateParameterObject* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="b8559-173">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="b8559-174">Vorlagenparameter werden dem Befehl dynamisch hinzugefügt, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="b8559-174">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="b8559-175">Wenn Sie die dynamischen Parameter verwenden möchten, geben Sie ein Minuszeichen (-) ein, um einen Parameternamen anzugeben, und verwenden Sie dann die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="b8559-175">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8559-176">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="b8559-176">-TemplateParameterObject</span></span>
<span data-ttu-id="b8559-177">Gibt eine Hashtabelle mit Vorlagenparameter Namen und-Werten an.</span><span class="sxs-lookup"><span data-stu-id="b8559-177">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="b8559-178">Wenn Sie Hilfe zu Hashtabellen in Windows PowerShell benötigen, geben Sie `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="b8559-178">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="b8559-179">Wenn eine Vorlage über Parameter verfügt, müssen Sie Parameterwerte angeben.</span><span class="sxs-lookup"><span data-stu-id="b8559-179">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="b8559-180">Vorlagenparameter werden dem Befehl dynamisch hinzugefügt, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="b8559-180">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8559-181">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="b8559-181">-TemplateParameterUri</span></span>
<span data-ttu-id="b8559-182">Gibt den URI einer Vorlagenparameter Datei an.</span><span class="sxs-lookup"><span data-stu-id="b8559-182">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8559-183">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="b8559-183">-TemplateUri</span></span>
<span data-ttu-id="b8559-184">Gibt den URI einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="b8559-184">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="b8559-185">Diese Datei kann eine benutzerdefinierte Vorlage oder eine Katalogvorlage sein, die als JSON-Datei gespeichert wird, beispielsweise mithilfe von **Save-AzResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="b8559-185">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="b8559-186">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b8559-186">-Confirm</span></span>
<span data-ttu-id="b8559-187">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8559-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8559-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8559-188">-WhatIf</span></span>
<span data-ttu-id="b8559-189">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8559-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8559-190">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8559-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8559-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8559-191">CommonParameters</span></span>
<span data-ttu-id="b8559-192">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8559-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8559-193">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8559-193">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8559-194">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b8559-194">INPUTS</span></span>

### <span data-ttu-id="b8559-195">Keine</span><span class="sxs-lookup"><span data-stu-id="b8559-195">None</span></span>

## <span data-ttu-id="b8559-196">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b8559-196">OUTPUTS</span></span>

### <span data-ttu-id="b8559-197">Microsoft. Azure. Commands. ResourceManager. Models. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b8559-197">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="b8559-198">Notizen</span><span class="sxs-lookup"><span data-stu-id="b8559-198">NOTES</span></span>

## <span data-ttu-id="b8559-199">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b8559-199">RELATED LINKS</span></span>

[<span data-ttu-id="b8559-200">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b8559-200">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="b8559-201">Neu – AzResource</span><span class="sxs-lookup"><span data-stu-id="b8559-201">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="b8559-202">Neu – AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b8559-202">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="b8559-203">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b8559-203">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="b8559-204">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b8559-204">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="b8559-205">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b8559-205">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


