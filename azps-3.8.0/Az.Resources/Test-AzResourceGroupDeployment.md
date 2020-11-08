---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 97a16dcebe2730fef1d770fe8cbbf54d5488b49a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996405"
---
# <span data-ttu-id="65fdb-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="65fdb-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="65fdb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65fdb-102">SYNOPSIS</span></span>
<span data-ttu-id="65fdb-103">Überprüft eine Ressourcengruppen Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="65fdb-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="65fdb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65fdb-104">SYNTAX</span></span>

### <span data-ttu-id="65fdb-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="65fdb-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65fdb-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="65fdb-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65fdb-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="65fdb-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65fdb-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="65fdb-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65fdb-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="65fdb-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65fdb-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="65fdb-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65fdb-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="65fdb-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65fdb-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="65fdb-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65fdb-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="65fdb-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65fdb-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="65fdb-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65fdb-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="65fdb-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65fdb-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="65fdb-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65fdb-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65fdb-117">DESCRIPTION</span></span>
<span data-ttu-id="65fdb-118">Das Cmdlet **Test-AzResourceGroupDeployment** bestimmt, ob eine Azure Resource Group-Bereitstellungsvorlage und deren Parameterwerte gültig sind.</span><span class="sxs-lookup"><span data-stu-id="65fdb-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="65fdb-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65fdb-119">EXAMPLES</span></span>

### <span data-ttu-id="65fdb-120">Beispiel 1: Testen der Bereitstellung mit einem benutzerdefinierten Vorlagenobjekt und einer Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="65fdb-120">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="65fdb-121">Dieser Befehl testet eine Bereitstellung in der angegebenen Ressourcengruppe mithilfe der Arbeitsspeicher-Hashtable, die aus der angegebenen Vorlagendatei und einer Parameterdatei erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="65fdb-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="65fdb-122">Beispiel 2: Testen der Bereitstellung über die Vorlagendatei und das Parameter Objekt</span><span class="sxs-lookup"><span data-stu-id="65fdb-122">Example 2: Test deployment via template file and parameter object</span></span>

```powershell
PS C:\> New-AzResourceGroupDeployment -Name testDeployment1 -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="65fdb-123">Mit diesem Befehl wird eine Bereitstellung in der angegebenen Ressourcengruppe und-Ressource mithilfe der bereitgestellten Vorlagendatei und einer Parameterdatei getestet.</span><span class="sxs-lookup"><span data-stu-id="65fdb-123">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="65fdb-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="65fdb-124">PARAMETERS</span></span>

### <span data-ttu-id="65fdb-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="65fdb-125">-ApiVersion</span></span>
<span data-ttu-id="65fdb-126">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="65fdb-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="65fdb-127">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="65fdb-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="65fdb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65fdb-128">-DefaultProfile</span></span>
<span data-ttu-id="65fdb-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="65fdb-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65fdb-130">-Modus</span><span class="sxs-lookup"><span data-stu-id="65fdb-130">-Mode</span></span>
<span data-ttu-id="65fdb-131">Gibt den Bereitstellungsmodus an.</span><span class="sxs-lookup"><span data-stu-id="65fdb-131">Specifies the deployment mode.</span></span>
<span data-ttu-id="65fdb-132">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="65fdb-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="65fdb-133">Inkrementelle</span><span class="sxs-lookup"><span data-stu-id="65fdb-133">Incremental</span></span>
- <span data-ttu-id="65fdb-134">Komplette</span><span class="sxs-lookup"><span data-stu-id="65fdb-134">Complete</span></span>

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

### <span data-ttu-id="65fdb-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="65fdb-135">-Pre</span></span>
<span data-ttu-id="65fdb-136">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="65fdb-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="65fdb-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65fdb-137">-ResourceGroupName</span></span>
<span data-ttu-id="65fdb-138">Gibt den Namen der zu testenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="65fdb-138">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="65fdb-139">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="65fdb-139">-RollBackDeploymentName</span></span>
<span data-ttu-id="65fdb-140">Rollback zur erfolgreichen Bereitstellung mit dem angegebenen Namen in der Ressourcengruppe sollte nicht verwendet werden, wenn-RollbackToLastDeployment verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="65fdb-140">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="65fdb-141">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="65fdb-141">-RollbackToLastDeployment</span></span>
<span data-ttu-id="65fdb-142">Rollback zur letzten erfolgreichen Bereitstellung in der Ressourcengruppe sollte nicht vorhanden sein, wenn-RollBackDeploymentName verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="65fdb-142">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="65fdb-143">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="65fdb-143">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="65fdb-144">Überspringt die dynamische PowerShell-Parameterverarbeitung, die überprüft, ob der angegebene Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="65fdb-144">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="65fdb-145">Mit dieser Prüfung wird der Benutzer aufgefordert, einen Wert für die fehlenden Parameter bereitzustellen, doch die Bereitstellung von-SkipTemplateParameterPrompt ignoriert diese Eingabeaufforderung und ist sofort fehlerhaft, wenn ein Parameter gefunden wurde, der in der Vorlage nicht gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="65fdb-145">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="65fdb-146">Für nicht interaktive Skripts kann-SkipTemplateParameterPrompt bereitgestellt werden, um eine bessere Fehlermeldung bereitzustellen, falls nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="65fdb-146">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="65fdb-147">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="65fdb-147">-TemplateFile</span></span>
<span data-ttu-id="65fdb-148">Gibt den vollständigen Pfad einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="65fdb-148">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="65fdb-149">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="65fdb-149">-TemplateObject</span></span>
<span data-ttu-id="65fdb-150">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="65fdb-150">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="65fdb-151">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="65fdb-151">-TemplateParameterFile</span></span>
<span data-ttu-id="65fdb-152">Gibt den vollständigen Pfad einer JSON-Datei an, die die Namen und Werte der Vorlagenparameter enthält.</span><span class="sxs-lookup"><span data-stu-id="65fdb-152">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="65fdb-153">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="65fdb-153">-TemplateParameterObject</span></span>
<span data-ttu-id="65fdb-154">Gibt eine Hashtabelle mit Vorlagenparameter Namen und-Werten an.</span><span class="sxs-lookup"><span data-stu-id="65fdb-154">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="65fdb-155">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="65fdb-155">-TemplateParameterUri</span></span>
<span data-ttu-id="65fdb-156">Gibt den URI einer Vorlagenparameter Datei an.</span><span class="sxs-lookup"><span data-stu-id="65fdb-156">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="65fdb-157">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="65fdb-157">-TemplateUri</span></span>
<span data-ttu-id="65fdb-158">Gibt den URI einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="65fdb-158">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="65fdb-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65fdb-159">CommonParameters</span></span>
<span data-ttu-id="65fdb-160">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65fdb-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65fdb-161">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65fdb-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65fdb-162">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65fdb-162">INPUTS</span></span>

### <span data-ttu-id="65fdb-163">System. String</span><span class="sxs-lookup"><span data-stu-id="65fdb-163">System.String</span></span>

### <span data-ttu-id="65fdb-164">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="65fdb-164">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="65fdb-165">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="65fdb-165">System.Collections.Hashtable</span></span>

## <span data-ttu-id="65fdb-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65fdb-166">OUTPUTS</span></span>

### <span data-ttu-id="65fdb-167">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="65fdb-167">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="65fdb-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="65fdb-168">NOTES</span></span>

## <span data-ttu-id="65fdb-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65fdb-169">RELATED LINKS</span></span>

[<span data-ttu-id="65fdb-170">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="65fdb-170">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="65fdb-171">Neu – AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="65fdb-171">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="65fdb-172">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="65fdb-172">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="65fdb-173">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="65fdb-173">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


