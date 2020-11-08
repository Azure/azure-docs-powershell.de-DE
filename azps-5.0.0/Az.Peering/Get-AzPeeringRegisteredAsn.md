---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d23a034b2c51f37116c605d786393ba504da3f26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176587"
---
# <span data-ttu-id="16c3d-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="16c3d-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="16c3d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="16c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="16c3d-103">Ruft den registrierten ASN für Internet Exchange Route Server-Typ Peering ab.</span><span class="sxs-lookup"><span data-stu-id="16c3d-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="16c3d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="16c3d-104">SYNTAX</span></span>

### <span data-ttu-id="16c3d-105">ByResourceGroupAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="16c3d-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16c3d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="16c3d-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16c3d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="16c3d-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16c3d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16c3d-108">DESCRIPTION</span></span>
<span data-ttu-id="16c3d-109">Abrufen oder Auflisten eines registrierten ASN.</span><span class="sxs-lookup"><span data-stu-id="16c3d-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="16c3d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="16c3d-110">EXAMPLES</span></span>

### <span data-ttu-id="16c3d-111">Liste der registrierten Lieferavise für Peering</span><span class="sxs-lookup"><span data-stu-id="16c3d-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="16c3d-112">Listet registrierte ASN auf.</span><span class="sxs-lookup"><span data-stu-id="16c3d-112">Lists registered asn.</span></span>

### <span data-ttu-id="16c3d-113">Ruft registrierte ASN für Peering nach Name ab</span><span class="sxs-lookup"><span data-stu-id="16c3d-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="16c3d-114">Ruft den registrierten Peering-ASN ab.</span><span class="sxs-lookup"><span data-stu-id="16c3d-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="16c3d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="16c3d-115">PARAMETERS</span></span>

### <span data-ttu-id="16c3d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c3d-116">-DefaultProfile</span></span>
<span data-ttu-id="16c3d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="16c3d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16c3d-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="16c3d-118">-InputObject</span></span>
<span data-ttu-id="16c3d-119">Verwenden eines Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="16c3d-119">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="16c3d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="16c3d-120">-Name</span></span>
<span data-ttu-id="16c3d-121">Der Name der registrierten ASN-Datei</span><span class="sxs-lookup"><span data-stu-id="16c3d-121">The name of the registered ASN</span></span>

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

### <span data-ttu-id="16c3d-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="16c3d-122">-PeeringName</span></span>
<span data-ttu-id="16c3d-123">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="16c3d-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="16c3d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16c3d-124">-ResourceGroupName</span></span>
<span data-ttu-id="16c3d-125">Der Name der vorhandenen Ressourcengruppe erstellen oder verwenden</span><span class="sxs-lookup"><span data-stu-id="16c3d-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="16c3d-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="16c3d-126">-ResourceId</span></span>
<span data-ttu-id="16c3d-127">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="16c3d-127">The resource id string name.</span></span>

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

### <span data-ttu-id="16c3d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c3d-128">CommonParameters</span></span>
<span data-ttu-id="16c3d-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16c3d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c3d-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16c3d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c3d-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="16c3d-131">INPUTS</span></span>

### <span data-ttu-id="16c3d-132">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="16c3d-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="16c3d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="16c3d-133">System.String</span></span>

## <span data-ttu-id="16c3d-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="16c3d-134">OUTPUTS</span></span>

### <span data-ttu-id="16c3d-135">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="16c3d-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="16c3d-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="16c3d-136">NOTES</span></span>

## <span data-ttu-id="16c3d-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="16c3d-137">RELATED LINKS</span></span>
