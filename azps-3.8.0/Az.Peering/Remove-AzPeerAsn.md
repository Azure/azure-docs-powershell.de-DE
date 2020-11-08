---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: d1ff0baeff3bf4b5747ff1d024b0de6e5184688a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002966"
---
# <span data-ttu-id="87a01-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="87a01-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="87a01-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="87a01-102">SYNOPSIS</span></span>
<span data-ttu-id="87a01-103">Peer-ASN entfernen</span><span class="sxs-lookup"><span data-stu-id="87a01-103">Remove Peer Asn</span></span>

## <span data-ttu-id="87a01-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="87a01-104">SYNTAX</span></span>

### <span data-ttu-id="87a01-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="87a01-105">Default (Default)</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87a01-106">ByName</span><span class="sxs-lookup"><span data-stu-id="87a01-106">ByName</span></span>
```
Remove-AzPeerAsn [-Name] <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87a01-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87a01-107">DESCRIPTION</span></span>
<span data-ttu-id="87a01-108">Entfernen eines PeerAsn aus dem Abonnement</span><span class="sxs-lookup"><span data-stu-id="87a01-108">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="87a01-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="87a01-109">EXAMPLES</span></span>

### <span data-ttu-id="87a01-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="87a01-110">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="87a01-111">Entfernt die Peer-ASN</span><span class="sxs-lookup"><span data-stu-id="87a01-111">Removes the Peer Asn</span></span>

## <span data-ttu-id="87a01-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="87a01-112">PARAMETERS</span></span>

### <span data-ttu-id="87a01-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87a01-113">-AsJob</span></span>
<span data-ttu-id="87a01-114">Im Hintergrund ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="87a01-114">Run in the background.</span></span>

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

### <span data-ttu-id="87a01-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87a01-115">-DefaultProfile</span></span>
<span data-ttu-id="87a01-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="87a01-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87a01-117">-Force</span><span class="sxs-lookup"><span data-stu-id="87a01-117">-Force</span></span>
<span data-ttu-id="87a01-118">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="87a01-118">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="87a01-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="87a01-119">-InputObject</span></span>
<span data-ttu-id="87a01-120">Das PeerAsn-Objekt.</span><span class="sxs-lookup"><span data-stu-id="87a01-120">The PeerAsn object.</span></span>

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

### <span data-ttu-id="87a01-121">-Name</span><span class="sxs-lookup"><span data-stu-id="87a01-121">-Name</span></span>
<span data-ttu-id="87a01-122">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="87a01-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="87a01-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87a01-123">-PassThru</span></span>
<span data-ttu-id="87a01-124">True zurück, wenn abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="87a01-124">Return true if complete</span></span>

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

### <span data-ttu-id="87a01-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="87a01-125">-Confirm</span></span>
<span data-ttu-id="87a01-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="87a01-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87a01-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87a01-127">-WhatIf</span></span>
<span data-ttu-id="87a01-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87a01-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87a01-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="87a01-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87a01-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87a01-130">CommonParameters</span></span>
<span data-ttu-id="87a01-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87a01-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87a01-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87a01-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87a01-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="87a01-133">INPUTS</span></span>

### <span data-ttu-id="87a01-134">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="87a01-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="87a01-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="87a01-135">OUTPUTS</span></span>

### <span data-ttu-id="87a01-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="87a01-136">System.Boolean</span></span>

## <span data-ttu-id="87a01-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="87a01-137">NOTES</span></span>

## <span data-ttu-id="87a01-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="87a01-138">RELATED LINKS</span></span>
