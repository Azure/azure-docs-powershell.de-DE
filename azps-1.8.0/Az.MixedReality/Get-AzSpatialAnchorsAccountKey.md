---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: ec84b4def7b1dfd19b2c85c71dc6562fa4cae763
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819035"
---
# <span data-ttu-id="6d9cb-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="6d9cb-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="6d9cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6d9cb-102">SYNOPSIS</span></span>
<span data-ttu-id="6d9cb-103">Abrufen von Schlüsseln des Spatial-Anker Kontos</span><span class="sxs-lookup"><span data-stu-id="6d9cb-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="6d9cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d9cb-104">SYNTAX</span></span>

### <span data-ttu-id="6d9cb-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6d9cb-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d9cb-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d9cb-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d9cb-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d9cb-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d9cb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d9cb-108">DESCRIPTION</span></span>
<span data-ttu-id="6d9cb-109">Abrufen von Entwickler Schlüsseln eines Spatial-Anker Kontos</span><span class="sxs-lookup"><span data-stu-id="6d9cb-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="6d9cb-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6d9cb-110">EXAMPLES</span></span>

### <span data-ttu-id="6d9cb-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6d9cb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="6d9cb-112">Holen Sie sich die Entwickler Schlüssel des Spatial-Anker Kontos "Beispiel" aus dem aktuellen Abonnement und der Ressourcengruppe "RG1".</span><span class="sxs-lookup"><span data-stu-id="6d9cb-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="6d9cb-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6d9cb-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="6d9cb-114">Holen Sie sich die Entwickler Schlüssel des räumlichen Anker Kontos "Beispiel" aus dem aktuellen Abonnement und der Ressourcengruppe "RG1" mit Rohrleitungen.</span><span class="sxs-lookup"><span data-stu-id="6d9cb-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="6d9cb-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d9cb-115">PARAMETERS</span></span>

### <span data-ttu-id="6d9cb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d9cb-116">-DefaultProfile</span></span>
<span data-ttu-id="6d9cb-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6d9cb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d9cb-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6d9cb-118">-InputObject</span></span>
<span data-ttu-id="6d9cb-119">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="6d9cb-119">The custom domain object.</span></span>

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

### <span data-ttu-id="6d9cb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6d9cb-120">-Name</span></span>
<span data-ttu-id="6d9cb-121">Konto Name für Spatial-Anker</span><span class="sxs-lookup"><span data-stu-id="6d9cb-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="6d9cb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d9cb-122">-ResourceGroupName</span></span>
<span data-ttu-id="6d9cb-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6d9cb-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="6d9cb-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6d9cb-124">-ResourceId</span></span>
<span data-ttu-id="6d9cb-125">Ressourcen-ID des Spatial-Anker Kontos</span><span class="sxs-lookup"><span data-stu-id="6d9cb-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="6d9cb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d9cb-126">CommonParameters</span></span>
<span data-ttu-id="6d9cb-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d9cb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6d9cb-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d9cb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d9cb-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6d9cb-129">INPUTS</span></span>

### <span data-ttu-id="6d9cb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6d9cb-130">System.String</span></span>

### <span data-ttu-id="6d9cb-131">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="6d9cb-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="6d9cb-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6d9cb-132">OUTPUTS</span></span>

### <span data-ttu-id="6d9cb-133">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6d9cb-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccountKeys</span></span>

## <span data-ttu-id="6d9cb-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="6d9cb-134">NOTES</span></span>

## <span data-ttu-id="6d9cb-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6d9cb-135">RELATED LINKS</span></span>
