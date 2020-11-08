---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: df298b41ea1efa4915cb7556b9fd07b1d8f3e2de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173194"
---
# <span data-ttu-id="36314-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="36314-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="36314-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="36314-102">SYNOPSIS</span></span>
<span data-ttu-id="36314-103">Erstellt einen privaten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="36314-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="36314-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="36314-104">SYNTAX</span></span>

### <span data-ttu-id="36314-105">Alle</span><span class="sxs-lookup"><span data-stu-id="36314-105">All</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36314-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36314-106">DESCRIPTION</span></span>

<span data-ttu-id="36314-107">Das Cmdlet **New-AzPrivateEndpoint** erstellt einen privaten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="36314-107">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="36314-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36314-108">EXAMPLES</span></span>

### <span data-ttu-id="36314-109">Beispiel 1: Erstellen eines privaten Endpunkts</span><span class="sxs-lookup"><span data-stu-id="36314-109">Example 1: Create a private endpoint</span></span>

<span data-ttu-id="36314-110">Im folgenden Beispiel wird ein privater Endpunkt mit einer bestimmten privaten Verbindungsdienst-ID im angegebenen Subnetz in einem virtuellen Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="36314-110">The following example creates a private endpoint with a specific private link service ID in the specified subnet in a virtual network.</span></span>

```powershell
$virtualNetwork = Get-AzVirtualNetwork -ResourceName 'myVirtualNetwork' -ResourceGroupName 'myResourceGroup'
$subnet = $virtualNetwork | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mySubnet'
$plsConnection= New-AzPrivateLinkServiceConnection -Name 'MyPLSConnections' -PrivateLinkServiceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService' -RequestMessage 'Please Approve my request'
New-AzPrivateEndpoint -Name 'MyPrivateEndpoint' -ResourceGroup 'myResourceGroup' -Location 'centralus' -PrivateLinkServiceConnection $plsConnection -Subnet $subnet
```

## <span data-ttu-id="36314-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="36314-111">PARAMETERS</span></span>

### <span data-ttu-id="36314-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36314-112">-AsJob</span></span>

<span data-ttu-id="36314-113">Führen Sie das Cmdlet als Job im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="36314-113">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="36314-114">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="36314-114">-ByManualRequest</span></span>

<span data-ttu-id="36314-115">Verwenden Sie die manuelle Anforderung, um die Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="36314-115">Use manual request to establish the connection.</span></span>

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

### <span data-ttu-id="36314-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36314-116">-DefaultProfile</span></span>

<span data-ttu-id="36314-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="36314-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36314-118">-Force</span><span class="sxs-lookup"><span data-stu-id="36314-118">-Force</span></span>

<span data-ttu-id="36314-119">Bitten Sie nicht um Bestätigung, um eine Ressource zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="36314-119">Do not ask for confirmation to overwrite a resource.</span></span>

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

### <span data-ttu-id="36314-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="36314-120">-Location</span></span>

<span data-ttu-id="36314-121">Gibt einen Speicherort für den privaten Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="36314-121">Specifies a location for the private endpoint.</span></span> <span data-ttu-id="36314-122">Verwenden [Sie Get-AzLocation](/powershell/module/az.resources/get-azlocation) , um gültige Werte für diesen Parameter zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="36314-122">Use [Get-AzLocation](/powershell/module/az.resources/get-azlocation) to determine valid values for this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36314-123">-Name</span><span class="sxs-lookup"><span data-stu-id="36314-123">-Name</span></span>

<span data-ttu-id="36314-124">Der Name des privaten Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="36314-124">Name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36314-125">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="36314-125">-PrivateLinkServiceConnection</span></span>

<span data-ttu-id="36314-126">Die Ressourcen-ID, um den privaten Endpunkt zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="36314-126">The resource ID to connect the private endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36314-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36314-127">-ResourceGroupName</span></span>

<span data-ttu-id="36314-128">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="36314-128">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36314-129">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="36314-129">-Subnet</span></span>

<span data-ttu-id="36314-130">Das Subnetz des privaten Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="36314-130">The subnet of the private endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36314-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="36314-131">-Tag</span></span>

<span data-ttu-id="36314-132">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="36314-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="36314-133">Beispiel: @ {Key0 = ' value0 '; key1 = $NULL; key2 = ' Value2 '}</span><span class="sxs-lookup"><span data-stu-id="36314-133">For example: @{key0='value0';key1=$null;key2='value2'}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36314-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="36314-134">-Confirm</span></span>

<span data-ttu-id="36314-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="36314-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36314-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36314-136">-WhatIf</span></span>

<span data-ttu-id="36314-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="36314-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36314-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="36314-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36314-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36314-139">CommonParameters</span></span>

<span data-ttu-id="36314-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36314-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36314-141">Weitere Informationen finden Sie unter [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="36314-141">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="36314-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="36314-142">INPUTS</span></span>

### <span data-ttu-id="36314-143">System. String</span><span class="sxs-lookup"><span data-stu-id="36314-143">System.String</span></span>

### <span data-ttu-id="36314-144">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="36314-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="36314-145">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceConnection []</span><span class="sxs-lookup"><span data-stu-id="36314-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="36314-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="36314-146">OUTPUTS</span></span>

### <span data-ttu-id="36314-147">Microsoft. Azure. Commands. Network. Models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="36314-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="36314-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="36314-148">NOTES</span></span>

## <span data-ttu-id="36314-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="36314-149">RELATED LINKS</span></span>

[<span data-ttu-id="36314-150">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="36314-150">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="36314-151">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="36314-151">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="36314-152">Neu – AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="36314-152">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)