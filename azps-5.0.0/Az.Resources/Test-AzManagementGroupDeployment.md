---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 4f4aa6972c8152e3340a9cc938df9cfa8b585dbd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179363"
---
# <span data-ttu-id="ca01a-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ca01a-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="ca01a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ca01a-102">SYNOPSIS</span></span>
<span data-ttu-id="ca01a-103">Überprüft eine Bereitstellung in einer Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="ca01a-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="ca01a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca01a-104">SYNTAX</span></span>

### <span data-ttu-id="ca01a-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="ca01a-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca01a-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ca01a-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca01a-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ca01a-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca01a-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ca01a-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca01a-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ca01a-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ca01a-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ca01a-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ca01a-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ca01a-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ca01a-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ca01a-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ca01a-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ca01a-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ca01a-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ca01a-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ca01a-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="ca01a-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca01a-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="ca01a-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca01a-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca01a-117">DESCRIPTION</span></span>
<span data-ttu-id="ca01a-118">Das Cmdlet **Test-AzManagementGroupDeployment** bestimmt, ob eine Bereitstellungsvorlage und deren Parameterwerte in einer Verwaltungsgruppe gültig sind.</span><span class="sxs-lookup"><span data-stu-id="ca01a-118">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="ca01a-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ca01a-119">EXAMPLES</span></span>

### <span data-ttu-id="ca01a-120">Beispiel 1: Testen der Bereitstellung mit einer benutzerdefinierten Vorlage und einer Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="ca01a-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="ca01a-121">Dieser Befehl testet eine Bereitstellung in der Verwaltungsgruppe "myMG" unter Verwendung der angegebenen Vorlagendatei und Parameterdatei.</span><span class="sxs-lookup"><span data-stu-id="ca01a-121">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="ca01a-122">Beispiel 2: Testen der Bereitstellung mit einem benutzerdefinierten Vorlagenobjekt und einer Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="ca01a-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="ca01a-123">Dieser Befehl testet eine Bereitstellung in der Verwaltungsgruppe "myMG" mithilfe der Arbeitsspeicher-Hashtable, die aus der angegebenen Vorlagendatei und einer Parameterdatei erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ca01a-123">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="ca01a-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca01a-124">PARAMETERS</span></span>

### <span data-ttu-id="ca01a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca01a-125">-DefaultProfile</span></span>
<span data-ttu-id="ca01a-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ca01a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca01a-127">-Standort</span><span class="sxs-lookup"><span data-stu-id="ca01a-127">-Location</span></span>
<span data-ttu-id="ca01a-128">Der Speicherort, an dem Bereitstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="ca01a-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="ca01a-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ca01a-129">-ManagementGroupId</span></span>
<span data-ttu-id="ca01a-130">Die Verwaltungsgruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="ca01a-130">The management group id.</span></span>

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

### <span data-ttu-id="ca01a-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="ca01a-131">-Pre</span></span>
<span data-ttu-id="ca01a-132">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="ca01a-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ca01a-133">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="ca01a-133">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="ca01a-134">Überspringt die dynamische PowerShell-Parameterverarbeitung, die überprüft, ob der angegebene Vorlagenparameter alle erforderlichen Parameter enthält, die von der Vorlage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca01a-134">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="ca01a-135">Mit dieser Prüfung wird der Benutzer aufgefordert, einen Wert für die fehlenden Parameter bereitzustellen, doch die Bereitstellung von-SkipTemplateParameterPrompt ignoriert diese Eingabeaufforderung und ist sofort fehlerhaft, wenn ein Parameter gefunden wurde, der in der Vorlage nicht gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca01a-135">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="ca01a-136">Für nicht interaktive Skripts kann-SkipTemplateParameterPrompt bereitgestellt werden, um eine bessere Fehlermeldung bereitzustellen, falls nicht alle erforderlichen Parameter erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="ca01a-136">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="ca01a-137">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="ca01a-137">-TemplateFile</span></span>
<span data-ttu-id="ca01a-138">Lokaler Pfad zur Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="ca01a-138">Local path to the template file.</span></span>

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

### <span data-ttu-id="ca01a-139">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="ca01a-139">-TemplateObject</span></span>
<span data-ttu-id="ca01a-140">Eine Hashtabelle, die die Vorlage darstellt.</span><span class="sxs-lookup"><span data-stu-id="ca01a-140">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="ca01a-141">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="ca01a-141">-TemplateParameterFile</span></span>
<span data-ttu-id="ca01a-142">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="ca01a-142">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="ca01a-143">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="ca01a-143">-TemplateParameterObject</span></span>
<span data-ttu-id="ca01a-144">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="ca01a-144">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="ca01a-145">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="ca01a-145">-TemplateParameterUri</span></span>
<span data-ttu-id="ca01a-146">URI zur Vorlagenparameter Datei.</span><span class="sxs-lookup"><span data-stu-id="ca01a-146">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="ca01a-147">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="ca01a-147">-TemplateUri</span></span>
<span data-ttu-id="ca01a-148">URI zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="ca01a-148">Uri to the template file.</span></span>

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

### <span data-ttu-id="ca01a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca01a-149">CommonParameters</span></span>
<span data-ttu-id="ca01a-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca01a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca01a-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca01a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca01a-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ca01a-152">INPUTS</span></span>

### <span data-ttu-id="ca01a-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ca01a-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ca01a-154">System. String</span><span class="sxs-lookup"><span data-stu-id="ca01a-154">System.String</span></span>

## <span data-ttu-id="ca01a-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ca01a-155">OUTPUTS</span></span>

### <span data-ttu-id="ca01a-156">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="ca01a-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="ca01a-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="ca01a-157">NOTES</span></span>

## <span data-ttu-id="ca01a-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ca01a-158">RELATED LINKS</span></span>
