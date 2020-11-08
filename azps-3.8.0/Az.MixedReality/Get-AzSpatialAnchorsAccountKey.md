---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: c5fc1c497bc0cb6f73aab4ddcfbc1ce127cc4545
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004722"
---
# <span data-ttu-id="74f8b-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="74f8b-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="74f8b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="74f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="74f8b-103">Abrufen von Schlüsseln des Spatial-Anker Kontos</span><span class="sxs-lookup"><span data-stu-id="74f8b-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="74f8b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="74f8b-104">SYNTAX</span></span>

### <span data-ttu-id="74f8b-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="74f8b-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74f8b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74f8b-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74f8b-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="74f8b-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74f8b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74f8b-108">DESCRIPTION</span></span>
<span data-ttu-id="74f8b-109">Abrufen von Entwickler Schlüsseln eines Spatial-Anker Kontos</span><span class="sxs-lookup"><span data-stu-id="74f8b-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="74f8b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="74f8b-110">EXAMPLES</span></span>

### <span data-ttu-id="74f8b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="74f8b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="74f8b-112">Holen Sie sich die Entwickler Schlüssel des Spatial-Anker Kontos "Beispiel" aus dem aktuellen Abonnement und der Ressourcengruppe "RG1".</span><span class="sxs-lookup"><span data-stu-id="74f8b-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="74f8b-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="74f8b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="74f8b-114">Holen Sie sich die Entwickler Schlüssel des räumlichen Anker Kontos "Beispiel" aus dem aktuellen Abonnement und der Ressourcengruppe "RG1" mit Rohrleitungen.</span><span class="sxs-lookup"><span data-stu-id="74f8b-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="74f8b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="74f8b-115">PARAMETERS</span></span>

### <span data-ttu-id="74f8b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74f8b-116">-DefaultProfile</span></span>
<span data-ttu-id="74f8b-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="74f8b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74f8b-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="74f8b-118">-InputObject</span></span>
<span data-ttu-id="74f8b-119">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="74f8b-119">The custom domain object.</span></span>

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

### <span data-ttu-id="74f8b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="74f8b-120">-Name</span></span>
<span data-ttu-id="74f8b-121">Konto Name für Spatial-Anker</span><span class="sxs-lookup"><span data-stu-id="74f8b-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="74f8b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74f8b-122">-ResourceGroupName</span></span>
<span data-ttu-id="74f8b-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="74f8b-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="74f8b-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="74f8b-124">-ResourceId</span></span>
<span data-ttu-id="74f8b-125">Ressourcen-ID des Spatial-Anker Kontos</span><span class="sxs-lookup"><span data-stu-id="74f8b-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="74f8b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f8b-126">CommonParameters</span></span>
<span data-ttu-id="74f8b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74f8b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="74f8b-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74f8b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f8b-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="74f8b-129">INPUTS</span></span>

### <span data-ttu-id="74f8b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="74f8b-130">System.String</span></span>

### <span data-ttu-id="74f8b-131">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="74f8b-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="74f8b-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="74f8b-132">OUTPUTS</span></span>

### <span data-ttu-id="74f8b-133">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="74f8b-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccountKeys</span></span>

## <span data-ttu-id="74f8b-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="74f8b-134">NOTES</span></span>

## <span data-ttu-id="74f8b-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="74f8b-135">RELATED LINKS</span></span>
