---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
ms.openlocfilehash: d7f52ded01ce5b785c1e935ba8d3ebf4b1c0a5fa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472110"
---
# <span data-ttu-id="4d9ff-101">Update-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="4d9ff-101">Update-AzVirtualRouter</span></span>

## <span data-ttu-id="4d9ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d9ff-102">SYNOPSIS</span></span>
<span data-ttu-id="4d9ff-103">Aktualisiert einen virtuellen Router.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-103">Updates a Virtual Router.</span></span> 

## <span data-ttu-id="4d9ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d9ff-104">SYNTAX</span></span>

### <span data-ttu-id="4d9ff-105">VirtualRouterNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4d9ff-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d9ff-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d9ff-106">VirtualRouterResourceIdParameterSet</span></span>
```
Update-AzVirtualRouter [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d9ff-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d9ff-107">DESCRIPTION</span></span>
<span data-ttu-id="4d9ff-108">Aktualisiert den virtuellen Router, um den Verzweigungs-zu-Verzweigungsverkehr zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-108">Updates Virtual Router to enable or disable branch to branch traffic.</span></span>

## <span data-ttu-id="4d9ff-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4d9ff-109">EXAMPLES</span></span>

### <span data-ttu-id="4d9ff-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4d9ff-110">Example 1</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName -AllowBranchToBranchTraffic
```

<span data-ttu-id="4d9ff-111">Aktualisiert den virtuellen Router, um Verzweigungs-zu-Verzweigungsverkehr zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-111">Updates the Virtual Router to allow branch to branch traffic</span></span>

### <span data-ttu-id="4d9ff-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4d9ff-112">Example 2</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName
```

<span data-ttu-id="4d9ff-113">Aktualisiert den virtuellen Router, um den Verzweigungs-zu-Verzweigungsverkehr zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-113">Updates the Virtual Router to block branch to branch traffic</span></span>

## <span data-ttu-id="4d9ff-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d9ff-114">PARAMETERS</span></span>

### <span data-ttu-id="4d9ff-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="4d9ff-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="4d9ff-116">Kennzeichnen Sie das Flag, um Verzweigungs-zu-Verzweigungsverkehr für den virtuellen Router zu erlauben.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-116">Flag to allow branch to branch traffic for virtual router.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9ff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d9ff-117">-DefaultProfile</span></span>
<span data-ttu-id="4d9ff-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d9ff-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d9ff-119">-ResourceGroupName</span></span>
<span data-ttu-id="4d9ff-120">Der Ressourcengruppenname des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-120">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d9ff-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d9ff-121">-ResourceId</span></span>
<span data-ttu-id="4d9ff-122">ResourceId des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-122">ResourceId of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d9ff-123">-RouterName</span><span class="sxs-lookup"><span data-stu-id="4d9ff-123">-RouterName</span></span>
<span data-ttu-id="4d9ff-124">Der Name des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-124">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d9ff-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d9ff-125">CommonParameters</span></span>
<span data-ttu-id="4d9ff-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d9ff-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d9ff-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d9ff-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d9ff-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4d9ff-128">INPUTS</span></span>

### <span data-ttu-id="4d9ff-129">System.String</span><span class="sxs-lookup"><span data-stu-id="4d9ff-129">System.String</span></span>

## <span data-ttu-id="4d9ff-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4d9ff-130">OUTPUTS</span></span>

### <span data-ttu-id="4d9ff-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="4d9ff-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="4d9ff-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4d9ff-132">NOTES</span></span>

## <span data-ttu-id="4d9ff-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4d9ff-133">RELATED LINKS</span></span>
