---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: caa0baf8e26ea2cec94a59bd2a86e6394b4ade91
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823824"
---
# <span data-ttu-id="e96fd-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e96fd-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="e96fd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e96fd-102">SYNOPSIS</span></span>
<span data-ttu-id="e96fd-103">Legt die Tags für eine vorhandene PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e96fd-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="e96fd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e96fd-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e96fd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e96fd-105">DESCRIPTION</span></span>
<span data-ttu-id="e96fd-106">Das Cmdlet " **Set-AzPublicIpPrefix** " legt die Tags für ein öffentliches IP-Präfix fest.</span><span class="sxs-lookup"><span data-stu-id="e96fd-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="e96fd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e96fd-107">EXAMPLES</span></span>

### <span data-ttu-id="e96fd-108">Einrichten der Tags für öffentliches IP-Präfix</span><span class="sxs-lookup"><span data-stu-id="e96fd-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="e96fd-109">Der erste Befehl ruft ein vorhandenes Öffentliches IP-Präfix ab, der zweite Befehl legt die Tags-Eigenschaft fest, und der dritte Befehl aktualisiert das vorhandene Objekt.</span><span class="sxs-lookup"><span data-stu-id="e96fd-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="e96fd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e96fd-110">PARAMETERS</span></span>

### <span data-ttu-id="e96fd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e96fd-111">-AsJob</span></span>
<span data-ttu-id="e96fd-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e96fd-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e96fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e96fd-113">-DefaultProfile</span></span>
<span data-ttu-id="e96fd-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e96fd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e96fd-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e96fd-115">-PublicIpPrefix</span></span>
<span data-ttu-id="e96fd-116">Die PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e96fd-116">The PublicIpPrefix</span></span>

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

### <span data-ttu-id="e96fd-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e96fd-117">-Confirm</span></span>
<span data-ttu-id="e96fd-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e96fd-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e96fd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e96fd-119">-WhatIf</span></span>
<span data-ttu-id="e96fd-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e96fd-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e96fd-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e96fd-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e96fd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e96fd-122">CommonParameters</span></span>
<span data-ttu-id="e96fd-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e96fd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e96fd-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e96fd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e96fd-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e96fd-125">INPUTS</span></span>

### <span data-ttu-id="e96fd-126">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e96fd-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="e96fd-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e96fd-127">OUTPUTS</span></span>

### <span data-ttu-id="e96fd-128">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e96fd-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="e96fd-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="e96fd-129">NOTES</span></span>

## <span data-ttu-id="e96fd-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e96fd-130">RELATED LINKS</span></span>

[<span data-ttu-id="e96fd-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e96fd-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="e96fd-132">Neu – AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e96fd-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="e96fd-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e96fd-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)
