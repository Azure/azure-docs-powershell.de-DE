---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ca54d2a8969313742711306c701de3aefe54b30c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176586"
---
# <span data-ttu-id="d1c12-101">Get-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="d1c12-101">Get-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="d1c12-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1c12-102">SYNOPSIS</span></span>
<span data-ttu-id="d1c12-103">Ruft das registrierte Präfix für Peerings ab oder listet es auf.</span><span class="sxs-lookup"><span data-stu-id="d1c12-103">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="d1c12-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1c12-104">SYNTAX</span></span>

### <span data-ttu-id="d1c12-105">ByResourceGroupAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d1c12-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1c12-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d1c12-106">InputObject</span></span>
```
Get-AzPeeringRegisteredPrefix [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1c12-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d1c12-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1c12-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1c12-108">DESCRIPTION</span></span>
<span data-ttu-id="d1c12-109">Ruft das registrierte Präfix für Peerings ab oder listet es auf.</span><span class="sxs-lookup"><span data-stu-id="d1c12-109">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="d1c12-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1c12-110">EXAMPLES</span></span>

### <span data-ttu-id="d1c12-111">Liste der registrierten Lieferavise für Peering</span><span class="sxs-lookup"><span data-stu-id="d1c12-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="d1c12-112">Listet registrierte ASN auf.</span><span class="sxs-lookup"><span data-stu-id="d1c12-112">Lists registered asn.</span></span>

### <span data-ttu-id="d1c12-113">Ruft registrierte ASN für Peering nach Name ab</span><span class="sxs-lookup"><span data-stu-id="d1c12-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredPrefixName
```

<span data-ttu-id="d1c12-114">Ruft den registrierten Peering-ASN ab.</span><span class="sxs-lookup"><span data-stu-id="d1c12-114">Gets registered peering asn.</span></span>

<span data-ttu-id="d1c12-115">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="d1c12-115">{{ Add example description here }}</span></span>

## <span data-ttu-id="d1c12-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1c12-116">PARAMETERS</span></span>

### <span data-ttu-id="d1c12-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1c12-117">-DefaultProfile</span></span>
<span data-ttu-id="d1c12-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d1c12-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1c12-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d1c12-119">-InputObject</span></span>
<span data-ttu-id="d1c12-120">Verwenden eines Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="d1c12-120">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="d1c12-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d1c12-121">-Name</span></span>
<span data-ttu-id="d1c12-122">Der Name des Präfixes.</span><span class="sxs-lookup"><span data-stu-id="d1c12-122">The name of prefix.</span></span>

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

### <span data-ttu-id="d1c12-123">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="d1c12-123">-PeeringName</span></span>
<span data-ttu-id="d1c12-124">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="d1c12-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="d1c12-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1c12-125">-ResourceGroupName</span></span>
<span data-ttu-id="d1c12-126">Der Name der vorhandenen Ressourcengruppe erstellen oder verwenden</span><span class="sxs-lookup"><span data-stu-id="d1c12-126">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="d1c12-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d1c12-127">-ResourceId</span></span>
<span data-ttu-id="d1c12-128">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="d1c12-128">The resource id string name.</span></span>

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

### <span data-ttu-id="d1c12-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1c12-129">CommonParameters</span></span>
<span data-ttu-id="d1c12-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1c12-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1c12-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1c12-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1c12-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1c12-132">INPUTS</span></span>

### <span data-ttu-id="d1c12-133">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="d1c12-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="d1c12-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d1c12-134">System.String</span></span>

## <span data-ttu-id="d1c12-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1c12-135">OUTPUTS</span></span>

### <span data-ttu-id="d1c12-136">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="d1c12-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="d1c12-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1c12-137">NOTES</span></span>

## <span data-ttu-id="d1c12-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1c12-138">RELATED LINKS</span></span>
