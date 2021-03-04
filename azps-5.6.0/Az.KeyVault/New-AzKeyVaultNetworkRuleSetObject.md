---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultnetworkrulesetobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
ms.openlocfilehash: 5f63ee4d1c55211b13eb525a76547064e61cba48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944068"
---
# <span data-ttu-id="50f22-101">New-AzKeyVaultNetworkRuleSetObject</span><span class="sxs-lookup"><span data-stu-id="50f22-101">New-AzKeyVaultNetworkRuleSetObject</span></span>

## <span data-ttu-id="50f22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50f22-102">SYNOPSIS</span></span>
<span data-ttu-id="50f22-103">Erstellen Sie ein Objekt, das die Netzwerkregeleinstellungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="50f22-103">Create an object representing the network rule settings.</span></span>

## <span data-ttu-id="50f22-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50f22-104">SYNTAX</span></span>

```
New-AzKeyVaultNetworkRuleSetObject [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>]
 [-Bypass <PSKeyVaultNetworkRuleBypassEnum>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50f22-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50f22-105">DESCRIPTION</span></span>
<span data-ttu-id="50f22-106">Erstellen Sie ein Objekt, das die Netzwerkregeleinstellungen darstellt, die beim Erstellen eines Tresors verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="50f22-106">Create an object representing the network rule settings that can be used when creating a vault.</span></span>

## <span data-ttu-id="50f22-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="50f22-107">EXAMPLES</span></span>

### <span data-ttu-id="50f22-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="50f22-108">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="50f22-109">Erstellen eines neuen Tresors und Angeben von Netzwerkregeln, um den Zugriff auf die angegebene IP-Adresse aus dem virtuellen Netzwerk zu ermöglichen, das von $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="50f22-109">Creating a new vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="50f22-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="50f22-110">PARAMETERS</span></span>

### <span data-ttu-id="50f22-111">-Bypass</span><span class="sxs-lookup"><span data-stu-id="50f22-111">-Bypass</span></span>
<span data-ttu-id="50f22-112">Gibt die Umgehung der Netzwerkregel an.</span><span class="sxs-lookup"><span data-stu-id="50f22-112">Specifies bypass of network rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f22-113">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="50f22-113">-DefaultAction</span></span>
<span data-ttu-id="50f22-114">Gibt die Standardaktion der Netzwerkregel an.</span><span class="sxs-lookup"><span data-stu-id="50f22-114">Specifies default action of network rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50f22-115">-DefaultProfile</span></span>
<span data-ttu-id="50f22-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="50f22-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50f22-117">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="50f22-117">-IpAddressRange</span></span>
<span data-ttu-id="50f22-118">Gibt zulässigen Netzwerk-IP-Adressbereich der Netzwerkregel an.</span><span class="sxs-lookup"><span data-stu-id="50f22-118">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f22-119">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="50f22-119">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="50f22-120">Gibt den zulässigen virtuellen Netzwerkressourcenbezeichner der Netzwerkregel an.</span><span class="sxs-lookup"><span data-stu-id="50f22-120">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f22-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50f22-121">CommonParameters</span></span>
<span data-ttu-id="50f22-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50f22-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50f22-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50f22-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50f22-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="50f22-124">INPUTS</span></span>

### <span data-ttu-id="50f22-125">Keine</span><span class="sxs-lookup"><span data-stu-id="50f22-125">None</span></span>

## <span data-ttu-id="50f22-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="50f22-126">OUTPUTS</span></span>

### <span data-ttu-id="50f22-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="50f22-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="50f22-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="50f22-128">NOTES</span></span>

## <span data-ttu-id="50f22-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="50f22-129">RELATED LINKS</span></span>
