---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: ff9ed8220cf2b30f2e652e207cb4d63db969a8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482361"
---
# <span data-ttu-id="878ee-101">Get-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="878ee-101">Get-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="878ee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="878ee-102">SYNOPSIS</span></span>
<span data-ttu-id="878ee-103">Ruft einen virtuellen Netzwerk Hahn ab</span><span class="sxs-lookup"><span data-stu-id="878ee-103">Gets a virtual network tap</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="878ee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="878ee-104">SYNTAX</span></span>

### <span data-ttu-id="878ee-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="878ee-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmVirtualNetworkTap -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="878ee-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="878ee-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="878ee-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="878ee-107">DESCRIPTION</span></span>
<span data-ttu-id="878ee-108">Das Cmdlet " **Get-AzureRmVirtualNetworkTap** " Ruft einen virtuellen Azure-Netzwerk Hahn oder eine Liste mit Azure-virtuellen Netzwerk-TAPS in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="878ee-108">The **Get-AzureRmVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="878ee-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="878ee-109">EXAMPLES</span></span>

### <span data-ttu-id="878ee-110">Beispiel 1: Abrufen eines virtuellen Netzwerk Hahns</span><span class="sxs-lookup"><span data-stu-id="878ee-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\>Get-AzureRmVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="878ee-111">Dieser Befehl ruft einen VirtualNetwork-Tap-Verweis für den angegebenen "VirtualTap1" in "ResourceGroup1" ab.</span><span class="sxs-lookup"><span data-stu-id="878ee-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

## <span data-ttu-id="878ee-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="878ee-112">PARAMETERS</span></span>

### <span data-ttu-id="878ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="878ee-113">-DefaultProfile</span></span>
<span data-ttu-id="878ee-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="878ee-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="878ee-115">-Name</span><span class="sxs-lookup"><span data-stu-id="878ee-115">-Name</span></span>
<span data-ttu-id="878ee-116">Der Name des Tap.</span><span class="sxs-lookup"><span data-stu-id="878ee-116">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="878ee-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="878ee-117">-ResourceGroupName</span></span>
<span data-ttu-id="878ee-118">Der Ressourcengruppenname des virtuellen Netzwerks Tippen Sie auf.</span><span class="sxs-lookup"><span data-stu-id="878ee-118">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="878ee-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="878ee-119">-ResourceId</span></span>
<span data-ttu-id="878ee-120">Ressourcenquelle der VirtualNetworkTap-Ressource</span><span class="sxs-lookup"><span data-stu-id="878ee-120">ResourceId of the VirtualNetworkTap resource</span></span>

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

### <span data-ttu-id="878ee-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="878ee-121">-Confirm</span></span>
<span data-ttu-id="878ee-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="878ee-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="878ee-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="878ee-123">-WhatIf</span></span>
<span data-ttu-id="878ee-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="878ee-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="878ee-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="878ee-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="878ee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="878ee-126">CommonParameters</span></span>
<span data-ttu-id="878ee-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="878ee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="878ee-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="878ee-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="878ee-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="878ee-129">INPUTS</span></span>

### <span data-ttu-id="878ee-130">System. String</span><span class="sxs-lookup"><span data-stu-id="878ee-130">System.String</span></span>

## <span data-ttu-id="878ee-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="878ee-131">OUTPUTS</span></span>

### <span data-ttu-id="878ee-132">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="878ee-132">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="878ee-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="878ee-133">NOTES</span></span>

## <span data-ttu-id="878ee-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="878ee-134">RELATED LINKS</span></span>
