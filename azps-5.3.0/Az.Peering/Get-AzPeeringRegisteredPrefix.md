---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ca54d2a8969313742711306c701de3aefe54b30c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473289"
---
# <span data-ttu-id="10000-101">Get-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="10000-101">Get-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="10000-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10000-102">SYNOPSIS</span></span>
<span data-ttu-id="10000-103">Ruft das registrierte Präfix für Peerings ab oder listet es auf.</span><span class="sxs-lookup"><span data-stu-id="10000-103">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="10000-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10000-104">SYNTAX</span></span>

### <span data-ttu-id="10000-105">ByResourceGroupAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="10000-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10000-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="10000-106">InputObject</span></span>
```
Get-AzPeeringRegisteredPrefix [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10000-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="10000-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="10000-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10000-108">DESCRIPTION</span></span>
<span data-ttu-id="10000-109">Ruft das registrierte Präfix für Peerings ab oder listet es auf.</span><span class="sxs-lookup"><span data-stu-id="10000-109">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="10000-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="10000-110">EXAMPLES</span></span>

### <span data-ttu-id="10000-111">Liste registrierter ASNs für Peering</span><span class="sxs-lookup"><span data-stu-id="10000-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="10000-112">Listen, die als "registriert" registriert sind.</span><span class="sxs-lookup"><span data-stu-id="10000-112">Lists registered asn.</span></span>

### <span data-ttu-id="10000-113">Wird asN für Peering nach Name registriert</span><span class="sxs-lookup"><span data-stu-id="10000-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredPrefixName
```

<span data-ttu-id="10000-114">Ruft asn registriertes Peering ab.</span><span class="sxs-lookup"><span data-stu-id="10000-114">Gets registered peering asn.</span></span>

<span data-ttu-id="10000-115">{{ Beispielbeschreibung hier hinzufügen }}</span><span class="sxs-lookup"><span data-stu-id="10000-115">{{ Add example description here }}</span></span>

## <span data-ttu-id="10000-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10000-116">PARAMETERS</span></span>

### <span data-ttu-id="10000-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10000-117">-DefaultProfile</span></span>
<span data-ttu-id="10000-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10000-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10000-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10000-119">-InputObject</span></span>
<span data-ttu-id="10000-120">Verwenden eines Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="10000-120">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10000-121">-Name</span><span class="sxs-lookup"><span data-stu-id="10000-121">-Name</span></span>
<span data-ttu-id="10000-122">Der Name des Präfixes.</span><span class="sxs-lookup"><span data-stu-id="10000-122">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10000-123">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="10000-123">-PeeringName</span></span>
<span data-ttu-id="10000-124">Der eindeutige Name von PSPeering.</span><span class="sxs-lookup"><span data-stu-id="10000-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="10000-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10000-125">-ResourceGroupName</span></span>
<span data-ttu-id="10000-126">Der Name einer vorhandenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="10000-126">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="10000-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10000-127">-ResourceId</span></span>
<span data-ttu-id="10000-128">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="10000-128">The resource id string name.</span></span>

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

### <span data-ttu-id="10000-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10000-129">CommonParameters</span></span>
<span data-ttu-id="10000-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10000-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10000-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10000-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10000-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="10000-132">INPUTS</span></span>

### <span data-ttu-id="10000-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="10000-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="10000-134">System.String</span><span class="sxs-lookup"><span data-stu-id="10000-134">System.String</span></span>

## <span data-ttu-id="10000-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="10000-135">OUTPUTS</span></span>

### <span data-ttu-id="10000-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="10000-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="10000-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="10000-137">NOTES</span></span>

## <span data-ttu-id="10000-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="10000-138">RELATED LINKS</span></span>
