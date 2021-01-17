---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: cf27cf7f82e44ec52978b3d04af973ba47cd1632
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384823"
---
# <span data-ttu-id="8a1e1-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="8a1e1-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="8a1e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a1e1-102">SYNOPSIS</span></span>
<span data-ttu-id="8a1e1-103">Erstellt einen neuen Peer ASN</span><span class="sxs-lookup"><span data-stu-id="8a1e1-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="8a1e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a1e1-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -ContactDetail <PSContactDetail[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a1e1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8a1e1-105">DESCRIPTION</span></span>
<span data-ttu-id="8a1e1-106">Erstellt ein neues PeerAsn-Objekt für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a1e1-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="8a1e1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8a1e1-107">EXAMPLES</span></span>

### <span data-ttu-id="8a1e1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8a1e1-108">Example 1</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="8a1e1-109">Erstellt einen neuen PeerAsn</span><span class="sxs-lookup"><span data-stu-id="8a1e1-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="8a1e1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a1e1-110">PARAMETERS</span></span>

### <span data-ttu-id="8a1e1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a1e1-111">-AsJob</span></span>
<span data-ttu-id="8a1e1-112">Führen Sie die Ausführung im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="8a1e1-112">Run in the background.</span></span>

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

### <span data-ttu-id="8a1e1-113">-ContactDetail</span><span class="sxs-lookup"><span data-stu-id="8a1e1-113">-ContactDetail</span></span>
<span data-ttu-id="8a1e1-114">E-Mail-Adressen, die zum Kontakt verwendet werden, wenn probleme in der Regel ein Netzwerkbetriebscenter auftreten</span><span class="sxs-lookup"><span data-stu-id="8a1e1-114">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a1e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a1e1-115">-DefaultProfile</span></span>
<span data-ttu-id="8a1e1-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a1e1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a1e1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8a1e1-117">-Name</span></span>
<span data-ttu-id="8a1e1-118">Der eindeutige Name von PSPeering.</span><span class="sxs-lookup"><span data-stu-id="8a1e1-118">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="8a1e1-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="8a1e1-119">-PeerAsn</span></span>
<span data-ttu-id="8a1e1-120">Die Peer-Asn-Ressourcen-ID. Verwenden Sie Get-AzPeerAsn, um die ID abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8a1e1-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="8a1e1-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="8a1e1-121">-PeerName</span></span>
<span data-ttu-id="8a1e1-122">Der eindeutige Name von PSPeering.</span><span class="sxs-lookup"><span data-stu-id="8a1e1-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="8a1e1-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a1e1-123">-Confirm</span></span>
<span data-ttu-id="8a1e1-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a1e1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a1e1-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8a1e1-125">-WhatIf</span></span>
<span data-ttu-id="8a1e1-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a1e1-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a1e1-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a1e1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a1e1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a1e1-128">CommonParameters</span></span>
<span data-ttu-id="8a1e1-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a1e1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a1e1-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a1e1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a1e1-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8a1e1-131">INPUTS</span></span>

### <span data-ttu-id="8a1e1-132">Keine</span><span class="sxs-lookup"><span data-stu-id="8a1e1-132">None</span></span>

## <span data-ttu-id="8a1e1-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8a1e1-133">OUTPUTS</span></span>

### <span data-ttu-id="8a1e1-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="8a1e1-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="8a1e1-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8a1e1-135">NOTES</span></span>

## <span data-ttu-id="8a1e1-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8a1e1-136">RELATED LINKS</span></span>
