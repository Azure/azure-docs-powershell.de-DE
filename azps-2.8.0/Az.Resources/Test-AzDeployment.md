---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
ms.openlocfilehash: 182cf4d60cf2b81f5a465f9ffad5d862b09e3787
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824900"
---
# <span data-ttu-id="b706e-101">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="b706e-101">Test-AzDeployment</span></span>

## <span data-ttu-id="b706e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b706e-102">SYNOPSIS</span></span>
<span data-ttu-id="b706e-103">Überprüft eine Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="b706e-103">Validates a deployment.</span></span>

## <span data-ttu-id="b706e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b706e-104">SYNTAX</span></span>

### <span data-ttu-id="b706e-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="b706e-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b706e-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b706e-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b706e-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b706e-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b706e-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b706e-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b706e-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b706e-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b706e-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b706e-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b706e-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b706e-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b706e-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b706e-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b706e-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b706e-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b706e-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b706e-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b706e-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b706e-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b706e-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b706e-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b706e-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b706e-117">DESCRIPTION</span></span>
<span data-ttu-id="b706e-118">Das Cmdlet **Test-AzDeployment** bestimmt, ob eine Bereitstellungsvorlage und deren Parameterwerte gültig sind.</span><span class="sxs-lookup"><span data-stu-id="b706e-118">The **Test-AzDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="b706e-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b706e-119">EXAMPLES</span></span>

### <span data-ttu-id="b706e-120">Beispiel 1: Testen der Bereitstellung mit einer benutzerdefinierten Vorlage und einer Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="b706e-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="b706e-121">Dieser Befehl testet eine Bereitstellung im aktuellen Abonnement Bereich unter Verwendung der angegebenen Vorlagendatei und Parameterdatei.</span><span class="sxs-lookup"><span data-stu-id="b706e-121">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="b706e-122">Beispiel 2: Testen der Bereitstellung mit einem benutzerdefinierten Vorlagenobjekt und einer Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="b706e-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="b706e-123">Dieser Befehl testet eine Bereitstellung im aktuellen Abonnement Bereich mithilfe der in Arbeitsspeicher erstellten Hashtable, die aus der angegebenen Vorlagendatei und einer Parameterdatei erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b706e-123">This command tests a deployment at the current subscription scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="b706e-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="b706e-124">PARAMETERS</span></span>

### <span data-ttu-id="b706e-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b706e-125">-ApiVersion</span></span>
<span data-ttu-id="b706e-126">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b706e-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b706e-127">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b706e-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b706e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b706e-128">-DefaultProfile</span></span>
<span data-ttu-id="b706e-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b706e-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b706e-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="b706e-130">-Location</span></span>
<span data-ttu-id="b706e-131">Der Speicherort, an dem Bereitstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b706e-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="b706e-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="b706e-132">-Pre</span></span>
<span data-ttu-id="b706e-133">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="b706e-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b706e-134">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="b706e-134">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="b706e-135">Überspringt die dynamische PowerShell-Parameterverarbeitung, die überprüft, ob der angegebene Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b706e-135">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="b706e-136">Mit dieser Prüfung wird der Benutzer aufgefordert, einen Wert für die fehlenden Parameter bereitzustellen, doch die Bereitstellung von-SkipTemplateParameterPrompt ignoriert diese Eingabeaufforderung und ist sofort fehlerhaft, wenn ein Parameter gefunden wurde, der in der Vorlage nicht gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="b706e-136">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="b706e-137">Für nicht interaktive Skripts kann-SkipTemplateParameterPrompt bereitgestellt werden, um eine bessere Fehlermeldung bereitzustellen, falls nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="b706e-137">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="b706e-138">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="b706e-138">-TemplateFile</span></span>
<span data-ttu-id="b706e-139">Lokaler Pfad zur Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="b706e-139">Local path to the template file.</span></span>

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

### <span data-ttu-id="b706e-140">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="b706e-140">-TemplateObject</span></span>
<span data-ttu-id="b706e-141">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="b706e-141">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="b706e-142">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="b706e-142">-TemplateParameterFile</span></span>
<span data-ttu-id="b706e-143">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="b706e-143">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="b706e-144">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="b706e-144">-TemplateParameterObject</span></span>
<span data-ttu-id="b706e-145">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="b706e-145">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="b706e-146">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="b706e-146">-TemplateParameterUri</span></span>
<span data-ttu-id="b706e-147">URI zur Vorlagenparameter Datei.</span><span class="sxs-lookup"><span data-stu-id="b706e-147">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="b706e-148">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="b706e-148">-TemplateUri</span></span>
<span data-ttu-id="b706e-149">URI zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="b706e-149">Uri to the template file.</span></span>

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

### <span data-ttu-id="b706e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b706e-150">CommonParameters</span></span>
<span data-ttu-id="b706e-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b706e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b706e-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b706e-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b706e-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b706e-153">INPUTS</span></span>

### <span data-ttu-id="b706e-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b706e-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b706e-155">System. String</span><span class="sxs-lookup"><span data-stu-id="b706e-155">System.String</span></span>

## <span data-ttu-id="b706e-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b706e-156">OUTPUTS</span></span>

### <span data-ttu-id="b706e-157">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="b706e-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="b706e-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="b706e-158">NOTES</span></span>

## <span data-ttu-id="b706e-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b706e-159">RELATED LINKS</span></span>
