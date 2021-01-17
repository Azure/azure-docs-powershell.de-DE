---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
ms.openlocfilehash: edbfdcdfc7e02c8bfdb266e1ec7a6b1308c07fa2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370906"
---
# <span data-ttu-id="f78d8-101">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f78d8-101">Set-AzNetworkProfile</span></span>

## <span data-ttu-id="f78d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f78d8-102">SYNOPSIS</span></span>
<span data-ttu-id="f78d8-103">Aktualisiert ein Netzwerkprofil.</span><span class="sxs-lookup"><span data-stu-id="f78d8-103">Updates a network profile.</span></span>

## <span data-ttu-id="f78d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f78d8-104">SYNTAX</span></span>

```
Set-AzNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f78d8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f78d8-105">DESCRIPTION</span></span>
<span data-ttu-id="f78d8-106">Das **Cmdlet "Set-AzPublicIpPrefix"** aktualisiert ein Netzwerkprofil.</span><span class="sxs-lookup"><span data-stu-id="f78d8-106">The **Set-AzPublicIpPrefix** cmdlet updates a network profile.</span></span>

## <span data-ttu-id="f78d8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f78d8-107">EXAMPLES</span></span>

### <span data-ttu-id="f78d8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f78d8-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzNetworkProfile
```

<span data-ttu-id="f78d8-109">Der erste Befehl ruft ein vorhandenes Netzwerkprofil ab.</span><span class="sxs-lookup"><span data-stu-id="f78d8-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="f78d8-110">Der zweite Befehl aktualisiert ein Tag, und der dritte Befehl fügt dem Netzwerkprofil eine Netzwerkschnittstellenkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="f78d8-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="f78d8-111">Mit dem vierten Befehl wird das Netzwerkprofil aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f78d8-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="f78d8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f78d8-112">PARAMETERS</span></span>

### <span data-ttu-id="f78d8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f78d8-113">-AsJob</span></span>
<span data-ttu-id="f78d8-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f78d8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f78d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f78d8-115">-DefaultProfile</span></span>
<span data-ttu-id="f78d8-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f78d8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f78d8-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f78d8-117">-NetworkProfile</span></span>
<span data-ttu-id="f78d8-118">Das Netzwerkprofil</span><span class="sxs-lookup"><span data-stu-id="f78d8-118">The network profile</span></span>

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

### <span data-ttu-id="f78d8-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f78d8-119">-Confirm</span></span>
<span data-ttu-id="f78d8-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f78d8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f78d8-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f78d8-121">-WhatIf</span></span>
<span data-ttu-id="f78d8-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f78d8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f78d8-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f78d8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f78d8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f78d8-124">CommonParameters</span></span>
<span data-ttu-id="f78d8-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f78d8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f78d8-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f78d8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f78d8-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f78d8-127">INPUTS</span></span>

### <span data-ttu-id="f78d8-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f78d8-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="f78d8-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f78d8-129">OUTPUTS</span></span>

### <span data-ttu-id="f78d8-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f78d8-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="f78d8-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f78d8-131">NOTES</span></span>

## <span data-ttu-id="f78d8-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f78d8-132">RELATED LINKS</span></span>

[<span data-ttu-id="f78d8-133">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f78d8-133">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="f78d8-134">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f78d8-134">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="f78d8-135">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f78d8-135">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)
