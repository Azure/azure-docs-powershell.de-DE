---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
ms.openlocfilehash: a0a1ab176c4e38e961f78e0230a46bc2eaea964a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384585"
---
# <span data-ttu-id="a8261-101">Set-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="a8261-101">Set-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="a8261-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8261-102">SYNOPSIS</span></span>
<span data-ttu-id="a8261-103">Legt einen registrierten ASN aus der übergeordneten Peeringressource fest oder aktualisiert den AsN.</span><span class="sxs-lookup"><span data-stu-id="a8261-103">Sets or updates a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="a8261-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a8261-104">SYNTAX</span></span>

### <span data-ttu-id="a8261-105">ByResourceGroupAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a8261-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8261-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a8261-106">InputObject</span></span>
```
Set-AzPeeringRegisteredAsn -InputObject <PSPeeringRegisteredAsn> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8261-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a8261-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8261-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a8261-108">DESCRIPTION</span></span>
<span data-ttu-id="a8261-109">Ermöglicht die Aktualisierung eines registrierten ASNs aus der übergeordneten Peeringressource.</span><span class="sxs-lookup"><span data-stu-id="a8261-109">Allows the updating of a registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="a8261-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a8261-110">EXAMPLES</span></span>

### <span data-ttu-id="a8261-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a8261-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredAsn -ResourceId $resourceId -Asn $asn
```

<span data-ttu-id="a8261-112">Aktualisiert den ASN nach Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a8261-112">Updates the ASN by resource id.</span></span>

## <span data-ttu-id="a8261-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8261-113">PARAMETERS</span></span>

### <span data-ttu-id="a8261-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8261-114">-AsJob</span></span>
<span data-ttu-id="a8261-115">Führen Sie die Ausführung im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="a8261-115">Run in the background.</span></span>

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

### <span data-ttu-id="a8261-116">-Asn</span><span class="sxs-lookup"><span data-stu-id="a8261-116">-Asn</span></span>
<span data-ttu-id="a8261-117">Der zu registrierte ASN</span><span class="sxs-lookup"><span data-stu-id="a8261-117">The ASN to be registered</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8261-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8261-118">-DefaultProfile</span></span>
<span data-ttu-id="a8261-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a8261-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8261-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8261-120">-InputObject</span></span>
<span data-ttu-id="a8261-121">Verwenden eines Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="a8261-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8261-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a8261-122">-Name</span></span>
<span data-ttu-id="a8261-123">Der zu registrierte ASN</span><span class="sxs-lookup"><span data-stu-id="a8261-123">The ASN to be registered</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, ByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8261-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="a8261-124">-PeeringName</span></span>
<span data-ttu-id="a8261-125">Der eindeutige Name von PSPeering.</span><span class="sxs-lookup"><span data-stu-id="a8261-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8261-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8261-126">-ResourceGroupName</span></span>
<span data-ttu-id="a8261-127">Der Name einer vorhandenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a8261-127">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8261-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8261-128">-ResourceId</span></span>
<span data-ttu-id="a8261-129">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a8261-129">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8261-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8261-130">-Confirm</span></span>
<span data-ttu-id="a8261-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a8261-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8261-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a8261-132">-WhatIf</span></span>
<span data-ttu-id="a8261-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8261-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8261-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a8261-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8261-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8261-135">CommonParameters</span></span>
<span data-ttu-id="a8261-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8261-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8261-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8261-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8261-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a8261-138">INPUTS</span></span>

### <span data-ttu-id="a8261-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="a8261-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

### <span data-ttu-id="a8261-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a8261-140">System.String</span></span>

## <span data-ttu-id="a8261-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a8261-141">OUTPUTS</span></span>

### <span data-ttu-id="a8261-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="a8261-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="a8261-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a8261-143">NOTES</span></span>

## <span data-ttu-id="a8261-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a8261-144">RELATED LINKS</span></span>
