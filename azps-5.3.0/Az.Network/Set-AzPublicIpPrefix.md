---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: 4244f8c97090009272933d73a64323e4af5dfbbf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473371"
---
# <span data-ttu-id="74535-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="74535-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="74535-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74535-102">SYNOPSIS</span></span>
<span data-ttu-id="74535-103">Legt die Markierungen für ein vorhandenes PublicIpPrefix fest.</span><span class="sxs-lookup"><span data-stu-id="74535-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="74535-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74535-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74535-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74535-105">DESCRIPTION</span></span>
<span data-ttu-id="74535-106">Das **Cmdlet "Set-AzPublicIpPrefix"** legt die Tags für ein öffentliches IP-Präfix fest.</span><span class="sxs-lookup"><span data-stu-id="74535-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="74535-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="74535-107">EXAMPLES</span></span>

### <span data-ttu-id="74535-108">Festlegen der Tags für das Präfix "Public IP"</span><span class="sxs-lookup"><span data-stu-id="74535-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="74535-109">Der erste Befehl ruft ein vorhandenes öffentliches IP-Präfix ab, der zweite Befehl legt die Tageigenschaft fest, und der dritte Befehl aktualisiert das vorhandene Objekt.</span><span class="sxs-lookup"><span data-stu-id="74535-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="74535-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74535-110">PARAMETERS</span></span>

### <span data-ttu-id="74535-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74535-111">-AsJob</span></span>
<span data-ttu-id="74535-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="74535-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74535-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74535-113">-DefaultProfile</span></span>
<span data-ttu-id="74535-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74535-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74535-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="74535-115">-PublicIpPrefix</span></span>
<span data-ttu-id="74535-116">The PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="74535-116">The PublicIpPrefix</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74535-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74535-117">-Confirm</span></span>
<span data-ttu-id="74535-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="74535-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74535-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="74535-119">-WhatIf</span></span>
<span data-ttu-id="74535-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74535-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74535-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74535-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74535-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74535-122">CommonParameters</span></span>
<span data-ttu-id="74535-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74535-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74535-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74535-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74535-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="74535-125">INPUTS</span></span>

### <span data-ttu-id="74535-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="74535-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="74535-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="74535-127">OUTPUTS</span></span>

### <span data-ttu-id="74535-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="74535-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="74535-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="74535-129">NOTES</span></span>

## <span data-ttu-id="74535-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="74535-130">RELATED LINKS</span></span>

[<span data-ttu-id="74535-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="74535-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="74535-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="74535-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="74535-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="74535-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)
