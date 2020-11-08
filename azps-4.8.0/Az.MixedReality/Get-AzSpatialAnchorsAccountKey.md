---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 81bce36cb1b8cd4737141e58ad3e220199e726cf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010150"
---
# <span data-ttu-id="e8526-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="e8526-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="e8526-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e8526-102">SYNOPSIS</span></span>
<span data-ttu-id="e8526-103">Abrufen von Schlüsseln des Spatial-Anker Kontos</span><span class="sxs-lookup"><span data-stu-id="e8526-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="e8526-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8526-104">SYNTAX</span></span>

### <span data-ttu-id="e8526-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e8526-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8526-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8526-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8526-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8526-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8526-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8526-108">DESCRIPTION</span></span>
<span data-ttu-id="e8526-109">Abrufen von Entwickler Schlüsseln eines Spatial-Anker Kontos</span><span class="sxs-lookup"><span data-stu-id="e8526-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="e8526-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e8526-110">EXAMPLES</span></span>

### <span data-ttu-id="e8526-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e8526-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="e8526-112">Holen Sie sich die Entwickler Schlüssel des Spatial-Anker Kontos "Beispiel" aus dem aktuellen Abonnement und der Ressourcengruppe "RG1".</span><span class="sxs-lookup"><span data-stu-id="e8526-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="e8526-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e8526-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="e8526-114">Holen Sie sich die Entwickler Schlüssel des räumlichen Anker Kontos "Beispiel" aus dem aktuellen Abonnement und der Ressourcengruppe "RG1" mit Rohrleitungen.</span><span class="sxs-lookup"><span data-stu-id="e8526-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="e8526-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8526-115">PARAMETERS</span></span>

### <span data-ttu-id="e8526-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8526-116">-DefaultProfile</span></span>
<span data-ttu-id="e8526-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e8526-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8526-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e8526-118">-InputObject</span></span>
<span data-ttu-id="e8526-119">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="e8526-119">The custom domain object.</span></span>

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

### <span data-ttu-id="e8526-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e8526-120">-Name</span></span>
<span data-ttu-id="e8526-121">Konto Name für Spatial-Anker</span><span class="sxs-lookup"><span data-stu-id="e8526-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="e8526-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8526-122">-ResourceGroupName</span></span>
<span data-ttu-id="e8526-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e8526-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="e8526-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e8526-124">-ResourceId</span></span>
<span data-ttu-id="e8526-125">Ressourcen-ID des Spatial-Anker Kontos</span><span class="sxs-lookup"><span data-stu-id="e8526-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="e8526-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8526-126">CommonParameters</span></span>
<span data-ttu-id="e8526-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8526-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e8526-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8526-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8526-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e8526-129">INPUTS</span></span>

### <span data-ttu-id="e8526-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e8526-130">System.String</span></span>

### <span data-ttu-id="e8526-131">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="e8526-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="e8526-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e8526-132">OUTPUTS</span></span>

### <span data-ttu-id="e8526-133">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e8526-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="e8526-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="e8526-134">NOTES</span></span>

## <span data-ttu-id="e8526-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e8526-135">RELATED LINKS</span></span>
