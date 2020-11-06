---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/new-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
ms.openlocfilehash: df6392e339063ccb2cc60411b77f73936071ab3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505489"
---
# <span data-ttu-id="f9f6c-101">New-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="f9f6c-101">New-AzureRmMlWebService</span></span>

## <span data-ttu-id="f9f6c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f9f6c-102">SYNOPSIS</span></span>
<span data-ttu-id="f9f6c-103">Erstellt einen neuen Webdienst.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-103">Creates a new web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9f6c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9f6c-104">SYNTAX</span></span>

### <span data-ttu-id="f9f6c-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="f9f6c-105">CreateFromFile</span></span>
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9f6c-106">CreateFromInstance</span><span class="sxs-lookup"><span data-stu-id="f9f6c-106">CreateFromInstance</span></span>
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9f6c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9f6c-107">DESCRIPTION</span></span>
<span data-ttu-id="f9f6c-108">Erstellt einen Azure Machine Learning-Webdienst in einer vorhandenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="f9f6c-109">Wenn ein Webdienst mit demselben Namen in der Ressourcengruppe vorhanden ist, fungiert der Anruf als Aktualisierungsvorgang, und der vorhandene Webdienst wird überschrieben.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="f9f6c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9f6c-110">EXAMPLES</span></span>

### <span data-ttu-id="f9f6c-111">--------------------------Beispiel 1: Erstellen eines neuen Diensts aus einer JSON-dateibasierten Definition--------------------------</span><span class="sxs-lookup"><span data-stu-id="f9f6c-111">--------------------------  Example 1: Create a new service from a Json file based definition  --------------------------</span></span>
```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="f9f6c-112">Erstellt einen neuen Azure Machine Learning-Webdienst mit dem Namen "mywebservicename" in der Gruppe "myresourcegroup" und der Region Süd-Zentralamerika, basierend auf der in der referenzierten JSON-Datei vorhandenen Definition.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="f9f6c-113">--------------------------Beispiel 2: Erstellen eines neuen Diensts aus einer Objektinstanz--------------------------</span><span class="sxs-lookup"><span data-stu-id="f9f6c-113">--------------------------  Example 2: Create a new service from an object instance  --------------------------</span></span>
```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="f9f6c-114">Sie können eine Webdienst-Objektinstanz abrufen, um Sie vor der Veröffentlichung als Ressource mithilfe des Import-AzureRmMlWebService-Cmdlets anzupassen.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="f9f6c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9f6c-115">PARAMETERS</span></span>

### <span data-ttu-id="f9f6c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9f6c-116">-DefaultProfile</span></span>
<span data-ttu-id="f9f6c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f9f6c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9f6c-118">-Definitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-118">-DefinitionFile</span></span>
<span data-ttu-id="f9f6c-119">Gibt an der Pfad zu der Datei, die die JSON-Formatdefinition des Webdiensts enthält.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-119">Specifes the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="f9f6c-120">Die neueste Spezifikation für die Webdienstdefinition finden Sie in der Prahlerei-Spezifikation unter https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="f9f6c-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

```yaml
Type: String
Parameter Sets: CreateFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f6c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f9f6c-121">-Force</span></span>
<span data-ttu-id="f9f6c-122">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f9f6c-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="f9f6c-123">-Location</span></span>
<span data-ttu-id="f9f6c-124">Der Bereich des Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-124">The region of the web service.</span></span>
<span data-ttu-id="f9f6c-125">Geben Sie einen Azure Data Center-Bereich ein, beispielsweise "West USA" oder "Südostasien".</span><span class="sxs-lookup"><span data-stu-id="f9f6c-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="f9f6c-126">Sie können einen Webdienst in jeder Region platzieren, die Ressourcen dieses Typs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="f9f6c-127">Der Webdienst muss sich nicht im gleichen Bereich Ihres Azure-Abonnements oder der gleichen Region wie seine Ressourcengruppe befinden.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="f9f6c-128">Ressourcengruppen können Webdienste aus verschiedenen Regionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="f9f6c-129">Wenn Sie ermitteln möchten, welche Regionen die einzelnen Ressourcentypen unterstützen, verwenden Sie die Get-AzureRmResourceProvider mit dem Cmdlet ProviderNamespace-Parameter.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-129">To determine which regions support each resource type, use the Get-AzureRmResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="f9f6c-130">-Name</span><span class="sxs-lookup"><span data-stu-id="f9f6c-130">-Name</span></span>
<span data-ttu-id="f9f6c-131">Der Name für den Webdienst.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-131">The name for the web service.</span></span>
<span data-ttu-id="f9f6c-132">Der Name muss in der Ressourcengruppe eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="f9f6c-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="f9f6c-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="f9f6c-134">Die Definition für den neuen Webdienst, die alle Eigenschaften enthält, aus denen sich der Dienst besteht.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="f9f6c-135">Dieser Parameter ist erforderlich und stellt eine Instanz der Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService-Klasse dar.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="f9f6c-136">Die neueste Spezifikation für die Webdienstdefinition finden Sie in der Prahlerei-Spezifikation unter https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="f9f6c-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

```yaml
Type: WebService
Parameter Sets: CreateFromInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9f6c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9f6c-137">-ResourceGroupName</span></span>
<span data-ttu-id="f9f6c-138">Die Ressourcengruppe, in der der Webdienst platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="f9f6c-139">Geben Sie einen Azure Data Center-Bereich ein, beispielsweise "West USA" oder "Südostasien".</span><span class="sxs-lookup"><span data-stu-id="f9f6c-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="f9f6c-140">Sie können einen Webdienst in jeder Region platzieren, die Ressourcen dieses Typs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="f9f6c-141">Der Webdienst muss sich nicht im gleichen Bereich Ihres Azure-Abonnements oder der gleichen Region wie seine Ressourcengruppe befinden.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="f9f6c-142">Ressourcengruppen können Webdienste aus verschiedenen Regionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="f9f6c-143">Wenn Sie ermitteln möchten, welche Regionen die einzelnen Ressourcentypen unterstützen, verwenden Sie die Get-AzureRmResourceProvider mit dem Cmdlet ProviderNamespace-Parameter.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-143">To determine which regions support each resource type, use the Get-AzureRmResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="f9f6c-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f9f6c-144">-Confirm</span></span>
<span data-ttu-id="f9f6c-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f6c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9f6c-146">-WhatIf</span></span>
<span data-ttu-id="f9f6c-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9f6c-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f6c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9f6c-149">CommonParameters</span></span>
<span data-ttu-id="f9f6c-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9f6c-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9f6c-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9f6c-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f9f6c-152">INPUTS</span></span>

### <span data-ttu-id="f9f6c-153">Webservice</span><span class="sxs-lookup"><span data-stu-id="f9f6c-153">WebService</span></span>
<span data-ttu-id="f9f6c-154">Der Parameter "NewWebServiceDefinition" akzeptiert den Wert vom Typ "Webservice" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-154">Parameter 'NewWebServiceDefinition' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="f9f6c-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f9f6c-155">OUTPUTS</span></span>

### <span data-ttu-id="f9f6c-156">Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="f9f6c-156">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="f9f6c-157">Eine zusammenfassende Beschreibung des Azure Machine Learning-Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-157">A summary description of the Azure Machine Learning web service.</span></span>
<span data-ttu-id="f9f6c-158">Ähnlich wie die Beschreibung, die durch Aufrufen des Get-AzureRmMlWebService-Cmdlets für einen vorhandenen Webdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-158">Similar to the description returned by calling the Get-AzureRmMlWebService cmdlet on an existing web service.</span></span>
<span data-ttu-id="f9f6c-159">Diese Beschreibung enthält keine vertraulichen Eigenschaften wie die Anmeldeinformationen des speicherkontos und die Zugriffstasten des Diensts.</span><span class="sxs-lookup"><span data-stu-id="f9f6c-159">This description does not contain sensitive properties such as storage account's credentials and the service's access keys.</span></span>

## <span data-ttu-id="f9f6c-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="f9f6c-160">NOTES</span></span>
<span data-ttu-id="f9f6c-161">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f9f6c-161">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f9f6c-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f9f6c-162">RELATED LINKS</span></span>

