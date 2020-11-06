---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 514d1257d917dc1bbf20f93d05236af9f36bd832
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480957"
---
# <span data-ttu-id="2de1d-101">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2de1d-101">New-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="2de1d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2de1d-102">SYNOPSIS</span></span>
<span data-ttu-id="2de1d-103">Fügt eine Azure-Bereitstellung zu einer Ressourcengruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="2de1d-103">Adds an Azure deployment to a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2de1d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2de1d-104">SYNTAX</span></span>

### <span data-ttu-id="2de1d-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="2de1d-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2de1d-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2de1d-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2de1d-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2de1d-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2de1d-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2de1d-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2de1d-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2de1d-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2de1d-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2de1d-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2de1d-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2de1d-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2de1d-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2de1d-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2de1d-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2de1d-113">DESCRIPTION</span></span>
<span data-ttu-id="2de1d-114">Mit dem Cmdlet **New-AzureRmResourceGroupDeployment** wird eine Bereitstellung zu einer vorhandenen Ressourcengruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2de1d-114">The **New-AzureRmResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="2de1d-115">Dazu gehören die Ressourcen, die für die Bereitstellung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="2de1d-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="2de1d-116">Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität, beispielsweise ein Datenbankserver, eine Datenbank, eine Website, einen virtuellen Computer oder ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="2de1d-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="2de1d-117">Eine Azure-Ressourcengruppe ist eine Sammlung von Azure-Ressourcen, die als Einheit bereitgestellt werden, beispielsweise die Website, den Datenbankserver und Datenbanken, die für eine Finanzwebsite erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="2de1d-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="2de1d-118">Eine Ressourcengruppen Bereitstellung verwendet eine Vorlage zum Hinzufügen von Ressourcen zu einer Ressourcengruppe und veröffentlicht diese, damit Sie in Azure verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="2de1d-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="2de1d-119">Verwenden Sie das New-AzureRmResource-Cmdlet, um einer Ressourcengruppe Ressourcen hinzuzufügen, ohne eine Vorlage zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2de1d-119">To add resources to a resource group without using a template, use the New-AzureRmResource cmdlet.</span></span>

<span data-ttu-id="2de1d-120">Wenn Sie eine Ressourcengruppen Bereitstellung hinzufügen möchten, geben Sie den Namen einer vorhandenen Ressourcengruppe und einer Ressourcengruppen Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="2de1d-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="2de1d-121">Eine Ressourcengruppen Vorlage ist eine JSON-Zeichenfolge, die eine Ressourcengruppe für einen komplexen cloudbasierten Dienst, beispielsweise ein Webportal, darstellt.</span><span class="sxs-lookup"><span data-stu-id="2de1d-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="2de1d-122">Die Vorlage enthält Parameterplatzhalter für erforderliche Ressourcen und konfigurierbare Eigenschaftswerte wie Namen und Größen.</span><span class="sxs-lookup"><span data-stu-id="2de1d-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="2de1d-123">Sie können viele Vorlagen im Azure-Vorlagenkatalog finden, oder Sie können eigene Vorlagen erstellen.</span><span class="sxs-lookup"><span data-stu-id="2de1d-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="2de1d-124">Sie können das Cmdlet **Get-AzureRmResourceGroupGalleryTemplate** verwenden, um eine Vorlage im Katalog zu finden.</span><span class="sxs-lookup"><span data-stu-id="2de1d-124">You can use the **Get-AzureRmResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>

<span data-ttu-id="2de1d-125">Wenn Sie eine benutzerdefinierte Vorlage zum Erstellen einer Ressourcengruppe verwenden möchten, geben Sie den Parameter " *Templatedatei* " oder " *TemplateUri* " an.</span><span class="sxs-lookup"><span data-stu-id="2de1d-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="2de1d-126">Jede Vorlage verfügt über Parameter für konfigurierbare Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2de1d-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="2de1d-127">Wenn Sie Werte für die Vorlagenparameter angeben möchten, geben Sie den *TemplateParameterFile* -Parameter oder den *TemplateParameterObject* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="2de1d-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="2de1d-128">Alternativ können Sie die Vorlagenparameter verwenden, die dem Befehl dynamisch hinzugefügt werden, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="2de1d-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="2de1d-129">Wenn Sie dynamische Parameter verwenden möchten, geben Sie Sie an der Eingabeaufforderung ein, oder geben Sie ein Minuszeichen (-) ein, um einen Parameter anzugeben, und verwenden Sie die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="2de1d-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="2de1d-130">Vorlagenparameter Werte, die Sie an der Eingabeaufforderung eingeben, haben Vorrang vor Werten in einem Vorlagenparameter Objekt oder einer Datei.</span><span class="sxs-lookup"><span data-stu-id="2de1d-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="2de1d-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2de1d-131">EXAMPLES</span></span>

### <span data-ttu-id="2de1d-132">Beispiel 1: Verwenden einer benutzerdefinierten Vorlage und einer Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="2de1d-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="2de1d-133">Dieser Befehl erstellt eine neue Bereitstellung mithilfe einer benutzerdefinierten Vorlage und einer Vorlagendatei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="2de1d-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="2de1d-134">Der Befehl verwendet den *Templatedatei* -Parameter, um die Vorlage und den *TemplateParameterFile* -Parameter anzugeben, um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="2de1d-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="2de1d-135">Die Version der Vorlage wird mithilfe des *TemplateVersion* -Parameters angegeben.</span><span class="sxs-lookup"><span data-stu-id="2de1d-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="2de1d-136">Parameter</span><span class="sxs-lookup"><span data-stu-id="2de1d-136">PARAMETERS</span></span>

### <span data-ttu-id="2de1d-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2de1d-137">-ApiVersion</span></span>
<span data-ttu-id="2de1d-138">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="2de1d-138">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="2de1d-139">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="2de1d-139">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2de1d-140">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2de1d-140">-AsJob</span></span>
<span data-ttu-id="2de1d-141">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2de1d-141">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2de1d-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de1d-142">-DefaultProfile</span></span>
<span data-ttu-id="2de1d-143">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2de1d-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2de1d-144">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="2de1d-144">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="2de1d-145">Gibt eine Debug-Protokollebene an.</span><span class="sxs-lookup"><span data-stu-id="2de1d-145">Specifies a debug log level.</span></span>
<span data-ttu-id="2de1d-146">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2de1d-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2de1d-147">RequestContent</span><span class="sxs-lookup"><span data-stu-id="2de1d-147">RequestContent</span></span>
- <span data-ttu-id="2de1d-148">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="2de1d-148">ResponseContent</span></span>
- <span data-ttu-id="2de1d-149">Alle</span><span class="sxs-lookup"><span data-stu-id="2de1d-149">All</span></span>
- <span data-ttu-id="2de1d-150">Keine</span><span class="sxs-lookup"><span data-stu-id="2de1d-150">None</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de1d-151">-Force</span><span class="sxs-lookup"><span data-stu-id="2de1d-151">-Force</span></span>
<span data-ttu-id="2de1d-152">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="2de1d-152">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2de1d-153">-Modus</span><span class="sxs-lookup"><span data-stu-id="2de1d-153">-Mode</span></span>
<span data-ttu-id="2de1d-154">Gibt den Bereitstellungsmodus an.</span><span class="sxs-lookup"><span data-stu-id="2de1d-154">Specifies the deployment mode.</span></span> <span data-ttu-id="2de1d-155">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2de1d-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2de1d-156">Komplette</span><span class="sxs-lookup"><span data-stu-id="2de1d-156">Complete</span></span>
- <span data-ttu-id="2de1d-157">Inkrementelle</span><span class="sxs-lookup"><span data-stu-id="2de1d-157">Incremental</span></span>

<span data-ttu-id="2de1d-158">Im vollständigen Modus löscht der Ressourcen-Manager Ressourcen, die in der Ressourcengruppe vorhanden sind, aber nicht in der Vorlage angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="2de1d-158">In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> <span data-ttu-id="2de1d-159">Im inkrementellen Modus hinterlässt der Ressourcen-Manager unveränderte Ressourcen, die in der Ressourcengruppe vorhanden sind, aber nicht in der Vorlage angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="2de1d-159">In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de1d-160">-Name</span><span class="sxs-lookup"><span data-stu-id="2de1d-160">-Name</span></span>
<span data-ttu-id="2de1d-161">Gibt den Namen der zu erstellende Ressourcengruppen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="2de1d-161">Specifies the name of the resource group deployment to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de1d-162">-Pre</span><span class="sxs-lookup"><span data-stu-id="2de1d-162">-Pre</span></span>
<span data-ttu-id="2de1d-163">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="2de1d-163">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2de1d-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2de1d-164">-ResourceGroupName</span></span>
<span data-ttu-id="2de1d-165">Gibt den Namen der Ressourcengruppe an, die bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2de1d-165">Specifies the name of the resource group to deploy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de1d-166">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="2de1d-166">-TemplateFile</span></span>
<span data-ttu-id="2de1d-167">Gibt den vollständigen Pfad einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="2de1d-167">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="2de1d-168">Hierbei kann es sich um eine benutzerdefinierte Vorlage oder eine Katalogvorlage handeln, die als JSON-Datei gespeichert wird, beispielsweise eine mit dem Cmdlet **Save-AzureRmResourceGroupGalleryTemplate** erstellte.</span><span class="sxs-lookup"><span data-stu-id="2de1d-168">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzureRmResourceGroupGalleryTemplate** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de1d-169">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="2de1d-169">-TemplateParameterFile</span></span>
<span data-ttu-id="2de1d-170">Gibt den vollständigen Pfad einer JSON-Datei an, die die Namen und Werte der Vorlagenparameter enthält.</span><span class="sxs-lookup"><span data-stu-id="2de1d-170">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="2de1d-171">Wenn eine Vorlage über Parameter verfügt, müssen Sie die Parameterwerte mit dem *TemplateParameterFile* -Parameter oder dem *TemplateParameterObject* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="2de1d-171">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="2de1d-172">Vorlagenparameter werden dem Befehl dynamisch hinzugefügt, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="2de1d-172">Template parameters are dynamically added to the command when you specify a template.</span></span>

<span data-ttu-id="2de1d-173">Wenn Sie die dynamischen Parameter verwenden möchten, geben Sie ein Minuszeichen (-) ein, um einen Parameternamen anzugeben, und verwenden Sie dann die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="2de1d-173">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de1d-174">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="2de1d-174">-TemplateParameterObject</span></span>
<span data-ttu-id="2de1d-175">Gibt eine Hashtabelle mit Vorlagenparameter Namen und-Werten an.</span><span class="sxs-lookup"><span data-stu-id="2de1d-175">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="2de1d-176">Wenn Sie Hilfe zu Hashtabellen in Windows PowerShell benötigen, geben Sie `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="2de1d-176">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="2de1d-177">Wenn eine Vorlage über Parameter verfügt, müssen Sie Parameterwerte angeben.</span><span class="sxs-lookup"><span data-stu-id="2de1d-177">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="2de1d-178">Vorlagenparameter werden dem Befehl dynamisch hinzugefügt, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="2de1d-178">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de1d-179">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="2de1d-179">-TemplateParameterUri</span></span>
<span data-ttu-id="2de1d-180">Gibt den URI einer Vorlagenparameter Datei an.</span><span class="sxs-lookup"><span data-stu-id="2de1d-180">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de1d-181">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="2de1d-181">-TemplateUri</span></span>
<span data-ttu-id="2de1d-182">Gibt den URI einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="2de1d-182">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="2de1d-183">Diese Datei kann eine benutzerdefinierte Vorlage oder eine Katalogvorlage sein, die als JSON-Datei gespeichert wird, beispielsweise mithilfe von **Save-AzureRmResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="2de1d-183">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzureRmResourceGroupGalleryTemplate**.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de1d-184">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2de1d-184">-Confirm</span></span>
<span data-ttu-id="2de1d-185">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2de1d-185">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2de1d-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2de1d-186">-WhatIf</span></span>
<span data-ttu-id="2de1d-187">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2de1d-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2de1d-188">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2de1d-188">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2de1d-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de1d-189">CommonParameters</span></span>
<span data-ttu-id="2de1d-190">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2de1d-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de1d-191">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2de1d-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de1d-192">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2de1d-192">INPUTS</span></span>

### <span data-ttu-id="2de1d-193">Keine</span><span class="sxs-lookup"><span data-stu-id="2de1d-193">None</span></span>

## <span data-ttu-id="2de1d-194">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2de1d-194">OUTPUTS</span></span>

### <span data-ttu-id="2de1d-195">Microsoft. Azure. Commands. ResourceManager. Models. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2de1d-195">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="2de1d-196">Notizen</span><span class="sxs-lookup"><span data-stu-id="2de1d-196">NOTES</span></span>

## <span data-ttu-id="2de1d-197">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2de1d-197">RELATED LINKS</span></span>

[<span data-ttu-id="2de1d-198">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2de1d-198">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="2de1d-199">Neu – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="2de1d-199">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="2de1d-200">Neu – AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2de1d-200">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="2de1d-201">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2de1d-201">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="2de1d-202">Stopp-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2de1d-202">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="2de1d-203">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2de1d-203">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


