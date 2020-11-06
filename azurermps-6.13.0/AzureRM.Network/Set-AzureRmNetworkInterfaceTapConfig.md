---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: b2034f27cb6c5332b190e3412963dde99f4c9ba0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476005"
---
# <span data-ttu-id="b0be0-101">Set-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="b0be0-101">Set-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="b0be0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b0be0-102">SYNOPSIS</span></span>
<span data-ttu-id="b0be0-103">Legt den Zielzustand einer Tap-Konfiguration fest.</span><span class="sxs-lookup"><span data-stu-id="b0be0-103">Sets the goal state of a Tap Configuration</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0be0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0be0-104">SYNTAX</span></span>

```
Set-AzureRmNetworkInterfaceTapConfig -NetworkInterfaceTapConfig <PSNetworkInterfaceTapConfiguration> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0be0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0be0-105">DESCRIPTION</span></span>
<span data-ttu-id="b0be0-106">Das **Set-AzureRmNetworkInterfaceTapConfig** legt den Zielstatus für eine Azure-Netzwerkschnittstelle fest.</span><span class="sxs-lookup"><span data-stu-id="b0be0-106">The **Set-AzureRmNetworkInterfaceTapConfig** sets the goal state for an Azure network interface.</span></span>

## <span data-ttu-id="b0be0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0be0-107">EXAMPLES</span></span>

### <span data-ttu-id="b0be0-108">Beispiel 1: Einrichten des TapConfiguration mit dem aktualisierten TapConfig-Namen</span><span class="sxs-lookup"><span data-stu-id="b0be0-108">Example 1: Set the TapConfiguration with updated TapConfig name</span></span>
```
PS C:\>$tapConfig = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
PS C:\>$tapConfig.Name = "NewTapName"
PS C:\>Set-AzureRmNetworkInterfaceTapConfig -NetworkInterfaceTapConfig $tapConfig
```

## <span data-ttu-id="b0be0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0be0-109">PARAMETERS</span></span>

### <span data-ttu-id="b0be0-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0be0-110">-AsJob</span></span>
<span data-ttu-id="b0be0-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b0be0-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0be0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0be0-112">-DefaultProfile</span></span>
<span data-ttu-id="b0be0-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b0be0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0be0-114">-Force</span><span class="sxs-lookup"><span data-stu-id="b0be0-114">-Force</span></span>
<span data-ttu-id="b0be0-115">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="b0be0-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b0be0-116">-NetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="b0be0-116">-NetworkInterfaceTapConfig</span></span>
<span data-ttu-id="b0be0-117">Network Interface Tippen Sie auf configurtion</span><span class="sxs-lookup"><span data-stu-id="b0be0-117">The NetworkInterface Tap configurtion</span></span>

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

### <span data-ttu-id="b0be0-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b0be0-118">-Confirm</span></span>
<span data-ttu-id="b0be0-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b0be0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0be0-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0be0-120">-WhatIf</span></span>
<span data-ttu-id="b0be0-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b0be0-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0be0-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b0be0-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0be0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0be0-123">CommonParameters</span></span>
<span data-ttu-id="b0be0-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0be0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0be0-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0be0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0be0-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b0be0-126">INPUTS</span></span>

### <span data-ttu-id="b0be0-127">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="b0be0-127">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="b0be0-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b0be0-128">OUTPUTS</span></span>

### <span data-ttu-id="b0be0-129">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b0be0-129">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="b0be0-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="b0be0-130">NOTES</span></span>

## <span data-ttu-id="b0be0-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b0be0-131">RELATED LINKS</span></span>
