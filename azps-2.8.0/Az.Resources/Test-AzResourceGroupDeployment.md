---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 01d7aa0cb0b363dac8e19e5b38796c43523d6296
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824899"
---
# <span data-ttu-id="1893c-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1893c-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="1893c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1893c-102">SYNOPSIS</span></span>
<span data-ttu-id="1893c-103">Überprüft eine Ressourcengruppen Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="1893c-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="1893c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1893c-104">SYNTAX</span></span>

### <span data-ttu-id="1893c-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="1893c-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1893c-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1893c-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1893c-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1893c-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1893c-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1893c-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1893c-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1893c-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1893c-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1893c-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1893c-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1893c-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1893c-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1893c-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1893c-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1893c-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1893c-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1893c-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1893c-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="1893c-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1893c-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="1893c-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1893c-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1893c-117">DESCRIPTION</span></span>
<span data-ttu-id="1893c-118">Das Cmdlet **Test-AzResourceGroupDeployment** bestimmt, ob eine Azure Resource Group-Bereitstellungsvorlage und deren Parameterwerte gültig sind.</span><span class="sxs-lookup"><span data-stu-id="1893c-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="1893c-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1893c-119">EXAMPLES</span></span>

### <span data-ttu-id="1893c-120">Beispiel 1: Testen der Bereitstellung mit einem benutzerdefinierten Vorlagenobjekt und einer Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="1893c-120">Example 1: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="1893c-121">Dieser Befehl testet eine Bereitstellung in der angegebenen Ressourcengruppe mithilfe der Arbeitsspeicher-Hashtable, die aus der angegebenen Vorlagendatei und einer Parameterdatei erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1893c-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="1893c-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="1893c-122">PARAMETERS</span></span>

### <span data-ttu-id="1893c-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1893c-123">-ApiVersion</span></span>
<span data-ttu-id="1893c-124">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="1893c-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="1893c-125">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="1893c-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="1893c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1893c-126">-DefaultProfile</span></span>
<span data-ttu-id="1893c-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1893c-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1893c-128">-Modus</span><span class="sxs-lookup"><span data-stu-id="1893c-128">-Mode</span></span>
<span data-ttu-id="1893c-129">Gibt den Bereitstellungsmodus an.</span><span class="sxs-lookup"><span data-stu-id="1893c-129">Specifies the deployment mode.</span></span>
<span data-ttu-id="1893c-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1893c-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1893c-131">Inkrementelle</span><span class="sxs-lookup"><span data-stu-id="1893c-131">Incremental</span></span>
- <span data-ttu-id="1893c-132">Komplette</span><span class="sxs-lookup"><span data-stu-id="1893c-132">Complete</span></span>

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

### <span data-ttu-id="1893c-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="1893c-133">-Pre</span></span>
<span data-ttu-id="1893c-134">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="1893c-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1893c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1893c-135">-ResourceGroupName</span></span>
<span data-ttu-id="1893c-136">Gibt den Namen der zu testenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1893c-136">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="1893c-137">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="1893c-137">-RollBackDeploymentName</span></span>
<span data-ttu-id="1893c-138">Rollback zur erfolgreichen Bereitstellung mit dem angegebenen Namen in der Ressourcengruppe sollte nicht verwendet werden, wenn-RollbackToLastDeployment verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1893c-138">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="1893c-139">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="1893c-139">-RollbackToLastDeployment</span></span>
<span data-ttu-id="1893c-140">Rollback zur letzten erfolgreichen Bereitstellung in der Ressourcengruppe sollte nicht vorhanden sein, wenn-RollBackDeploymentName verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1893c-140">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="1893c-141">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="1893c-141">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="1893c-142">Überspringt die dynamische PowerShell-Parameterverarbeitung, die überprüft, ob der angegebene Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1893c-142">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="1893c-143">Mit dieser Prüfung wird der Benutzer aufgefordert, einen Wert für die fehlenden Parameter bereitzustellen, doch die Bereitstellung von-SkipTemplateParameterPrompt ignoriert diese Eingabeaufforderung und ist sofort fehlerhaft, wenn ein Parameter gefunden wurde, der in der Vorlage nicht gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="1893c-143">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="1893c-144">Für nicht interaktive Skripts kann-SkipTemplateParameterPrompt bereitgestellt werden, um eine bessere Fehlermeldung bereitzustellen, falls nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="1893c-144">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="1893c-145">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="1893c-145">-TemplateFile</span></span>
<span data-ttu-id="1893c-146">Gibt den vollständigen Pfad einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="1893c-146">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="1893c-147">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="1893c-147">-TemplateObject</span></span>
<span data-ttu-id="1893c-148">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="1893c-148">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="1893c-149">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="1893c-149">-TemplateParameterFile</span></span>
<span data-ttu-id="1893c-150">Gibt den vollständigen Pfad einer JSON-Datei an, die die Namen und Werte der Vorlagenparameter enthält.</span><span class="sxs-lookup"><span data-stu-id="1893c-150">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="1893c-151">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="1893c-151">-TemplateParameterObject</span></span>
<span data-ttu-id="1893c-152">Gibt eine Hashtabelle mit Vorlagenparameter Namen und-Werten an.</span><span class="sxs-lookup"><span data-stu-id="1893c-152">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="1893c-153">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="1893c-153">-TemplateParameterUri</span></span>
<span data-ttu-id="1893c-154">Gibt den URI einer Vorlagenparameter Datei an.</span><span class="sxs-lookup"><span data-stu-id="1893c-154">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="1893c-155">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="1893c-155">-TemplateUri</span></span>
<span data-ttu-id="1893c-156">Gibt den URI einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="1893c-156">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="1893c-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1893c-157">CommonParameters</span></span>
<span data-ttu-id="1893c-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1893c-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1893c-159">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1893c-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1893c-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1893c-160">INPUTS</span></span>

### <span data-ttu-id="1893c-161">System. String</span><span class="sxs-lookup"><span data-stu-id="1893c-161">System.String</span></span>

### <span data-ttu-id="1893c-162">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="1893c-162">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="1893c-163">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1893c-163">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1893c-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1893c-164">OUTPUTS</span></span>

### <span data-ttu-id="1893c-165">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="1893c-165">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="1893c-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="1893c-166">NOTES</span></span>

## <span data-ttu-id="1893c-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1893c-167">RELATED LINKS</span></span>

[<span data-ttu-id="1893c-168">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1893c-168">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="1893c-169">Neu – AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1893c-169">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="1893c-170">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1893c-170">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="1893c-171">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1893c-171">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


