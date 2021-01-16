---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 52fc2a3c84c70d52c173bc256ca2b0d952307e91
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294479"
---
# <span data-ttu-id="f740b-101">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="f740b-101">Remove-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="f740b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f740b-102">SYNOPSIS</span></span>
<span data-ttu-id="f740b-103">Entfernt eine Anzapfkonfiguration von einer bestimmten Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="f740b-103">Removes a tap configuration from given network interface</span></span>

## <span data-ttu-id="f740b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f740b-104">SYNTAX</span></span>

### <span data-ttu-id="f740b-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f740b-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f740b-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f740b-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f740b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f740b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f740b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f740b-108">DESCRIPTION</span></span>
<span data-ttu-id="f740b-109">Das **Cmdlet "Remove-AzNetworkInterfaceTapConfig"** entfernt eine Azure-Tippkonfiguration aus einer Netzwerkschnittstellenliste.</span><span class="sxs-lookup"><span data-stu-id="f740b-109">The **Remove-AzNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="f740b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f740b-110">EXAMPLES</span></span>

### <span data-ttu-id="f740b-111">Beispiel 1: Entfernen einer Tippkonfiguration</span><span class="sxs-lookup"><span data-stu-id="f740b-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="f740b-112">Mit diesem Befehl wird die TapConfiguration aus NetworkInterface1 in einer Ressourcengruppe "ResourceGroup1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="f740b-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="f740b-113">Da der *Parameter "Force"* nicht verwendet wird, wird der Benutzer aufgefordert, diese Aktion zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="f740b-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="f740b-114">Beispiel 2: Entfernen einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="f740b-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="f740b-115">Mit diesem Befehl wird die TapConfiguration aus NetworkInterface1 in einer Ressourcengruppe "ResourceGroup1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="f740b-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="f740b-116">Da der *Parameter "Force"* verwendet wird, wird der Benutzer nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="f740b-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="f740b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f740b-117">PARAMETERS</span></span>

### <span data-ttu-id="f740b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f740b-118">-DefaultProfile</span></span>
<span data-ttu-id="f740b-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f740b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f740b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f740b-120">-Force</span></span>
<span data-ttu-id="f740b-121">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="f740b-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f740b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f740b-122">-InputObject</span></span>
<span data-ttu-id="f740b-123">Verweis auf NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="f740b-123">Reference to NetworkInterfaceTapConfig.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f740b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f740b-124">-Name</span></span>
<span data-ttu-id="f740b-125">Der Name des virtuellen Netzwerk-Peerings.</span><span class="sxs-lookup"><span data-stu-id="f740b-125">The virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f740b-126">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="f740b-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="f740b-127">Der Name des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="f740b-127">The virtual network name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f740b-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f740b-128">-PassThru</span></span>
<span data-ttu-id="f740b-129">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f740b-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f740b-130">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="f740b-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f740b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f740b-131">-ResourceGroupName</span></span>
<span data-ttu-id="f740b-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f740b-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f740b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f740b-133">-ResourceId</span></span>
<span data-ttu-id="f740b-134">NetworkInterfaceTapConfig-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f740b-134">NetworkInterfaceTapConfig resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f740b-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f740b-135">-Confirm</span></span>
<span data-ttu-id="f740b-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f740b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f740b-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f740b-137">-WhatIf</span></span>
<span data-ttu-id="f740b-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f740b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f740b-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f740b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f740b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f740b-140">CommonParameters</span></span>
<span data-ttu-id="f740b-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f740b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f740b-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f740b-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f740b-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f740b-143">INPUTS</span></span>

### <span data-ttu-id="f740b-144">System.String</span><span class="sxs-lookup"><span data-stu-id="f740b-144">System.String</span></span>

### <span data-ttu-id="f740b-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="f740b-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="f740b-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f740b-146">OUTPUTS</span></span>

### <span data-ttu-id="f740b-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f740b-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="f740b-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f740b-148">NOTES</span></span>

## <span data-ttu-id="f740b-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f740b-149">RELATED LINKS</span></span>

[<span data-ttu-id="f740b-150">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="f740b-150">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="f740b-151">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="f740b-151">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="f740b-152">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="f740b-152">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
