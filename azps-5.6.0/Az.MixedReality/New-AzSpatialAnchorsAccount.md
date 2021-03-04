---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/new-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
ms.openlocfilehash: a2a6dafe9aedfc41200e12bb3c583ad1b5fb02b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927875"
---
# <span data-ttu-id="75195-101">New-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="75195-101">New-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="75195-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75195-102">SYNOPSIS</span></span>
<span data-ttu-id="75195-103">Erstellen eines Kontos für räumliche Anker</span><span class="sxs-lookup"><span data-stu-id="75195-103">Create Spatial Anchors Account</span></span>

## <span data-ttu-id="75195-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75195-104">SYNTAX</span></span>

```
New-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75195-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75195-105">DESCRIPTION</span></span>
<span data-ttu-id="75195-106">Erstellen Sie ein neues Konto für räumliche Anker in bestimmten Abonnements, Ressourcengruppen und Regionen.</span><span class="sxs-lookup"><span data-stu-id="75195-106">Create a new Spatial Anchors Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="75195-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="75195-107">EXAMPLES</span></span>

### <span data-ttu-id="75195-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="75195-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSpatialAnchorsAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="75195-109">Erstellen Sie im aktuellen Abonnement, der Ressourcengruppe "rg1" und "Central US" ein neues Beispiel für das Konto für räumliche Anker.</span><span class="sxs-lookup"><span data-stu-id="75195-109">Create a new Spatial Anchors Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="75195-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="75195-110">PARAMETERS</span></span>

### <span data-ttu-id="75195-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="75195-111">-Confirm</span></span>
<span data-ttu-id="75195-112">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="75195-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75195-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75195-113">-DefaultProfile</span></span>
<span data-ttu-id="75195-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="75195-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75195-115">-Location</span><span class="sxs-lookup"><span data-stu-id="75195-115">-Location</span></span>
<span data-ttu-id="75195-116">Standort des Kontos für räumliche Anker.</span><span class="sxs-lookup"><span data-stu-id="75195-116">Spatial Anchors Account Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75195-117">-Name</span><span class="sxs-lookup"><span data-stu-id="75195-117">-Name</span></span>
<span data-ttu-id="75195-118">Name des Kontos "Räumliche Anker".</span><span class="sxs-lookup"><span data-stu-id="75195-118">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75195-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75195-119">-ResourceGroupName</span></span>
<span data-ttu-id="75195-120">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="75195-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75195-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75195-121">-WhatIf</span></span>
<span data-ttu-id="75195-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75195-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75195-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75195-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75195-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75195-124">CommonParameters</span></span>
<span data-ttu-id="75195-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75195-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="75195-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75195-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75195-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="75195-127">INPUTS</span></span>

### <span data-ttu-id="75195-128">Keine</span><span class="sxs-lookup"><span data-stu-id="75195-128">None</span></span>

## <span data-ttu-id="75195-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="75195-129">OUTPUTS</span></span>

### <span data-ttu-id="75195-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="75195-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="75195-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="75195-131">NOTES</span></span>

## <span data-ttu-id="75195-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="75195-132">RELATED LINKS</span></span>
