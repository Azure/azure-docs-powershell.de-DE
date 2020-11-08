---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
ms.openlocfilehash: e4751232969c407484b978d495d348dc61810715
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178401"
---
# <span data-ttu-id="5c9ca-101">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="5c9ca-101">Get-AzSearchService</span></span>

## <span data-ttu-id="5c9ca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5c9ca-102">SYNOPSIS</span></span>
<span data-ttu-id="5c9ca-103">Ruft einen Azure-Suchdienst ab.</span><span class="sxs-lookup"><span data-stu-id="5c9ca-103">Gets an Azure Search service.</span></span>

## <span data-ttu-id="5c9ca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c9ca-104">SYNTAX</span></span>

### <span data-ttu-id="5c9ca-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5c9ca-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSearchService [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c9ca-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c9ca-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c9ca-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c9ca-107">DESCRIPTION</span></span>
<span data-ttu-id="5c9ca-108">Das Cmdlet " **Get-AzSearchService** " Ruft den angegebenen Azure-Suchdienst ab.</span><span class="sxs-lookup"><span data-stu-id="5c9ca-108">The **Get-AzSearchService** cmdlet gets the specified Azure Search service.</span></span>

## <span data-ttu-id="5c9ca-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5c9ca-109">EXAMPLES</span></span>

### <span data-ttu-id="5c9ca-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5c9ca-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchService -ResourceGroupName felixwa-01


ResourceGroupName : felixwa-01
Name              : felixwa-basic-search
Location          : West US
Sku               : Basic
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/felixwa-01/providers/Microsoft.Search/searchServices/felixwa-basic-search
```

<span data-ttu-id="5c9ca-111">Rufen Sie einen Azure-Suchdienst mit angegebenen Parametern ab.</span><span class="sxs-lookup"><span data-stu-id="5c9ca-111">Get an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="5c9ca-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c9ca-112">PARAMETERS</span></span>

### <span data-ttu-id="5c9ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c9ca-113">-DefaultProfile</span></span>
<span data-ttu-id="5c9ca-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5c9ca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c9ca-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5c9ca-115">-Name</span></span>
<span data-ttu-id="5c9ca-116">Name des Suchdiensts</span><span class="sxs-lookup"><span data-stu-id="5c9ca-116">Search Service name.</span></span>

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

### <span data-ttu-id="5c9ca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c9ca-117">-ResourceGroupName</span></span>
<span data-ttu-id="5c9ca-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5c9ca-118">Resource Group name.</span></span>

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

### <span data-ttu-id="5c9ca-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5c9ca-119">-ResourceId</span></span>
<span data-ttu-id="5c9ca-120">Ressourcen-ID des Suchdiensts.</span><span class="sxs-lookup"><span data-stu-id="5c9ca-120">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="5c9ca-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c9ca-121">CommonParameters</span></span>
<span data-ttu-id="5c9ca-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c9ca-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c9ca-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c9ca-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c9ca-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5c9ca-124">INPUTS</span></span>

### <span data-ttu-id="5c9ca-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5c9ca-125">System.String</span></span>

## <span data-ttu-id="5c9ca-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5c9ca-126">OUTPUTS</span></span>

### <span data-ttu-id="5c9ca-127">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="5c9ca-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="5c9ca-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="5c9ca-128">NOTES</span></span>

## <span data-ttu-id="5c9ca-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5c9ca-129">RELATED LINKS</span></span>

[<span data-ttu-id="5c9ca-130">Neu – AzSearchService</span><span class="sxs-lookup"><span data-stu-id="5c9ca-130">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="5c9ca-131">Satz-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="5c9ca-131">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="5c9ca-132">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="5c9ca-132">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)