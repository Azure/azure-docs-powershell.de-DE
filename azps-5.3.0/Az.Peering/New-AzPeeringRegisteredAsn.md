---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d4521c06cafac21c554620bbc55f7555db6e0279
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384753"
---
# <span data-ttu-id="65f84-101">New-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="65f84-101">New-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="65f84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65f84-102">SYNOPSIS</span></span>
<span data-ttu-id="65f84-103">Erstellen eines registrierten ASNs für Peering</span><span class="sxs-lookup"><span data-stu-id="65f84-103">Create registered ASN for peering</span></span>

## <span data-ttu-id="65f84-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65f84-104">SYNTAX</span></span>

### <span data-ttu-id="65f84-105">ByResourceGroupAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="65f84-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65f84-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="65f84-106">InputObject</span></span>
```
New-AzPeeringRegisteredAsn -InputObject <PSPeering> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65f84-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="65f84-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65f84-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65f84-108">DESCRIPTION</span></span>
<span data-ttu-id="65f84-109">Erstellen Sie registrierte ASNs für Peeringobjekte.</span><span class="sxs-lookup"><span data-stu-id="65f84-109">Create registered ASNs for peering objects.</span></span>

## <span data-ttu-id="65f84-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="65f84-110">EXAMPLES</span></span>

### <span data-ttu-id="65f84-111">Peering erhalten und einen registrierten ASN erstellen</span><span class="sxs-lookup"><span data-stu-id="65f84-111">Get peering and create a registered ASN</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredAsn -Name $asnName -Asn $asn
```

<span data-ttu-id="65f84-112">Holen Sie sich das Peering, dem Sie einen registrierten ASN hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="65f84-112">Get the peering you want to add a registered ASN.</span></span> <span data-ttu-id="65f84-113">Übergeben Sie dies dann an das Commandlet.</span><span class="sxs-lookup"><span data-stu-id="65f84-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="65f84-114">Verwenden der PeeringressourceId zum Erstellen eines registrierten Asns</span><span class="sxs-lookup"><span data-stu-id="65f84-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredAsn -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="65f84-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65f84-115">PARAMETERS</span></span>

### <span data-ttu-id="65f84-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65f84-116">-AsJob</span></span>
<span data-ttu-id="65f84-117">Führen Sie die Ausführung im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="65f84-117">Run in the background.</span></span>

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

### <span data-ttu-id="65f84-118">-Asn</span><span class="sxs-lookup"><span data-stu-id="65f84-118">-Asn</span></span>
<span data-ttu-id="65f84-119">Der zu registrierte ASN</span><span class="sxs-lookup"><span data-stu-id="65f84-119">The ASN to be registered</span></span>

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

### <span data-ttu-id="65f84-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65f84-120">-DefaultProfile</span></span>
<span data-ttu-id="65f84-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="65f84-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65f84-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65f84-122">-InputObject</span></span>
<span data-ttu-id="65f84-123">Verwenden eines Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="65f84-123">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="65f84-124">-Name</span><span class="sxs-lookup"><span data-stu-id="65f84-124">-Name</span></span>
<span data-ttu-id="65f84-125">Der zu registrierte ASN</span><span class="sxs-lookup"><span data-stu-id="65f84-125">The ASN to be registered</span></span>

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

### <span data-ttu-id="65f84-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="65f84-126">-PeeringName</span></span>
<span data-ttu-id="65f84-127">Der eindeutige Name von PSPeering.</span><span class="sxs-lookup"><span data-stu-id="65f84-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="65f84-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65f84-128">-ResourceGroupName</span></span>
<span data-ttu-id="65f84-129">Der Name einer vorhandenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="65f84-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="65f84-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65f84-130">-ResourceId</span></span>
<span data-ttu-id="65f84-131">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="65f84-131">The resource id string name.</span></span>

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

### <span data-ttu-id="65f84-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65f84-132">-Confirm</span></span>
<span data-ttu-id="65f84-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="65f84-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65f84-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="65f84-134">-WhatIf</span></span>
<span data-ttu-id="65f84-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65f84-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65f84-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="65f84-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65f84-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65f84-137">CommonParameters</span></span>
<span data-ttu-id="65f84-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65f84-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65f84-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65f84-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65f84-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="65f84-140">INPUTS</span></span>

### <span data-ttu-id="65f84-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="65f84-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="65f84-142">System.String</span><span class="sxs-lookup"><span data-stu-id="65f84-142">System.String</span></span>

## <span data-ttu-id="65f84-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="65f84-143">OUTPUTS</span></span>

### <span data-ttu-id="65f84-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="65f84-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="65f84-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="65f84-145">NOTES</span></span>

## <span data-ttu-id="65f84-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="65f84-146">RELATED LINKS</span></span>
