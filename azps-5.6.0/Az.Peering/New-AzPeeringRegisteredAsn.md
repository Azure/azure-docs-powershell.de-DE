---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
ms.openlocfilehash: 8d5567d99d7ba7470fb44738bed128d8a438c733
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937648"
---
# <span data-ttu-id="4a220-101">New-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="4a220-101">New-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="4a220-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a220-102">SYNOPSIS</span></span>
<span data-ttu-id="4a220-103">Erstellen eines registrierten ASNs für Peering</span><span class="sxs-lookup"><span data-stu-id="4a220-103">Create registered ASN for peering</span></span>

## <span data-ttu-id="4a220-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a220-104">SYNTAX</span></span>

### <span data-ttu-id="4a220-105">ByResourceGroupAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4a220-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a220-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4a220-106">InputObject</span></span>
```
New-AzPeeringRegisteredAsn -InputObject <PSPeering> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a220-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4a220-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a220-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a220-108">DESCRIPTION</span></span>
<span data-ttu-id="4a220-109">Erstellen Sie registrierte ASNs für Peeringobjekte.</span><span class="sxs-lookup"><span data-stu-id="4a220-109">Create registered ASNs for peering objects.</span></span>

## <span data-ttu-id="4a220-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4a220-110">EXAMPLES</span></span>

### <span data-ttu-id="4a220-111">Peering erhalten und einen registrierten ASN erstellen</span><span class="sxs-lookup"><span data-stu-id="4a220-111">Get peering and create a registered ASN</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredAsn -Name $asnName -Asn $asn
```

<span data-ttu-id="4a220-112">Holen Sie sich das Peering, das Sie einem registrierten ASN hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="4a220-112">Get the peering you want to add a registered ASN.</span></span> <span data-ttu-id="4a220-113">Übergeben Sie diese dann an das Commandlet.</span><span class="sxs-lookup"><span data-stu-id="4a220-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="4a220-114">Verwenden von Peering resourceId zum Erstellen eines registrierten Asns</span><span class="sxs-lookup"><span data-stu-id="4a220-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredAsn -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="4a220-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4a220-115">PARAMETERS</span></span>

### <span data-ttu-id="4a220-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a220-116">-AsJob</span></span>
<span data-ttu-id="4a220-117">Führen Sie im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="4a220-117">Run in the background.</span></span>

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

### <span data-ttu-id="4a220-118">-Asn</span><span class="sxs-lookup"><span data-stu-id="4a220-118">-Asn</span></span>
<span data-ttu-id="4a220-119">Der zu registrierte ASN</span><span class="sxs-lookup"><span data-stu-id="4a220-119">The ASN to be registered</span></span>

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

### <span data-ttu-id="4a220-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a220-120">-DefaultProfile</span></span>
<span data-ttu-id="4a220-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a220-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a220-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a220-122">-InputObject</span></span>
<span data-ttu-id="4a220-123">Verwenden eines Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="4a220-123">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a220-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4a220-124">-Name</span></span>
<span data-ttu-id="4a220-125">Der zu registrierte ASN</span><span class="sxs-lookup"><span data-stu-id="4a220-125">The ASN to be registered</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a220-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="4a220-126">-PeeringName</span></span>
<span data-ttu-id="4a220-127">Der eindeutige Name des PSPeerings.</span><span class="sxs-lookup"><span data-stu-id="4a220-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="4a220-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a220-128">-ResourceGroupName</span></span>
<span data-ttu-id="4a220-129">Erstellen oder Verwenden eines vorhandenen Ressourcengruppennamens.</span><span class="sxs-lookup"><span data-stu-id="4a220-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="4a220-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a220-130">-ResourceId</span></span>
<span data-ttu-id="4a220-131">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="4a220-131">The resource id string name.</span></span>

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

### <span data-ttu-id="4a220-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4a220-132">-Confirm</span></span>
<span data-ttu-id="4a220-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4a220-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a220-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a220-134">-WhatIf</span></span>
<span data-ttu-id="4a220-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a220-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a220-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a220-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a220-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a220-137">CommonParameters</span></span>
<span data-ttu-id="4a220-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a220-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a220-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a220-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a220-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4a220-140">INPUTS</span></span>

### <span data-ttu-id="4a220-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="4a220-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="4a220-142">System.String</span><span class="sxs-lookup"><span data-stu-id="4a220-142">System.String</span></span>

## <span data-ttu-id="4a220-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4a220-143">OUTPUTS</span></span>

### <span data-ttu-id="4a220-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="4a220-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="4a220-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4a220-145">NOTES</span></span>

## <span data-ttu-id="4a220-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4a220-146">RELATED LINKS</span></span>
