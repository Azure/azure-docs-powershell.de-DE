---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: 2937aafbcffd2444051b9bed0a764cb3aede6c52
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943979"
---
# <span data-ttu-id="195b6-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="195b6-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="195b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="195b6-102">SYNOPSIS</span></span>
<span data-ttu-id="195b6-103">Legt die Tags für ein vorhandenes PublicIpPrefix fest.</span><span class="sxs-lookup"><span data-stu-id="195b6-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="195b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="195b6-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="195b6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="195b6-105">DESCRIPTION</span></span>
<span data-ttu-id="195b6-106">Das **Cmdlet Set-AzPublicIpPrefix** legt die Tags für ein öffentliches IP-Präfix fest.</span><span class="sxs-lookup"><span data-stu-id="195b6-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="195b6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="195b6-107">EXAMPLES</span></span>

### <span data-ttu-id="195b6-108">Festlegen der Tags für öffentliches IP-Präfix</span><span class="sxs-lookup"><span data-stu-id="195b6-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="195b6-109">Der erste Befehl ruft ein vorhandenes öffentliches IP-Präfix ab, der zweite Befehl legt die Tags-Eigenschaft fest, und der dritte Befehl aktualisiert das vorhandene Objekt.</span><span class="sxs-lookup"><span data-stu-id="195b6-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="195b6-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="195b6-110">PARAMETERS</span></span>

### <span data-ttu-id="195b6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="195b6-111">-AsJob</span></span>
<span data-ttu-id="195b6-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="195b6-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="195b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="195b6-113">-DefaultProfile</span></span>
<span data-ttu-id="195b6-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="195b6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="195b6-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="195b6-115">-PublicIpPrefix</span></span>
<span data-ttu-id="195b6-116">Das PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="195b6-116">The PublicIpPrefix</span></span>

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

### <span data-ttu-id="195b6-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="195b6-117">-Confirm</span></span>
<span data-ttu-id="195b6-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="195b6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="195b6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="195b6-119">-WhatIf</span></span>
<span data-ttu-id="195b6-120">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="195b6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="195b6-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="195b6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="195b6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="195b6-122">CommonParameters</span></span>
<span data-ttu-id="195b6-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="195b6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="195b6-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="195b6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="195b6-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="195b6-125">INPUTS</span></span>

### <span data-ttu-id="195b6-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="195b6-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="195b6-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="195b6-127">OUTPUTS</span></span>

### <span data-ttu-id="195b6-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="195b6-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="195b6-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="195b6-129">NOTES</span></span>

## <span data-ttu-id="195b6-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="195b6-130">RELATED LINKS</span></span>

[<span data-ttu-id="195b6-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="195b6-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="195b6-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="195b6-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="195b6-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="195b6-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)
