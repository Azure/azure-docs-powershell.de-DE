---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 5ba079a17dcfb0a263766237adbbec9beb4cc64c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170304"
---
# <span data-ttu-id="f2737-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="f2737-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="f2737-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2737-102">SYNOPSIS</span></span>
<span data-ttu-id="f2737-103">Konto "Räumliche Anker löschen"</span><span class="sxs-lookup"><span data-stu-id="f2737-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="f2737-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2737-104">SYNTAX</span></span>

### <span data-ttu-id="f2737-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f2737-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2737-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2737-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2737-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2737-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2737-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2737-108">DESCRIPTION</span></span>
<span data-ttu-id="f2737-109">Löschen Sie das angegebene Räumliche Ankerkonto aus bestimmten Abonnements und Ressourcengruppen.</span><span class="sxs-lookup"><span data-stu-id="f2737-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="f2737-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f2737-110">EXAMPLES</span></span>

### <span data-ttu-id="f2737-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f2737-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="f2737-112">Löschen Sie "Beispiel" "Räumliche Anker" aus der aktuellen Abonnement- und Ressourcengruppe "rg1".</span><span class="sxs-lookup"><span data-stu-id="f2737-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="f2737-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2737-113">PARAMETERS</span></span>

### <span data-ttu-id="f2737-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2737-114">-Confirm</span></span>
<span data-ttu-id="f2737-115">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2737-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2737-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2737-116">-DefaultProfile</span></span>
<span data-ttu-id="f2737-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2737-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2737-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2737-118">-InputObject</span></span>
<span data-ttu-id="f2737-119">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="f2737-119">The custom domain object.</span></span>

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

### <span data-ttu-id="f2737-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f2737-120">-Name</span></span>
<span data-ttu-id="f2737-121">Kontoname für räumliche Anker.</span><span class="sxs-lookup"><span data-stu-id="f2737-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="f2737-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2737-122">-PassThru</span></span>
<span data-ttu-id="f2737-123">Rückgabeobjekt bei Angabe</span><span class="sxs-lookup"><span data-stu-id="f2737-123">Return object if specified.</span></span>

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

### <span data-ttu-id="f2737-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2737-124">-ResourceGroupName</span></span>
<span data-ttu-id="f2737-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="f2737-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="f2737-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2737-126">-ResourceId</span></span>
<span data-ttu-id="f2737-127">Ressourcen-ID des Räumlichen Ankerkontos.</span><span class="sxs-lookup"><span data-stu-id="f2737-127">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="f2737-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f2737-128">-WhatIf</span></span>
<span data-ttu-id="f2737-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2737-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2737-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2737-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2737-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2737-131">CommonParameters</span></span>
<span data-ttu-id="f2737-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2737-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f2737-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2737-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2737-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f2737-134">INPUTS</span></span>

### <span data-ttu-id="f2737-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f2737-135">System.String</span></span>

### <span data-ttu-id="f2737-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="f2737-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="f2737-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f2737-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f2737-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f2737-138">OUTPUTS</span></span>

### <span data-ttu-id="f2737-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f2737-139">System.Boolean</span></span>

## <span data-ttu-id="f2737-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f2737-140">NOTES</span></span>

## <span data-ttu-id="f2737-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f2737-141">RELATED LINKS</span></span>
