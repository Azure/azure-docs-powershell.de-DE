---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
ms.openlocfilehash: 6ae61090f98cbb9929cc5ad1b2745fbf88f21a2a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166276"
---
# <span data-ttu-id="f1113-101">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f1113-101">New-AzIpGroup</span></span>

## <span data-ttu-id="f1113-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1113-102">SYNOPSIS</span></span>
<span data-ttu-id="f1113-103">Erstellt eine Azure-IpGroup.</span><span class="sxs-lookup"><span data-stu-id="f1113-103">Creates an Azure IpGroup.</span></span>

## <span data-ttu-id="f1113-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1113-104">SYNTAX</span></span>

```
New-AzIpGroup -Name <String> -ResourceGroupName <String> [-IpAddress <String[]>] -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1113-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1113-105">DESCRIPTION</span></span>
<span data-ttu-id="f1113-106">Das Cmdlet " **New-AzIpGroup** " erstellt ein Azure-IpGroup</span><span class="sxs-lookup"><span data-stu-id="f1113-106">The **New-AzIpGroup** cmdlet creates an Azure IpGroup</span></span>

## <span data-ttu-id="f1113-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1113-107">EXAMPLES</span></span>

### <span data-ttu-id="f1113-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f1113-108">Example 1</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US'
```

### <span data-ttu-id="f1113-109">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f1113-109">Example 2</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US' -IpAddress 10.0.0.0/24,11.9.0.0/24
```

## <span data-ttu-id="f1113-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1113-110">PARAMETERS</span></span>

### <span data-ttu-id="f1113-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1113-111">-AsJob</span></span>
<span data-ttu-id="f1113-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f1113-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1113-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1113-113">-DefaultProfile</span></span>
<span data-ttu-id="f1113-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f1113-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1113-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f1113-115">-Force</span></span>
<span data-ttu-id="f1113-116">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="f1113-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1113-117">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="f1113-117">-IpAddress</span></span>
<span data-ttu-id="f1113-118">In der IpGroup definierte ipaddresss</span><span class="sxs-lookup"><span data-stu-id="f1113-118">IpAddresses defined in the IpGroup</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1113-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="f1113-119">-Location</span></span>
<span data-ttu-id="f1113-120">Die Position.</span><span class="sxs-lookup"><span data-stu-id="f1113-120">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1113-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f1113-121">-Name</span></span>
<span data-ttu-id="f1113-122">Der Name des ipgroup.</span><span class="sxs-lookup"><span data-stu-id="f1113-122">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1113-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1113-123">-ResourceGroupName</span></span>
<span data-ttu-id="f1113-124">Der Ressourcengruppenname des ipgroup.</span><span class="sxs-lookup"><span data-stu-id="f1113-124">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1113-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="f1113-125">-Tag</span></span>
<span data-ttu-id="f1113-126">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="f1113-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1113-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f1113-127">-Confirm</span></span>
<span data-ttu-id="f1113-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1113-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1113-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1113-129">-WhatIf</span></span>
<span data-ttu-id="f1113-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1113-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1113-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1113-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1113-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1113-132">CommonParameters</span></span>
<span data-ttu-id="f1113-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1113-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1113-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1113-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1113-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1113-135">INPUTS</span></span>

### <span data-ttu-id="f1113-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f1113-136">System.String</span></span>

### <span data-ttu-id="f1113-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f1113-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="f1113-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f1113-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f1113-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1113-139">OUTPUTS</span></span>

### <span data-ttu-id="f1113-140">Microsoft. Azure. Commands. Network. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="f1113-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="f1113-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1113-141">NOTES</span></span>

## <span data-ttu-id="f1113-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1113-142">RELATED LINKS</span></span>
