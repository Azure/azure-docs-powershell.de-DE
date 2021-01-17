---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 81bce36cb1b8cd4737141e58ad3e220199e726cf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469351"
---
# <span data-ttu-id="c39ed-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="c39ed-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="c39ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c39ed-102">SYNOPSIS</span></span>
<span data-ttu-id="c39ed-103">Schlüssel des Kontos "Räumliche Anker" erhalten</span><span class="sxs-lookup"><span data-stu-id="c39ed-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="c39ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c39ed-104">SYNTAX</span></span>

### <span data-ttu-id="c39ed-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c39ed-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c39ed-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c39ed-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c39ed-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="c39ed-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c39ed-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c39ed-108">DESCRIPTION</span></span>
<span data-ttu-id="c39ed-109">Holen Sie sich die Entwicklerschlüssel des Räumlichen Ankerkontos.</span><span class="sxs-lookup"><span data-stu-id="c39ed-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="c39ed-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c39ed-110">EXAMPLES</span></span>

### <span data-ttu-id="c39ed-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c39ed-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="c39ed-112">Holen Sie sich die Entwicklerschlüssel des Räumlichen Ankerkontos "Beispiel" aus der aktuellen Abonnement- und Ressourcengruppe "rg1".</span><span class="sxs-lookup"><span data-stu-id="c39ed-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="c39ed-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c39ed-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="c39ed-114">Holen Sie sich die Entwicklerschlüssel des Räumlichen Ankerkontos "Beispiel" aus der aktuellen Abonnement- und Ressourcengruppe "rg1" mit Piping.</span><span class="sxs-lookup"><span data-stu-id="c39ed-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="c39ed-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c39ed-115">PARAMETERS</span></span>

### <span data-ttu-id="c39ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c39ed-116">-DefaultProfile</span></span>
<span data-ttu-id="c39ed-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c39ed-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c39ed-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c39ed-118">-InputObject</span></span>
<span data-ttu-id="c39ed-119">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="c39ed-119">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c39ed-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c39ed-120">-Name</span></span>
<span data-ttu-id="c39ed-121">Kontoname für räumliche Anker.</span><span class="sxs-lookup"><span data-stu-id="c39ed-121">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c39ed-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c39ed-122">-ResourceGroupName</span></span>
<span data-ttu-id="c39ed-123">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="c39ed-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c39ed-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c39ed-124">-ResourceId</span></span>
<span data-ttu-id="c39ed-125">Ressourcen-ID des Räumlichen Ankerkontos.</span><span class="sxs-lookup"><span data-stu-id="c39ed-125">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c39ed-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c39ed-126">CommonParameters</span></span>
<span data-ttu-id="c39ed-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c39ed-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c39ed-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c39ed-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c39ed-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c39ed-129">INPUTS</span></span>

### <span data-ttu-id="c39ed-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c39ed-130">System.String</span></span>

### <span data-ttu-id="c39ed-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="c39ed-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="c39ed-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c39ed-132">OUTPUTS</span></span>

### <span data-ttu-id="c39ed-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c39ed-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="c39ed-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c39ed-134">NOTES</span></span>

## <span data-ttu-id="c39ed-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c39ed-135">RELATED LINKS</span></span>
