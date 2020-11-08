---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 7030fcef733b9bfb8e59f1bc79a373f89bddfc61
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178461"
---
# <span data-ttu-id="b377c-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b377c-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="b377c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b377c-102">SYNOPSIS</span></span>
<span data-ttu-id="b377c-103">Erstellt eine Konfiguration des Back-End-Adresspools für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="b377c-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="b377c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b377c-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b377c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b377c-105">DESCRIPTION</span></span>
<span data-ttu-id="b377c-106">Das Cmdlet **New-AzLoadBalancerBackendAddressPoolConfig** erstellt eine Konfiguration des Back-End-Adresspools für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="b377c-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="b377c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b377c-107">EXAMPLES</span></span>

### <span data-ttu-id="b377c-108">Beispiel 1: Erstellen einer Konfiguration des Back-End-Adresspools für ein Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="b377c-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="b377c-109">Dieser Befehl erstellt eine Konfiguration des Back-End-Adresspools mit dem Namen BackendAddressPool02 für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="b377c-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="b377c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b377c-110">PARAMETERS</span></span>

### <span data-ttu-id="b377c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b377c-111">-DefaultProfile</span></span>
<span data-ttu-id="b377c-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b377c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b377c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b377c-113">-Name</span></span>
<span data-ttu-id="b377c-114">Gibt den Namen der zu erstellende Adresspool Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="b377c-114">Specifies the name of the address pool configuration to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b377c-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b377c-115">-Confirm</span></span>
<span data-ttu-id="b377c-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b377c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b377c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b377c-117">-WhatIf</span></span>
<span data-ttu-id="b377c-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b377c-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b377c-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b377c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b377c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b377c-120">CommonParameters</span></span>
<span data-ttu-id="b377c-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b377c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b377c-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b377c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b377c-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b377c-123">INPUTS</span></span>

### <span data-ttu-id="b377c-124">Keine</span><span class="sxs-lookup"><span data-stu-id="b377c-124">None</span></span>

## <span data-ttu-id="b377c-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b377c-125">OUTPUTS</span></span>

### <span data-ttu-id="b377c-126">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b377c-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="b377c-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="b377c-127">NOTES</span></span>

## <span data-ttu-id="b377c-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b377c-128">RELATED LINKS</span></span>

[<span data-ttu-id="b377c-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b377c-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="b377c-130">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b377c-130">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="b377c-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b377c-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


