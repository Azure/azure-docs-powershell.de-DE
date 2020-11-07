---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermdeployment
schema: 2.0.0
ms.openlocfilehash: 51d0405ffbedf5ad5a708fdcf9184ef49dc6ecdb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849475"
---
# <span data-ttu-id="b2e27-101">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b2e27-101">Test-AzureRmDeployment</span></span>

## <span data-ttu-id="b2e27-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2e27-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e27-103">Überprüft eine Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="b2e27-103">Validates a deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2e27-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2e27-104">SYNTAX</span></span>

### <span data-ttu-id="b2e27-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="b2e27-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2e27-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b2e27-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2e27-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b2e27-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2e27-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b2e27-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2e27-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b2e27-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2e27-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b2e27-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2e27-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b2e27-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2e27-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b2e27-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2e27-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2e27-113">DESCRIPTION</span></span>
<span data-ttu-id="b2e27-114">Das Cmdlet **Test-AzureRmDeployment** bestimmt, ob eine Bereitstellungsvorlage und deren Parameterwerte gültig sind.</span><span class="sxs-lookup"><span data-stu-id="b2e27-114">The **Test-AzureRmDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="b2e27-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2e27-115">EXAMPLES</span></span>

### <span data-ttu-id="b2e27-116">Beispiel 1: Testen der Bereitstellung mit einer benutzerdefinierten Vorlage und einer Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="b2e27-116">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\>Test-AzureRmDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="b2e27-117">Dieser Befehl testet eine Bereitstellung im aktuellen Abonnement Bereich unter Verwendung der angegebenen Vorlagendatei und Parameterdatei.</span><span class="sxs-lookup"><span data-stu-id="b2e27-117">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

## <span data-ttu-id="b2e27-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2e27-118">PARAMETERS</span></span>

### <span data-ttu-id="b2e27-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b2e27-119">-ApiVersion</span></span>
<span data-ttu-id="b2e27-120">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2e27-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b2e27-121">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b2e27-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b2e27-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e27-122">-DefaultProfile</span></span>
<span data-ttu-id="b2e27-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b2e27-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e27-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="b2e27-124">-Location</span></span>
<span data-ttu-id="b2e27-125">Der Speicherort, an dem Bereitstellungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b2e27-125">The location to store deployment data.</span></span>

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

### <span data-ttu-id="b2e27-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="b2e27-126">-Pre</span></span>
<span data-ttu-id="b2e27-127">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="b2e27-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b2e27-128">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="b2e27-128">-TemplateFile</span></span>
<span data-ttu-id="b2e27-129">Lokaler Pfad zur Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="b2e27-129">Local path to the template file.</span></span>

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

### <span data-ttu-id="b2e27-130">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="b2e27-130">-TemplateParameterFile</span></span>
<span data-ttu-id="b2e27-131">Eine Datei mit den Vorlagenparametern.</span><span class="sxs-lookup"><span data-stu-id="b2e27-131">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="b2e27-132">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="b2e27-132">-TemplateParameterObject</span></span>
<span data-ttu-id="b2e27-133">Eine Hashtabelle, die die Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="b2e27-133">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="b2e27-134">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="b2e27-134">-TemplateParameterUri</span></span>
<span data-ttu-id="b2e27-135">URI zur Vorlagenparameter Datei.</span><span class="sxs-lookup"><span data-stu-id="b2e27-135">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="b2e27-136">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="b2e27-136">-TemplateUri</span></span>
<span data-ttu-id="b2e27-137">URI zur Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="b2e27-137">Uri to the template file.</span></span>

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

### <span data-ttu-id="b2e27-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e27-138">CommonParameters</span></span>
<span data-ttu-id="b2e27-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2e27-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e27-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2e27-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e27-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2e27-141">INPUTS</span></span>

### <span data-ttu-id="b2e27-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b2e27-142">System.String</span></span>
<span data-ttu-id="b2e27-143">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b2e27-143">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode System.Collections.Hashtable</span></span>

## <span data-ttu-id="b2e27-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2e27-144">OUTPUTS</span></span>

### <span data-ttu-id="b2e27-145">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="b2e27-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="b2e27-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2e27-146">NOTES</span></span>

## <span data-ttu-id="b2e27-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2e27-147">RELATED LINKS</span></span>
