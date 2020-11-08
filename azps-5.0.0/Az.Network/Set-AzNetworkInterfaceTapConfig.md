---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 31a02e6f27d766d9f74b34c331a69c66e82d8fc5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178719"
---
# <span data-ttu-id="329a5-101">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="329a5-101">Set-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="329a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="329a5-102">SYNOPSIS</span></span>
<span data-ttu-id="329a5-103">Aktualisiert eine Tap-Konfiguration für eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="329a5-103">Updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="329a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="329a5-104">SYNTAX</span></span>

```
Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="329a5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="329a5-105">DESCRIPTION</span></span>
<span data-ttu-id="329a5-106">Die **Gruppe AzNetworkInterfaceTapConfig** aktualisiert eine Tap-Konfiguration für eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="329a5-106">The **Set-AzNetworkInterfaceTapConfig** updates a tap configuration for a network interface.</span></span>

## <span data-ttu-id="329a5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="329a5-107">EXAMPLES</span></span>

### <span data-ttu-id="329a5-108">Beispiel 1: Einrichten des TapConfiguration mit dem aktualisierten TapConfig-Namen</span><span class="sxs-lookup"><span data-stu-id="329a5-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="329a5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="329a5-109">PARAMETERS</span></span>

### <span data-ttu-id="329a5-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="329a5-110">-AsJob</span></span>
<span data-ttu-id="329a5-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="329a5-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="329a5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="329a5-112">-DefaultProfile</span></span>
<span data-ttu-id="329a5-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="329a5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="329a5-114">-Force</span><span class="sxs-lookup"><span data-stu-id="329a5-114">-Force</span></span>
<span data-ttu-id="329a5-115">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="329a5-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="329a5-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="329a5-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="329a5-117">Die Network Interface-Tap-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="329a5-117">The NetworkInterface Tap configuration</span></span>

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

### <span data-ttu-id="329a5-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="329a5-118">-Confirm</span></span>
<span data-ttu-id="329a5-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="329a5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="329a5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="329a5-120">-WhatIf</span></span>
<span data-ttu-id="329a5-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="329a5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="329a5-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="329a5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="329a5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="329a5-123">CommonParameters</span></span>
<span data-ttu-id="329a5-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="329a5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="329a5-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="329a5-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="329a5-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="329a5-126">INPUTS</span></span>

### <span data-ttu-id="329a5-127">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="329a5-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="329a5-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="329a5-128">OUTPUTS</span></span>

### <span data-ttu-id="329a5-129">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="329a5-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="329a5-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="329a5-130">NOTES</span></span>

## <span data-ttu-id="329a5-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="329a5-131">RELATED LINKS</span></span>

[<span data-ttu-id="329a5-132">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="329a5-132">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="329a5-133">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="329a5-133">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="329a5-134">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="329a5-134">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)
