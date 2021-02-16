---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 5988aed4ca0560daedc1470198e0b02975f18196
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157529"
---
# <span data-ttu-id="12cdf-101">New-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="12cdf-101">New-AzMlWebService</span></span>

## <span data-ttu-id="12cdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12cdf-102">SYNOPSIS</span></span>
<span data-ttu-id="12cdf-103">Erstellt einen neuen Webdienst.</span><span class="sxs-lookup"><span data-stu-id="12cdf-103">Creates a new web service.</span></span>

## <span data-ttu-id="12cdf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12cdf-104">SYNTAX</span></span>

### <span data-ttu-id="12cdf-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="12cdf-105">CreateFromFile</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12cdf-106">CreateFromInstance</span><span class="sxs-lookup"><span data-stu-id="12cdf-106">CreateFromInstance</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12cdf-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12cdf-107">DESCRIPTION</span></span>
<span data-ttu-id="12cdf-108">Erstellt einen Azure Machine Learning-Webdienst in einer vorhandenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="12cdf-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="12cdf-109">Wenn in der Ressourcengruppe ein Webdienst mit demselben Namen vorhanden ist, fungiert der Aufruf als Aktualisierungsvorgang, und der vorhandene Webdienst wird überschrieben.</span><span class="sxs-lookup"><span data-stu-id="12cdf-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="12cdf-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="12cdf-110">EXAMPLES</span></span>

### <span data-ttu-id="12cdf-111">Beispiel 1: Erstellen eines neuen Diensts aus einer Json-Datei-basierten Definition</span><span class="sxs-lookup"><span data-stu-id="12cdf-111">Example 1: Create a new service from a Json file based definition</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="12cdf-112">Erstellt einen neuen Azure Machine Learning-Webdienst mit dem Namen "mywebservicename" in der Gruppe "myresourcegroup" und der Region "USA, Süd-Mitte", basierend auf der Definition in der json-Datei, auf die verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="12cdf-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="12cdf-113">Beispiel 2: Erstellen eines neuen Diensts aus einer Objektinstanz</span><span class="sxs-lookup"><span data-stu-id="12cdf-113">Example 2: Create a new service from an object instance</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="12cdf-114">Sie können eine Webdienstobjektinstanz abrufen, die Sie vor der Veröffentlichung als Ressource anpassen möchten, indem Sie das cmdlet Import-AzMlWebService verwenden.</span><span class="sxs-lookup"><span data-stu-id="12cdf-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="12cdf-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12cdf-115">PARAMETERS</span></span>

### <span data-ttu-id="12cdf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12cdf-116">-DefaultProfile</span></span>
<span data-ttu-id="12cdf-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="12cdf-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12cdf-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="12cdf-118">-DefinitionFile</span></span>
<span data-ttu-id="12cdf-119">Gibt den Pfad zu der Datei an, die die Definition des JSON-Formats des Webdiensts enthält.</span><span class="sxs-lookup"><span data-stu-id="12cdf-119">Specifies the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="12cdf-120">Die neueste Spezifikation für die Webdienstdefinition finden Sie in der "swagger"-Spezifikation https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning unter.</span><span class="sxs-lookup"><span data-stu-id="12cdf-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

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

### <span data-ttu-id="12cdf-121">-Force</span><span class="sxs-lookup"><span data-stu-id="12cdf-121">-Force</span></span>
<span data-ttu-id="12cdf-122">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="12cdf-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="12cdf-123">-Location</span><span class="sxs-lookup"><span data-stu-id="12cdf-123">-Location</span></span>
<span data-ttu-id="12cdf-124">Die Region des Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="12cdf-124">The region of the web service.</span></span>
<span data-ttu-id="12cdf-125">Geben Sie eine Region für das Azure-Rechenzentrum ein, z. B. "Usa, Westen" oder "Südostasien".</span><span class="sxs-lookup"><span data-stu-id="12cdf-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="12cdf-126">Sie können einen Webdienst in einer beliebigen Region platzieren, die Ressourcen dieses Typs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12cdf-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="12cdf-127">Der Webdienst muss sich nicht in derselben Region wie Ihr Abonnement oder in derselben Region wie die Ressourcengruppe der Gruppe der Ressourcen enthalten.</span><span class="sxs-lookup"><span data-stu-id="12cdf-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="12cdf-128">Ressourcengruppen können Webdienste aus unterschiedlichen Regionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="12cdf-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="12cdf-129">Um festzustellen, welche Regionen die einzelnen Ressourcentypen unterstützen, verwenden Get-AzResourceProvider mit dem Cmdlet für den ProviderNamespace-Parameter.</span><span class="sxs-lookup"><span data-stu-id="12cdf-129">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="12cdf-130">-Name</span><span class="sxs-lookup"><span data-stu-id="12cdf-130">-Name</span></span>
<span data-ttu-id="12cdf-131">Der Name des Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="12cdf-131">The name for the web service.</span></span>
<span data-ttu-id="12cdf-132">Der Name muss in der Ressourcengruppe eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="12cdf-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="12cdf-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="12cdf-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="12cdf-134">Die Definition für den neuen Webdienst, die alle Eigenschaften enthält, aus denen der Dienst wird.</span><span class="sxs-lookup"><span data-stu-id="12cdf-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="12cdf-135">Dieser Parameter ist erforderlich und stellt eine Instanz der Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService-Klasse dar.</span><span class="sxs-lookup"><span data-stu-id="12cdf-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="12cdf-136">Die neueste Spezifikation für die Webdienstdefinition finden Sie in der "swagger"-Spezifikation https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json unter.</span><span class="sxs-lookup"><span data-stu-id="12cdf-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

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

### <span data-ttu-id="12cdf-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12cdf-137">-ResourceGroupName</span></span>
<span data-ttu-id="12cdf-138">Die Ressourcengruppe, in der der Webdienst platzieren werden soll.</span><span class="sxs-lookup"><span data-stu-id="12cdf-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="12cdf-139">Geben Sie eine Region für das Azure-Rechenzentrum ein, z. B. "Usa, Westen" oder "Südostasien".</span><span class="sxs-lookup"><span data-stu-id="12cdf-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="12cdf-140">Sie können einen Webdienst in einer beliebigen Region platzieren, die Ressourcen dieses Typs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12cdf-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="12cdf-141">Der Webdienst muss sich nicht in derselben Region wie Ihr Abonnement oder in derselben Region wie die Ressourcengruppe der Gruppe der Ressourcen enthalten.</span><span class="sxs-lookup"><span data-stu-id="12cdf-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="12cdf-142">Ressourcengruppen können Webdienste aus unterschiedlichen Regionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="12cdf-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="12cdf-143">Um festzustellen, welche Regionen die einzelnen Ressourcentypen unterstützen, verwenden Get-AzResourceProvider mit dem Cmdlet für den ProviderNamespace-Parameter.</span><span class="sxs-lookup"><span data-stu-id="12cdf-143">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="12cdf-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12cdf-144">-Confirm</span></span>
<span data-ttu-id="12cdf-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12cdf-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12cdf-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="12cdf-146">-WhatIf</span></span>
<span data-ttu-id="12cdf-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12cdf-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12cdf-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12cdf-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12cdf-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12cdf-149">CommonParameters</span></span>
<span data-ttu-id="12cdf-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12cdf-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12cdf-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12cdf-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12cdf-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="12cdf-152">INPUTS</span></span>

### <span data-ttu-id="12cdf-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="12cdf-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="12cdf-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="12cdf-154">OUTPUTS</span></span>

### <span data-ttu-id="12cdf-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="12cdf-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="12cdf-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="12cdf-156">NOTES</span></span>
<span data-ttu-id="12cdf-157">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="12cdf-157">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="12cdf-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="12cdf-158">RELATED LINKS</span></span>
