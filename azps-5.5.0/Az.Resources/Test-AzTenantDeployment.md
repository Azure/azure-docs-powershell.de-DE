---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
ms.openlocfilehash: 5144dacb044523c2ad72d0a9c24aa43427f14f99
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145969"
---
# <span data-ttu-id="7c047-101">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="7c047-101">Test-AzTenantDeployment</span></span>

## <span data-ttu-id="7c047-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c047-102">SYNOPSIS</span></span>
<span data-ttu-id="7c047-103">Überprüft eine Bereitstellung im Mandantenbereich.</span><span class="sxs-lookup"><span data-stu-id="7c047-103">Validates a deployment at tenant scope.</span></span>

## <span data-ttu-id="7c047-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c047-104">SYNTAX</span></span>

### <span data-ttu-id="7c047-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="7c047-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c047-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7c047-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c047-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7c047-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c047-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7c047-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c047-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7c047-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c047-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7c047-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c047-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7c047-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c047-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7c047-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c047-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7c047-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c047-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7c047-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c047-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="7c047-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c047-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="7c047-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c047-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c047-117">DESCRIPTION</span></span>
<span data-ttu-id="7c047-118">Das **Cmdlet "Test-AzTenantDeployment"** bestimmt, ob eine Bereitstellungsvorlage und ihre Parameterwerte im aktuellen Mandantenbereich gültig sind.</span><span class="sxs-lookup"><span data-stu-id="7c047-118">The **Test-AzTenantDeployment** cmdlet determines whether a deployment template and its parameter values are valid at the current tenant scope.</span></span>

## <span data-ttu-id="7c047-119">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7c047-119">EXAMPLES</span></span>

### <span data-ttu-id="7c047-120">Beispiel 1: Testen der Bereitstellung mit einer benutzerdefinierten Vorlage und einer Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="7c047-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="7c047-121">Mit diesem Befehl wird eine Bereitstellung im aktuellen Mandantenbereich mithilfe der angegebenen Vorlagendatei und Parameterdatei getestet.</span><span class="sxs-lookup"><span data-stu-id="7c047-121">This command tests a deployment at the current tenant scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="7c047-122">Beispiel 2: Testen der Bereitstellung mit einem benutzerdefinierten Vorlagenobjekt und einer Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="7c047-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="7c047-123">Dieser Befehl testet eine Bereitstellung im aktuellen Mandantenbereich mithilfe einer Speicherhashtable, die aus der angegebenen Vorlagendatei erstellt wurde, und einer Parameterdatei.</span><span class="sxs-lookup"><span data-stu-id="7c047-123">This command tests a deployment at the current tenant scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="7c047-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c047-124">PARAMETERS</span></span>

### <span data-ttu-id="7c047-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c047-125">-DefaultProfile</span></span>
<span data-ttu-id="7c047-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c047-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c047-127">-Location</span><span class="sxs-lookup"><span data-stu-id="7c047-127">-Location</span></span>
<span data-ttu-id="7c047-128">Der Speicherort zum Speichern von Bereitstellungsdaten.</span><span class="sxs-lookup"><span data-stu-id="7c047-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="7c047-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="7c047-129">-Pre</span></span>
<span data-ttu-id="7c047-130">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c047-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7c047-131">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="7c047-131">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="7c047-132">Überspringt die Verarbeitung dynamischer PowerShell-Parameter, die überprüft, ob der bereitgestellte Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c047-132">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="7c047-133">Bei dieser Überprüfung müsste der Benutzer einen Wert für die fehlenden Parameter angeben. Wenn jedoch "-SkipTemplateParameterPrompt" angegeben wird, wird diese Eingabeaufforderung und der Fehler sofort ignoriert, wenn ein Parameter nicht in der Vorlage gebunden wurde.</span><span class="sxs-lookup"><span data-stu-id="7c047-133">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="7c047-134">Bei nicht interaktiven Skripts kann "-SkipTemplateParameterPrompt" bereitgestellt werden, um eine bessere Fehlermeldung für den Fall zu liefern, dass nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="7c047-134">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="7c047-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="7c047-135">-TemplateFile</span></span>
<span data-ttu-id="7c047-136">Lokaler Pfad zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="7c047-136">Local path to the template file.</span></span>

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

### <span data-ttu-id="7c047-137">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="7c047-137">-TemplateObject</span></span>
<span data-ttu-id="7c047-138">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="7c047-138">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="7c047-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="7c047-139">-TemplateParameterFile</span></span>
<span data-ttu-id="7c047-140">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="7c047-140">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="7c047-141">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="7c047-141">-TemplateParameterObject</span></span>
<span data-ttu-id="7c047-142">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="7c047-142">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="7c047-143">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="7c047-143">-TemplateParameterUri</span></span>
<span data-ttu-id="7c047-144">URI der Vorlagenparameterdatei.</span><span class="sxs-lookup"><span data-stu-id="7c047-144">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="7c047-145">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="7c047-145">-TemplateUri</span></span>
<span data-ttu-id="7c047-146">URI der Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="7c047-146">Uri to the template file.</span></span>

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

### <span data-ttu-id="7c047-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c047-147">CommonParameters</span></span>
<span data-ttu-id="7c047-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c047-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c047-149">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c047-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c047-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7c047-150">INPUTS</span></span>

### <span data-ttu-id="7c047-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7c047-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7c047-152">System.String</span><span class="sxs-lookup"><span data-stu-id="7c047-152">System.String</span></span>

## <span data-ttu-id="7c047-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7c047-153">OUTPUTS</span></span>

### <span data-ttu-id="7c047-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="7c047-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="7c047-155">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7c047-155">NOTES</span></span>

## <span data-ttu-id="7c047-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7c047-156">RELATED LINKS</span></span>
