---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: f53733976d946b61fc143e0a2b2e9be71017b7f6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003557"
---
# <span data-ttu-id="b226e-101">Get-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b226e-101">Get-AzFirewallPolicy</span></span>

## <span data-ttu-id="b226e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b226e-102">SYNOPSIS</span></span>
<span data-ttu-id="b226e-103">Ruft eine Azure-Firewall-Richtlinie ab</span><span class="sxs-lookup"><span data-stu-id="b226e-103">Gets a Azure Firewall Policy</span></span>

## <span data-ttu-id="b226e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b226e-104">SYNTAX</span></span>

### <span data-ttu-id="b226e-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b226e-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b226e-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b226e-106">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b226e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b226e-107">DESCRIPTION</span></span>
<span data-ttu-id="b226e-108">Das Cmdlet " **Get-AzFirewallPolicy** " ruft mindestens eine Firewall in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="b226e-108">The **Get-AzFirewallPolicy** cmdlet gets one or more Firewalls in a resource group</span></span>

## <span data-ttu-id="b226e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b226e-109">EXAMPLES</span></span>

### <span data-ttu-id="b226e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b226e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

<span data-ttu-id="b226e-111">In diesem Beispiel wird eine Firewall-Richtlinie mit dem Namen "firewallPolicy" in der Ressourcengruppe "TestRg" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b226e-111">This example get a firewall policy named "firewallPolicy" in the resource group "TestRg"</span></span>

## <span data-ttu-id="b226e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b226e-112">PARAMETERS</span></span>

### <span data-ttu-id="b226e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b226e-113">-DefaultProfile</span></span>
<span data-ttu-id="b226e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b226e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b226e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b226e-115">-Name</span></span>
<span data-ttu-id="b226e-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="b226e-116">The resource name.</span></span>

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

### <span data-ttu-id="b226e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b226e-117">-ResourceGroupName</span></span>
<span data-ttu-id="b226e-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b226e-118">The resource group name.</span></span>

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

### <span data-ttu-id="b226e-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b226e-119">-ResourceId</span></span>
<span data-ttu-id="b226e-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b226e-120">The resource Id.</span></span>

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

### <span data-ttu-id="b226e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b226e-121">CommonParameters</span></span>
<span data-ttu-id="b226e-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b226e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b226e-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b226e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b226e-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b226e-124">INPUTS</span></span>

### <span data-ttu-id="b226e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b226e-125">System.String</span></span>

## <span data-ttu-id="b226e-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b226e-126">OUTPUTS</span></span>

### <span data-ttu-id="b226e-127">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="b226e-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="b226e-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. Models. PSAzureFirewall, Microsoft. Azure. PowerShell. Cmdlets. Network, Version = 1.12.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b226e-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b226e-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="b226e-129">NOTES</span></span>

## <span data-ttu-id="b226e-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b226e-130">RELATED LINKS</span></span>
