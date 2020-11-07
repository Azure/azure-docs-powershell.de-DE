---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 325888f510f967f93aca5b3ef50294dd83971213
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650669"
---
# <span data-ttu-id="66558-101">New-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="66558-101">New-AzMlWebService</span></span>

## <span data-ttu-id="66558-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66558-102">SYNOPSIS</span></span>
<span data-ttu-id="66558-103">Erstellt einen neuen Webdienst.</span><span class="sxs-lookup"><span data-stu-id="66558-103">Creates a new web service.</span></span>

## <span data-ttu-id="66558-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66558-104">SYNTAX</span></span>

### <span data-ttu-id="66558-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="66558-105">CreateFromFile</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66558-106">CreateFromInstance</span><span class="sxs-lookup"><span data-stu-id="66558-106">CreateFromInstance</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66558-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66558-107">DESCRIPTION</span></span>
<span data-ttu-id="66558-108">Erstellt einen Azure Machine Learning-Webdienst in einer vorhandenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="66558-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="66558-109">Wenn ein Webdienst mit demselben Namen in der Ressourcengruppe vorhanden ist, fungiert der Anruf als Aktualisierungsvorgang, und der vorhandene Webdienst wird überschrieben.</span><span class="sxs-lookup"><span data-stu-id="66558-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="66558-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66558-110">EXAMPLES</span></span>

### <span data-ttu-id="66558-111">Beispiel 1: Erstellen eines neuen Diensts aus einer JSON-dateibasierten Definition</span><span class="sxs-lookup"><span data-stu-id="66558-111">Example 1: Create a new service from a Json file based definition</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="66558-112">Erstellt einen neuen Azure Machine Learning-Webdienst mit dem Namen "mywebservicename" in der Gruppe "myresourcegroup" und der Region Süd-Zentralamerika, basierend auf der in der referenzierten JSON-Datei vorhandenen Definition.</span><span class="sxs-lookup"><span data-stu-id="66558-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="66558-113">Beispiel 2: Erstellen eines neuen Diensts aus einer Objektinstanz</span><span class="sxs-lookup"><span data-stu-id="66558-113">Example 2: Create a new service from an object instance</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="66558-114">Sie können eine Webdienst-Objektinstanz abrufen, um Sie vor der Veröffentlichung als Ressource mithilfe des Import-AzMlWebService-Cmdlets anzupassen.</span><span class="sxs-lookup"><span data-stu-id="66558-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="66558-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="66558-115">PARAMETERS</span></span>

### <span data-ttu-id="66558-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66558-116">-DefaultProfile</span></span>
<span data-ttu-id="66558-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="66558-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66558-118">-Definitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="66558-118">-DefinitionFile</span></span>
<span data-ttu-id="66558-119">Gibt den Pfad zu der Datei an, die die JSON-Formatdefinition des Webdiensts enthält.</span><span class="sxs-lookup"><span data-stu-id="66558-119">Specifies the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="66558-120">Die neueste Spezifikation für die Webdienstdefinition finden Sie in der Prahlerei-Spezifikation unter https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="66558-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

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

### <span data-ttu-id="66558-121">-Force</span><span class="sxs-lookup"><span data-stu-id="66558-121">-Force</span></span>
<span data-ttu-id="66558-122">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="66558-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="66558-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="66558-123">-Location</span></span>
<span data-ttu-id="66558-124">Der Bereich des Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="66558-124">The region of the web service.</span></span>
<span data-ttu-id="66558-125">Geben Sie einen Azure Data Center-Bereich ein, beispielsweise "West USA" oder "Südostasien".</span><span class="sxs-lookup"><span data-stu-id="66558-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="66558-126">Sie können einen Webdienst in jeder Region platzieren, die Ressourcen dieses Typs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="66558-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="66558-127">Der Webdienst muss sich nicht im gleichen Bereich Ihres Azure-Abonnements oder der gleichen Region wie seine Ressourcengruppe befinden.</span><span class="sxs-lookup"><span data-stu-id="66558-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="66558-128">Ressourcengruppen können Webdienste aus verschiedenen Regionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="66558-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="66558-129">Wenn Sie ermitteln möchten, welche Regionen die einzelnen Ressourcentypen unterstützen, verwenden Sie die Get-AzResourceProvider mit dem Cmdlet ProviderNamespace-Parameter.</span><span class="sxs-lookup"><span data-stu-id="66558-129">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="66558-130">-Name</span><span class="sxs-lookup"><span data-stu-id="66558-130">-Name</span></span>
<span data-ttu-id="66558-131">Der Name für den Webdienst.</span><span class="sxs-lookup"><span data-stu-id="66558-131">The name for the web service.</span></span>
<span data-ttu-id="66558-132">Der Name muss in der Ressourcengruppe eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="66558-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="66558-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="66558-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="66558-134">Die Definition für den neuen Webdienst, die alle Eigenschaften enthält, aus denen sich der Dienst besteht.</span><span class="sxs-lookup"><span data-stu-id="66558-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="66558-135">Dieser Parameter ist erforderlich und stellt eine Instanz der Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService-Klasse dar.</span><span class="sxs-lookup"><span data-stu-id="66558-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="66558-136">Die neueste Spezifikation für die Webdienstdefinition finden Sie in der Prahlerei-Spezifikation unter https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="66558-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

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

### <span data-ttu-id="66558-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66558-137">-ResourceGroupName</span></span>
<span data-ttu-id="66558-138">Die Ressourcengruppe, in der der Webdienst platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="66558-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="66558-139">Geben Sie einen Azure Data Center-Bereich ein, beispielsweise "West USA" oder "Südostasien".</span><span class="sxs-lookup"><span data-stu-id="66558-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="66558-140">Sie können einen Webdienst in jeder Region platzieren, die Ressourcen dieses Typs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="66558-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="66558-141">Der Webdienst muss sich nicht im gleichen Bereich Ihres Azure-Abonnements oder der gleichen Region wie seine Ressourcengruppe befinden.</span><span class="sxs-lookup"><span data-stu-id="66558-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="66558-142">Ressourcengruppen können Webdienste aus verschiedenen Regionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="66558-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="66558-143">Wenn Sie ermitteln möchten, welche Regionen die einzelnen Ressourcentypen unterstützen, verwenden Sie die Get-AzResourceProvider mit dem Cmdlet ProviderNamespace-Parameter.</span><span class="sxs-lookup"><span data-stu-id="66558-143">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="66558-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="66558-144">-Confirm</span></span>
<span data-ttu-id="66558-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66558-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66558-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66558-146">-WhatIf</span></span>
<span data-ttu-id="66558-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66558-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66558-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66558-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66558-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66558-149">CommonParameters</span></span>
<span data-ttu-id="66558-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66558-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66558-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66558-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66558-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66558-152">INPUTS</span></span>

### <span data-ttu-id="66558-153">Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="66558-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="66558-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66558-154">OUTPUTS</span></span>

### <span data-ttu-id="66558-155">Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="66558-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="66558-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="66558-156">NOTES</span></span>
<span data-ttu-id="66558-157">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="66558-157">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="66558-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66558-158">RELATED LINKS</span></span>
