---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
ms.openlocfilehash: 2cb7bc759847af456286bfc611904922a26dc443
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173250"
---
# <span data-ttu-id="1ddf1-101">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="1ddf1-101">Add-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="1ddf1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1ddf1-102">SYNOPSIS</span></span>
<span data-ttu-id="1ddf1-103">Hinzufügen eines Peers zu einem Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="1ddf1-103">Add a Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="1ddf1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ddf1-104">SYNTAX</span></span>

```
Add-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ddf1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ddf1-105">DESCRIPTION</span></span>
<span data-ttu-id="1ddf1-106">Das **Add-AzVirtualRouterPeer-** Cmdlet fügt einen VirtualRouter-Peer zu einem Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="1ddf1-106">The **Add-AzVirtualRouterPeer** cmdlet adds a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="1ddf1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ddf1-107">EXAMPLES</span></span>

### <span data-ttu-id="1ddf1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1ddf1-108">Example 1</span></span>
```powershell
Add-AzVirtualRouterPeer 1ResourceGroupName virtualRouterRG -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="1ddf1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ddf1-109">PARAMETERS</span></span>

### <span data-ttu-id="1ddf1-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ddf1-110">-AsJob</span></span>
<span data-ttu-id="1ddf1-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1ddf1-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ddf1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ddf1-112">-DefaultProfile</span></span>
<span data-ttu-id="1ddf1-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1ddf1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ddf1-114">-Force</span><span class="sxs-lookup"><span data-stu-id="1ddf1-114">-Force</span></span>
<span data-ttu-id="1ddf1-115">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="1ddf1-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1ddf1-116">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="1ddf1-116">-PeerAsn</span></span>
<span data-ttu-id="1ddf1-117">Peer-ASN.</span><span class="sxs-lookup"><span data-stu-id="1ddf1-117">Peer ASN.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ddf1-118">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="1ddf1-118">-PeerIp</span></span>
<span data-ttu-id="1ddf1-119">Peer-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="1ddf1-119">Peer Ip.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ddf1-120">-PeerName</span><span class="sxs-lookup"><span data-stu-id="1ddf1-120">-PeerName</span></span>
<span data-ttu-id="1ddf1-121">Der Name des virtuellen Router-Peers.</span><span class="sxs-lookup"><span data-stu-id="1ddf1-121">The name of the virtual router Peer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ddf1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ddf1-122">-ResourceGroupName</span></span>
<span data-ttu-id="1ddf1-123">Der Name der Ressourcengruppe des virtuellen Routers/Peers.</span><span class="sxs-lookup"><span data-stu-id="1ddf1-123">The resource group name of the virtual router/peer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ddf1-124">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="1ddf1-124">-VirtualRouterName</span></span>
<span data-ttu-id="1ddf1-125">Der virtuelle Router, auf dem Peer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1ddf1-125">The virtual router where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ddf1-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1ddf1-126">-Confirm</span></span>
<span data-ttu-id="1ddf1-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ddf1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ddf1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ddf1-128">-WhatIf</span></span>
<span data-ttu-id="1ddf1-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ddf1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ddf1-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ddf1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ddf1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ddf1-131">CommonParameters</span></span>
<span data-ttu-id="1ddf1-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ddf1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ddf1-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ddf1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ddf1-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1ddf1-134">INPUTS</span></span>

### <span data-ttu-id="1ddf1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1ddf1-135">System.String</span></span>

### <span data-ttu-id="1ddf1-136">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="1ddf1-136">System.UInt32</span></span>

## <span data-ttu-id="1ddf1-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1ddf1-137">OUTPUTS</span></span>

### <span data-ttu-id="1ddf1-138">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="1ddf1-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="1ddf1-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="1ddf1-139">NOTES</span></span>

## <span data-ttu-id="1ddf1-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1ddf1-140">RELATED LINKS</span></span>
