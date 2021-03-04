---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/test-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
ms.openlocfilehash: 5a7bb411c5b2881361c1f9dfe7e675450f76e318
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923936"
---
# <span data-ttu-id="f3713-101">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f3713-101">Test-AzDeployment</span></span>

## <span data-ttu-id="f3713-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3713-102">SYNOPSIS</span></span>
<span data-ttu-id="f3713-103">Überprüft eine Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="f3713-103">Validates a deployment.</span></span>

## <span data-ttu-id="f3713-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3713-104">SYNTAX</span></span>

### <span data-ttu-id="f3713-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="f3713-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3713-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f3713-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3713-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f3713-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3713-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f3713-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3713-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f3713-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3713-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f3713-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3713-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f3713-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3713-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="f3713-112">ByTemplateSpecResourceIdAndParams</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3713-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f3713-113">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3713-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f3713-114">ByTemplateFileAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3713-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f3713-115">ByTemplateUriAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3713-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="f3713-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3713-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f3713-117">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3713-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f3713-118">ByTemplateUriWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3713-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="f3713-119">ByTemplateSpecResourceId</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3713-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3713-120">DESCRIPTION</span></span>
<span data-ttu-id="f3713-121">Das **Cmdlet Test-AzDeployment** bestimmt, ob eine Bereitstellungsvorlage und ihre Parameterwerte gültig sind.</span><span class="sxs-lookup"><span data-stu-id="f3713-121">The **Test-AzDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="f3713-122">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f3713-122">EXAMPLES</span></span>

### <span data-ttu-id="f3713-123">Beispiel 1: Testen der Bereitstellung mit einer benutzerdefinierten Vorlage und Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="f3713-123">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="f3713-124">Mit diesem Befehl wird eine Bereitstellung im aktuellen Abonnementbereich mithilfe der angegebenen Vorlagendatei und Parameterdatei getestet.</span><span class="sxs-lookup"><span data-stu-id="f3713-124">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="f3713-125">Beispiel 2: Testen der Bereitstellung mit einem benutzerdefinierten Vorlagenobjekt und einer Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="f3713-125">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="f3713-126">Mit diesem Befehl wird eine Bereitstellung im aktuellen Abonnementbereich mithilfe einer In-Memory-Hashtable getestet, die aus der angegebenen Vorlagendatei und einer Parameterdatei erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f3713-126">This command tests a deployment at the current subscription scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="f3713-127">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f3713-127">PARAMETERS</span></span>

### <span data-ttu-id="f3713-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3713-128">-DefaultProfile</span></span>
<span data-ttu-id="f3713-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3713-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3713-130">-Location</span><span class="sxs-lookup"><span data-stu-id="f3713-130">-Location</span></span>
<span data-ttu-id="f3713-131">Der Speicherort zum Speichern von Bereitstellungsdaten.</span><span class="sxs-lookup"><span data-stu-id="f3713-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="f3713-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="f3713-132">-Pre</span></span>
<span data-ttu-id="f3713-133">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3713-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f3713-134">-QueryString</span><span class="sxs-lookup"><span data-stu-id="f3713-134">-QueryString</span></span>
<span data-ttu-id="f3713-135">Die Abfragezeichenfolge (z. B. ein SAS-Token), die mit dem Parameter TemplateUri verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3713-135">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="f3713-136">Würde bei verknüpften Vorlagen verwendet</span><span class="sxs-lookup"><span data-stu-id="f3713-136">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="f3713-137">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="f3713-137">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="f3713-138">Überspringt die PowerShell-Dynamische Parameterverarbeitung, die überprüft, ob der bereitgestellte Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3713-138">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="f3713-139">Bei dieser Überprüfung wird der Benutzer aufgefordert, einen Wert für die fehlenden Parameter zur Verfügung zu stellen. Wenn jedoch -SkipTemplateParameterPrompt angegeben wird, werden diese Eingabeaufforderung und der Fehler sofort ignoriert, wenn festgestellt wurde, dass ein Parameter nicht in der Vorlage gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="f3713-139">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="f3713-140">Für nicht interaktive Skripts kann -SkipTemplateParameterPrompt bereitgestellt werden, um eine bessere Fehlermeldung für den Fall zu liefern, dass nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="f3713-140">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="f3713-141">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f3713-141">-TemplateFile</span></span>
<span data-ttu-id="f3713-142">Lokaler Pfad zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="f3713-142">Local path to the template file.</span></span> <span data-ttu-id="f3713-143">Unterstützter Vorlagendateityp: json und bicep.</span><span class="sxs-lookup"><span data-stu-id="f3713-143">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="f3713-144">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="f3713-144">-TemplateObject</span></span>
<span data-ttu-id="f3713-145">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="f3713-145">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="f3713-146">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="f3713-146">-TemplateParameterFile</span></span>
<span data-ttu-id="f3713-147">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="f3713-147">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="f3713-148">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="f3713-148">-TemplateParameterObject</span></span>
<span data-ttu-id="f3713-149">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="f3713-149">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="f3713-150">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="f3713-150">-TemplateParameterUri</span></span>
<span data-ttu-id="f3713-151">URI für die Vorlagenparameterdatei.</span><span class="sxs-lookup"><span data-stu-id="f3713-151">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="f3713-152">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="f3713-152">-TemplateSpecId</span></span>
<span data-ttu-id="f3713-153">Ressourcen-ID der zu bereitstellende TemplateSpec.</span><span class="sxs-lookup"><span data-stu-id="f3713-153">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="f3713-154">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="f3713-154">-TemplateUri</span></span>
<span data-ttu-id="f3713-155">URI für die Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="f3713-155">Uri to the template file.</span></span>

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

### <span data-ttu-id="f3713-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3713-156">CommonParameters</span></span>
<span data-ttu-id="f3713-157">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3713-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3713-158">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3713-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3713-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f3713-159">INPUTS</span></span>

### <span data-ttu-id="f3713-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f3713-160">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f3713-161">System.String</span><span class="sxs-lookup"><span data-stu-id="f3713-161">System.String</span></span>

## <span data-ttu-id="f3713-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f3713-162">OUTPUTS</span></span>

### <span data-ttu-id="f3713-163">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="f3713-163">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="f3713-164">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f3713-164">NOTES</span></span>

## <span data-ttu-id="f3713-165">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f3713-165">RELATED LINKS</span></span>
