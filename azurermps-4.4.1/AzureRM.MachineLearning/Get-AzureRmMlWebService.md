---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
ms.openlocfilehash: 14fbb8631a15321df9ae6834456649d00caae897
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504910"
---
# <span data-ttu-id="b033e-101">Get-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="b033e-101">Get-AzureRmMlWebService</span></span>

## <span data-ttu-id="b033e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b033e-102">SYNOPSIS</span></span>
<span data-ttu-id="b033e-103">Ruft die Zusammenfassungsinformationen für einen oder mehrere Webdienste ab.</span><span class="sxs-lookup"><span data-stu-id="b033e-103">Retrieves the summary information for one or more web services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b033e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b033e-104">SYNTAX</span></span>

```
Get-AzureRmMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b033e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b033e-105">DESCRIPTION</span></span>
<span data-ttu-id="b033e-106">Ruft Webdienst-Definition Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="b033e-106">Retrieves web service defintion information.</span></span>
<span data-ttu-id="b033e-107">Je nach paramenters gibt das Cmdlet die Definition für einen bestimmten Webdienst, eine Sammlung von Definitionen für die Webdienste für eine angegebene Ressourcengruppe innerhalb des aktuellen Abonnements oder eine Sammlung von Definitionen für die Webdienste innerhalb des aktuellen Abonnements zurück.</span><span class="sxs-lookup"><span data-stu-id="b033e-107">Depending on the paramenters passed, the cmdlet returns the defintion for a specific web service, a collection of defintions for the web services for a specified resource group within the current subscription, or a collection of defintions for the web services within the current subscription.</span></span>

## <span data-ttu-id="b033e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b033e-108">EXAMPLES</span></span>

### <span data-ttu-id="b033e-109">--------------------------Beispiel 1: Abrufen von Details zu bestimmten Webdienst--------------------------</span><span class="sxs-lookup"><span data-stu-id="b033e-109">--------------------------  Example 1: Get details of specific web service  --------------------------</span></span>
<span data-ttu-id="b033e-110">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="b033e-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="b033e-111">--------------------------Beispiel 2: Abrufen aller Webdienst Ressourcen im aktuellen Abonnement--------------------------</span><span class="sxs-lookup"><span data-stu-id="b033e-111">--------------------------  Example 2: Get all web service resources in current subscription  --------------------------</span></span>
<span data-ttu-id="b033e-112">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="b033e-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService
```

### <span data-ttu-id="b033e-113">--------------------------Beispiel 3: Abrufen aller Webdienste im aktuellen Abonnement und der angegebenen Ressourcengruppe--------------------------</span><span class="sxs-lookup"><span data-stu-id="b033e-113">--------------------------  Example 3: Get all web services in the current subscription and given resource group  --------------------------</span></span>
<span data-ttu-id="b033e-114">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="b033e-114">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="b033e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b033e-115">PARAMETERS</span></span>

### <span data-ttu-id="b033e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b033e-116">-Name</span></span>
<span data-ttu-id="b033e-117">Der Name des Webdiensts, für den die Details abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b033e-117">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="b033e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b033e-118">-ResourceGroupName</span></span>
<span data-ttu-id="b033e-119">Die Ressourcengruppe, aus der die Details für den Webdienst abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b033e-119">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="b033e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b033e-120">-DefaultProfile</span></span>
<span data-ttu-id="b033e-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b033e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b033e-122">-Region</span><span class="sxs-lookup"><span data-stu-id="b033e-122">-Region</span></span>
<span data-ttu-id="b033e-123">Der Name des Bereichs</span><span class="sxs-lookup"><span data-stu-id="b033e-123">The name of region</span></span>

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

### <span data-ttu-id="b033e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b033e-124">CommonParameters</span></span>
<span data-ttu-id="b033e-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b033e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b033e-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b033e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b033e-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b033e-127">INPUTS</span></span>

## <span data-ttu-id="b033e-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b033e-128">OUTPUTS</span></span>

### <span data-ttu-id="b033e-129">Keine</span><span class="sxs-lookup"><span data-stu-id="b033e-129">None</span></span>

## <span data-ttu-id="b033e-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="b033e-130">NOTES</span></span>
<span data-ttu-id="b033e-131">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="b033e-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="b033e-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b033e-132">RELATED LINKS</span></span>

