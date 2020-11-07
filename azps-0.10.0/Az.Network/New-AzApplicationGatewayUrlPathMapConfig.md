---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 590793e8a2caeb360b88a7d41d91dcea07baacfd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841372"
---
# <span data-ttu-id="043ed-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="043ed-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="043ed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="043ed-102">SYNOPSIS</span></span>
<span data-ttu-id="043ed-103">Erstellt ein Array von URL-Pfad Zuordnungen zu einem Back-End-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="043ed-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="043ed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="043ed-104">SYNTAX</span></span>

### <span data-ttu-id="043ed-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="043ed-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="043ed-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="043ed-106">SetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="043ed-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="043ed-107">DESCRIPTION</span></span>
<span data-ttu-id="043ed-108">Das Cmdlet **New-AzApplicationGatewayUrlPathMapConfig** erstellt ein Array von URL-Pfad Zuordnungen zu einem Back-End-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="043ed-108">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="043ed-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="043ed-109">EXAMPLES</span></span>

### <span data-ttu-id="043ed-110">Beispiel 1: Erstellen eines Arrays von URL-Pfad Zuordnungen zu einem Back-End-Serverpool</span><span class="sxs-lookup"><span data-stu-id="043ed-110">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="043ed-111">Dieser Befehl erstellt ein Array von URL-Pfad Zuordnungen zu einem Back-End-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="043ed-111">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="043ed-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="043ed-112">PARAMETERS</span></span>

### <span data-ttu-id="043ed-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="043ed-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="043ed-114">Gibt den Standard-Back-End-Adresspool an, der weitergeleitet werden soll, falls keine der im *pathRules* -Parameter angegebenen Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="043ed-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043ed-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="043ed-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="043ed-116">Gibt die Standard-ID des Back-End-Adresspools an.</span><span class="sxs-lookup"><span data-stu-id="043ed-116">Specifies the default backend address pool ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043ed-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="043ed-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="043ed-118">Gibt die standardmäßigen HTTP-Back-End-Einstellungen an, die verwendet werden sollen, falls keine der im *pathRules* -Parameter angegebenen Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="043ed-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043ed-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="043ed-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="043ed-120">Gibt die Standard-Back-End-HTTP-Einstellungen-ID an.</span><span class="sxs-lookup"><span data-stu-id="043ed-120">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043ed-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="043ed-121">-DefaultProfile</span></span>
<span data-ttu-id="043ed-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="043ed-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043ed-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="043ed-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="043ed-124">Standard RedirectConfiguration für Application Gateway</span><span class="sxs-lookup"><span data-stu-id="043ed-124">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043ed-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="043ed-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="043ed-126">ID des Application Gateway Standard RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="043ed-126">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043ed-127">-Name</span><span class="sxs-lookup"><span data-stu-id="043ed-127">-Name</span></span>
<span data-ttu-id="043ed-128">Gibt den vom Cmdlet erstellten URL-Pfad Zuordnungsnamen an.</span><span class="sxs-lookup"><span data-stu-id="043ed-128">Specifies the URL path map name that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043ed-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="043ed-129">-PathRules</span></span>
<span data-ttu-id="043ed-130">Gibt eine Liste von Pfadregeln an.</span><span class="sxs-lookup"><span data-stu-id="043ed-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="043ed-131">Beachten Sie, dass die Pfadregeln in der Reihenfolge vertraulich sind, dass Sie in der angegebenen Reihenfolge angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="043ed-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043ed-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="043ed-132">CommonParameters</span></span>
<span data-ttu-id="043ed-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="043ed-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="043ed-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="043ed-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="043ed-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="043ed-135">INPUTS</span></span>

## <span data-ttu-id="043ed-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="043ed-136">OUTPUTS</span></span>

### <span data-ttu-id="043ed-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="043ed-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="043ed-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="043ed-138">NOTES</span></span>

## <span data-ttu-id="043ed-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="043ed-139">RELATED LINKS</span></span>

[<span data-ttu-id="043ed-140">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="043ed-140">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="043ed-141">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="043ed-141">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="043ed-142">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="043ed-142">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="043ed-143">Satz-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="043ed-143">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


