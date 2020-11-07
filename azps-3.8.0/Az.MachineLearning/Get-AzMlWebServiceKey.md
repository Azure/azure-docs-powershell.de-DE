---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
ms.openlocfilehash: e6da366738bf6b1d56c9500ddd6064c6505a5936
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846231"
---
# <span data-ttu-id="18775-101">Get-AzMlWebServiceKey</span><span class="sxs-lookup"><span data-stu-id="18775-101">Get-AzMlWebServiceKey</span></span>

## <span data-ttu-id="18775-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="18775-102">SYNOPSIS</span></span>
<span data-ttu-id="18775-103">Ruft die Schlüssel des Webdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="18775-103">Retrieves the web service's keys.</span></span>

## <span data-ttu-id="18775-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="18775-104">SYNTAX</span></span>

### <span data-ttu-id="18775-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="18775-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="18775-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="18775-106">GetByInstance</span></span>
```
Get-AzMlWebServiceKey -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18775-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18775-107">DESCRIPTION</span></span>
<span data-ttu-id="18775-108">Ruft die Zugriffstasten für die Runtime-APIs des Azure Machine Learning-Webdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="18775-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="18775-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18775-109">EXAMPLES</span></span>

### <span data-ttu-id="18775-110">Beispiel 1: Abrufen der Schlüssel für einen Webdienst, der durch die Ressourcengruppe und den Namen angegeben wird</span><span class="sxs-lookup"><span data-stu-id="18775-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="18775-111">Beispiel 2: Abrufen von Schlüsseln für Webdienst Instanzen</span><span class="sxs-lookup"><span data-stu-id="18775-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzMlWebServiceKey -MlWebService $mlService
```

<span data-ttu-id="18775-112">$mlService ist ein Objekt vom Typ Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService.</span><span class="sxs-lookup"><span data-stu-id="18775-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="18775-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="18775-113">PARAMETERS</span></span>

### <span data-ttu-id="18775-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18775-114">-DefaultProfile</span></span>
<span data-ttu-id="18775-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="18775-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18775-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="18775-116">-MlWebService</span></span>
<span data-ttu-id="18775-117">Der Name des Webdiensts, für den die Zugriffstasten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="18775-117">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="18775-118">-Name</span><span class="sxs-lookup"><span data-stu-id="18775-118">-Name</span></span>
<span data-ttu-id="18775-119">Der Name des Webdiensts, für den die Zugriffstasten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="18775-119">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="18775-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18775-120">-ResourceGroupName</span></span>
<span data-ttu-id="18775-121">Die Ressourcengruppe für den Webdienst.</span><span class="sxs-lookup"><span data-stu-id="18775-121">The resource group for the web service.</span></span>

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

### <span data-ttu-id="18775-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18775-122">CommonParameters</span></span>
<span data-ttu-id="18775-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18775-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18775-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18775-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18775-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="18775-125">INPUTS</span></span>

### <span data-ttu-id="18775-126">Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="18775-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="18775-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="18775-127">OUTPUTS</span></span>

### <span data-ttu-id="18775-128">Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="18775-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="18775-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="18775-129">NOTES</span></span>
<span data-ttu-id="18775-130">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="18775-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="18775-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="18775-131">RELATED LINKS</span></span>
