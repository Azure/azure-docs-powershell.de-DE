---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 3442c5a16493d42dbbfd6460f398b37bb92d6d72
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821264"
---
# <span data-ttu-id="1983c-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1983c-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="1983c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1983c-102">SYNOPSIS</span></span>
<span data-ttu-id="1983c-103">Aktualisiert eine Firewall-Richtlinie für Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="1983c-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="1983c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1983c-104">SYNTAX</span></span>

### <span data-ttu-id="1983c-105">ByFactoryObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="1983c-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1983c-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="1983c-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1983c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1983c-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1983c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1983c-108">DESCRIPTION</span></span>
<span data-ttu-id="1983c-109">Das Cmdlet " **Satz-AzApplicationGatewayFirewallPolicy** " aktualisiert eine Azure Application Gateway-Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="1983c-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="1983c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1983c-110">EXAMPLES</span></span>

### <span data-ttu-id="1983c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1983c-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="1983c-112">Dieser Befehl aktualisiert die Firewall-Richtlinie des Anwendungs Gateways mit den Einstellungen in der $AppGwFirewallPolicy-Variable und speichert das aktualisierte Gateway in der $UpdatedAppGwFirewallPolicy-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1983c-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="1983c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1983c-113">PARAMETERS</span></span>

### <span data-ttu-id="1983c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1983c-114">-AsJob</span></span>
<span data-ttu-id="1983c-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1983c-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1983c-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="1983c-116">-CustomRule</span></span>
<span data-ttu-id="1983c-117">Die Liste der customrules</span><span class="sxs-lookup"><span data-stu-id="1983c-117">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1983c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1983c-118">-DefaultProfile</span></span>
<span data-ttu-id="1983c-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1983c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1983c-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1983c-120">-InputObject</span></span>
<span data-ttu-id="1983c-121">Die applicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1983c-121">The applicationGatewayFirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1983c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1983c-122">-Name</span></span>
<span data-ttu-id="1983c-123">Der Name der Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="1983c-123">The Firewall Policy Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1983c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1983c-124">-ResourceGroupName</span></span>
<span data-ttu-id="1983c-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1983c-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1983c-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1983c-126">-ResourceId</span></span>
<span data-ttu-id="1983c-127">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="1983c-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1983c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1983c-128">CommonParameters</span></span>
<span data-ttu-id="1983c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1983c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1983c-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1983c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1983c-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1983c-131">INPUTS</span></span>

### <span data-ttu-id="1983c-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1983c-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="1983c-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1983c-133">OUTPUTS</span></span>

### <span data-ttu-id="1983c-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1983c-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="1983c-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="1983c-135">NOTES</span></span>

## <span data-ttu-id="1983c-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1983c-136">RELATED LINKS</span></span>
