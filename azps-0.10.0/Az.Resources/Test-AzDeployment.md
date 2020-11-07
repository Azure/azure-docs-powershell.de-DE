---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-Azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Test-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Test-AzDeployment.md
ms.openlocfilehash: 77c2a712a3d44d963fd08642d1a1c88b5d8c81e1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843172"
---
# <span data-ttu-id="72165-101">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="72165-101">Test-AzDeployment</span></span>

## <span data-ttu-id="72165-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72165-102">SYNOPSIS</span></span>
<span data-ttu-id="72165-103">Überprüft eine Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="72165-103">Validates a deployment.</span></span>

## <span data-ttu-id="72165-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72165-104">SYNTAX</span></span>

### <span data-ttu-id="72165-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="72165-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzDeployment -Location <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72165-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="72165-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72165-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="72165-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72165-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="72165-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72165-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="72165-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72165-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="72165-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72165-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="72165-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72165-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="72165-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72165-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72165-113">DESCRIPTION</span></span>
<span data-ttu-id="72165-114">Das Cmdlet **Test-AzDeployment** bestimmt, ob eine Bereitstellungsvorlage und deren Parameterwerte gültig sind.</span><span class="sxs-lookup"><span data-stu-id="72165-114">The **Test-AzDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="72165-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72165-115">EXAMPLES</span></span>

### <span data-ttu-id="72165-116">Beispiel 1: Testen der Bereitstellung mit einer benutzerdefinierten Vorlage und einer Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="72165-116">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\>Test-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="72165-117">Dieser Befehl testet eine Bereitstellung im aktuellen Abonnement Bereich unter Verwendung der angegebenen Vorlagendatei und Parameterdatei.</span><span class="sxs-lookup"><span data-stu-id="72165-117">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

## <span data-ttu-id="72165-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="72165-118">PARAMETERS</span></span>

### <span data-ttu-id="72165-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="72165-119">-ApiVersion</span></span>
<span data-ttu-id="72165-120">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="72165-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="72165-121">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="72165-121">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72165-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72165-122">-DefaultProfile</span></span>
<span data-ttu-id="72165-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="72165-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72165-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="72165-124">-Location</span></span>
<span data-ttu-id="72165-125">Der Speicherort, an dem Bereitstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="72165-125">The location to store deployment data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72165-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="72165-126">-Pre</span></span>
<span data-ttu-id="72165-127">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="72165-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72165-128">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="72165-128">-TemplateFile</span></span>
<span data-ttu-id="72165-129">Lokaler Pfad zur Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="72165-129">Local path to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72165-130">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="72165-130">-TemplateParameterFile</span></span>
<span data-ttu-id="72165-131">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="72165-131">A file that has the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72165-132">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="72165-132">-TemplateParameterObject</span></span>
<span data-ttu-id="72165-133">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="72165-133">A hash table which represents the parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72165-134">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="72165-134">-TemplateParameterUri</span></span>
<span data-ttu-id="72165-135">URI zur Vorlagenparameter Datei.</span><span class="sxs-lookup"><span data-stu-id="72165-135">Uri to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72165-136">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="72165-136">-TemplateUri</span></span>
<span data-ttu-id="72165-137">URI zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="72165-137">Uri to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72165-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72165-138">CommonParameters</span></span>
<span data-ttu-id="72165-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72165-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72165-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72165-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72165-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72165-141">INPUTS</span></span>

### <span data-ttu-id="72165-142">System. String</span><span class="sxs-lookup"><span data-stu-id="72165-142">System.String</span></span>
<span data-ttu-id="72165-143">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="72165-143">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode System.Collections.Hashtable</span></span>

## <span data-ttu-id="72165-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72165-144">OUTPUTS</span></span>

### <span data-ttu-id="72165-145">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="72165-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="72165-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="72165-146">NOTES</span></span>

## <span data-ttu-id="72165-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72165-147">RELATED LINKS</span></span>
