---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservicekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: 7d0df70118f50274ccecfd730e752efabcf52519
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496002"
---
# <span data-ttu-id="734ac-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="734ac-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="734ac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="734ac-102">SYNOPSIS</span></span>
<span data-ttu-id="734ac-103">Ruft die Schlüssel des Webdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="734ac-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="734ac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="734ac-104">SYNTAX</span></span>

### <span data-ttu-id="734ac-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="734ac-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="734ac-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="734ac-106">GetByInstance</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="734ac-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="734ac-107">DESCRIPTION</span></span>
<span data-ttu-id="734ac-108">Ruft die Zugriffstasten für die Runtime-APIs des Azure Machine Learning-Webdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="734ac-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="734ac-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="734ac-109">EXAMPLES</span></span>

### <span data-ttu-id="734ac-110">Beispiel 1: Abrufen der Schlüssel für einen Webdienst, der durch die Ressourcengruppe und den Namen angegeben wird</span><span class="sxs-lookup"><span data-stu-id="734ac-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="734ac-111">Beispiel 2: Abrufen von Schlüsseln für Webdienst Instanzen</span><span class="sxs-lookup"><span data-stu-id="734ac-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="734ac-112">$mlService ist ein Objekt vom Typ Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService.</span><span class="sxs-lookup"><span data-stu-id="734ac-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="734ac-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="734ac-113">PARAMETERS</span></span>

### <span data-ttu-id="734ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="734ac-114">-DefaultProfile</span></span>
<span data-ttu-id="734ac-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="734ac-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="734ac-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="734ac-116">-MlWebService</span></span>
<span data-ttu-id="734ac-117">Der Name des Webdiensts, für den die Zugriffstasten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="734ac-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: GetByInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="734ac-118">-Name</span><span class="sxs-lookup"><span data-stu-id="734ac-118">-Name</span></span>
<span data-ttu-id="734ac-119">Der Name des Webdiensts, für den die Zugriffstasten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="734ac-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="734ac-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="734ac-120">-ResourceGroupName</span></span>
<span data-ttu-id="734ac-121">Die Ressourcengruppe für den Webdienst.</span><span class="sxs-lookup"><span data-stu-id="734ac-121">The resource group for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="734ac-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="734ac-122">CommonParameters</span></span>
<span data-ttu-id="734ac-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="734ac-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="734ac-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="734ac-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="734ac-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="734ac-125">INPUTS</span></span>

### <span data-ttu-id="734ac-126">Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="734ac-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="734ac-127">Parameter: MlWebService (ByValue)</span><span class="sxs-lookup"><span data-stu-id="734ac-127">Parameters: MlWebService (ByValue)</span></span>

## <span data-ttu-id="734ac-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="734ac-128">OUTPUTS</span></span>

### <span data-ttu-id="734ac-129">Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="734ac-129">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="734ac-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="734ac-130">NOTES</span></span>
<span data-ttu-id="734ac-131">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="734ac-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="734ac-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="734ac-132">RELATED LINKS</span></span>
