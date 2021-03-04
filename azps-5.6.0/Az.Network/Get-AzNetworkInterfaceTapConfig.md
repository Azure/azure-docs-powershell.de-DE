---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 1c46cb01a2b30853248ca941cbb61d8b0429fc49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919891"
---
# <span data-ttu-id="8da13-101">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8da13-101">Get-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="8da13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8da13-102">SYNOPSIS</span></span>
<span data-ttu-id="8da13-103">Ruft eine Tap-Konfigurationsressource ab.</span><span class="sxs-lookup"><span data-stu-id="8da13-103">Gets a Tap configuration resource.</span></span>

## <span data-ttu-id="8da13-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8da13-104">SYNTAX</span></span>

### <span data-ttu-id="8da13-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8da13-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8da13-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8da13-106">GetByResourceIdParameterSet</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8da13-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8da13-107">DESCRIPTION</span></span>
<span data-ttu-id="8da13-108">Das **Get-AzNetworkInterfaceTapConfig-Cmdlet** erhält eine Azure Tap-Konfiguration für eine bestimmte Ressourcengruppe, Netzwerkschnittstelle und tippt auf Konfigurationsname oder Liste der Tippkonfigurationen in einer Ressourcengruppe und Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8da13-108">The **Get-AzNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="8da13-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8da13-109">EXAMPLES</span></span>

### <span data-ttu-id="8da13-110">Beispiel 1: Alle Tippkonfigurationen für eine bestimmte Netzwerkschnittstelle erhalten</span><span class="sxs-lookup"><span data-stu-id="8da13-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="8da13-111">Dieser Befehl ruft Tippkonfigurationen ab, die für die angegebene Netzwerkschnittstelle hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="8da13-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="8da13-112">Beispiel 2: Erhalten einer bestimmten Tippkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8da13-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="8da13-113">Dieser Befehl ruft eine spezifische Tippkonfiguration ab, die für die angegebene Netzwerkschnittstelle hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="8da13-113">This command gets specific tap configuration added for the given network interface.</span></span>

### <span data-ttu-id="8da13-114">Beispiel 3: Erhalten einer bestimmten Tippkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8da13-114">Example 3: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

<span data-ttu-id="8da13-115">Dieser Befehl ruft Tippkonfigurationen ab, die für die angegebene Netzwerkschnittstelle hinzugefügt wurden, und der Name beginnt mit "tapconfig".</span><span class="sxs-lookup"><span data-stu-id="8da13-115">This command gets tap configurations added for the given network interface with name starting with "tapconfig".</span></span>

## <span data-ttu-id="8da13-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8da13-116">PARAMETERS</span></span>

### <span data-ttu-id="8da13-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da13-117">-DefaultProfile</span></span>
<span data-ttu-id="8da13-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8da13-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8da13-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8da13-119">-Name</span></span>
<span data-ttu-id="8da13-120">Name der spezifischen Tippkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="8da13-120">Name of the specific tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="8da13-121">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="8da13-121">-NetworkInterfaceName</span></span>
<span data-ttu-id="8da13-122">Der Name der Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8da13-122">The Network Interface name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da13-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8da13-123">-ResourceGroupName</span></span>
<span data-ttu-id="8da13-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8da13-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da13-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8da13-125">-ResourceId</span></span>
<span data-ttu-id="8da13-126">ResourceId der TapConfiguration-Ressource</span><span class="sxs-lookup"><span data-stu-id="8da13-126">ResourceId of the TapConfiguration resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da13-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8da13-127">-Confirm</span></span>
<span data-ttu-id="8da13-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8da13-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8da13-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8da13-129">-WhatIf</span></span>
<span data-ttu-id="8da13-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8da13-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8da13-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8da13-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8da13-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da13-132">CommonParameters</span></span>
<span data-ttu-id="8da13-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8da13-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da13-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8da13-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da13-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8da13-135">INPUTS</span></span>

### <span data-ttu-id="8da13-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8da13-136">System.String</span></span>

## <span data-ttu-id="8da13-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8da13-137">OUTPUTS</span></span>

### <span data-ttu-id="8da13-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="8da13-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="8da13-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8da13-139">NOTES</span></span>

## <span data-ttu-id="8da13-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8da13-140">RELATED LINKS</span></span>

[<span data-ttu-id="8da13-141">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8da13-141">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="8da13-142">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8da13-142">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="8da13-143">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8da13-143">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
