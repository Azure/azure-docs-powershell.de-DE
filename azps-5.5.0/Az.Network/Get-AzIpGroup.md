---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
ms.openlocfilehash: 11c5e3ff2d8ee548917de7a94b1a592ae4cce52b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156996"
---
# <span data-ttu-id="db406-101">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="db406-101">Get-AzIpGroup</span></span>

## <span data-ttu-id="db406-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db406-102">SYNOPSIS</span></span>
<span data-ttu-id="db406-103">Azure IpGroup erhalten</span><span class="sxs-lookup"><span data-stu-id="db406-103">Get an Azure IpGroup</span></span>

## <span data-ttu-id="db406-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db406-104">SYNTAX</span></span>

### <span data-ttu-id="db406-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="db406-105">IpGroupNameParameterSet</span></span>
```
Get-AzIpGroup -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db406-106">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db406-106">IpGroupResourceIdParameterSet</span></span>
```
Get-AzIpGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db406-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db406-107">DESCRIPTION</span></span>
<span data-ttu-id="db406-108">Das **Cmdlet "Get-AzIpGroup"** erhält eine Azure IpGroup.</span><span class="sxs-lookup"><span data-stu-id="db406-108">The **Get-AzIpGroup** cmdlet gets an Azure IpGroup</span></span>

## <span data-ttu-id="db406-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="db406-109">EXAMPLES</span></span>

### <span data-ttu-id="db406-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="db406-110">Example 1</span></span>
```powershell
Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="db406-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="db406-111">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Get-AzIpGroup -ResourceId $ipGroupId
```

## <span data-ttu-id="db406-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db406-112">PARAMETERS</span></span>

### <span data-ttu-id="db406-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db406-113">-DefaultProfile</span></span>
<span data-ttu-id="db406-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db406-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db406-115">-Name</span><span class="sxs-lookup"><span data-stu-id="db406-115">-Name</span></span>
<span data-ttu-id="db406-116">Der Name der ipgroup.</span><span class="sxs-lookup"><span data-stu-id="db406-116">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db406-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db406-117">-ResourceGroupName</span></span>
<span data-ttu-id="db406-118">Der Ressourcengruppenname der IP-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="db406-118">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db406-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db406-119">-ResourceId</span></span>
<span data-ttu-id="db406-120">ResourceId der ipgroup.</span><span class="sxs-lookup"><span data-stu-id="db406-120">ResourceId of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db406-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db406-121">CommonParameters</span></span>
<span data-ttu-id="db406-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db406-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db406-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db406-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db406-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="db406-124">INPUTS</span></span>

### <span data-ttu-id="db406-125">System.String</span><span class="sxs-lookup"><span data-stu-id="db406-125">System.String</span></span>

## <span data-ttu-id="db406-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="db406-126">OUTPUTS</span></span>

### <span data-ttu-id="db406-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="db406-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="db406-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="db406-128">NOTES</span></span>

## <span data-ttu-id="db406-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="db406-129">RELATED LINKS</span></span>
