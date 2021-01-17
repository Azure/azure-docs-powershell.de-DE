---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
ms.openlocfilehash: e6da366738bf6b1d56c9500ddd6064c6505a5936
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360799"
---
# <span data-ttu-id="acbbb-101">Get-AzMlWebServiceKey</span><span class="sxs-lookup"><span data-stu-id="acbbb-101">Get-AzMlWebServiceKey</span></span>

## <span data-ttu-id="acbbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acbbb-102">SYNOPSIS</span></span>
<span data-ttu-id="acbbb-103">Ruft die Schlüssel des Webdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="acbbb-103">Retrieves the web service's keys.</span></span>

## <span data-ttu-id="acbbb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="acbbb-104">SYNTAX</span></span>

### <span data-ttu-id="acbbb-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="acbbb-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="acbbb-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="acbbb-106">GetByInstance</span></span>
```
Get-AzMlWebServiceKey -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="acbbb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="acbbb-107">DESCRIPTION</span></span>
<span data-ttu-id="acbbb-108">Ruft die Zugriffstasten für die Laufzeit-APIs des Azure Machine Learning-Webdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="acbbb-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="acbbb-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="acbbb-109">EXAMPLES</span></span>

### <span data-ttu-id="acbbb-110">Beispiel 1: Erhalten der Schlüssel für einen Webdienst, angegeben durch Ressourcengruppe und -name</span><span class="sxs-lookup"><span data-stu-id="acbbb-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="acbbb-111">Beispiel 2: Erhalten von Schlüsseln für eine Webdienstinstanz</span><span class="sxs-lookup"><span data-stu-id="acbbb-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzMlWebServiceKey -MlWebService $mlService
```

<span data-ttu-id="acbbb-112">$mlService ist ein Objekt vom Typ "Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService".</span><span class="sxs-lookup"><span data-stu-id="acbbb-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="acbbb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acbbb-113">PARAMETERS</span></span>

### <span data-ttu-id="acbbb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acbbb-114">-DefaultProfile</span></span>
<span data-ttu-id="acbbb-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="acbbb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="acbbb-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="acbbb-116">-MlWebService</span></span>
<span data-ttu-id="acbbb-117">Der Name des Webdiensts, für den die Zugriffstasten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="acbbb-117">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="acbbb-118">-Name</span><span class="sxs-lookup"><span data-stu-id="acbbb-118">-Name</span></span>
<span data-ttu-id="acbbb-119">Der Name des Webdiensts, für den die Zugriffstasten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="acbbb-119">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="acbbb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acbbb-120">-ResourceGroupName</span></span>
<span data-ttu-id="acbbb-121">Die Ressourcengruppe für den Webdienst.</span><span class="sxs-lookup"><span data-stu-id="acbbb-121">The resource group for the web service.</span></span>

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

### <span data-ttu-id="acbbb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acbbb-122">CommonParameters</span></span>
<span data-ttu-id="acbbb-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acbbb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acbbb-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acbbb-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acbbb-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="acbbb-125">INPUTS</span></span>

### <span data-ttu-id="acbbb-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="acbbb-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="acbbb-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="acbbb-127">OUTPUTS</span></span>

### <span data-ttu-id="acbbb-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="acbbb-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="acbbb-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="acbbb-129">NOTES</span></span>
<span data-ttu-id="acbbb-130">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="acbbb-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="acbbb-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="acbbb-131">RELATED LINKS</span></span>
