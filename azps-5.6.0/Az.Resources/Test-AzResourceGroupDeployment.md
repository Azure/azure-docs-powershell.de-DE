---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 0e0d4645901f60f9e290d197a47b133d6bf3db8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930843"
---
# <span data-ttu-id="08edb-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="08edb-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="08edb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08edb-102">SYNOPSIS</span></span>
<span data-ttu-id="08edb-103">Überprüft eine Ressourcengruppenbereitstellung.</span><span class="sxs-lookup"><span data-stu-id="08edb-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="08edb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08edb-104">SYNTAX</span></span>

### <span data-ttu-id="08edb-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="08edb-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08edb-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="08edb-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08edb-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="08edb-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08edb-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="08edb-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08edb-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="08edb-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08edb-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="08edb-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08edb-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="08edb-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08edb-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="08edb-112">ByTemplateSpecResourceIdAndParams</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08edb-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="08edb-113">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08edb-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="08edb-114">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08edb-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="08edb-115">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08edb-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="08edb-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08edb-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="08edb-117">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08edb-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="08edb-118">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08edb-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="08edb-119">ByTemplateSpecResourceId</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08edb-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08edb-120">DESCRIPTION</span></span>
<span data-ttu-id="08edb-121">Das **Cmdlet Test-AzResourceGroupDeployment** bestimmt, ob eine Bereitstellungsvorlage für Azure-Ressourcengruppen und deren Parameterwerte gültig sind.</span><span class="sxs-lookup"><span data-stu-id="08edb-121">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="08edb-122">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="08edb-122">EXAMPLES</span></span>

### <span data-ttu-id="08edb-123">Beispiel 1: Testen der Bereitstellung mit einem benutzerdefinierten Vorlagenobjekt und einer Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="08edb-123">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="08edb-124">Mit diesem Befehl wird eine Bereitstellung in der angegebenen Ressourcengruppe mithilfe einer In-Memory-Hashtable getestet, die aus der angegebenen Vorlagendatei und einer Parameterdatei erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="08edb-124">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="08edb-125">Beispiel 2: Testen der Bereitstellung über Vorlagendatei und Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="08edb-125">Example 2: Test deployment via template file and parameter file</span></span>

```powershell
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="08edb-126">Mit diesem Befehl wird eine Bereitstellung in der angegebenen Ressourcengruppe und -ressource mithilfe der bereitgestellten Vorlagendatei und einer Parameterdatei getestet.</span><span class="sxs-lookup"><span data-stu-id="08edb-126">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="08edb-127">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="08edb-127">PARAMETERS</span></span>

### <span data-ttu-id="08edb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08edb-128">-DefaultProfile</span></span>
<span data-ttu-id="08edb-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="08edb-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08edb-130">-Modus</span><span class="sxs-lookup"><span data-stu-id="08edb-130">-Mode</span></span>
<span data-ttu-id="08edb-131">Gibt den Bereitstellungsmodus an.</span><span class="sxs-lookup"><span data-stu-id="08edb-131">Specifies the deployment mode.</span></span>
<span data-ttu-id="08edb-132">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="08edb-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="08edb-133">Inkrementell</span><span class="sxs-lookup"><span data-stu-id="08edb-133">Incremental</span></span>
- <span data-ttu-id="08edb-134">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="08edb-134">Complete</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08edb-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="08edb-135">-Pre</span></span>
<span data-ttu-id="08edb-136">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="08edb-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="08edb-137">-QueryString</span><span class="sxs-lookup"><span data-stu-id="08edb-137">-QueryString</span></span>
<span data-ttu-id="08edb-138">Die Abfragezeichenfolge (z. B. ein SAS-Token), die mit dem Parameter TemplateUri verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="08edb-138">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="08edb-139">Würde bei verknüpften Vorlagen verwendet</span><span class="sxs-lookup"><span data-stu-id="08edb-139">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="08edb-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08edb-140">-ResourceGroupName</span></span>
<span data-ttu-id="08edb-141">Gibt den Namen der zu testenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="08edb-141">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="08edb-142">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="08edb-142">-RollBackDeploymentName</span></span>
<span data-ttu-id="08edb-143">Ein Rollback auf die erfolgreiche Bereitstellung mit dem angegebenen Namen in der Ressourcengruppe sollte nicht verwendet werden, wenn -RollbackToLastDeployment verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="08edb-143">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="08edb-144">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="08edb-144">-RollbackToLastDeployment</span></span>
<span data-ttu-id="08edb-145">Ein Rollback zur letzten erfolgreichen Bereitstellung in der Ressourcengruppe sollte nicht vorhanden sein, wenn -RollBackDeploymentName verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="08edb-145">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="08edb-146">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="08edb-146">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="08edb-147">Überspringt die PowerShell-Dynamische Parameterverarbeitung, die überprüft, ob der bereitgestellte Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08edb-147">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="08edb-148">Bei dieser Überprüfung wird der Benutzer aufgefordert, einen Wert für die fehlenden Parameter zur Verfügung zu stellen. Wenn jedoch -SkipTemplateParameterPrompt angegeben wird, werden diese Eingabeaufforderung und der Fehler sofort ignoriert, wenn festgestellt wurde, dass ein Parameter nicht in der Vorlage gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="08edb-148">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="08edb-149">Für nicht interaktive Skripts kann -SkipTemplateParameterPrompt bereitgestellt werden, um eine bessere Fehlermeldung für den Fall zu liefern, dass nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="08edb-149">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="08edb-150">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="08edb-150">-TemplateFile</span></span>
<span data-ttu-id="08edb-151">Gibt den vollständigen Pfad einer Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="08edb-151">Specifies the full path of a template file.</span></span> <span data-ttu-id="08edb-152">Unterstützter Vorlagendateityp: json und bicep.</span><span class="sxs-lookup"><span data-stu-id="08edb-152">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="08edb-153">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="08edb-153">-TemplateObject</span></span>
<span data-ttu-id="08edb-154">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="08edb-154">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="08edb-155">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="08edb-155">-TemplateParameterFile</span></span>
<span data-ttu-id="08edb-156">Gibt den vollständigen Pfad einer JSON-Datei an, der die Namen und Werte der Vorlagenparameter enthält.</span><span class="sxs-lookup"><span data-stu-id="08edb-156">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="08edb-157">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="08edb-157">-TemplateParameterObject</span></span>
<span data-ttu-id="08edb-158">Gibt eine Hashtabelle mit Vorlagenparameternamen und -werten an.</span><span class="sxs-lookup"><span data-stu-id="08edb-158">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="08edb-159">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="08edb-159">-TemplateParameterUri</span></span>
<span data-ttu-id="08edb-160">Gibt den URI einer Vorlagenparameterdatei an.</span><span class="sxs-lookup"><span data-stu-id="08edb-160">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="08edb-161">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="08edb-161">-TemplateSpecId</span></span>
<span data-ttu-id="08edb-162">Ressourcen-ID der zu bereitstellende TemplateSpec.</span><span class="sxs-lookup"><span data-stu-id="08edb-162">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="08edb-163">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="08edb-163">-TemplateUri</span></span>
<span data-ttu-id="08edb-164">Gibt den URI einer Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="08edb-164">Specifies the URI of a template file.</span></span>

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

### <span data-ttu-id="08edb-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08edb-165">CommonParameters</span></span>
<span data-ttu-id="08edb-166">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08edb-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08edb-167">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08edb-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08edb-168">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="08edb-168">INPUTS</span></span>

### <span data-ttu-id="08edb-169">System.String</span><span class="sxs-lookup"><span data-stu-id="08edb-169">System.String</span></span>

### <span data-ttu-id="08edb-170">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="08edb-170">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="08edb-171">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="08edb-171">System.Collections.Hashtable</span></span>

## <span data-ttu-id="08edb-172">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="08edb-172">OUTPUTS</span></span>

### <span data-ttu-id="08edb-173">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="08edb-173">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="08edb-174">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="08edb-174">NOTES</span></span>

## <span data-ttu-id="08edb-175">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="08edb-175">RELATED LINKS</span></span>

[<span data-ttu-id="08edb-176">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="08edb-176">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="08edb-177">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="08edb-177">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="08edb-178">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="08edb-178">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="08edb-179">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="08edb-179">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


