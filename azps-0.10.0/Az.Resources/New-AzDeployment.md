---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: 97d6b11a4993ced62b84de24c501a2c438173141
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843351"
---
# <span data-ttu-id="3767b-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="3767b-101">New-AzDeployment</span></span>

## <span data-ttu-id="3767b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3767b-102">SYNOPSIS</span></span>
<span data-ttu-id="3767b-103">Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="3767b-103">Creat a deployment</span></span>

## <span data-ttu-id="3767b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3767b-104">SYNTAX</span></span>

### <span data-ttu-id="3767b-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="3767b-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3767b-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3767b-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3767b-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3767b-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3767b-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3767b-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3767b-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3767b-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3767b-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3767b-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3767b-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3767b-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3767b-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="3767b-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3767b-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3767b-113">DESCRIPTION</span></span>
<span data-ttu-id="3767b-114">Mit dem Cmdlet **New-AzDeployment** wird eine Bereitstellung im aktuellen Abonnement Bereich hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3767b-114">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="3767b-115">Dazu gehören die Ressourcen, die für die Bereitstellung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="3767b-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="3767b-116">Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität.</span><span class="sxs-lookup"><span data-stu-id="3767b-116">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="3767b-117">Eine Ressource kann in einer Ressourcengruppe wie Datenbankserver, Datenbank, Website, virtueller Computer oder Speicherkonto Leben.</span><span class="sxs-lookup"><span data-stu-id="3767b-117">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span> <span data-ttu-id="3767b-118">Oder es kann sich um eine Ressource auf Abonnementebene wie Rollendefinition, Richtliniendefinition usw. handeln.</span><span class="sxs-lookup"><span data-stu-id="3767b-118">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="3767b-119">Verwenden Sie zum Hinzufügen von Ressourcen zu einer Ressourcengruppe das **New-AzDeployment-** Objekt, das eine Bereitstellung in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="3767b-119">To add resources to a resource group, use the **New-AzDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="3767b-120">Mit dem Cmdlet **New-AzDeployment** wird eine Bereitstellung im aktuellen Abonnement Bereich erstellt, in dem die Ressourcen auf Abonnementebene bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3767b-120">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span> 

<span data-ttu-id="3767b-121">Wenn Sie eine Bereitstellung bei einem Abonnement hinzufügen möchten, geben Sie den Speicherort und eine Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="3767b-121">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="3767b-122">Der Speicherort weist Azure Resource Manager an, wo die Bereitstellungsdaten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3767b-122">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="3767b-123">Bei der Vorlage handelt es sich um eine JSON-Zeichenfolge, die einzelne Ressourcen enthält, die bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3767b-123">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="3767b-124">Die Vorlage enthält Parameterplatzhalter für erforderliche Ressourcen und konfigurierbare Eigenschaftswerte wie Namen und Größen.</span><span class="sxs-lookup"><span data-stu-id="3767b-124">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="3767b-125">Wenn Sie eine benutzerdefinierte Vorlage für die Bereitstellung verwenden möchten, geben Sie den Parameter " *Templatedatei* " oder " *TemplateUri* " an.</span><span class="sxs-lookup"><span data-stu-id="3767b-125">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="3767b-126">Jede Vorlage verfügt über Parameter für konfigurierbare Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3767b-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="3767b-127">Wenn Sie Werte für die Vorlagenparameter angeben möchten, geben Sie den *TemplateParameterFile* -Parameter oder den *TemplateParameterObject* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="3767b-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="3767b-128">Alternativ können Sie die Vorlagenparameter verwenden, die dem Befehl dynamisch hinzugefügt werden, wenn Sie eine Vorlage angeben.</span><span class="sxs-lookup"><span data-stu-id="3767b-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="3767b-129">Wenn Sie dynamische Parameter verwenden möchten, geben Sie Sie an der Eingabeaufforderung ein, oder geben Sie ein Minuszeichen (-) ein, um einen Parameter anzugeben, und verwenden Sie die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="3767b-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="3767b-130">Vorlagenparameter Werte, die Sie an der Eingabeaufforderung eingeben, haben Vorrang vor Werten in einem Vorlagenparameter Objekt oder einer Datei.</span><span class="sxs-lookup"><span data-stu-id="3767b-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="3767b-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3767b-131">EXAMPLES</span></span>

### <span data-ttu-id="3767b-132">Beispiel 1: Verwenden einer benutzerdefinierten Vorlage und einer Parameterdatei zum Erstellen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="3767b-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="3767b-133">Dieser Befehl erstellt eine neue Bereitstellung im aktuellen Abonnement Bereich mithilfe einer benutzerdefinierten Vorlage und einer Vorlagendatei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="3767b-133">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="3767b-134">Der Befehl verwendet den *Templatedatei* -Parameter, um die Vorlage und den *TemplateParameterFile* -Parameter anzugeben, um eine Datei anzugeben, die Parameter und Parameterwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="3767b-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="3767b-135">Die Version der Vorlage wird mithilfe des *TemplateVersion* -Parameters angegeben.</span><span class="sxs-lookup"><span data-stu-id="3767b-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="3767b-136">Parameter</span><span class="sxs-lookup"><span data-stu-id="3767b-136">PARAMETERS</span></span>

### <span data-ttu-id="3767b-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3767b-137">-ApiVersion</span></span>
<span data-ttu-id="3767b-138">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3767b-138">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3767b-139">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="3767b-139">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="3767b-140">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3767b-140">-AsJob</span></span>
<span data-ttu-id="3767b-141">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3767b-141">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3767b-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3767b-142">-DefaultProfile</span></span>
<span data-ttu-id="3767b-143">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3767b-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3767b-144">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="3767b-144">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="3767b-145">Die Debug-Protokollebene der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="3767b-145">The deployment debug log level.</span></span>

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

### <span data-ttu-id="3767b-146">-Standort</span><span class="sxs-lookup"><span data-stu-id="3767b-146">-Location</span></span>
<span data-ttu-id="3767b-147">Der Speicherort, an dem Bereitstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3767b-147">The location to store deployment data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3767b-148">-Name</span><span class="sxs-lookup"><span data-stu-id="3767b-148">-Name</span></span>
<span data-ttu-id="3767b-149">Der Name der Bereitstellung, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3767b-149">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="3767b-150">Nur gültig, wenn eine Vorlage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3767b-150">Only valid when a template is used.</span></span>
<span data-ttu-id="3767b-151">Wenn eine Vorlage verwendet wird und der Benutzer keinen Bereitstellungsnamen angibt, verwenden Sie die aktuelle Uhrzeit wie "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="3767b-151">When a template is used, if the user doesn't specify a deployment name, use the current time, like "20131223140835".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3767b-152">-Pre</span><span class="sxs-lookup"><span data-stu-id="3767b-152">-Pre</span></span>
<span data-ttu-id="3767b-153">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="3767b-153">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3767b-154">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="3767b-154">-TemplateFile</span></span>
<span data-ttu-id="3767b-155">Lokaler Pfad zur Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="3767b-155">Local path to the template file.</span></span>

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

### <span data-ttu-id="3767b-156">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="3767b-156">-TemplateParameterFile</span></span>
<span data-ttu-id="3767b-157">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="3767b-157">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="3767b-158">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="3767b-158">-TemplateParameterObject</span></span>
<span data-ttu-id="3767b-159">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="3767b-159">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="3767b-160">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="3767b-160">-TemplateParameterUri</span></span>
<span data-ttu-id="3767b-161">URI zur Vorlagenparameter Datei.</span><span class="sxs-lookup"><span data-stu-id="3767b-161">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="3767b-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="3767b-162">-TemplateUri</span></span>
<span data-ttu-id="3767b-163">URI zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="3767b-163">Uri to the template file.</span></span>

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

### <span data-ttu-id="3767b-164">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3767b-164">-Confirm</span></span>
<span data-ttu-id="3767b-165">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3767b-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3767b-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3767b-166">-WhatIf</span></span>
<span data-ttu-id="3767b-167">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3767b-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3767b-168">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3767b-168">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3767b-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3767b-169">CommonParameters</span></span>
<span data-ttu-id="3767b-170">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3767b-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3767b-171">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3767b-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3767b-172">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3767b-172">INPUTS</span></span>

### <span data-ttu-id="3767b-173">System. String</span><span class="sxs-lookup"><span data-stu-id="3767b-173">System.String</span></span>
<span data-ttu-id="3767b-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3767b-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3767b-175">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3767b-175">OUTPUTS</span></span>

### <span data-ttu-id="3767b-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="3767b-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="3767b-177">Notizen</span><span class="sxs-lookup"><span data-stu-id="3767b-177">NOTES</span></span>

## <span data-ttu-id="3767b-178">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3767b-178">RELATED LINKS</span></span>
