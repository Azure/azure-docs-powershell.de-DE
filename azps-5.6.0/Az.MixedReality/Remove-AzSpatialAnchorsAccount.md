---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 502b7b7c97752758003c1a7f0ad007e3e6cf67e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932800"
---
# <span data-ttu-id="72db7-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="72db7-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="72db7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72db7-102">SYNOPSIS</span></span>
<span data-ttu-id="72db7-103">Löschen eines Kontos für räumliche Anker</span><span class="sxs-lookup"><span data-stu-id="72db7-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="72db7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72db7-104">SYNTAX</span></span>

### <span data-ttu-id="72db7-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="72db7-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72db7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="72db7-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72db7-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="72db7-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72db7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72db7-108">DESCRIPTION</span></span>
<span data-ttu-id="72db7-109">Löschen Sie das angegebene Konto für räumliche Anker aus einer bestimmten Abonnement- und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="72db7-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="72db7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="72db7-110">EXAMPLES</span></span>

### <span data-ttu-id="72db7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="72db7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="72db7-112">Löschen Sie das Konto "Beispiel" für räumliche Anker aus dem aktuellen Abonnement und der Ressourcengruppe "rg1".</span><span class="sxs-lookup"><span data-stu-id="72db7-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="72db7-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="72db7-113">PARAMETERS</span></span>

### <span data-ttu-id="72db7-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="72db7-114">-Confirm</span></span>
<span data-ttu-id="72db7-115">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72db7-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72db7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72db7-116">-DefaultProfile</span></span>
<span data-ttu-id="72db7-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72db7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72db7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72db7-118">-InputObject</span></span>
<span data-ttu-id="72db7-119">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="72db7-119">The custom domain object.</span></span>

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

### <span data-ttu-id="72db7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="72db7-120">-Name</span></span>
<span data-ttu-id="72db7-121">Name des Kontos "Räumliche Anker".</span><span class="sxs-lookup"><span data-stu-id="72db7-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="72db7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72db7-122">-PassThru</span></span>
<span data-ttu-id="72db7-123">Rückgabeobjekt, wenn angegeben.</span><span class="sxs-lookup"><span data-stu-id="72db7-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72db7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72db7-124">-ResourceGroupName</span></span>
<span data-ttu-id="72db7-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="72db7-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="72db7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72db7-126">-ResourceId</span></span>
<span data-ttu-id="72db7-127">Ressourcen-ID des Kontos für räumliche Anker.</span><span class="sxs-lookup"><span data-stu-id="72db7-127">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="72db7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72db7-128">-WhatIf</span></span>
<span data-ttu-id="72db7-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72db7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72db7-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72db7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72db7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72db7-131">CommonParameters</span></span>
<span data-ttu-id="72db7-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72db7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="72db7-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72db7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72db7-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="72db7-134">INPUTS</span></span>

### <span data-ttu-id="72db7-135">System.String</span><span class="sxs-lookup"><span data-stu-id="72db7-135">System.String</span></span>

### <span data-ttu-id="72db7-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="72db7-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="72db7-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="72db7-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="72db7-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="72db7-138">OUTPUTS</span></span>

### <span data-ttu-id="72db7-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="72db7-139">System.Boolean</span></span>

## <span data-ttu-id="72db7-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="72db7-140">NOTES</span></span>

## <span data-ttu-id="72db7-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="72db7-141">RELATED LINKS</span></span>
