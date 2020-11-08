---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: f53733976d946b61fc143e0a2b2e9be71017b7f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174348"
---
# <span data-ttu-id="89885-101">Get-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="89885-101">Get-AzFirewallPolicy</span></span>

## <span data-ttu-id="89885-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="89885-102">SYNOPSIS</span></span>
<span data-ttu-id="89885-103">Ruft eine Azure-Firewall-Richtlinie ab</span><span class="sxs-lookup"><span data-stu-id="89885-103">Gets a Azure Firewall Policy</span></span>

## <span data-ttu-id="89885-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="89885-104">SYNTAX</span></span>

### <span data-ttu-id="89885-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="89885-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="89885-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89885-106">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89885-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89885-107">DESCRIPTION</span></span>
<span data-ttu-id="89885-108">Das Cmdlet " **Get-AzFirewallPolicy** " ruft mindestens eine Firewall in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="89885-108">The **Get-AzFirewallPolicy** cmdlet gets one or more Firewalls in a resource group</span></span>

## <span data-ttu-id="89885-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89885-109">EXAMPLES</span></span>

### <span data-ttu-id="89885-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="89885-110">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

<span data-ttu-id="89885-111">In diesem Beispiel wird eine Firewall-Richtlinie mit dem Namen "firewallPolicy" in der Ressourcengruppe "TestRg" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="89885-111">This example get a firewall policy named "firewallPolicy" in the resource group "TestRg"</span></span>

## <span data-ttu-id="89885-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="89885-112">PARAMETERS</span></span>

### <span data-ttu-id="89885-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89885-113">-DefaultProfile</span></span>
<span data-ttu-id="89885-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="89885-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89885-115">-Name</span><span class="sxs-lookup"><span data-stu-id="89885-115">-Name</span></span>
<span data-ttu-id="89885-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="89885-116">The resource name.</span></span>

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

### <span data-ttu-id="89885-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89885-117">-ResourceGroupName</span></span>
<span data-ttu-id="89885-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="89885-118">The resource group name.</span></span>

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

### <span data-ttu-id="89885-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="89885-119">-ResourceId</span></span>
<span data-ttu-id="89885-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="89885-120">The resource Id.</span></span>

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

### <span data-ttu-id="89885-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89885-121">CommonParameters</span></span>
<span data-ttu-id="89885-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89885-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89885-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89885-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89885-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="89885-124">INPUTS</span></span>

### <span data-ttu-id="89885-125">System. String</span><span class="sxs-lookup"><span data-stu-id="89885-125">System.String</span></span>

## <span data-ttu-id="89885-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="89885-126">OUTPUTS</span></span>

### <span data-ttu-id="89885-127">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="89885-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="89885-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. Models. PSAzureFirewall, Microsoft. Azure. PowerShell. Cmdlets. Network, Version = 1.12.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="89885-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="89885-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="89885-129">NOTES</span></span>

## <span data-ttu-id="89885-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="89885-130">RELATED LINKS</span></span>
