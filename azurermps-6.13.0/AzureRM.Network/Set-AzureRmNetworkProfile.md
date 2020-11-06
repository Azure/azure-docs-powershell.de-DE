---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkProfile.md
ms.openlocfilehash: 370229f44b260367759ca2f51319258627d3d8c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476001"
---
# <span data-ttu-id="558bb-101">Set-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="558bb-101">Set-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="558bb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="558bb-102">SYNOPSIS</span></span>
<span data-ttu-id="558bb-103">Legt den Zielstatus für ein vorhandenes Netzwerkprofil fest</span><span class="sxs-lookup"><span data-stu-id="558bb-103">Sets the goal state for an existing network profile</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="558bb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="558bb-104">SYNTAX</span></span>

```
Set-AzureRmNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="558bb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="558bb-105">DESCRIPTION</span></span>
<span data-ttu-id="558bb-106">Das Cmdlet " **Set-AzureRmPublicIpPrefix** " legt den Zielstatus für ein Netzwerkprofil fest.</span><span class="sxs-lookup"><span data-stu-id="558bb-106">The **Set-AzureRmPublicIpPrefix** cmdlet sets the goal state for a network profile.</span></span>

## <span data-ttu-id="558bb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="558bb-107">EXAMPLES</span></span>

### <span data-ttu-id="558bb-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="558bb-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzureRmNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzureRmNetworkProfile
```

<span data-ttu-id="558bb-109">Der erste Befehl ruft ein vorhandenes Netzwerkprofil ab.</span><span class="sxs-lookup"><span data-stu-id="558bb-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="558bb-110">Der zweite Befehl aktualisiert eine Kategorie, und die dritte fügt eine Netzwerkschnittstellenkonfiguration für das Netzwerkprofil hinzu.</span><span class="sxs-lookup"><span data-stu-id="558bb-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="558bb-111">Der vierte Befehl aktualisiert das Netzwerkprofil.</span><span class="sxs-lookup"><span data-stu-id="558bb-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="558bb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="558bb-112">PARAMETERS</span></span>

### <span data-ttu-id="558bb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="558bb-113">-AsJob</span></span>
<span data-ttu-id="558bb-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="558bb-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="558bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="558bb-115">-DefaultProfile</span></span>
<span data-ttu-id="558bb-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="558bb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="558bb-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="558bb-117">-NetworkProfile</span></span>
<span data-ttu-id="558bb-118">Das Netzwerkprofil</span><span class="sxs-lookup"><span data-stu-id="558bb-118">The network profile</span></span>

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

### <span data-ttu-id="558bb-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="558bb-119">-Confirm</span></span>
<span data-ttu-id="558bb-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="558bb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="558bb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="558bb-121">-WhatIf</span></span>
<span data-ttu-id="558bb-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="558bb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="558bb-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="558bb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="558bb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="558bb-124">CommonParameters</span></span>
<span data-ttu-id="558bb-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="558bb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="558bb-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="558bb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="558bb-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="558bb-127">INPUTS</span></span>

### <span data-ttu-id="558bb-128">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="558bb-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="558bb-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="558bb-129">OUTPUTS</span></span>

### <span data-ttu-id="558bb-130">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="558bb-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="558bb-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="558bb-131">NOTES</span></span>

## <span data-ttu-id="558bb-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="558bb-132">RELATED LINKS</span></span>
