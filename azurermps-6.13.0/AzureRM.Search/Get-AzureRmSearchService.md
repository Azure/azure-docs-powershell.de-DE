---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchService.md
ms.openlocfilehash: 57b09ea3267447f16ceadf4d1eae51f997c53a82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480058"
---
# <span data-ttu-id="8f1d3-101">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="8f1d3-101">Get-AzureRmSearchService</span></span>

## <span data-ttu-id="8f1d3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8f1d3-102">SYNOPSIS</span></span>
<span data-ttu-id="8f1d3-103">Ruft einen Azure-Suchdienst ab.</span><span class="sxs-lookup"><span data-stu-id="8f1d3-103">Gets an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f1d3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f1d3-104">SYNTAX</span></span>

### <span data-ttu-id="8f1d3-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f1d3-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmSearchService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f1d3-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f1d3-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f1d3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f1d3-107">DESCRIPTION</span></span>
<span data-ttu-id="8f1d3-108">Das Cmdlet " **Get-AzureRmSearchService** " Ruft den angegebenen Azure-Suchdienst ab.</span><span class="sxs-lookup"><span data-stu-id="8f1d3-108">The **Get-AzureRmSearchService** cmdlet gets the specified Azure Search service.</span></span>

## <span data-ttu-id="8f1d3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f1d3-109">EXAMPLES</span></span>

### <span data-ttu-id="8f1d3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8f1d3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchService -ResourceGroupName felixwa-01


ResourceGroupName : felixwa-01
Name              : felixwa-basic-search
Location          : West US
Sku               : Basic
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/felixwa-01/providers/Microsoft.Search/searchServices/felixwa-basic-search
```

<span data-ttu-id="8f1d3-111">Rufen Sie einen Azure-Suchdienst mit angegebenen Parametern ab.</span><span class="sxs-lookup"><span data-stu-id="8f1d3-111">Get an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="8f1d3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f1d3-112">PARAMETERS</span></span>

### <span data-ttu-id="8f1d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f1d3-113">-DefaultProfile</span></span>
<span data-ttu-id="8f1d3-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8f1d3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f1d3-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8f1d3-115">-Name</span></span>
<span data-ttu-id="8f1d3-116">Name des Suchdiensts</span><span class="sxs-lookup"><span data-stu-id="8f1d3-116">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1d3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f1d3-117">-ResourceGroupName</span></span>
<span data-ttu-id="8f1d3-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8f1d3-118">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1d3-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8f1d3-119">-ResourceId</span></span>
<span data-ttu-id="8f1d3-120">Ressourcen-ID des Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="8f1d3-120">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f1d3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f1d3-121">CommonParameters</span></span>
<span data-ttu-id="8f1d3-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f1d3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f1d3-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f1d3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f1d3-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8f1d3-124">INPUTS</span></span>

### <span data-ttu-id="8f1d3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8f1d3-125">System.String</span></span>

## <span data-ttu-id="8f1d3-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8f1d3-126">OUTPUTS</span></span>

### <span data-ttu-id="8f1d3-127">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="8f1d3-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="8f1d3-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f1d3-128">NOTES</span></span>

## <span data-ttu-id="8f1d3-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8f1d3-129">RELATED LINKS</span></span>

[<span data-ttu-id="8f1d3-130">Neu – AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="8f1d3-130">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="8f1d3-131">Satz-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="8f1d3-131">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

[<span data-ttu-id="8f1d3-132">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="8f1d3-132">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
