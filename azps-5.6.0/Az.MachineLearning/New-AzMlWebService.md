---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 1a48438d6cec1621361a00cefa2bfead28117b97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922896"
---
# <span data-ttu-id="1ffad-101">New-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="1ffad-101">New-AzMlWebService</span></span>

## <span data-ttu-id="1ffad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ffad-102">SYNOPSIS</span></span>
<span data-ttu-id="1ffad-103">Erstellt einen neuen Webdienst.</span><span class="sxs-lookup"><span data-stu-id="1ffad-103">Creates a new web service.</span></span>

## <span data-ttu-id="1ffad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ffad-104">SYNTAX</span></span>

### <span data-ttu-id="1ffad-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="1ffad-105">CreateFromFile</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ffad-106">CreateFromInstance</span><span class="sxs-lookup"><span data-stu-id="1ffad-106">CreateFromInstance</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ffad-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ffad-107">DESCRIPTION</span></span>
<span data-ttu-id="1ffad-108">Erstellt einen Azure Machine Learning-Webdienst in einer vorhandenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1ffad-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="1ffad-109">Wenn ein Webdienst mit demselben Namen in der Ressourcengruppe vorhanden ist, fungiert der Aufruf als Aktualisierungsvorgang, und der vorhandene Webdienst wird überschrieben.</span><span class="sxs-lookup"><span data-stu-id="1ffad-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="1ffad-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1ffad-110">EXAMPLES</span></span>

### <span data-ttu-id="1ffad-111">Beispiel 1: Erstellen eines neuen Diensts aus einer Json-dateibasierten Definition</span><span class="sxs-lookup"><span data-stu-id="1ffad-111">Example 1: Create a new service from a Json file based definition</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="1ffad-112">Erstellt einen neuen Azure Machine Learning-Webdienst mit dem Namen "mywebservicename" in der Gruppe "myresourcegroup" und der Region "South Central US", basierend auf der Definition, die in der json-Datei auf referenziert ist.</span><span class="sxs-lookup"><span data-stu-id="1ffad-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="1ffad-113">Beispiel 2: Erstellen eines neuen Diensts aus einer Objektinstanz</span><span class="sxs-lookup"><span data-stu-id="1ffad-113">Example 2: Create a new service from an object instance</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="1ffad-114">Sie können eine Webdienstobjektinstanz abrufen, die Sie vor der Veröffentlichung als Ressource anpassen möchten, indem Sie das cmdlet Import-AzMlWebService verwenden.</span><span class="sxs-lookup"><span data-stu-id="1ffad-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="1ffad-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1ffad-115">PARAMETERS</span></span>

### <span data-ttu-id="1ffad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ffad-116">-DefaultProfile</span></span>
<span data-ttu-id="1ffad-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1ffad-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ffad-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="1ffad-118">-DefinitionFile</span></span>
<span data-ttu-id="1ffad-119">Gibt den Pfad zu der Datei an, der die JSON-Formatdefinition des Webdiensts enthält.</span><span class="sxs-lookup"><span data-stu-id="1ffad-119">Specifies the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="1ffad-120">Die neueste Spezifikation für die Webdienstdefinition finden Sie in der Swaggerspezifikation unter https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="1ffad-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ffad-121">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="1ffad-121">-Force</span></span>
<span data-ttu-id="1ffad-122">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="1ffad-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1ffad-123">-Location</span><span class="sxs-lookup"><span data-stu-id="1ffad-123">-Location</span></span>
<span data-ttu-id="1ffad-124">Die Region des Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="1ffad-124">The region of the web service.</span></span>
<span data-ttu-id="1ffad-125">Geben Sie eine Azure-Rechenzentrumsregion ein, z. B. "West US" oder "Südostasien".</span><span class="sxs-lookup"><span data-stu-id="1ffad-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="1ffad-126">Sie können einen Webdienst in einer beliebigen Region platzieren, die Ressourcen dieses Typs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1ffad-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="1ffad-127">Der Webdienst muss sich nicht in derselben Region wie Ihr Azure-Abonnement oder in derselben Region wie seine Ressourcengruppe enthalten.</span><span class="sxs-lookup"><span data-stu-id="1ffad-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="1ffad-128">Ressourcengruppen können Webdienste aus verschiedenen Regionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="1ffad-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="1ffad-129">Um zu ermitteln, welche Regionen die einzelnen Ressourcentypen unterstützen, verwenden Get-AzResourceProvider mit dem Cmdlet für den ProviderNamespace-Parameter.</span><span class="sxs-lookup"><span data-stu-id="1ffad-129">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="1ffad-130">-Name</span><span class="sxs-lookup"><span data-stu-id="1ffad-130">-Name</span></span>
<span data-ttu-id="1ffad-131">Der Name für den Webdienst.</span><span class="sxs-lookup"><span data-stu-id="1ffad-131">The name for the web service.</span></span>
<span data-ttu-id="1ffad-132">Der Name muss in der Ressourcengruppe eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="1ffad-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="1ffad-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="1ffad-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="1ffad-134">Die Definition für den neuen Webdienst, die alle Eigenschaften enthält, aus denen der Dienst ist.</span><span class="sxs-lookup"><span data-stu-id="1ffad-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="1ffad-135">Dieser Parameter ist erforderlich und stellt eine Instanz der Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService-Klasse dar.</span><span class="sxs-lookup"><span data-stu-id="1ffad-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="1ffad-136">Die neueste Spezifikation für die Webdienstdefinition finden Sie in der Swaggerspezifikation unter https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="1ffad-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: CreateFromInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ffad-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ffad-137">-ResourceGroupName</span></span>
<span data-ttu-id="1ffad-138">Die Ressourcengruppe, in der der Webdienst zu platzieren ist.</span><span class="sxs-lookup"><span data-stu-id="1ffad-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="1ffad-139">Geben Sie eine Azure-Rechenzentrumsregion ein, z. B. "West US" oder "Südostasien".</span><span class="sxs-lookup"><span data-stu-id="1ffad-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="1ffad-140">Sie können einen Webdienst in einer beliebigen Region platzieren, die Ressourcen dieses Typs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1ffad-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="1ffad-141">Der Webdienst muss sich nicht in derselben Region wie Ihr Azure-Abonnement oder in derselben Region wie seine Ressourcengruppe enthalten.</span><span class="sxs-lookup"><span data-stu-id="1ffad-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="1ffad-142">Ressourcengruppen können Webdienste aus verschiedenen Regionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="1ffad-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="1ffad-143">Um zu ermitteln, welche Regionen die einzelnen Ressourcentypen unterstützen, verwenden Get-AzResourceProvider mit dem Cmdlet für den ProviderNamespace-Parameter.</span><span class="sxs-lookup"><span data-stu-id="1ffad-143">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="1ffad-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1ffad-144">-Confirm</span></span>
<span data-ttu-id="1ffad-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ffad-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ffad-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ffad-146">-WhatIf</span></span>
<span data-ttu-id="1ffad-147">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ffad-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ffad-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ffad-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ffad-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ffad-149">CommonParameters</span></span>
<span data-ttu-id="1ffad-150">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ffad-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ffad-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ffad-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ffad-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1ffad-152">INPUTS</span></span>

### <span data-ttu-id="1ffad-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="1ffad-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="1ffad-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1ffad-154">OUTPUTS</span></span>

### <span data-ttu-id="1ffad-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="1ffad-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="1ffad-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1ffad-156">NOTES</span></span>
<span data-ttu-id="1ffad-157">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="1ffad-157">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="1ffad-158">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1ffad-158">RELATED LINKS</span></span>
