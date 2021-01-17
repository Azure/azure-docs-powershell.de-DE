---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: f53733976d946b61fc143e0a2b2e9be71017b7f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472246"
---
# <span data-ttu-id="6b396-101">Get-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="6b396-101">Get-AzFirewallPolicy</span></span>

## <span data-ttu-id="6b396-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b396-102">SYNOPSIS</span></span>
<span data-ttu-id="6b396-103">Bekommt eine Azure-Firewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="6b396-103">Gets a Azure Firewall Policy</span></span>

## <span data-ttu-id="6b396-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b396-104">SYNTAX</span></span>

### <span data-ttu-id="6b396-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b396-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b396-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b396-106">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b396-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b396-107">DESCRIPTION</span></span>
<span data-ttu-id="6b396-108">Das **Cmdlet "Get-AzFirewallPolicy"** ruft eine oder mehrere Firewalls in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="6b396-108">The **Get-AzFirewallPolicy** cmdlet gets one or more Firewalls in a resource group</span></span>

## <span data-ttu-id="6b396-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6b396-109">EXAMPLES</span></span>

### <span data-ttu-id="6b396-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6b396-110">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

<span data-ttu-id="6b396-111">In diesem Beispiel wird eine Firewallrichtlinie namens "firewallPolicy" in der Ressourcengruppe "TestRg"</span><span class="sxs-lookup"><span data-stu-id="6b396-111">This example get a firewall policy named "firewallPolicy" in the resource group "TestRg"</span></span>

## <span data-ttu-id="6b396-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b396-112">PARAMETERS</span></span>

### <span data-ttu-id="6b396-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b396-113">-DefaultProfile</span></span>
<span data-ttu-id="6b396-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b396-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b396-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6b396-115">-Name</span></span>
<span data-ttu-id="6b396-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="6b396-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b396-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b396-117">-ResourceGroupName</span></span>
<span data-ttu-id="6b396-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6b396-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b396-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b396-119">-ResourceId</span></span>
<span data-ttu-id="6b396-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="6b396-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b396-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b396-121">CommonParameters</span></span>
<span data-ttu-id="6b396-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b396-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b396-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b396-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b396-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6b396-124">INPUTS</span></span>

### <span data-ttu-id="6b396-125">System.String</span><span class="sxs-lookup"><span data-stu-id="6b396-125">System.String</span></span>

## <span data-ttu-id="6b396-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6b396-126">OUTPUTS</span></span>

### <span data-ttu-id="6b396-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="6b396-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="6b396-128">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="6b396-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6b396-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6b396-129">NOTES</span></span>

## <span data-ttu-id="6b396-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6b396-130">RELATED LINKS</span></span>
