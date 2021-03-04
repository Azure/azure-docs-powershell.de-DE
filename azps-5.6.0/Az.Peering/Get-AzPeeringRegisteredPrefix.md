---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 4eb704682885e5040913e08c5242d4142a387ef7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937736"
---
# <span data-ttu-id="dc99f-101">Get-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="dc99f-101">Get-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="dc99f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc99f-102">SYNOPSIS</span></span>
<span data-ttu-id="dc99f-103">Ruft das registrierte Präfix für Peerings ab oder listet es auf.</span><span class="sxs-lookup"><span data-stu-id="dc99f-103">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="dc99f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc99f-104">SYNTAX</span></span>

### <span data-ttu-id="dc99f-105">ByResourceGroupAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="dc99f-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc99f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="dc99f-106">InputObject</span></span>
```
Get-AzPeeringRegisteredPrefix [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc99f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dc99f-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc99f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc99f-108">DESCRIPTION</span></span>
<span data-ttu-id="dc99f-109">Ruft das registrierte Präfix für Peerings ab oder listet es auf.</span><span class="sxs-lookup"><span data-stu-id="dc99f-109">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="dc99f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dc99f-110">EXAMPLES</span></span>

### <span data-ttu-id="dc99f-111">Liste registrierter ASNs für Peering</span><span class="sxs-lookup"><span data-stu-id="dc99f-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="dc99f-112">Listen, die als registriert sind.</span><span class="sxs-lookup"><span data-stu-id="dc99f-112">Lists registered asn.</span></span>

### <span data-ttu-id="dc99f-113">Ruft registriertes ASN für Peering nach Name ab</span><span class="sxs-lookup"><span data-stu-id="dc99f-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredPrefixName
```

<span data-ttu-id="dc99f-114">Ruft registriertes Peering ab.</span><span class="sxs-lookup"><span data-stu-id="dc99f-114">Gets registered peering asn.</span></span>

<span data-ttu-id="dc99f-115">{{ Beispielbeschreibung hier hinzufügen }}</span><span class="sxs-lookup"><span data-stu-id="dc99f-115">{{ Add example description here }}</span></span>

## <span data-ttu-id="dc99f-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dc99f-116">PARAMETERS</span></span>

### <span data-ttu-id="dc99f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc99f-117">-DefaultProfile</span></span>
<span data-ttu-id="dc99f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc99f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc99f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc99f-119">-InputObject</span></span>
<span data-ttu-id="dc99f-120">Verwenden eines Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="dc99f-120">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="dc99f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="dc99f-121">-Name</span></span>
<span data-ttu-id="dc99f-122">Der Name des Präfixes.</span><span class="sxs-lookup"><span data-stu-id="dc99f-122">The name of prefix.</span></span>

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

### <span data-ttu-id="dc99f-123">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="dc99f-123">-PeeringName</span></span>
<span data-ttu-id="dc99f-124">Der eindeutige Name des PSPeerings.</span><span class="sxs-lookup"><span data-stu-id="dc99f-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="dc99f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc99f-125">-ResourceGroupName</span></span>
<span data-ttu-id="dc99f-126">Erstellen oder Verwenden eines vorhandenen Ressourcengruppennamens.</span><span class="sxs-lookup"><span data-stu-id="dc99f-126">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="dc99f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc99f-127">-ResourceId</span></span>
<span data-ttu-id="dc99f-128">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="dc99f-128">The resource id string name.</span></span>

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

### <span data-ttu-id="dc99f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc99f-129">CommonParameters</span></span>
<span data-ttu-id="dc99f-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc99f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc99f-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc99f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc99f-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dc99f-132">INPUTS</span></span>

### <span data-ttu-id="dc99f-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="dc99f-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="dc99f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="dc99f-134">System.String</span></span>

## <span data-ttu-id="dc99f-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dc99f-135">OUTPUTS</span></span>

### <span data-ttu-id="dc99f-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="dc99f-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="dc99f-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dc99f-137">NOTES</span></span>

## <span data-ttu-id="dc99f-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dc99f-138">RELATED LINKS</span></span>
