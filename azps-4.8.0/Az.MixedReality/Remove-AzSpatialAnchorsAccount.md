---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 5ba079a17dcfb0a263766237adbbec9beb4cc64c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009210"
---
# <span data-ttu-id="fd18c-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="fd18c-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="fd18c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fd18c-102">SYNOPSIS</span></span>
<span data-ttu-id="fd18c-103">Löschen eines Spatial-Anker Kontos</span><span class="sxs-lookup"><span data-stu-id="fd18c-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="fd18c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd18c-104">SYNTAX</span></span>

### <span data-ttu-id="fd18c-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd18c-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd18c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd18c-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd18c-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd18c-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd18c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd18c-108">DESCRIPTION</span></span>
<span data-ttu-id="fd18c-109">Löschen eines angegebenen Spatial-Anker Kontos aus einer bestimmten Abonnement-und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fd18c-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="fd18c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd18c-110">EXAMPLES</span></span>

### <span data-ttu-id="fd18c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fd18c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="fd18c-112">Löschen eines räumlichen Anker Kontos "Beispiel" aus dem aktuellen Abonnement und der Ressourcengruppe "RG1"</span><span class="sxs-lookup"><span data-stu-id="fd18c-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="fd18c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd18c-113">PARAMETERS</span></span>

### <span data-ttu-id="fd18c-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fd18c-114">-Confirm</span></span>
<span data-ttu-id="fd18c-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd18c-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd18c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd18c-116">-DefaultProfile</span></span>
<span data-ttu-id="fd18c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fd18c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd18c-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fd18c-118">-InputObject</span></span>
<span data-ttu-id="fd18c-119">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="fd18c-119">The custom domain object.</span></span>

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

### <span data-ttu-id="fd18c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fd18c-120">-Name</span></span>
<span data-ttu-id="fd18c-121">Konto Name für Spatial-Anker</span><span class="sxs-lookup"><span data-stu-id="fd18c-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="fd18c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd18c-122">-PassThru</span></span>
<span data-ttu-id="fd18c-123">Gibt das Objekt zurück, wenn angegeben.</span><span class="sxs-lookup"><span data-stu-id="fd18c-123">Return object if specified.</span></span>

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

### <span data-ttu-id="fd18c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd18c-124">-ResourceGroupName</span></span>
<span data-ttu-id="fd18c-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fd18c-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="fd18c-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fd18c-126">-ResourceId</span></span>
<span data-ttu-id="fd18c-127">Ressourcen-ID des Spatial-Anker Kontos</span><span class="sxs-lookup"><span data-stu-id="fd18c-127">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="fd18c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd18c-128">-WhatIf</span></span>
<span data-ttu-id="fd18c-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd18c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd18c-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd18c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd18c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd18c-131">CommonParameters</span></span>
<span data-ttu-id="fd18c-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd18c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fd18c-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd18c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd18c-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fd18c-134">INPUTS</span></span>

### <span data-ttu-id="fd18c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="fd18c-135">System.String</span></span>

### <span data-ttu-id="fd18c-136">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="fd18c-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="fd18c-137">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="fd18c-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fd18c-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fd18c-138">OUTPUTS</span></span>

### <span data-ttu-id="fd18c-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd18c-139">System.Boolean</span></span>

## <span data-ttu-id="fd18c-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="fd18c-140">NOTES</span></span>

## <span data-ttu-id="fd18c-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fd18c-141">RELATED LINKS</span></span>
