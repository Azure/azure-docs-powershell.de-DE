---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: fa4c6db39de9f0d27fa80c4ee09e4decb319e2aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296045"
---
# <span data-ttu-id="ca953-101">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ca953-101">Get-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="ca953-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca953-102">SYNOPSIS</span></span>
<span data-ttu-id="ca953-103">Ruft eine Anzapfkonfigurationsressource ab.</span><span class="sxs-lookup"><span data-stu-id="ca953-103">Gets a Tap configuration resource.</span></span>

## <span data-ttu-id="ca953-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca953-104">SYNTAX</span></span>

### <span data-ttu-id="ca953-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ca953-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca953-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca953-106">GetByResourceIdParameterSet</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca953-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ca953-107">DESCRIPTION</span></span>
<span data-ttu-id="ca953-108">Das **Cmdlet "Get-AzNetworkInterfaceTapConfig"** ruft eine Azure -Anzapfkonfiguration für eine bestimmte Ressourcengruppe, Netzwerkschnittstelle und tippen Sie auf den Konfigurationsnamen oder die Liste der Anzapfkonfigurationen in einer Ressourcengruppe und Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="ca953-108">The **Get-AzNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="ca953-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ca953-109">EXAMPLES</span></span>

### <span data-ttu-id="ca953-110">Beispiel 1: Alle Tippkonfigurationen für eine bestimmte Netzwerkschnittstelle erhalten</span><span class="sxs-lookup"><span data-stu-id="ca953-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="ca953-111">Mit diesem Befehl werden Tippkonfigurationen für die angegebene Netzwerkschnittstelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ca953-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="ca953-112">Beispiel 2: Erhalten einer bestimmten Tippkonfiguration</span><span class="sxs-lookup"><span data-stu-id="ca953-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="ca953-113">Mit diesem Befehl wird eine spezifische Tippkonfiguration für die angegebene Netzwerkschnittstelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ca953-113">This command gets specific tap configuration added for the given network interface.</span></span>

### <span data-ttu-id="ca953-114">Beispiel 3: Erhalten einer bestimmten Tippkonfiguration</span><span class="sxs-lookup"><span data-stu-id="ca953-114">Example 3: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

<span data-ttu-id="ca953-115">Mit diesem Befehl werden Tippkonfigurationen für die angegebene Netzwerkschnittstelle hinzugefügt, deren Name mit "tapconfig" beginnt.</span><span class="sxs-lookup"><span data-stu-id="ca953-115">This command gets tap configurations added for the given network interface with name starting with "tapconfig".</span></span>

## <span data-ttu-id="ca953-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca953-116">PARAMETERS</span></span>

### <span data-ttu-id="ca953-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca953-117">-DefaultProfile</span></span>
<span data-ttu-id="ca953-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca953-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca953-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ca953-119">-Name</span></span>
<span data-ttu-id="ca953-120">Name der spezifischen Tippkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="ca953-120">Name of the specific tap configuration.</span></span>

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

### <span data-ttu-id="ca953-121">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="ca953-121">-NetworkInterfaceName</span></span>
<span data-ttu-id="ca953-122">Der Name der Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ca953-122">The Network Interface name.</span></span>

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

### <span data-ttu-id="ca953-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca953-123">-ResourceGroupName</span></span>
<span data-ttu-id="ca953-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ca953-124">The resource group name.</span></span>

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

### <span data-ttu-id="ca953-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca953-125">-ResourceId</span></span>
<span data-ttu-id="ca953-126">ResourceId der Ressource "TapConfiguration"</span><span class="sxs-lookup"><span data-stu-id="ca953-126">ResourceId of the TapConfiguration resource</span></span>

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

### <span data-ttu-id="ca953-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca953-127">-Confirm</span></span>
<span data-ttu-id="ca953-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ca953-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca953-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ca953-129">-WhatIf</span></span>
<span data-ttu-id="ca953-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca953-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca953-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ca953-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca953-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca953-132">CommonParameters</span></span>
<span data-ttu-id="ca953-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca953-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca953-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca953-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca953-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ca953-135">INPUTS</span></span>

### <span data-ttu-id="ca953-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ca953-136">System.String</span></span>

## <span data-ttu-id="ca953-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ca953-137">OUTPUTS</span></span>

### <span data-ttu-id="ca953-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca953-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="ca953-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ca953-139">NOTES</span></span>

## <span data-ttu-id="ca953-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ca953-140">RELATED LINKS</span></span>

[<span data-ttu-id="ca953-141">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ca953-141">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="ca953-142">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ca953-142">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="ca953-143">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ca953-143">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
