---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
ms.openlocfilehash: be34a81e28f2a11ed604afe922694872fedb5f0a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386026"
---
# <span data-ttu-id="d5a0a-101">Get-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="d5a0a-101">Get-AzMlWebService</span></span>

## <span data-ttu-id="d5a0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5a0a-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a0a-103">Ruft die zusammenfassenden Informationen für einen oder mehrere Webdienste ab.</span><span class="sxs-lookup"><span data-stu-id="d5a0a-103">Retrieves the summary information for one or more web services.</span></span>

## <span data-ttu-id="d5a0a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5a0a-104">SYNTAX</span></span>

```
Get-AzMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5a0a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5a0a-105">DESCRIPTION</span></span>
<span data-ttu-id="d5a0a-106">Ruft Webdienstdefinitionsinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="d5a0a-106">Retrieves web service definition information.</span></span>
<span data-ttu-id="d5a0a-107">Je nach den übergebenen Parametern gibt das Cmdlet die Definition für einen bestimmten Webdienst, eine Sammlung von Definitionen für die Webdienste für eine bestimmte Ressourcengruppe im aktuellen Abonnement oder eine Sammlung von Definitionen für die Webdienste im aktuellen Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="d5a0a-107">Depending on the parameters passed, the cmdlet returns the definition for a specific web service, a collection of definitions for the web services for a specified resource group within the current subscription, or a collection of definitions for the web services within the current subscription.</span></span>

## <span data-ttu-id="d5a0a-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d5a0a-108">EXAMPLES</span></span>

### <span data-ttu-id="d5a0a-109">Beispiel 1: Anzeigen von Details zu einem bestimmten Webdienst</span><span class="sxs-lookup"><span data-stu-id="d5a0a-109">Example 1: Get details of specific web service</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="d5a0a-110">Beispiel 2: Alle Webdienstressourcen im aktuellen Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="d5a0a-110">Example 2: Get all web service resources in current subscription</span></span>
```
Get-AzMlWebService
```

### <span data-ttu-id="d5a0a-111">Beispiel 3: Alle Webdienste im aktuellen Abonnement und der angegebenen Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="d5a0a-111">Example 3: Get all web services in the current subscription and given resource group</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="d5a0a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5a0a-112">PARAMETERS</span></span>

### <span data-ttu-id="d5a0a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a0a-113">-DefaultProfile</span></span>
<span data-ttu-id="d5a0a-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d5a0a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5a0a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d5a0a-115">-Name</span></span>
<span data-ttu-id="d5a0a-116">Der Name des Webdiensts, für den die Details abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d5a0a-116">The name of the web service for which the details are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a0a-117">-Region</span><span class="sxs-lookup"><span data-stu-id="d5a0a-117">-Region</span></span>
<span data-ttu-id="d5a0a-118">Der Name der Region</span><span class="sxs-lookup"><span data-stu-id="d5a0a-118">The name of region</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a0a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5a0a-119">-ResourceGroupName</span></span>
<span data-ttu-id="d5a0a-120">Die Ressourcengruppe, aus der die Details für den Webdienst abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d5a0a-120">The resource group from which the details for the web service are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a0a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a0a-121">CommonParameters</span></span>
<span data-ttu-id="d5a0a-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5a0a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a0a-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5a0a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a0a-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d5a0a-124">INPUTS</span></span>

### <span data-ttu-id="d5a0a-125">Keine</span><span class="sxs-lookup"><span data-stu-id="d5a0a-125">None</span></span>

## <span data-ttu-id="d5a0a-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d5a0a-126">OUTPUTS</span></span>

### <span data-ttu-id="d5a0a-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="d5a0a-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="d5a0a-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d5a0a-128">NOTES</span></span>
<span data-ttu-id="d5a0a-129">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="d5a0a-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="d5a0a-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d5a0a-130">RELATED LINKS</span></span>
