---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 5ee86c91b1dc1354b078b727e3bc9ebfe5a43bfe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145972"
---
# <span data-ttu-id="6f0e8-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f0e8-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="6f0e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f0e8-102">SYNOPSIS</span></span>
<span data-ttu-id="6f0e8-103">Überprüft die Bereitstellung einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6f0e8-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="6f0e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f0e8-104">SYNTAX</span></span>

### <span data-ttu-id="6f0e8-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="6f0e8-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f0e8-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="6f0e8-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f0e8-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="6f0e8-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f0e8-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="6f0e8-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f0e8-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="6f0e8-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f0e8-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="6f0e8-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f0e8-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="6f0e8-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f0e8-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="6f0e8-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f0e8-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="6f0e8-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f0e8-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="6f0e8-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f0e8-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="6f0e8-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f0e8-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="6f0e8-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f0e8-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f0e8-117">DESCRIPTION</span></span>
<span data-ttu-id="6f0e8-118">Das **Cmdlet "Test-AzResourceGroupDeployment"** bestimmt, ob eine Bereitstellungsvorlage für eine Azure-Ressourcengruppe und deren Parameterwerte gültig sind.</span><span class="sxs-lookup"><span data-stu-id="6f0e8-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="6f0e8-119">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6f0e8-119">EXAMPLES</span></span>

### <span data-ttu-id="6f0e8-120">Beispiel 1: Testen der Bereitstellung mit einem benutzerdefinierten Vorlagenobjekt und einer Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="6f0e8-120">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="6f0e8-121">Mit diesem Befehl wird eine Bereitstellung in der angegebenen Ressourcengruppe mithilfe einer Speicherhashtable getestet, die aus der angegebenen Vorlagendatei erstellt wurde, und einer Parameterdatei.</span><span class="sxs-lookup"><span data-stu-id="6f0e8-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="6f0e8-122">Beispiel 2: Testen der Bereitstellung über Vorlagendatei und Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="6f0e8-122">Example 2: Test deployment via template file and parameter file</span></span>

```powershell
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="6f0e8-123">Mit diesem Befehl wird eine Bereitstellung in der angegebenen Ressourcengruppe und Ressource mithilfe der bereitgestellten Vorlagendatei und einer Parameterdatei getestet.</span><span class="sxs-lookup"><span data-stu-id="6f0e8-123">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="6f0e8-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f0e8-124">PARAMETERS</span></span>

### <span data-ttu-id="6f0e8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f0e8-125">-DefaultProfile</span></span>
<span data-ttu-id="6f0e8-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6f0e8-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f0e8-127">-Mode</span><span class="sxs-lookup"><span data-stu-id="6f0e8-127">-Mode</span></span>
<span data-ttu-id="6f0e8-128">Gibt den Bereitstellungsmodus an.</span><span class="sxs-lookup"><span data-stu-id="6f0e8-128">Specifies the deployment mode.</span></span>
<span data-ttu-id="6f0e8-129">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="6f0e8-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6f0e8-130">Inkrementell</span><span class="sxs-lookup"><span data-stu-id="6f0e8-130">Incremental</span></span>
- <span data-ttu-id="6f0e8-131">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="6f0e8-131">Complete</span></span>

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

### <span data-ttu-id="6f0e8-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="6f0e8-132">-Pre</span></span>
<span data-ttu-id="6f0e8-133">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6f0e8-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6f0e8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f0e8-134">-ResourceGroupName</span></span>
<span data-ttu-id="6f0e8-135">Gibt den Namen der zu testden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="6f0e8-135">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="6f0e8-136">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="6f0e8-136">-RollBackDeploymentName</span></span>
<span data-ttu-id="6f0e8-137">Ein Rollback zur erfolgreichen Bereitstellung unter dem angegebenen Namen in der Ressourcengruppe sollte nicht verwendet werden, wenn "-RollbackToLastDeployment" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6f0e8-137">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="6f0e8-138">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="6f0e8-138">-RollbackToLastDeployment</span></span>
<span data-ttu-id="6f0e8-139">Ein Rollback zur letzten erfolgreichen Bereitstellung in der Ressourcengruppe sollte nicht vorhanden sein, wenn "-RollBackDeploymentName" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6f0e8-139">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="6f0e8-140">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="6f0e8-140">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="6f0e8-141">Überspringt die Verarbeitung dynamischer PowerShell-Parameter, die überprüft, ob der bereitgestellte Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f0e8-141">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="6f0e8-142">Bei dieser Überprüfung müsste der Benutzer einen Wert für die fehlenden Parameter angeben. Wenn jedoch "-SkipTemplateParameterPrompt" angegeben wird, wird diese Eingabeaufforderung und der Fehler sofort ignoriert, wenn ein Parameter nicht in der Vorlage gebunden wurde.</span><span class="sxs-lookup"><span data-stu-id="6f0e8-142">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="6f0e8-143">Bei nicht interaktiven Skripts kann "-SkipTemplateParameterPrompt" bereitgestellt werden, um eine bessere Fehlermeldung für den Fall zu liefern, dass nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="6f0e8-143">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="6f0e8-144">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="6f0e8-144">-TemplateFile</span></span>
<span data-ttu-id="6f0e8-145">Gibt den vollständigen Pfad einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="6f0e8-145">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="6f0e8-146">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="6f0e8-146">-TemplateObject</span></span>
<span data-ttu-id="6f0e8-147">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="6f0e8-147">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="6f0e8-148">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="6f0e8-148">-TemplateParameterFile</span></span>
<span data-ttu-id="6f0e8-149">Gibt den vollständigen Pfad einer JSON-Datei an, die die Namen und Werte der Vorlagenparameter enthält.</span><span class="sxs-lookup"><span data-stu-id="6f0e8-149">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="6f0e8-150">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="6f0e8-150">-TemplateParameterObject</span></span>
<span data-ttu-id="6f0e8-151">Gibt eine Hashtabelle mit Vorlagenparameternamen und -werten an.</span><span class="sxs-lookup"><span data-stu-id="6f0e8-151">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="6f0e8-152">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="6f0e8-152">-TemplateParameterUri</span></span>
<span data-ttu-id="6f0e8-153">Gibt den URI einer Vorlagenparameterdatei an.</span><span class="sxs-lookup"><span data-stu-id="6f0e8-153">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="6f0e8-154">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="6f0e8-154">-TemplateUri</span></span>
<span data-ttu-id="6f0e8-155">Gibt den URI einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="6f0e8-155">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="6f0e8-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f0e8-156">CommonParameters</span></span>
<span data-ttu-id="6f0e8-157">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f0e8-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f0e8-158">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f0e8-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f0e8-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6f0e8-159">INPUTS</span></span>

### <span data-ttu-id="6f0e8-160">System.String</span><span class="sxs-lookup"><span data-stu-id="6f0e8-160">System.String</span></span>

### <span data-ttu-id="6f0e8-161">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="6f0e8-161">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="6f0e8-162">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6f0e8-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6f0e8-163">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6f0e8-163">OUTPUTS</span></span>

### <span data-ttu-id="6f0e8-164">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="6f0e8-164">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="6f0e8-165">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6f0e8-165">NOTES</span></span>

## <span data-ttu-id="6f0e8-166">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6f0e8-166">RELATED LINKS</span></span>

[<span data-ttu-id="6f0e8-167">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f0e8-167">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="6f0e8-168">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f0e8-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="6f0e8-169">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f0e8-169">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="6f0e8-170">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f0e8-170">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


