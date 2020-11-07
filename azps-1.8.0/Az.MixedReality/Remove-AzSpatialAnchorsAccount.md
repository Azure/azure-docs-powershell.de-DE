---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 2d164e08876b5489ec45ce146f4f3c7cee3ee6d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819031"
---
# <span data-ttu-id="12d98-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="12d98-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="12d98-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12d98-102">SYNOPSIS</span></span>
<span data-ttu-id="12d98-103">Löschen eines Spatial-Anker Kontos</span><span class="sxs-lookup"><span data-stu-id="12d98-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="12d98-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12d98-104">SYNTAX</span></span>

### <span data-ttu-id="12d98-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="12d98-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12d98-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12d98-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12d98-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="12d98-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12d98-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12d98-108">DESCRIPTION</span></span>
<span data-ttu-id="12d98-109">Löschen eines angegebenen Spatial-Anker Kontos aus einer bestimmten Abonnement-und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="12d98-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="12d98-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12d98-110">EXAMPLES</span></span>

### <span data-ttu-id="12d98-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="12d98-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="12d98-112">Löschen eines räumlichen Anker Kontos "Beispiel" aus dem aktuellen Abonnement und der Ressourcengruppe "RG1"</span><span class="sxs-lookup"><span data-stu-id="12d98-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="12d98-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="12d98-113">PARAMETERS</span></span>

### <span data-ttu-id="12d98-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="12d98-114">-Confirm</span></span>
<span data-ttu-id="12d98-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12d98-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12d98-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12d98-116">-DefaultProfile</span></span>
<span data-ttu-id="12d98-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="12d98-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12d98-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="12d98-118">-InputObject</span></span>
<span data-ttu-id="12d98-119">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="12d98-119">The custom domain object.</span></span>

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

### <span data-ttu-id="12d98-120">-Name</span><span class="sxs-lookup"><span data-stu-id="12d98-120">-Name</span></span>
<span data-ttu-id="12d98-121">Konto Name für Spatial-Anker</span><span class="sxs-lookup"><span data-stu-id="12d98-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="12d98-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12d98-122">-PassThru</span></span>
<span data-ttu-id="12d98-123">Gibt das Objekt zurück, wenn angegeben.</span><span class="sxs-lookup"><span data-stu-id="12d98-123">Return object if specified.</span></span>

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

### <span data-ttu-id="12d98-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12d98-124">-ResourceGroupName</span></span>
<span data-ttu-id="12d98-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="12d98-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="12d98-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="12d98-126">-ResourceId</span></span>
<span data-ttu-id="12d98-127">Ressourcen-ID des Spatial-Anker Kontos</span><span class="sxs-lookup"><span data-stu-id="12d98-127">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="12d98-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12d98-128">-WhatIf</span></span>
<span data-ttu-id="12d98-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12d98-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12d98-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12d98-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12d98-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12d98-131">CommonParameters</span></span>
<span data-ttu-id="12d98-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12d98-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="12d98-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12d98-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12d98-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12d98-134">INPUTS</span></span>

### <span data-ttu-id="12d98-135">System. String</span><span class="sxs-lookup"><span data-stu-id="12d98-135">System.String</span></span>

### <span data-ttu-id="12d98-136">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="12d98-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="12d98-137">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="12d98-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="12d98-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12d98-138">OUTPUTS</span></span>

### <span data-ttu-id="12d98-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="12d98-139">System.Boolean</span></span>

## <span data-ttu-id="12d98-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="12d98-140">NOTES</span></span>

## <span data-ttu-id="12d98-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12d98-141">RELATED LINKS</span></span>
