---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
ms.openlocfilehash: 73e20db774e6df70086eef6dc61a2ba9ecfb8689
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650678"
---
# <span data-ttu-id="a54a3-101">Get-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="a54a3-101">Get-AzMlWebService</span></span>

## <span data-ttu-id="a54a3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a54a3-102">SYNOPSIS</span></span>
<span data-ttu-id="a54a3-103">Ruft die Zusammenfassungsinformationen für einen oder mehrere Webdienste ab.</span><span class="sxs-lookup"><span data-stu-id="a54a3-103">Retrieves the summary information for one or more web services.</span></span>

## <span data-ttu-id="a54a3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a54a3-104">SYNTAX</span></span>

```
Get-AzMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a54a3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a54a3-105">DESCRIPTION</span></span>
<span data-ttu-id="a54a3-106">Ruft Webdienst Definitionsinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="a54a3-106">Retrieves web service definition information.</span></span>
<span data-ttu-id="a54a3-107">Je nach den übergebenen Parametern gibt das Cmdlet die Definition für einen bestimmten Webdienst, eine Sammlung von Definitionen für die Webdienste für eine angegebene Ressourcengruppe innerhalb des aktuellen Abonnements oder eine Sammlung von Definitionen für die Webdienste innerhalb des aktuellen Abonnements zurück.</span><span class="sxs-lookup"><span data-stu-id="a54a3-107">Depending on the parameters passed, the cmdlet returns the definition for a specific web service, a collection of definitions for the web services for a specified resource group within the current subscription, or a collection of definitions for the web services within the current subscription.</span></span>

## <span data-ttu-id="a54a3-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a54a3-108">EXAMPLES</span></span>

### <span data-ttu-id="a54a3-109">Beispiel 1: Abrufen von Details zu bestimmten Webdiensten</span><span class="sxs-lookup"><span data-stu-id="a54a3-109">Example 1: Get details of specific web service</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="a54a3-110">Beispiel 2: Abrufen aller Webdienst Ressourcen im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="a54a3-110">Example 2: Get all web service resources in current subscription</span></span>
```
Get-AzMlWebService
```

### <span data-ttu-id="a54a3-111">Beispiel 3: Abrufen aller Webdienste im aktuellen Abonnement und der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a54a3-111">Example 3: Get all web services in the current subscription and given resource group</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="a54a3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a54a3-112">PARAMETERS</span></span>

### <span data-ttu-id="a54a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a54a3-113">-DefaultProfile</span></span>
<span data-ttu-id="a54a3-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a54a3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a54a3-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a54a3-115">-Name</span></span>
<span data-ttu-id="a54a3-116">Der Name des Webdiensts, für den die Details abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a54a3-116">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="a54a3-117">-Region</span><span class="sxs-lookup"><span data-stu-id="a54a3-117">-Region</span></span>
<span data-ttu-id="a54a3-118">Der Name des Bereichs</span><span class="sxs-lookup"><span data-stu-id="a54a3-118">The name of region</span></span>

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

### <span data-ttu-id="a54a3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a54a3-119">-ResourceGroupName</span></span>
<span data-ttu-id="a54a3-120">Die Ressourcengruppe, aus der die Details für den Webdienst abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a54a3-120">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="a54a3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a54a3-121">CommonParameters</span></span>
<span data-ttu-id="a54a3-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a54a3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a54a3-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a54a3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a54a3-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a54a3-124">INPUTS</span></span>

### <span data-ttu-id="a54a3-125">Keine</span><span class="sxs-lookup"><span data-stu-id="a54a3-125">None</span></span>

## <span data-ttu-id="a54a3-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a54a3-126">OUTPUTS</span></span>

### <span data-ttu-id="a54a3-127">Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="a54a3-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="a54a3-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="a54a3-128">NOTES</span></span>
<span data-ttu-id="a54a3-129">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="a54a3-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="a54a3-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a54a3-130">RELATED LINKS</span></span>
