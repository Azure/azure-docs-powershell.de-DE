---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
ms.openlocfilehash: 5cb8c8f93b491476e01d5ae54cf2db93ac4a848a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944831"
---
# <span data-ttu-id="643d0-101">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="643d0-101">Set-AzNetworkProfile</span></span>

## <span data-ttu-id="643d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="643d0-102">SYNOPSIS</span></span>
<span data-ttu-id="643d0-103">Aktualisiert ein Netzwerkprofil.</span><span class="sxs-lookup"><span data-stu-id="643d0-103">Updates a network profile.</span></span>

## <span data-ttu-id="643d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="643d0-104">SYNTAX</span></span>

```
Set-AzNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="643d0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="643d0-105">DESCRIPTION</span></span>
<span data-ttu-id="643d0-106">Das **Cmdlet Set-AzPublicIpPrefix** aktualisiert ein Netzwerkprofil.</span><span class="sxs-lookup"><span data-stu-id="643d0-106">The **Set-AzPublicIpPrefix** cmdlet updates a network profile.</span></span>

## <span data-ttu-id="643d0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="643d0-107">EXAMPLES</span></span>

### <span data-ttu-id="643d0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="643d0-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzNetworkProfile
```

<span data-ttu-id="643d0-109">Der erste Befehl ruft ein vorhandenes Netzwerkprofil ab.</span><span class="sxs-lookup"><span data-stu-id="643d0-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="643d0-110">Der zweite Befehl aktualisiert ein Tag, und der dritte Befehl fügt eine Netzwerkschnittstellenkonfiguration im Netzwerkprofil hinzu.</span><span class="sxs-lookup"><span data-stu-id="643d0-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="643d0-111">Mit dem vierten Befehl wird das Netzwerkprofil aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="643d0-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="643d0-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="643d0-112">PARAMETERS</span></span>

### <span data-ttu-id="643d0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="643d0-113">-AsJob</span></span>
<span data-ttu-id="643d0-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="643d0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="643d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="643d0-115">-DefaultProfile</span></span>
<span data-ttu-id="643d0-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="643d0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="643d0-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="643d0-117">-NetworkProfile</span></span>
<span data-ttu-id="643d0-118">Das Netzwerkprofil</span><span class="sxs-lookup"><span data-stu-id="643d0-118">The network profile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="643d0-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="643d0-119">-Confirm</span></span>
<span data-ttu-id="643d0-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="643d0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="643d0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="643d0-121">-WhatIf</span></span>
<span data-ttu-id="643d0-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="643d0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="643d0-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="643d0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="643d0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="643d0-124">CommonParameters</span></span>
<span data-ttu-id="643d0-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="643d0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="643d0-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="643d0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="643d0-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="643d0-127">INPUTS</span></span>

### <span data-ttu-id="643d0-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="643d0-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="643d0-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="643d0-129">OUTPUTS</span></span>

### <span data-ttu-id="643d0-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="643d0-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="643d0-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="643d0-131">NOTES</span></span>

## <span data-ttu-id="643d0-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="643d0-132">RELATED LINKS</span></span>

[<span data-ttu-id="643d0-133">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="643d0-133">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="643d0-134">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="643d0-134">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="643d0-135">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="643d0-135">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)
