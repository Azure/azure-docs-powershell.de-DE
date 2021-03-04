---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlwebservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
ms.openlocfilehash: 05adf2476c922fdea17a69bd33f74570309349ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923555"
---
# <span data-ttu-id="f444c-101">Get-AzMlWebServiceKey</span><span class="sxs-lookup"><span data-stu-id="f444c-101">Get-AzMlWebServiceKey</span></span>

## <span data-ttu-id="f444c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f444c-102">SYNOPSIS</span></span>
<span data-ttu-id="f444c-103">Ruft die Schlüssel des Webdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="f444c-103">Retrieves the web service's keys.</span></span>

## <span data-ttu-id="f444c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f444c-104">SYNTAX</span></span>

### <span data-ttu-id="f444c-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f444c-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f444c-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="f444c-106">GetByInstance</span></span>
```
Get-AzMlWebServiceKey -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f444c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f444c-107">DESCRIPTION</span></span>
<span data-ttu-id="f444c-108">Ruft die Zugriffstasten für die Laufzeit-APIs des Azure Machine Learning-Webdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="f444c-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="f444c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f444c-109">EXAMPLES</span></span>

### <span data-ttu-id="f444c-110">Beispiel 1: Holen Sie sich die Schlüssel für einen Webdienst, der durch Ressourcengruppe und -name angegeben ist</span><span class="sxs-lookup"><span data-stu-id="f444c-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="f444c-111">Beispiel 2 : Schlüssel für die Webdienstinstanz erhalten</span><span class="sxs-lookup"><span data-stu-id="f444c-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzMlWebServiceKey -MlWebService $mlService
```

<span data-ttu-id="f444c-112">$mlService ist ein Objekt vom Typ Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span><span class="sxs-lookup"><span data-stu-id="f444c-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="f444c-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f444c-113">PARAMETERS</span></span>

### <span data-ttu-id="f444c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f444c-114">-DefaultProfile</span></span>
<span data-ttu-id="f444c-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f444c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f444c-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="f444c-116">-MlWebService</span></span>
<span data-ttu-id="f444c-117">Der Name des Webdiensts, für den die Zugriffstasten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f444c-117">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="f444c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f444c-118">-Name</span></span>
<span data-ttu-id="f444c-119">Der Name des Webdiensts, für den die Zugriffstasten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f444c-119">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="f444c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f444c-120">-ResourceGroupName</span></span>
<span data-ttu-id="f444c-121">Die Ressourcengruppe für den Webdienst.</span><span class="sxs-lookup"><span data-stu-id="f444c-121">The resource group for the web service.</span></span>

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

### <span data-ttu-id="f444c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f444c-122">CommonParameters</span></span>
<span data-ttu-id="f444c-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f444c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f444c-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f444c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f444c-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f444c-125">INPUTS</span></span>

### <span data-ttu-id="f444c-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="f444c-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="f444c-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f444c-127">OUTPUTS</span></span>

### <span data-ttu-id="f444c-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="f444c-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="f444c-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f444c-129">NOTES</span></span>
<span data-ttu-id="f444c-130">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f444c-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f444c-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f444c-131">RELATED LINKS</span></span>
