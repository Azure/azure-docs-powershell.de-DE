---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservicekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: a0019b418fbf71a9b8010b4256a062a943244a9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497610"
---
# <span data-ttu-id="c1ff0-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="c1ff0-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="c1ff0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c1ff0-102">SYNOPSIS</span></span>
<span data-ttu-id="c1ff0-103">Ruft die Schlüssel des Webdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="c1ff0-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1ff0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1ff0-104">SYNTAX</span></span>

### <span data-ttu-id="c1ff0-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c1ff0-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1ff0-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="c1ff0-106">GetByInstance</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1ff0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1ff0-107">DESCRIPTION</span></span>
<span data-ttu-id="c1ff0-108">Ruft die Zugriffstasten für die Runtime-APIs des Azure Machine Learning-Webdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="c1ff0-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="c1ff0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1ff0-109">EXAMPLES</span></span>

### <span data-ttu-id="c1ff0-110">--------------------------Beispiel 1: Abrufen der Schlüssel für einen Webdienst, der durch die Ressourcengruppe und den Namen angegeben wird--------------------------</span><span class="sxs-lookup"><span data-stu-id="c1ff0-110">--------------------------  Example 1 - Get the keys for a web service specified by resource group and name  --------------------------</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="c1ff0-111">--------------------------Beispiel 2: Abrufen von Schlüsseln für Webdienst Instanzen--------------------------</span><span class="sxs-lookup"><span data-stu-id="c1ff0-111">--------------------------  Example 2 - Get keys for web service instance  --------------------------</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="c1ff0-112">$mlService ist ein Objekt vom Typ Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService.</span><span class="sxs-lookup"><span data-stu-id="c1ff0-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="c1ff0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1ff0-113">PARAMETERS</span></span>

### <span data-ttu-id="c1ff0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1ff0-114">-DefaultProfile</span></span>
<span data-ttu-id="c1ff0-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c1ff0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1ff0-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="c1ff0-116">-MlWebService</span></span>
<span data-ttu-id="c1ff0-117">Der Name des Webdiensts, für den die Zugriffstasten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c1ff0-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: WebService
Parameter Sets: GetByInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ff0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c1ff0-118">-Name</span></span>
<span data-ttu-id="c1ff0-119">Der Name des Webdiensts, für den die Zugriffstasten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c1ff0-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ff0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1ff0-120">-ResourceGroupName</span></span>
<span data-ttu-id="c1ff0-121">Die Ressourcengruppe für den Webdienst.</span><span class="sxs-lookup"><span data-stu-id="c1ff0-121">The resource group for the web service.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ff0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1ff0-122">CommonParameters</span></span>
<span data-ttu-id="c1ff0-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1ff0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1ff0-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1ff0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1ff0-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c1ff0-125">INPUTS</span></span>

### <span data-ttu-id="c1ff0-126">Webservice</span><span class="sxs-lookup"><span data-stu-id="c1ff0-126">WebService</span></span>
<span data-ttu-id="c1ff0-127">Der Parameter "MlWebService" akzeptiert den Wert vom Typ "Webservice" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c1ff0-127">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="c1ff0-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c1ff0-128">OUTPUTS</span></span>

### <span data-ttu-id="c1ff0-129">Keine</span><span class="sxs-lookup"><span data-stu-id="c1ff0-129">None</span></span>

## <span data-ttu-id="c1ff0-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="c1ff0-130">NOTES</span></span>
<span data-ttu-id="c1ff0-131">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="c1ff0-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="c1ff0-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c1ff0-132">RELATED LINKS</span></span>

