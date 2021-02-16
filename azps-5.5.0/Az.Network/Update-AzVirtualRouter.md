---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
ms.openlocfilehash: d7f52ded01ce5b785c1e935ba8d3ebf4b1c0a5fa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160505"
---
# <span data-ttu-id="9d949-101">Update-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="9d949-101">Update-AzVirtualRouter</span></span>

## <span data-ttu-id="9d949-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d949-102">SYNOPSIS</span></span>
<span data-ttu-id="9d949-103">Aktualisiert einen virtuellen Router.</span><span class="sxs-lookup"><span data-stu-id="9d949-103">Updates a Virtual Router.</span></span> 

## <span data-ttu-id="9d949-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d949-104">SYNTAX</span></span>

### <span data-ttu-id="9d949-105">VirtualRouterNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9d949-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d949-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d949-106">VirtualRouterResourceIdParameterSet</span></span>
```
Update-AzVirtualRouter [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d949-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d949-107">DESCRIPTION</span></span>
<span data-ttu-id="9d949-108">Aktualisiert den virtuellen Router, um den Verzweigungs-zu-Verzweigungsverkehr zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="9d949-108">Updates Virtual Router to enable or disable branch to branch traffic.</span></span>

## <span data-ttu-id="9d949-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9d949-109">EXAMPLES</span></span>

### <span data-ttu-id="9d949-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9d949-110">Example 1</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName -AllowBranchToBranchTraffic
```

<span data-ttu-id="9d949-111">Aktualisiert den virtuellen Router, um Verzweigungs-zu-Verzweigungsverkehr zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="9d949-111">Updates the Virtual Router to allow branch to branch traffic</span></span>

### <span data-ttu-id="9d949-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9d949-112">Example 2</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName
```

<span data-ttu-id="9d949-113">Aktualisiert den virtuellen Router, um den Verzweigungs-zu-Verzweigungsverkehr zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="9d949-113">Updates the Virtual Router to block branch to branch traffic</span></span>

## <span data-ttu-id="9d949-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d949-114">PARAMETERS</span></span>

### <span data-ttu-id="9d949-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="9d949-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="9d949-116">Flag zum Zulassen des Verzweigungs-zu-Verzweigungsverkehrs für den virtuellen Router.</span><span class="sxs-lookup"><span data-stu-id="9d949-116">Flag to allow branch to branch traffic for virtual router.</span></span>

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

### <span data-ttu-id="9d949-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d949-117">-DefaultProfile</span></span>
<span data-ttu-id="9d949-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d949-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d949-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d949-119">-ResourceGroupName</span></span>
<span data-ttu-id="9d949-120">Der Ressourcengruppenname des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="9d949-120">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="9d949-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d949-121">-ResourceId</span></span>
<span data-ttu-id="9d949-122">ResourceId des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="9d949-122">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="9d949-123">-RouterName</span><span class="sxs-lookup"><span data-stu-id="9d949-123">-RouterName</span></span>
<span data-ttu-id="9d949-124">Der Name des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="9d949-124">The name of the virtual router.</span></span>

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

### <span data-ttu-id="9d949-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d949-125">CommonParameters</span></span>
<span data-ttu-id="9d949-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d949-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d949-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d949-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d949-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9d949-128">INPUTS</span></span>

### <span data-ttu-id="9d949-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9d949-129">System.String</span></span>

## <span data-ttu-id="9d949-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9d949-130">OUTPUTS</span></span>

### <span data-ttu-id="9d949-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="9d949-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="9d949-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9d949-132">NOTES</span></span>

## <span data-ttu-id="9d949-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9d949-133">RELATED LINKS</span></span>
