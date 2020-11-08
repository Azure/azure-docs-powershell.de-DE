---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 52fc2a3c84c70d52c173bc256ca2b0d952307e91
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177461"
---
# <span data-ttu-id="02a75-101">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="02a75-101">Remove-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="02a75-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="02a75-102">SYNOPSIS</span></span>
<span data-ttu-id="02a75-103">Entfernt eine Tap-Konfiguration aus der angegebenen Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="02a75-103">Removes a tap configuration from given network interface</span></span>

## <span data-ttu-id="02a75-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="02a75-104">SYNTAX</span></span>

### <span data-ttu-id="02a75-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="02a75-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02a75-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02a75-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02a75-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02a75-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02a75-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02a75-108">DESCRIPTION</span></span>
<span data-ttu-id="02a75-109">Das Cmdlet **Remove-AzNetworkInterfaceTapConfig** entfernt eine Azure Tap-Konfiguration aus einer Netzwerkschnittstellen Liste.</span><span class="sxs-lookup"><span data-stu-id="02a75-109">The **Remove-AzNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="02a75-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02a75-110">EXAMPLES</span></span>

### <span data-ttu-id="02a75-111">Beispiel 1: Entfernen einer Tap-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="02a75-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="02a75-112">Dieser Befehl entfernt die TapConfiguration aus NetworkInterface1 in einer Ressourcengruppe ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="02a75-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="02a75-113">Da der Parameter *Force* nicht verwendet wird, wird der Benutzer aufgefordert, diese Aktion zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="02a75-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="02a75-114">Beispiel 2: Entfernen einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="02a75-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="02a75-115">Dieser Befehl entfernt die TapConfiguration aus NetworkInterface1 in einer Ressourcengruppe ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="02a75-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="02a75-116">Da der Parameter *Force* verwendet wird, wird der Benutzer nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="02a75-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="02a75-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="02a75-117">PARAMETERS</span></span>

### <span data-ttu-id="02a75-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a75-118">-DefaultProfile</span></span>
<span data-ttu-id="02a75-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="02a75-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02a75-120">-Force</span><span class="sxs-lookup"><span data-stu-id="02a75-120">-Force</span></span>
<span data-ttu-id="02a75-121">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="02a75-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="02a75-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="02a75-122">-InputObject</span></span>
<span data-ttu-id="02a75-123">Verweis auf NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="02a75-123">Reference to NetworkInterfaceTapConfig.</span></span>

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

### <span data-ttu-id="02a75-124">-Name</span><span class="sxs-lookup"><span data-stu-id="02a75-124">-Name</span></span>
<span data-ttu-id="02a75-125">Der Name des virtuellen Netzwerk Peerings.</span><span class="sxs-lookup"><span data-stu-id="02a75-125">The virtual network peering name.</span></span>

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

### <span data-ttu-id="02a75-126">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="02a75-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="02a75-127">Der Name des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="02a75-127">The virtual network name.</span></span>

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

### <span data-ttu-id="02a75-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02a75-128">-PassThru</span></span>
<span data-ttu-id="02a75-129">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="02a75-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="02a75-130">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="02a75-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="02a75-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02a75-131">-ResourceGroupName</span></span>
<span data-ttu-id="02a75-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="02a75-132">The resource group name.</span></span>

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

### <span data-ttu-id="02a75-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="02a75-133">-ResourceId</span></span>
<span data-ttu-id="02a75-134">NetworkInterfaceTapConfig-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="02a75-134">NetworkInterfaceTapConfig resource id.</span></span>

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

### <span data-ttu-id="02a75-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="02a75-135">-Confirm</span></span>
<span data-ttu-id="02a75-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="02a75-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02a75-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02a75-137">-WhatIf</span></span>
<span data-ttu-id="02a75-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="02a75-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02a75-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="02a75-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02a75-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a75-140">CommonParameters</span></span>
<span data-ttu-id="02a75-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02a75-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a75-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02a75-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a75-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="02a75-143">INPUTS</span></span>

### <span data-ttu-id="02a75-144">System. String</span><span class="sxs-lookup"><span data-stu-id="02a75-144">System.String</span></span>

### <span data-ttu-id="02a75-145">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="02a75-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="02a75-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="02a75-146">OUTPUTS</span></span>

### <span data-ttu-id="02a75-147">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="02a75-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="02a75-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="02a75-148">NOTES</span></span>

## <span data-ttu-id="02a75-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="02a75-149">RELATED LINKS</span></span>

[<span data-ttu-id="02a75-150">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="02a75-150">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="02a75-151">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="02a75-151">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="02a75-152">Satz-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="02a75-152">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
