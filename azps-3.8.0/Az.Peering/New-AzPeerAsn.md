---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: f811f73b50f88a256de62069a287d113607e7ee1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004681"
---
# <span data-ttu-id="f9b63-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="f9b63-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="f9b63-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f9b63-102">SYNOPSIS</span></span>
<span data-ttu-id="f9b63-103">Erstellt eine neue Peer-ASN</span><span class="sxs-lookup"><span data-stu-id="f9b63-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="f9b63-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9b63-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -Email <String[]> -Phone <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9b63-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9b63-105">DESCRIPTION</span></span>
<span data-ttu-id="f9b63-106">Erstellt ein neues PeerAsn-Objekt für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f9b63-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="f9b63-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9b63-107">EXAMPLES</span></span>

### <span data-ttu-id="f9b63-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f9b63-108">Example 1</span></span>
```powershell
PS C:> New-AzPeerAsn -Name Contoso65050 -PeerName Contoso -PeerAsn 65050 -Emails noc@contoso.com -Phone "888-888-8889"

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="f9b63-109">Erstellt eine neue PeerAsn</span><span class="sxs-lookup"><span data-stu-id="f9b63-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="f9b63-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9b63-110">PARAMETERS</span></span>

### <span data-ttu-id="f9b63-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9b63-111">-AsJob</span></span>
<span data-ttu-id="f9b63-112">Im Hintergrund ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f9b63-112">Run in the background.</span></span>

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

### <span data-ttu-id="f9b63-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b63-113">-DefaultProfile</span></span>
<span data-ttu-id="f9b63-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f9b63-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9b63-115">– E-Mail</span><span class="sxs-lookup"><span data-stu-id="f9b63-115">-Email</span></span>
<span data-ttu-id="f9b63-116">E-Mail</span><span class="sxs-lookup"><span data-stu-id="f9b63-116">Email</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9b63-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f9b63-117">-Name</span></span>
<span data-ttu-id="f9b63-118">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="f9b63-118">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9b63-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="f9b63-119">-PeerAsn</span></span>
<span data-ttu-id="f9b63-120">Die Peer-ASN-Ressourcen-ID. verwenden Sie Get-AzPeerAsn, um die ID abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f9b63-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9b63-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="f9b63-121">-PeerName</span></span>
<span data-ttu-id="f9b63-122">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="f9b63-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="f9b63-123">-Telefon</span><span class="sxs-lookup"><span data-stu-id="f9b63-123">-Phone</span></span>
<span data-ttu-id="f9b63-124">Telefon</span><span class="sxs-lookup"><span data-stu-id="f9b63-124">Phone</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9b63-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f9b63-125">-Confirm</span></span>
<span data-ttu-id="f9b63-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f9b63-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9b63-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9b63-127">-WhatIf</span></span>
<span data-ttu-id="f9b63-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9b63-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9b63-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9b63-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9b63-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9b63-130">CommonParameters</span></span>
<span data-ttu-id="f9b63-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9b63-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9b63-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9b63-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9b63-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f9b63-133">INPUTS</span></span>

### <span data-ttu-id="f9b63-134">Keine</span><span class="sxs-lookup"><span data-stu-id="f9b63-134">None</span></span>

## <span data-ttu-id="f9b63-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f9b63-135">OUTPUTS</span></span>

### <span data-ttu-id="f9b63-136">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="f9b63-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="f9b63-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="f9b63-137">NOTES</span></span>

## <span data-ttu-id="f9b63-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f9b63-138">RELATED LINKS</span></span>
