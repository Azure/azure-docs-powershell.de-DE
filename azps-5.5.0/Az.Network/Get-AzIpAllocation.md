---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
ms.openlocfilehash: 89a0276a94ffa2729c5803a017e297ff05e84534
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157004"
---
# <span data-ttu-id="4a97b-101">Get-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="4a97b-101">Get-AzIpAllocation</span></span>

## <span data-ttu-id="4a97b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a97b-102">SYNOPSIS</span></span>
<span data-ttu-id="4a97b-103">Ruft eine Azure IpAllocation ab.</span><span class="sxs-lookup"><span data-stu-id="4a97b-103">Gets a Azure IpAllocation.</span></span>

## <span data-ttu-id="4a97b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a97b-104">SYNTAX</span></span>

### <span data-ttu-id="4a97b-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a97b-105">GetByNameParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a97b-106">ListParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a97b-106">ListParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a97b-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a97b-107">GetByResourceIdParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a97b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a97b-108">DESCRIPTION</span></span>
<span data-ttu-id="4a97b-109">Das **Cmdlet "Get-AzIpAllocation"** erhält eine Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="4a97b-109">The **Get-AzIpAllocation** cmdlet gets an Azure IpAllocation</span></span>

## <span data-ttu-id="4a97b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4a97b-110">EXAMPLES</span></span>

### <span data-ttu-id="4a97b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4a97b-111">Example 1</span></span>
```powershell
Get-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="4a97b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a97b-112">PARAMETERS</span></span>

### <span data-ttu-id="4a97b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a97b-113">-DefaultProfile</span></span>
<span data-ttu-id="4a97b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a97b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a97b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4a97b-115">-Name</span></span>
<span data-ttu-id="4a97b-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="4a97b-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a97b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a97b-117">-ResourceGroupName</span></span>
<span data-ttu-id="4a97b-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4a97b-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a97b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a97b-119">-ResourceId</span></span>
<span data-ttu-id="4a97b-120">IpAllocation-ID</span><span class="sxs-lookup"><span data-stu-id="4a97b-120">IpAllocation Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a97b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a97b-121">CommonParameters</span></span>
<span data-ttu-id="4a97b-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a97b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a97b-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a97b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a97b-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4a97b-124">INPUTS</span></span>

### <span data-ttu-id="4a97b-125">System.String</span><span class="sxs-lookup"><span data-stu-id="4a97b-125">System.String</span></span>

## <span data-ttu-id="4a97b-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4a97b-126">OUTPUTS</span></span>

### <span data-ttu-id="4a97b-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="4a97b-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="4a97b-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4a97b-128">NOTES</span></span>

## <span data-ttu-id="4a97b-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4a97b-129">RELATED LINKS</span></span>
