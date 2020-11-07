---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: 2f6c4f410c7d4f92c8dcd911e0c113f2a91b304c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665299"
---
# <span data-ttu-id="1e979-101">Get-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="1e979-101">Get-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="1e979-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e979-102">SYNOPSIS</span></span>
<span data-ttu-id="1e979-103">Ruft eine Tap-Konfigurationsressource ab.</span><span class="sxs-lookup"><span data-stu-id="1e979-103">Gets a Tap configuration resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e979-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e979-104">SYNTAX</span></span>

### <span data-ttu-id="1e979-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1e979-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e979-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e979-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e979-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e979-107">DESCRIPTION</span></span>
<span data-ttu-id="1e979-108">Das Cmdlet " **Get-AzureRmNetworkInterfaceTapConfig** " Ruft eine Azure Tap-Konfiguration für eine bestimmte Ressourcengruppe, eine Netzwerkschnittstelle und tippen auf den Konfigurationsnamen oder die Liste der TAP-Konfigurationen in einer Ressourcengruppe und Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="1e979-108">The **Get-AzureRmNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="1e979-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e979-109">EXAMPLES</span></span>

### <span data-ttu-id="1e979-110">Beispiel 1: Abrufen aller Tap-Konfigurationen für eine bestimmte Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="1e979-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="1e979-111">Mit diesem Befehl werden die für die angegebene Netzwerkschnittstelle hinzugefügten Tap-Konfigurationen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1e979-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="1e979-112">Beispiel 2: Abrufen einer bestimmten Tap-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="1e979-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="1e979-113">Mit diesem Befehl wird eine bestimmte Tap-Konfiguration für die angegebene Netzwerkschnittstelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1e979-113">This command gets specific tap configuration added for the given network interface.</span></span>

## <span data-ttu-id="1e979-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e979-114">PARAMETERS</span></span>

### <span data-ttu-id="1e979-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e979-115">-DefaultProfile</span></span>
<span data-ttu-id="1e979-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1e979-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e979-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1e979-117">-Name</span></span>
<span data-ttu-id="1e979-118">Der Name der bestimmten Tap-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1e979-118">Name of the specific tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e979-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="1e979-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="1e979-120">Der Name der Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1e979-120">The Network Interface name.</span></span>

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

### <span data-ttu-id="1e979-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e979-121">-ResourceGroupName</span></span>
<span data-ttu-id="1e979-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1e979-122">The resource group name.</span></span>

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

### <span data-ttu-id="1e979-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1e979-123">-ResourceId</span></span>
<span data-ttu-id="1e979-124">Ressourcenquelle der TapConfiguration-Ressource</span><span class="sxs-lookup"><span data-stu-id="1e979-124">ResourceId of the TapConfiguration resource</span></span>

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

### <span data-ttu-id="1e979-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1e979-125">-Confirm</span></span>
<span data-ttu-id="1e979-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e979-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e979-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e979-127">-WhatIf</span></span>
<span data-ttu-id="1e979-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e979-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e979-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e979-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e979-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e979-130">CommonParameters</span></span>
<span data-ttu-id="1e979-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e979-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e979-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e979-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e979-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e979-133">INPUTS</span></span>

### <span data-ttu-id="1e979-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1e979-134">System.String</span></span>

## <span data-ttu-id="1e979-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e979-135">OUTPUTS</span></span>

### <span data-ttu-id="1e979-136">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e979-136">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="1e979-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e979-137">NOTES</span></span>

## <span data-ttu-id="1e979-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e979-138">RELATED LINKS</span></span>
