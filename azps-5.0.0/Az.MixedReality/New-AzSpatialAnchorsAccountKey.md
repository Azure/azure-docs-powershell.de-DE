---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 35c00fca10223a22d586efba8961dd9cab6b0faf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177513"
---
# <span data-ttu-id="9e3a2-101">New-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="9e3a2-101">New-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="9e3a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9e3a2-102">SYNOPSIS</span></span>
<span data-ttu-id="9e3a2-103">Schlüssel des Spatial-Anker Kontos neu generieren</span><span class="sxs-lookup"><span data-stu-id="9e3a2-103">Regenerate key of Spatial Anchors Account</span></span>

## <span data-ttu-id="9e3a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e3a2-104">SYNTAX</span></span>

### <span data-ttu-id="9e3a2-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e3a2-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e3a2-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e3a2-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e3a2-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e3a2-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e3a2-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e3a2-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e3a2-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e3a2-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e3a2-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e3a2-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e3a2-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e3a2-111">DESCRIPTION</span></span>
<span data-ttu-id="9e3a2-112">Erneutes Generieren des Primärschlüssels oder des sekundären Schlüssels eines Spatial-Anker Kontos</span><span class="sxs-lookup"><span data-stu-id="9e3a2-112">Regenerate primary key or secondary key of Spatial Anchors Account.</span></span>

## <span data-ttu-id="9e3a2-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9e3a2-113">EXAMPLES</span></span>

### <span data-ttu-id="9e3a2-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9e3a2-114">Example 1</span></span>
```powershell
PS C:\> New-AzSpatialAnchorsAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="9e3a2-115">Sekundärer Schlüssel des räumlichen Verankerungs Kontos erneut generieren "Beispiel" in der Ressourcengruppe "RG1".</span><span class="sxs-lookup"><span data-stu-id="9e3a2-115">Regenerate secondary key of Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="9e3a2-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9e3a2-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | New-AzSpatialAnchorsAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="9e3a2-117">Regenerieren des sekundären Schlüssels des räumlichen Anker Kontos "Beispiel" aus dem aktuellen Abonnement und der Ressourcengruppe "RG1" mit Rohrleitungen.</span><span class="sxs-lookup"><span data-stu-id="9e3a2-117">Regenerate secondary key of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="9e3a2-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e3a2-118">PARAMETERS</span></span>

### <span data-ttu-id="9e3a2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e3a2-119">-DefaultProfile</span></span>
<span data-ttu-id="9e3a2-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9e3a2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e3a2-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9e3a2-121">-Force</span></span>
<span data-ttu-id="9e3a2-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="9e3a2-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9e3a2-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9e3a2-123">-InputObject</span></span>
<span data-ttu-id="9e3a2-124">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="9e3a2-124">The custom domain object.</span></span>

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

### <span data-ttu-id="9e3a2-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9e3a2-125">-Name</span></span>
<span data-ttu-id="9e3a2-126">Konto Name für Spatial-Anker</span><span class="sxs-lookup"><span data-stu-id="9e3a2-126">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="9e3a2-127">– Primär</span><span class="sxs-lookup"><span data-stu-id="9e3a2-127">-Primary</span></span>
<span data-ttu-id="9e3a2-128">Primärschlüssel des Spatial-Anker Kontos neu generieren</span><span class="sxs-lookup"><span data-stu-id="9e3a2-128">Regenerate primary key of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="9e3a2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e3a2-129">-ResourceGroupName</span></span>
<span data-ttu-id="9e3a2-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9e3a2-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="9e3a2-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9e3a2-131">-ResourceId</span></span>
<span data-ttu-id="9e3a2-132">Ressourcen-ID des Spatial-Anker Kontos</span><span class="sxs-lookup"><span data-stu-id="9e3a2-132">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="9e3a2-133">-Sekundäre</span><span class="sxs-lookup"><span data-stu-id="9e3a2-133">-Secondary</span></span>
<span data-ttu-id="9e3a2-134">Primärschlüssel des Spatial-Anker Kontos neu generieren</span><span class="sxs-lookup"><span data-stu-id="9e3a2-134">Regenerate primary key of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="9e3a2-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9e3a2-135">-Confirm</span></span>
<span data-ttu-id="9e3a2-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e3a2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e3a2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e3a2-137">-WhatIf</span></span>
<span data-ttu-id="9e3a2-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e3a2-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e3a2-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e3a2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e3a2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e3a2-140">CommonParameters</span></span>
<span data-ttu-id="9e3a2-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e3a2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9e3a2-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e3a2-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e3a2-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9e3a2-143">INPUTS</span></span>

### <span data-ttu-id="9e3a2-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9e3a2-144">System.String</span></span>

### <span data-ttu-id="9e3a2-145">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="9e3a2-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="9e3a2-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9e3a2-146">OUTPUTS</span></span>

### <span data-ttu-id="9e3a2-147">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9e3a2-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="9e3a2-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="9e3a2-148">NOTES</span></span>

## <span data-ttu-id="9e3a2-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9e3a2-149">RELATED LINKS</span></span>
