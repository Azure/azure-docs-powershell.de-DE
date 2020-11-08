---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultnetworkrulesetobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
ms.openlocfilehash: 318d5915e07ac55430dbe8e1788d862673dc5998
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166431"
---
# <span data-ttu-id="8cbd6-101">New-AzKeyVaultNetworkRuleSetObject</span><span class="sxs-lookup"><span data-stu-id="8cbd6-101">New-AzKeyVaultNetworkRuleSetObject</span></span>

## <span data-ttu-id="8cbd6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8cbd6-102">SYNOPSIS</span></span>
<span data-ttu-id="8cbd6-103">Erstellen Sie ein Objekt, das die Netzwerkregel Einstellungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="8cbd6-103">Create an object representing the network rule settings.</span></span>

## <span data-ttu-id="8cbd6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cbd6-104">SYNTAX</span></span>

```
New-AzKeyVaultNetworkRuleSetObject [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>]
 [-Bypass <PSKeyVaultNetworkRuleBypassEnum>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cbd6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cbd6-105">DESCRIPTION</span></span>
<span data-ttu-id="8cbd6-106">Erstellen Sie ein Objekt, das die Netzwerkregel Einstellungen darstellt, die beim Erstellen eines Tresors verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="8cbd6-106">Create an object representing the network rule settings that can be used when creating a vault.</span></span>

## <span data-ttu-id="8cbd6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8cbd6-107">EXAMPLES</span></span>

### <span data-ttu-id="8cbd6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8cbd6-108">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="8cbd6-109">Erstellen eines neuen Tresors und Angeben von Netzwerkregeln zum Zulassen des Zugriffs auf die angegebene IP-Adresse aus dem virtuellen Netzwerk, das von $myNetworkResId identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="8cbd6-109">Creating a new vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="8cbd6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cbd6-110">PARAMETERS</span></span>

### <span data-ttu-id="8cbd6-111">-Bypass</span><span class="sxs-lookup"><span data-stu-id="8cbd6-111">-Bypass</span></span>
<span data-ttu-id="8cbd6-112">Gibt die Umgehung der Netzwerkregel an.</span><span class="sxs-lookup"><span data-stu-id="8cbd6-112">Specifies bypass of network rule.</span></span>

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

### <span data-ttu-id="8cbd6-113">– Standardmäßig</span><span class="sxs-lookup"><span data-stu-id="8cbd6-113">-DefaultAction</span></span>
<span data-ttu-id="8cbd6-114">Gibt die Standardaktion der Netzwerkregel an.</span><span class="sxs-lookup"><span data-stu-id="8cbd6-114">Specifies default action of network rule.</span></span>

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

### <span data-ttu-id="8cbd6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cbd6-115">-DefaultProfile</span></span>
<span data-ttu-id="8cbd6-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8cbd6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cbd6-117">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="8cbd6-117">-IpAddressRange</span></span>
<span data-ttu-id="8cbd6-118">Gibt den zulässigen Netzwerk-IP-Adressbereich der Netzwerkregel an.</span><span class="sxs-lookup"><span data-stu-id="8cbd6-118">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="8cbd6-119">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="8cbd6-119">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="8cbd6-120">Gibt den zulässigen virtuellen Netzwerk-Ressourcenbezeichner der Netzwerkregel an.</span><span class="sxs-lookup"><span data-stu-id="8cbd6-120">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="8cbd6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cbd6-121">CommonParameters</span></span>
<span data-ttu-id="8cbd6-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cbd6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cbd6-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8cbd6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cbd6-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8cbd6-124">INPUTS</span></span>

### <span data-ttu-id="8cbd6-125">Keine</span><span class="sxs-lookup"><span data-stu-id="8cbd6-125">None</span></span>

## <span data-ttu-id="8cbd6-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8cbd6-126">OUTPUTS</span></span>

### <span data-ttu-id="8cbd6-127">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8cbd6-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="8cbd6-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="8cbd6-128">NOTES</span></span>

## <span data-ttu-id="8cbd6-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8cbd6-129">RELATED LINKS</span></span>
