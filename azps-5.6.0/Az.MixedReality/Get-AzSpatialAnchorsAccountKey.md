---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 351b7a2412a861fcebc456d165e9fc4eddea5122
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921147"
---
# <span data-ttu-id="9d28e-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="9d28e-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="9d28e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d28e-102">SYNOPSIS</span></span>
<span data-ttu-id="9d28e-103">Schlüssel des Kontos "Räumliche Anker" erhalten</span><span class="sxs-lookup"><span data-stu-id="9d28e-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="9d28e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d28e-104">SYNTAX</span></span>

### <span data-ttu-id="9d28e-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9d28e-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d28e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d28e-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d28e-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d28e-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d28e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d28e-108">DESCRIPTION</span></span>
<span data-ttu-id="9d28e-109">Holen Sie sich Entwicklerschlüssel für das Spatial Anchors-Konto.</span><span class="sxs-lookup"><span data-stu-id="9d28e-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="9d28e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9d28e-110">EXAMPLES</span></span>

### <span data-ttu-id="9d28e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9d28e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="9d28e-112">Holen Sie sich Entwicklerschlüssel des "Beispiels" für das Spatial Anchors-Konto aus dem aktuellen Abonnement und der Ressourcengruppe "rg1".</span><span class="sxs-lookup"><span data-stu-id="9d28e-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="9d28e-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9d28e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="9d28e-114">Holen Sie sich Entwicklerschlüssel des "Beispiels" für das Spatial Anchors-Konto aus dem aktuellen Abonnement und der Ressourcengruppe "rg1" mit Piping.</span><span class="sxs-lookup"><span data-stu-id="9d28e-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="9d28e-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9d28e-115">PARAMETERS</span></span>

### <span data-ttu-id="9d28e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d28e-116">-DefaultProfile</span></span>
<span data-ttu-id="9d28e-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d28e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d28e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d28e-118">-InputObject</span></span>
<span data-ttu-id="9d28e-119">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="9d28e-119">The custom domain object.</span></span>

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

### <span data-ttu-id="9d28e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9d28e-120">-Name</span></span>
<span data-ttu-id="9d28e-121">Name des Kontos "Räumliche Anker".</span><span class="sxs-lookup"><span data-stu-id="9d28e-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="9d28e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d28e-122">-ResourceGroupName</span></span>
<span data-ttu-id="9d28e-123">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="9d28e-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="9d28e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d28e-124">-ResourceId</span></span>
<span data-ttu-id="9d28e-125">Ressourcen-ID des Kontos für räumliche Anker.</span><span class="sxs-lookup"><span data-stu-id="9d28e-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="9d28e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d28e-126">CommonParameters</span></span>
<span data-ttu-id="9d28e-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d28e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9d28e-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d28e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d28e-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9d28e-129">INPUTS</span></span>

### <span data-ttu-id="9d28e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9d28e-130">System.String</span></span>

### <span data-ttu-id="9d28e-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="9d28e-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="9d28e-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9d28e-132">OUTPUTS</span></span>

### <span data-ttu-id="9d28e-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9d28e-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="9d28e-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9d28e-134">NOTES</span></span>

## <span data-ttu-id="9d28e-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9d28e-135">RELATED LINKS</span></span>
