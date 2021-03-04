---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 5c341677f5bc741f5848508f80b1a29e29c90b17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919715"
---
# <span data-ttu-id="8e2ac-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="8e2ac-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="8e2ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e2ac-102">SYNOPSIS</span></span>
<span data-ttu-id="8e2ac-103">Ruft eine private Linkressource ab.</span><span class="sxs-lookup"><span data-stu-id="8e2ac-103">Gets a private link resource.</span></span>

## <span data-ttu-id="8e2ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e2ac-104">SYNTAX</span></span>

### <span data-ttu-id="8e2ac-105">ByPrivateLinkResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e2ac-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e2ac-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="8e2ac-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="8e2ac-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e2ac-107">DESCRIPTION</span></span>
<span data-ttu-id="8e2ac-108">Das **Get-AzPrivateLinkResource-Cmdlet** ruft alle Linkressourcen ab und gehört zu PrivateLinkResource.</span><span class="sxs-lookup"><span data-stu-id="8e2ac-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="8e2ac-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8e2ac-109">EXAMPLES</span></span>

### <span data-ttu-id="8e2ac-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8e2ac-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="8e2ac-111">In diesem Beispiel werden alle privaten Verknüpfungsressourcen nbelong zu sql server mit dem Namen mySql aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e2ac-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="8e2ac-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8e2ac-112">PARAMETERS</span></span>

### <span data-ttu-id="8e2ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e2ac-113">-DefaultProfile</span></span>
<span data-ttu-id="8e2ac-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e2ac-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e2ac-115">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="8e2ac-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="8e2ac-116">Die Azure-Ressourcen-Manager-ID der privaten Linkressource.</span><span class="sxs-lookup"><span data-stu-id="8e2ac-116">The Azure resource manager id of the private link resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPrivateLinkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e2ac-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="8e2ac-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="8e2ac-118">Der Ressourcentyp für private Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="8e2ac-118">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e2ac-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e2ac-119">-ResourceGroupName</span></span>
<span data-ttu-id="8e2ac-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8e2ac-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e2ac-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8e2ac-121">-ServiceName</span></span>
<span data-ttu-id="8e2ac-122">Der Name des privaten Linkdiensts.</span><span class="sxs-lookup"><span data-stu-id="8e2ac-122">The private link service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e2ac-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e2ac-123">CommonParameters</span></span>
<span data-ttu-id="8e2ac-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e2ac-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e2ac-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e2ac-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e2ac-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8e2ac-126">INPUTS</span></span>

### <span data-ttu-id="8e2ac-127">System.String</span><span class="sxs-lookup"><span data-stu-id="8e2ac-127">System.String</span></span>

## <span data-ttu-id="8e2ac-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8e2ac-128">OUTPUTS</span></span>

### <span data-ttu-id="8e2ac-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8e2ac-129">System.Boolean</span></span>

## <span data-ttu-id="8e2ac-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8e2ac-130">NOTES</span></span>

## <span data-ttu-id="8e2ac-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8e2ac-131">RELATED LINKS</span></span>
