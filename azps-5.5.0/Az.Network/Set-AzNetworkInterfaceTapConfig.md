---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 31a02e6f27d766d9f74b34c331a69c66e82d8fc5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156684"
---
# <span data-ttu-id="015c0-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="015c0-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="015c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="015c0-102">SYNOPSIS</span></span>
<span data-ttu-id="015c0-103">Aktualisiert eine Anzapfkonfiguration für eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="015c0-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="015c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="015c0-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="015c0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="015c0-105">DESCRIPTION</span></span>
<span data-ttu-id="015c0-106">**Set-AzNetworkInterfaceTapConfig** aktualisiert eine Anzapfkonfiguration für eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="015c0-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="015c0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="015c0-107">EXAMPLES</span></span>

### <span data-ttu-id="015c0-108">Beispiel 1: Festlegen der TapConfiguration mit dem aktualisierten Namen "TapConfig"</span><span class="sxs-lookup"><span data-stu-id="015c0-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="015c0-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="015c0-109">PARAMETERS</span></span>

### <span data-ttu-id="015c0-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="015c0-110">-AsJob</span></span>
<span data-ttu-id="015c0-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="015c0-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="015c0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="015c0-112">-DefaultProfile</span></span>
<span data-ttu-id="015c0-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="015c0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="015c0-114">-Force</span><span class="sxs-lookup"><span data-stu-id="015c0-114">-Force</span></span>
<span data-ttu-id="015c0-115">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="015c0-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="015c0-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="015c0-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="015c0-117">Konfiguration von "NetworkInterface-Anzapfen"</span><span class="sxs-lookup"><span data-stu-id="015c0-117">The NetworkInterface Tap configuration</span></span>

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

### <span data-ttu-id="015c0-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="015c0-118">-Confirm</span></span>
<span data-ttu-id="015c0-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="015c0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="015c0-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="015c0-120">-WhatIf</span></span>
<span data-ttu-id="015c0-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="015c0-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="015c0-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="015c0-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="015c0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="015c0-123">CommonParameters</span></span>
<span data-ttu-id="015c0-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="015c0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="015c0-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="015c0-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="015c0-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="015c0-126">INPUTS</span></span>

### <span data-ttu-id="015c0-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="015c0-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="015c0-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="015c0-128">OUTPUTS</span></span>

### <span data-ttu-id="015c0-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="015c0-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="015c0-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="015c0-130">NOTES</span></span>

## <span data-ttu-id="015c0-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="015c0-131">RELATED LINKS</span></span>

[<span data-ttu-id="015c0-132">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="015c0-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="015c0-133">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="015c0-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="015c0-134">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="015c0-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)
