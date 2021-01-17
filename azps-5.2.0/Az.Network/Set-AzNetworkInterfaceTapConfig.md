---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 31a02e6f27d766d9f74b34c331a69c66e82d8fc5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370920"
---
# <span data-ttu-id="4a0b9-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="4a0b9-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="4a0b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a0b9-102">SYNOPSIS</span></span>
<span data-ttu-id="4a0b9-103">Aktualisiert eine Anzapfkonfiguration für eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4a0b9-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="4a0b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a0b9-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a0b9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a0b9-105">DESCRIPTION</span></span>
<span data-ttu-id="4a0b9-106">**Set-AzNetworkInterfaceTapConfig** aktualisiert eine Anzapfkonfiguration für eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4a0b9-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="4a0b9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4a0b9-107">EXAMPLES</span></span>

### <span data-ttu-id="4a0b9-108">Beispiel 1: Festlegen der TapConfiguration mit dem aktualisierten Namen "TapConfig"</span><span class="sxs-lookup"><span data-stu-id="4a0b9-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="4a0b9-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a0b9-109">PARAMETERS</span></span>

### <span data-ttu-id="4a0b9-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a0b9-110">-AsJob</span></span>
<span data-ttu-id="4a0b9-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4a0b9-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a0b9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a0b9-112">-DefaultProfile</span></span>
<span data-ttu-id="4a0b9-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a0b9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a0b9-114">-Force</span><span class="sxs-lookup"><span data-stu-id="4a0b9-114">-Force</span></span>
<span data-ttu-id="4a0b9-115">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="4a0b9-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4a0b9-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="4a0b9-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="4a0b9-117">Konfiguration von "NetworkInterface Tap"</span><span class="sxs-lookup"><span data-stu-id="4a0b9-117">The NetworkInterface Tap configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a0b9-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a0b9-118">-Confirm</span></span>
<span data-ttu-id="4a0b9-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4a0b9-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a0b9-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4a0b9-120">-WhatIf</span></span>
<span data-ttu-id="4a0b9-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a0b9-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a0b9-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a0b9-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a0b9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a0b9-123">CommonParameters</span></span>
<span data-ttu-id="4a0b9-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a0b9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a0b9-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a0b9-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a0b9-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4a0b9-126">INPUTS</span></span>

### <span data-ttu-id="4a0b9-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a0b9-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="4a0b9-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4a0b9-128">OUTPUTS</span></span>

### <span data-ttu-id="4a0b9-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4a0b9-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="4a0b9-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4a0b9-130">NOTES</span></span>

## <span data-ttu-id="4a0b9-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4a0b9-131">RELATED LINKS</span></span>

[<span data-ttu-id="4a0b9-132">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="4a0b9-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="4a0b9-133">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="4a0b9-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="4a0b9-134">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="4a0b9-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)
