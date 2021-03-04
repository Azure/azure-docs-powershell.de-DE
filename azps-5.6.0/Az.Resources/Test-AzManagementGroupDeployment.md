---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 6ecdf53ecd762c0c3b8ef378b1e8bc78b301a012
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935499"
---
# <span data-ttu-id="201c2-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="201c2-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="201c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="201c2-102">SYNOPSIS</span></span>
<span data-ttu-id="201c2-103">Überprüft eine Bereitstellung in einer Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="201c2-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="201c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="201c2-104">SYNTAX</span></span>

### <span data-ttu-id="201c2-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="201c2-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="201c2-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="201c2-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="201c2-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="201c2-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="201c2-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="201c2-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="201c2-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="201c2-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="201c2-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="201c2-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="201c2-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="201c2-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="201c2-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="201c2-112">ByTemplateSpecResourceIdAndParams</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterFile <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="201c2-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="201c2-113">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="201c2-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="201c2-114">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="201c2-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="201c2-115">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="201c2-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="201c2-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterUri <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="201c2-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="201c2-117">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="201c2-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="201c2-118">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="201c2-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="201c2-119">ByTemplateSpecResourceId</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="201c2-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="201c2-120">DESCRIPTION</span></span>
<span data-ttu-id="201c2-121">Das **Cmdlet Test-AzManagementGroupDeployment** bestimmt, ob eine Bereitstellungsvorlage und ihre Parameterwerte in einer Verwaltungsgruppe gültig sind.</span><span class="sxs-lookup"><span data-stu-id="201c2-121">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="201c2-122">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="201c2-122">EXAMPLES</span></span>

### <span data-ttu-id="201c2-123">Beispiel 1: Testen der Bereitstellung mit einer benutzerdefinierten Vorlage und Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="201c2-123">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="201c2-124">Mit diesem Befehl wird eine Bereitstellung in der Verwaltungsgruppe "myMG" mithilfe der angegebenen Vorlagendatei und Parameterdatei getestet.</span><span class="sxs-lookup"><span data-stu-id="201c2-124">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="201c2-125">Beispiel 2: Testen der Bereitstellung mit einem benutzerdefinierten Vorlagenobjekt und einer Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="201c2-125">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="201c2-126">Mit diesem Befehl wird eine Bereitstellung in der Verwaltungsgruppe "myMG" mithilfe einer Speicherhashtable getestet, die aus der angegebenen Vorlagendatei und einer Parameterdatei erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="201c2-126">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="201c2-127">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="201c2-127">PARAMETERS</span></span>

### <span data-ttu-id="201c2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="201c2-128">-DefaultProfile</span></span>
<span data-ttu-id="201c2-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="201c2-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="201c2-130">-Location</span><span class="sxs-lookup"><span data-stu-id="201c2-130">-Location</span></span>
<span data-ttu-id="201c2-131">Der Speicherort zum Speichern von Bereitstellungsdaten.</span><span class="sxs-lookup"><span data-stu-id="201c2-131">The location to store deployment data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="201c2-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="201c2-132">-ManagementGroupId</span></span>
<span data-ttu-id="201c2-133">Die Id der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="201c2-133">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="201c2-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="201c2-134">-Pre</span></span>
<span data-ttu-id="201c2-135">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="201c2-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="201c2-136">-QueryString</span><span class="sxs-lookup"><span data-stu-id="201c2-136">-QueryString</span></span>
<span data-ttu-id="201c2-137">Die Abfragezeichenfolge (z. B. ein SAS-Token), die mit dem Parameter TemplateUri verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="201c2-137">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="201c2-138">Würde bei verknüpften Vorlagen verwendet</span><span class="sxs-lookup"><span data-stu-id="201c2-138">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="201c2-139">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="201c2-139">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="201c2-140">Überspringt die PowerShell-Dynamische Parameterverarbeitung, die überprüft, ob der bereitgestellte Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="201c2-140">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="201c2-141">Bei dieser Überprüfung wird der Benutzer aufgefordert, einen Wert für die fehlenden Parameter zur Verfügung zu stellen. Wenn jedoch -SkipTemplateParameterPrompt angegeben wird, werden diese Eingabeaufforderung und der Fehler sofort ignoriert, wenn festgestellt wurde, dass ein Parameter nicht in der Vorlage gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="201c2-141">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="201c2-142">Für nicht interaktive Skripts kann -SkipTemplateParameterPrompt bereitgestellt werden, um eine bessere Fehlermeldung für den Fall zu liefern, dass nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="201c2-142">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="201c2-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="201c2-143">-TemplateFile</span></span>
<span data-ttu-id="201c2-144">Lokaler Pfad zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="201c2-144">Local path to the template file.</span></span> <span data-ttu-id="201c2-145">Unterstützter Vorlagendateityp: json und bicep.</span><span class="sxs-lookup"><span data-stu-id="201c2-145">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="201c2-146">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="201c2-146">-TemplateObject</span></span>
<span data-ttu-id="201c2-147">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="201c2-147">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="201c2-148">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="201c2-148">-TemplateParameterFile</span></span>
<span data-ttu-id="201c2-149">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="201c2-149">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="201c2-150">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="201c2-150">-TemplateParameterObject</span></span>
<span data-ttu-id="201c2-151">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="201c2-151">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="201c2-152">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="201c2-152">-TemplateParameterUri</span></span>
<span data-ttu-id="201c2-153">URI für die Vorlagenparameterdatei.</span><span class="sxs-lookup"><span data-stu-id="201c2-153">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="201c2-154">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="201c2-154">-TemplateSpecId</span></span>
<span data-ttu-id="201c2-155">Ressourcen-ID der zu bereitstellende TemplateSpec.</span><span class="sxs-lookup"><span data-stu-id="201c2-155">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="201c2-156">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="201c2-156">-TemplateUri</span></span>
<span data-ttu-id="201c2-157">URI für die Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="201c2-157">Uri to the template file.</span></span>

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

### <span data-ttu-id="201c2-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="201c2-158">CommonParameters</span></span>
<span data-ttu-id="201c2-159">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="201c2-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="201c2-160">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="201c2-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="201c2-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="201c2-161">INPUTS</span></span>

### <span data-ttu-id="201c2-162">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="201c2-162">System.Collections.Hashtable</span></span>

### <span data-ttu-id="201c2-163">System.String</span><span class="sxs-lookup"><span data-stu-id="201c2-163">System.String</span></span>

## <span data-ttu-id="201c2-164">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="201c2-164">OUTPUTS</span></span>

### <span data-ttu-id="201c2-165">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="201c2-165">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="201c2-166">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="201c2-166">NOTES</span></span>

## <span data-ttu-id="201c2-167">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="201c2-167">RELATED LINKS</span></span>
