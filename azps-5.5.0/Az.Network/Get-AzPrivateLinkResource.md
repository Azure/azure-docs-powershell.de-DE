---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 7517509c64c66506444c3ed627338a0f9546a00b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151953"
---
# <span data-ttu-id="717a8-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="717a8-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="717a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="717a8-102">SYNOPSIS</span></span>
<span data-ttu-id="717a8-103">Ruft eine Ressource für einen privaten Link ab.</span><span class="sxs-lookup"><span data-stu-id="717a8-103">Gets a private link resource.</span></span>

## <span data-ttu-id="717a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="717a8-104">SYNTAX</span></span>

### <span data-ttu-id="717a8-105">ByPrivateLinkResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="717a8-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="717a8-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="717a8-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="717a8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="717a8-107">DESCRIPTION</span></span>
<span data-ttu-id="717a8-108">Das **Get-AzPrivateLinkResource-Cmdlet** ruft alle Verknüpfungsressourcen ab, die zu "PrivateLinkResource" gehören.</span><span class="sxs-lookup"><span data-stu-id="717a8-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="717a8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="717a8-109">EXAMPLES</span></span>

### <span data-ttu-id="717a8-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="717a8-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="717a8-111">In diesem Beispiel werden alle privaten Verknüpfungsressourcen "nbelong" mit dem Sql Server "mySql" aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="717a8-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="717a8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="717a8-112">PARAMETERS</span></span>

### <span data-ttu-id="717a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="717a8-113">-DefaultProfile</span></span>
<span data-ttu-id="717a8-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="717a8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="717a8-115">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="717a8-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="717a8-116">Die Azure-Ressourcen-Manager-ID der Ressource für privaten Link.</span><span class="sxs-lookup"><span data-stu-id="717a8-116">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="717a8-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="717a8-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="717a8-118">Der Ressourcentyp für private Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="717a8-118">The private link resource type.</span></span>

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

### <span data-ttu-id="717a8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="717a8-119">-ResourceGroupName</span></span>
<span data-ttu-id="717a8-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="717a8-120">The resource group name.</span></span>

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

### <span data-ttu-id="717a8-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="717a8-121">-ServiceName</span></span>
<span data-ttu-id="717a8-122">Der Name des privaten Linkdiensts.</span><span class="sxs-lookup"><span data-stu-id="717a8-122">The private link service name.</span></span>

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

### <span data-ttu-id="717a8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="717a8-123">CommonParameters</span></span>
<span data-ttu-id="717a8-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="717a8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="717a8-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="717a8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="717a8-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="717a8-126">INPUTS</span></span>

### <span data-ttu-id="717a8-127">System.String</span><span class="sxs-lookup"><span data-stu-id="717a8-127">System.String</span></span>

## <span data-ttu-id="717a8-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="717a8-128">OUTPUTS</span></span>

### <span data-ttu-id="717a8-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="717a8-129">System.Boolean</span></span>

## <span data-ttu-id="717a8-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="717a8-130">NOTES</span></span>

## <span data-ttu-id="717a8-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="717a8-131">RELATED LINKS</span></span>
