---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 4f4aa6972c8152e3340a9cc938df9cfa8b585dbd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367337"
---
# <span data-ttu-id="2f0ac-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2f0ac-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="2f0ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f0ac-102">SYNOPSIS</span></span>
<span data-ttu-id="2f0ac-103">Überprüft eine Bereitstellung in einer Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2f0ac-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="2f0ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f0ac-104">SYNTAX</span></span>

### <span data-ttu-id="2f0ac-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="2f0ac-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f0ac-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2f0ac-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f0ac-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2f0ac-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f0ac-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2f0ac-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f0ac-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2f0ac-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f0ac-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2f0ac-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f0ac-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2f0ac-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f0ac-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2f0ac-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f0ac-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2f0ac-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f0ac-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2f0ac-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f0ac-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2f0ac-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f0ac-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2f0ac-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f0ac-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f0ac-117">DESCRIPTION</span></span>
<span data-ttu-id="2f0ac-118">Das **Cmdlet "Test-AzManagementGroupDeployment"** bestimmt, ob eine Bereitstellungsvorlage und deren Parameterwerte in einer Verwaltungsgruppe gültig sind.</span><span class="sxs-lookup"><span data-stu-id="2f0ac-118">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="2f0ac-119">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2f0ac-119">EXAMPLES</span></span>

### <span data-ttu-id="2f0ac-120">Beispiel 1: Testen der Bereitstellung mit einer benutzerdefinierten Vorlage und einer Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="2f0ac-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="2f0ac-121">Mit diesem Befehl wird eine Bereitstellung in der Verwaltungsgruppe "myMG" mithilfe der angegebenen Vorlagendatei und Parameterdatei getestet.</span><span class="sxs-lookup"><span data-stu-id="2f0ac-121">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="2f0ac-122">Beispiel 2: Testen der Bereitstellung mit einem benutzerdefinierten Vorlagenobjekt und einer Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="2f0ac-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="2f0ac-123">Mit diesem Befehl wird eine Bereitstellung in der Verwaltungsgruppe "myMG" mithilfe einer Speicherhashtable getestet, die aus der angegebenen Vorlagendatei und einer Parameterdatei erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2f0ac-123">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="2f0ac-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f0ac-124">PARAMETERS</span></span>

### <span data-ttu-id="2f0ac-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f0ac-125">-DefaultProfile</span></span>
<span data-ttu-id="2f0ac-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f0ac-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f0ac-127">-Location</span><span class="sxs-lookup"><span data-stu-id="2f0ac-127">-Location</span></span>
<span data-ttu-id="2f0ac-128">Der Speicherort zum Speichern von Bereitstellungsdaten.</span><span class="sxs-lookup"><span data-stu-id="2f0ac-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="2f0ac-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="2f0ac-129">-ManagementGroupId</span></span>
<span data-ttu-id="2f0ac-130">Die ID der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2f0ac-130">The management group id.</span></span>

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

### <span data-ttu-id="2f0ac-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="2f0ac-131">-Pre</span></span>
<span data-ttu-id="2f0ac-132">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f0ac-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2f0ac-133">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="2f0ac-133">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="2f0ac-134">Überspringt die Verarbeitung dynamischer PowerShell-Parameter, die überprüft, ob der bereitgestellte Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f0ac-134">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="2f0ac-135">Bei dieser Überprüfung müsste der Benutzer einen Wert für die fehlenden Parameter angeben. Wenn jedoch "-SkipTemplateParameterPrompt" angegeben wird, wird diese Eingabeaufforderung und der Fehler sofort ignoriert, wenn ein Parameter nicht in der Vorlage gebunden wurde.</span><span class="sxs-lookup"><span data-stu-id="2f0ac-135">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="2f0ac-136">Bei nicht interaktiven Skripts kann "-SkipTemplateParameterPrompt" bereitgestellt werden, um eine bessere Fehlermeldung für den Fall zu liefern, dass nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="2f0ac-136">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="2f0ac-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="2f0ac-137">-TemplateFile</span></span>
<span data-ttu-id="2f0ac-138">Lokaler Pfad zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="2f0ac-138">Local path to the template file.</span></span>

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

### <span data-ttu-id="2f0ac-139">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="2f0ac-139">-TemplateObject</span></span>
<span data-ttu-id="2f0ac-140">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="2f0ac-140">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="2f0ac-141">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="2f0ac-141">-TemplateParameterFile</span></span>
<span data-ttu-id="2f0ac-142">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="2f0ac-142">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="2f0ac-143">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="2f0ac-143">-TemplateParameterObject</span></span>
<span data-ttu-id="2f0ac-144">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="2f0ac-144">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="2f0ac-145">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="2f0ac-145">-TemplateParameterUri</span></span>
<span data-ttu-id="2f0ac-146">URI der Vorlagenparameterdatei.</span><span class="sxs-lookup"><span data-stu-id="2f0ac-146">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="2f0ac-147">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="2f0ac-147">-TemplateUri</span></span>
<span data-ttu-id="2f0ac-148">URI der Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="2f0ac-148">Uri to the template file.</span></span>

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

### <span data-ttu-id="2f0ac-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f0ac-149">CommonParameters</span></span>
<span data-ttu-id="2f0ac-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f0ac-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f0ac-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f0ac-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f0ac-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2f0ac-152">INPUTS</span></span>

### <span data-ttu-id="2f0ac-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2f0ac-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2f0ac-154">System.String</span><span class="sxs-lookup"><span data-stu-id="2f0ac-154">System.String</span></span>

## <span data-ttu-id="2f0ac-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2f0ac-155">OUTPUTS</span></span>

### <span data-ttu-id="2f0ac-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="2f0ac-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="2f0ac-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2f0ac-157">NOTES</span></span>

## <span data-ttu-id="2f0ac-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2f0ac-158">RELATED LINKS</span></span>
