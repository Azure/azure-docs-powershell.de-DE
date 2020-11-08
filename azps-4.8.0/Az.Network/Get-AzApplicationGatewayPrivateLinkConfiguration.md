---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2c9f006c9e719380abd1f1f5dbb6c6233346a563
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167208"
---
# <span data-ttu-id="6219c-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6219c-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="6219c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6219c-102">SYNOPSIS</span></span>
<span data-ttu-id="6219c-103">Ruft die Konfiguration privater Links für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="6219c-103">Gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="6219c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6219c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6219c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6219c-105">DESCRIPTION</span></span>
<span data-ttu-id="6219c-106">Das Cmdlet " **Get-AzApplicationGatewayPrivateLinkConfiguration** " Ruft die private Link Konfiguration eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="6219c-106">The **Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="6219c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6219c-107">EXAMPLES</span></span>

### <span data-ttu-id="6219c-108">Beispiel 1: Abrufen einer angegebenen Konfiguration privater Links</span><span class="sxs-lookup"><span data-stu-id="6219c-108">Example 1 : Get a specified private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfiguration = Get-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -ApplicationGateway $AppGw
```

<span data-ttu-id="6219c-109">Der erste Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 aus der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="6219c-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6219c-110">Der zweite Befehl ruft die private Link-Konfiguration mit dem Namen privateLinkConfig01 aus $AppGw ab und speichert Sie in der $PrivateLinkConfiguration-Variablen.</span><span class="sxs-lookup"><span data-stu-id="6219c-110">The second command gets the private link configuration named privateLinkConfig01 from $AppGw and stores it in the $PrivateLinkConfiguration variable.</span></span>

### <span data-ttu-id="6219c-111">Beispiel 2: Abrufen einer Liste der Konfiguration privater Links</span><span class="sxs-lookup"><span data-stu-id="6219c-111">Example 2 : Get a list of private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfigurations = Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="6219c-112">Der erste Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 aus der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="6219c-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6219c-113">Der zweite Befehl ruft alle privaten Link Konfigurationen aus $AppGw ab und speichert Sie in der $PrivateLinkConfigurations-Variablen.</span><span class="sxs-lookup"><span data-stu-id="6219c-113">The second command gets all the private link configurations from $AppGw and stores it in the $PrivateLinkConfigurations variable.</span></span>

## <span data-ttu-id="6219c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="6219c-114">PARAMETERS</span></span>

### <span data-ttu-id="6219c-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6219c-115">-ApplicationGateway</span></span>
<span data-ttu-id="6219c-116">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="6219c-116">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6219c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6219c-117">-DefaultProfile</span></span>
<span data-ttu-id="6219c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6219c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6219c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6219c-119">-Name</span></span>
<span data-ttu-id="6219c-120">Der Name der privateLink-Konfiguration des Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="6219c-120">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="6219c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6219c-121">CommonParameters</span></span>
<span data-ttu-id="6219c-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6219c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6219c-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6219c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6219c-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6219c-124">INPUTS</span></span>

### <span data-ttu-id="6219c-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6219c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6219c-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6219c-126">OUTPUTS</span></span>

### <span data-ttu-id="6219c-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6219c-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="6219c-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="6219c-128">NOTES</span></span>

## <span data-ttu-id="6219c-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6219c-129">RELATED LINKS</span></span>

[<span data-ttu-id="6219c-130">Neu – AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6219c-130">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="6219c-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6219c-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="6219c-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6219c-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="6219c-133">Satz-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6219c-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)