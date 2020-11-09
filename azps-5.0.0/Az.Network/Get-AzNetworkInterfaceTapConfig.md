---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: fa4c6db39de9f0d27fa80c4ee09e4decb319e2aa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302134"
---
# <span data-ttu-id="e59fb-101">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e59fb-101">Get-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="e59fb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e59fb-102">SYNOPSIS</span></span>
<span data-ttu-id="e59fb-103">Ruft eine Tap-Konfigurationsressource ab.</span><span class="sxs-lookup"><span data-stu-id="e59fb-103">Gets a Tap configuration resource.</span></span>

## <span data-ttu-id="e59fb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e59fb-104">SYNTAX</span></span>

### <span data-ttu-id="e59fb-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e59fb-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e59fb-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e59fb-106">GetByResourceIdParameterSet</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e59fb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e59fb-107">DESCRIPTION</span></span>
<span data-ttu-id="e59fb-108">Das Cmdlet " **Get-AzNetworkInterfaceTapConfig** " Ruft eine Azure Tap-Konfiguration für eine bestimmte Ressourcengruppe, eine Netzwerkschnittstelle und tippen auf den Konfigurationsnamen oder die Liste der TAP-Konfigurationen in einer Ressourcengruppe und Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="e59fb-108">The **Get-AzNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="e59fb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e59fb-109">EXAMPLES</span></span>

### <span data-ttu-id="e59fb-110">Beispiel 1: Abrufen aller Tap-Konfigurationen für eine bestimmte Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="e59fb-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="e59fb-111">Mit diesem Befehl werden die für die angegebene Netzwerkschnittstelle hinzugefügten Tap-Konfigurationen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e59fb-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="e59fb-112">Beispiel 2: Abrufen einer bestimmten Tap-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="e59fb-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="e59fb-113">Mit diesem Befehl wird eine bestimmte Tap-Konfiguration für die angegebene Netzwerkschnittstelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e59fb-113">This command gets specific tap configuration added for the given network interface.</span></span>

### <span data-ttu-id="e59fb-114">Beispiel 3: Abrufen einer bestimmten Tap-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="e59fb-114">Example 3: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

<span data-ttu-id="e59fb-115">Dieser Befehl ruft die für die angegebene Netzwerkschnittstelle hinzugefügten Tap-Konfigurationen mit dem Namen ab "tapconfig" auf.</span><span class="sxs-lookup"><span data-stu-id="e59fb-115">This command gets tap configurations added for the given network interface with name starting with "tapconfig".</span></span>

## <span data-ttu-id="e59fb-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="e59fb-116">PARAMETERS</span></span>

### <span data-ttu-id="e59fb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e59fb-117">-DefaultProfile</span></span>
<span data-ttu-id="e59fb-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e59fb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e59fb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e59fb-119">-Name</span></span>
<span data-ttu-id="e59fb-120">Der Name der bestimmten Tap-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e59fb-120">Name of the specific tap configuration.</span></span>

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

### <span data-ttu-id="e59fb-121">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="e59fb-121">-NetworkInterfaceName</span></span>
<span data-ttu-id="e59fb-122">Der Name der Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e59fb-122">The Network Interface name.</span></span>

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

### <span data-ttu-id="e59fb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e59fb-123">-ResourceGroupName</span></span>
<span data-ttu-id="e59fb-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e59fb-124">The resource group name.</span></span>

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

### <span data-ttu-id="e59fb-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e59fb-125">-ResourceId</span></span>
<span data-ttu-id="e59fb-126">Ressourcenquelle der TapConfiguration-Ressource</span><span class="sxs-lookup"><span data-stu-id="e59fb-126">ResourceId of the TapConfiguration resource</span></span>

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

### <span data-ttu-id="e59fb-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e59fb-127">-Confirm</span></span>
<span data-ttu-id="e59fb-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e59fb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e59fb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e59fb-129">-WhatIf</span></span>
<span data-ttu-id="e59fb-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e59fb-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e59fb-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e59fb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e59fb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e59fb-132">CommonParameters</span></span>
<span data-ttu-id="e59fb-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e59fb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e59fb-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e59fb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e59fb-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e59fb-135">INPUTS</span></span>

### <span data-ttu-id="e59fb-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e59fb-136">System.String</span></span>

## <span data-ttu-id="e59fb-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e59fb-137">OUTPUTS</span></span>

### <span data-ttu-id="e59fb-138">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="e59fb-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="e59fb-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="e59fb-139">NOTES</span></span>

## <span data-ttu-id="e59fb-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e59fb-140">RELATED LINKS</span></span>

[<span data-ttu-id="e59fb-141">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e59fb-141">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="e59fb-142">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e59fb-142">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="e59fb-143">Satz-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e59fb-143">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
