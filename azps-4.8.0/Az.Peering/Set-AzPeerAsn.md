---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: ec7003b90d9489f2966d4fd1ebe3e3fb3fa74ce5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174233"
---
# <span data-ttu-id="f9617-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="f9617-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="f9617-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f9617-102">SYNOPSIS</span></span>
<span data-ttu-id="f9617-103">Aktualisieren von Kontaktinformationen</span><span class="sxs-lookup"><span data-stu-id="f9617-103">Update Contact Information</span></span>

## <span data-ttu-id="f9617-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9617-104">SYNTAX</span></span>

```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9617-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9617-105">DESCRIPTION</span></span>
<span data-ttu-id="f9617-106">Ermöglicht es Ihnen, Kontaktinformationen für eine PeerAsn im Abonnement zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f9617-106">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="f9617-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9617-107">EXAMPLES</span></span>

### <span data-ttu-id="f9617-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f9617-108">Example 1</span></span>
```powershell
#Get the Peer ASN object
PS C:> Get-AzPeerAsn -PeerName Contoso | Set-AzPeerAsn -Email noc1@contoso.com

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="f9617-109">Fügt der Peer-ASN eine e-Mail-Adresse hinzu.</span><span class="sxs-lookup"><span data-stu-id="f9617-109">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="f9617-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9617-110">PARAMETERS</span></span>

### <span data-ttu-id="f9617-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9617-111">-AsJob</span></span>
<span data-ttu-id="f9617-112">Im Hintergrund ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f9617-112">Run in the background.</span></span>

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

### <span data-ttu-id="f9617-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9617-113">-DefaultProfile</span></span>
<span data-ttu-id="f9617-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f9617-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9617-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f9617-115">-InputObject</span></span>
<span data-ttu-id="f9617-116">{{Fill Inputobject Description}}</span><span class="sxs-lookup"><span data-stu-id="f9617-116">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9617-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f9617-117">-Confirm</span></span>
<span data-ttu-id="f9617-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f9617-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9617-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9617-119">-WhatIf</span></span>
<span data-ttu-id="f9617-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9617-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9617-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9617-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9617-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9617-122">CommonParameters</span></span>
<span data-ttu-id="f9617-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9617-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9617-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9617-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9617-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f9617-125">INPUTS</span></span>

### <span data-ttu-id="f9617-126">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="f9617-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="f9617-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f9617-127">OUTPUTS</span></span>

### <span data-ttu-id="f9617-128">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="f9617-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="f9617-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="f9617-129">NOTES</span></span>

## <span data-ttu-id="f9617-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f9617-130">RELATED LINKS</span></span>
