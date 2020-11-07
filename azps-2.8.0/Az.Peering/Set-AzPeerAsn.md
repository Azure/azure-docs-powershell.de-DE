---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: 81398d4ab62db1b8dca573dfd6beccde3be63700
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824003"
---
# <span data-ttu-id="f8161-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="f8161-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="f8161-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8161-102">SYNOPSIS</span></span>
<span data-ttu-id="f8161-103">Aktualisieren von Kontaktinformationen</span><span class="sxs-lookup"><span data-stu-id="f8161-103">Update Contact Information</span></span>

## <span data-ttu-id="f8161-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8161-104">SYNTAX</span></span>

### <span data-ttu-id="f8161-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f8161-105">ByName (Default)</span></span>
```
Set-AzPeerAsn [-Name] <String> [-Email <String[]>] [-Phone <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8161-106">Standard</span><span class="sxs-lookup"><span data-stu-id="f8161-106">Default</span></span>
```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-Email <String[]>] [-Phone <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8161-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8161-107">DESCRIPTION</span></span>
<span data-ttu-id="f8161-108">Ermöglicht es Ihnen, Kontaktinformationen für eine PeerAsn im Abonnement zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f8161-108">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="f8161-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8161-109">EXAMPLES</span></span>

### <span data-ttu-id="f8161-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f8161-110">Example 1</span></span>
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

<span data-ttu-id="f8161-111">Fügt der Peer-ASN eine e-Mail-Adresse hinzu.</span><span class="sxs-lookup"><span data-stu-id="f8161-111">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="f8161-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8161-112">PARAMETERS</span></span>

### <span data-ttu-id="f8161-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8161-113">-AsJob</span></span>
<span data-ttu-id="f8161-114">Im Hintergrund ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f8161-114">Run in the background.</span></span>

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

### <span data-ttu-id="f8161-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8161-115">-DefaultProfile</span></span>
<span data-ttu-id="f8161-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f8161-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8161-117">– E-Mail</span><span class="sxs-lookup"><span data-stu-id="f8161-117">-Email</span></span>
<span data-ttu-id="f8161-118">E-Mail</span><span class="sxs-lookup"><span data-stu-id="f8161-118">Email</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8161-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f8161-119">-InputObject</span></span>
<span data-ttu-id="f8161-120">{{Fill Inputobject Description}}</span><span class="sxs-lookup"><span data-stu-id="f8161-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8161-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f8161-121">-Name</span></span>
<span data-ttu-id="f8161-122">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="f8161-122">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8161-123">-Telefon</span><span class="sxs-lookup"><span data-stu-id="f8161-123">-Phone</span></span>
<span data-ttu-id="f8161-124">Telefon</span><span class="sxs-lookup"><span data-stu-id="f8161-124">Phone</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8161-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f8161-125">-Confirm</span></span>
<span data-ttu-id="f8161-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8161-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8161-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8161-127">-WhatIf</span></span>
<span data-ttu-id="f8161-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8161-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8161-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8161-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8161-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8161-130">CommonParameters</span></span>
<span data-ttu-id="f8161-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8161-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8161-132">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8161-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8161-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8161-133">INPUTS</span></span>

### <span data-ttu-id="f8161-134">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="f8161-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="f8161-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8161-135">OUTPUTS</span></span>

### <span data-ttu-id="f8161-136">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="f8161-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="f8161-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8161-137">NOTES</span></span>

## <span data-ttu-id="f8161-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8161-138">RELATED LINKS</span></span>
