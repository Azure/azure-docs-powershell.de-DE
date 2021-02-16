---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 35c00fca10223a22d586efba8961dd9cab6b0faf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152249"
---
# <span data-ttu-id="dc0db-101">New-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="dc0db-101">New-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="dc0db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc0db-102">SYNOPSIS</span></span>
<span data-ttu-id="dc0db-103">Schlüssel des Kontos für räumliche Anker erneut erstellen</span><span class="sxs-lookup"><span data-stu-id="dc0db-103">Regenerate key of Spatial Anchors Account</span></span>

## <span data-ttu-id="dc0db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc0db-104">SYNTAX</span></span>

### <span data-ttu-id="dc0db-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc0db-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc0db-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc0db-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc0db-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc0db-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc0db-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc0db-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc0db-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc0db-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc0db-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc0db-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc0db-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc0db-111">DESCRIPTION</span></span>
<span data-ttu-id="dc0db-112">Erstellen Sie den Primärschlüssel oder sekundären Schlüssel des Kontos für räumliche Anker erneut.</span><span class="sxs-lookup"><span data-stu-id="dc0db-112">Regenerate primary key or secondary key of Spatial Anchors Account.</span></span>

## <span data-ttu-id="dc0db-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dc0db-113">EXAMPLES</span></span>

### <span data-ttu-id="dc0db-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dc0db-114">Example 1</span></span>
```powershell
PS C:\> New-AzSpatialAnchorsAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="dc0db-115">Erstellen Sie für "Beispiel" in der Ressourcengruppe "rg1" den sekundären Schlüssel des Räumlichen Ankerkontos erneut.</span><span class="sxs-lookup"><span data-stu-id="dc0db-115">Regenerate secondary key of Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="dc0db-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="dc0db-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | New-AzSpatialAnchorsAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="dc0db-117">Erstellen Sie den sekundären Schlüssel des Räumlichen Ankerkontos "Beispiel" aus der aktuellen Abonnement- und Ressourcengruppe "rg1" mit Piping.</span><span class="sxs-lookup"><span data-stu-id="dc0db-117">Regenerate secondary key of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="dc0db-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc0db-118">PARAMETERS</span></span>

### <span data-ttu-id="dc0db-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc0db-119">-DefaultProfile</span></span>
<span data-ttu-id="dc0db-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc0db-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc0db-121">-Force</span><span class="sxs-lookup"><span data-stu-id="dc0db-121">-Force</span></span>
<span data-ttu-id="dc0db-122">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="dc0db-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0db-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc0db-123">-InputObject</span></span>
<span data-ttu-id="dc0db-124">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="dc0db-124">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineRegeneratePrimaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc0db-125">-Name</span><span class="sxs-lookup"><span data-stu-id="dc0db-125">-Name</span></span>
<span data-ttu-id="dc0db-126">Kontoname für räumliche Anker.</span><span class="sxs-lookup"><span data-stu-id="dc0db-126">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0db-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="dc0db-127">-Primary</span></span>
<span data-ttu-id="dc0db-128">Erstellen Sie den Primärschlüssel des Kontos für räumliche Anker erneut.</span><span class="sxs-lookup"><span data-stu-id="dc0db-128">Regenerate primary key of Spatial Anchors Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegeneratePrimaryKeyParameterSet, ResourceIdRegeneratePrimaryKeyParameterSet, PipelineRegeneratePrimaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0db-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc0db-129">-ResourceGroupName</span></span>
<span data-ttu-id="dc0db-130">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="dc0db-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0db-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc0db-131">-ResourceId</span></span>
<span data-ttu-id="dc0db-132">Ressourcen-ID des Räumlichen Ankerkontos.</span><span class="sxs-lookup"><span data-stu-id="dc0db-132">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdRegeneratePrimaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc0db-133">-Secondary</span><span class="sxs-lookup"><span data-stu-id="dc0db-133">-Secondary</span></span>
<span data-ttu-id="dc0db-134">Erstellen Sie den Primärschlüssel des Kontos für räumliche Anker erneut.</span><span class="sxs-lookup"><span data-stu-id="dc0db-134">Regenerate primary key of Spatial Anchors Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegenerateSecondaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0db-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc0db-135">-Confirm</span></span>
<span data-ttu-id="dc0db-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dc0db-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0db-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="dc0db-137">-WhatIf</span></span>
<span data-ttu-id="dc0db-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc0db-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc0db-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dc0db-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0db-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc0db-140">CommonParameters</span></span>
<span data-ttu-id="dc0db-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc0db-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="dc0db-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc0db-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc0db-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dc0db-143">INPUTS</span></span>

### <span data-ttu-id="dc0db-144">System.String</span><span class="sxs-lookup"><span data-stu-id="dc0db-144">System.String</span></span>

### <span data-ttu-id="dc0db-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="dc0db-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="dc0db-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dc0db-146">OUTPUTS</span></span>

### <span data-ttu-id="dc0db-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="dc0db-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="dc0db-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dc0db-148">NOTES</span></span>

## <span data-ttu-id="dc0db-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dc0db-149">RELATED LINKS</span></span>
