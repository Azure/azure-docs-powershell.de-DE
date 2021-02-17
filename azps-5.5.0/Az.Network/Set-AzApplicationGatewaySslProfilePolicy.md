---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 7d04d73905bde7ab008c6910cab708e209125316
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407997"
---
# <span data-ttu-id="c73b2-101">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="c73b2-101">Set-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="c73b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c73b2-102">SYNOPSIS</span></span>
<span data-ttu-id="c73b2-103">Ändert die "SSL"-Richtlinie eines Anwendungsgateways-SSL-Profils.</span><span class="sxs-lookup"><span data-stu-id="c73b2-103">Modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="c73b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c73b2-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DisabledSslProtocols <String[]>] [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c73b2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c73b2-105">DESCRIPTION</span></span>
<span data-ttu-id="c73b2-106">Das **Cmdlet "Set-AzApplicationGatewaySslProfilePolicy"** ändert die "SSL-Richtlinie" eines Anwendungsgateways-SSL-Profils.</span><span class="sxs-lookup"><span data-stu-id="c73b2-106">The **Set-AzApplicationGatewaySslProfilePolicy** cmdlet modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="c73b2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c73b2-107">EXAMPLES</span></span>

### <span data-ttu-id="c73b2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c73b2-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $profile = Set-AzApplicationGatewaySslProfilePolicy -SslProfile $profile -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="c73b2-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="c73b2-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="c73b2-110">Der zweite Befehl ruft das ssl-Profil "SslProfile01" für $AppGw und speichert die Einstellungen in der $profile Variable.</span><span class="sxs-lookup"><span data-stu-id="c73b2-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="c73b2-111">Der letzte Befehl ändert die ssl-Richtlinie des ssl-Profilobjekts, das in der $profile.</span><span class="sxs-lookup"><span data-stu-id="c73b2-111">The last command modifies the ssl policy of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="c73b2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c73b2-112">PARAMETERS</span></span>

### <span data-ttu-id="c73b2-113">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="c73b2-113">-CipherSuite</span></span>
<span data-ttu-id="c73b2-114">Ssl cipher suites to be enabled in the specified order to application gateway</span><span class="sxs-lookup"><span data-stu-id="c73b2-114">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c73b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c73b2-115">-DefaultProfile</span></span>
<span data-ttu-id="c73b2-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c73b2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c73b2-117">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="c73b2-117">-DisabledSslProtocols</span></span>
<span data-ttu-id="c73b2-118">Liste der zu deaktivierenden SSL-Protokolle</span><span class="sxs-lookup"><span data-stu-id="c73b2-118">List of SSL protocols to be disabled</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c73b2-119">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="c73b2-119">-MinProtocolVersion</span></span>
<span data-ttu-id="c73b2-120">Mindestversion des ssl-Protokolls, die auf dem Anwendungsgateway unterstützt werden soll</span><span class="sxs-lookup"><span data-stu-id="c73b2-120">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c73b2-121">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="c73b2-121">-PolicyName</span></span>
<span data-ttu-id="c73b2-122">Name der vordefinierten Richtlinie in Ssl</span><span class="sxs-lookup"><span data-stu-id="c73b2-122">Name of Ssl predefined policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c73b2-123">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="c73b2-123">-PolicyType</span></span>
<span data-ttu-id="c73b2-124">Typ der Ssl-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="c73b2-124">Type of Ssl Policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c73b2-125">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="c73b2-125">-SslProfile</span></span>
<span data-ttu-id="c73b2-126">Das Anwendungsgateway-SSL-Profil</span><span class="sxs-lookup"><span data-stu-id="c73b2-126">The application gateway SSL profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c73b2-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c73b2-127">-Confirm</span></span>
<span data-ttu-id="c73b2-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c73b2-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c73b2-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c73b2-129">-WhatIf</span></span>
<span data-ttu-id="c73b2-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c73b2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c73b2-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c73b2-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c73b2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c73b2-132">CommonParameters</span></span>
<span data-ttu-id="c73b2-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c73b2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c73b2-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c73b2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c73b2-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c73b2-135">INPUTS</span></span>

### <span data-ttu-id="c73b2-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c73b2-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="c73b2-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c73b2-137">OUTPUTS</span></span>

### <span data-ttu-id="c73b2-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c73b2-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="c73b2-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c73b2-139">NOTES</span></span>

## <span data-ttu-id="c73b2-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c73b2-140">RELATED LINKS</span></span>



[<span data-ttu-id="c73b2-141">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="c73b2-141">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="c73b2-142">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="c73b2-142">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)
