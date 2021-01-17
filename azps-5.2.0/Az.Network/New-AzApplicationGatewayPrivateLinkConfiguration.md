---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: df616c0b8e6d2fdb7de3567c921714251093fd60
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371690"
---
# <span data-ttu-id="30fdb-101">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="30fdb-101">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="30fdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30fdb-102">SYNOPSIS</span></span>
<span data-ttu-id="30fdb-103">Erstellt eine Konfiguration für private Links für ein Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="30fdb-103">Creates a private link configuration for an application gateway</span></span>

## <span data-ttu-id="30fdb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30fdb-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30fdb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30fdb-105">DESCRIPTION</span></span>
<span data-ttu-id="30fdb-106">Das **Cmdlet "New-AzApplicationGatewayPrivateLinkConfiguration"** erstellt eine PrivateLink-Konfiguration für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="30fdb-106">The **New-AzApplicationGatewayPrivateLinkConfiguration** cmdlet creates an PrivateLink Configuration for an Azure application gateway.</span></span>
<span data-ttu-id="30fdb-107">Die Konfiguration privater Links muss einer Frontend-IP-Konfiguration zugeordnet sein, um die Funktion für private Links zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="30fdb-107">The private link configuration must be associated to a frontend ip configuration to enable the private link functionality.</span></span>
<span data-ttu-id="30fdb-108">Eine Konfiguration für private Links kann nur einer Frontend-IP-Konfiguration auf dem Anwendungsgateway zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="30fdb-108">One private link configuration can atmost be associated to only one frontend ip configuration on application gateway.</span></span>

## <span data-ttu-id="30fdb-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="30fdb-109">EXAMPLES</span></span>

### <span data-ttu-id="30fdb-110">Beispiel 1: Erstellen einer Konfiguration für private Verknüpfungen mit einer einzelnen Ip-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="30fdb-110">Example 1: Create an Private Link Configuration with single Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

<span data-ttu-id="30fdb-111">Dieser Befehl erstellt eine PrivateLink-Konfiguration namens 'privateLinkConfig01' und speichert das Ergebnis in der Variablen namens $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="30fdb-111">This command creates an PrivateLink configuration named 'privateLinkConfig01' and stores the result in the variable named $PrivateLinkConfiguration.</span></span>

### <span data-ttu-id="30fdb-112">Beispiel 2: Erstellen einer Konfiguration für private Verknüpfungen mit mehreren Ip-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="30fdb-112">Example 2: Create an Private Link Configuration with multiple Ip Configurations</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

<span data-ttu-id="30fdb-113">Dieser Befehl erstellt eine PrivateLink-Konfiguration namens 'privateLinkConfig01' mit zwei ipConfigurations und speichert das Ergebnis in der Variablen namens $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="30fdb-113">This command creates an PrivateLink configuration named 'privateLinkConfig01' with two ipConfigurations and stores the result in the variable named $PrivateLinkConfiguration.</span></span> 

## <span data-ttu-id="30fdb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30fdb-114">PARAMETERS</span></span>

### <span data-ttu-id="30fdb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30fdb-115">-DefaultProfile</span></span>
<span data-ttu-id="30fdb-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="30fdb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30fdb-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="30fdb-117">-IpConfiguration</span></span>
<span data-ttu-id="30fdb-118">Die Liste der "ipConfiguration"</span><span class="sxs-lookup"><span data-stu-id="30fdb-118">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30fdb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="30fdb-119">-Name</span></span>
<span data-ttu-id="30fdb-120">Der Name der Konfiguration "privateLink"</span><span class="sxs-lookup"><span data-stu-id="30fdb-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="30fdb-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30fdb-121">-Confirm</span></span>
<span data-ttu-id="30fdb-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="30fdb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30fdb-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="30fdb-123">-WhatIf</span></span>
<span data-ttu-id="30fdb-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="30fdb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30fdb-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="30fdb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30fdb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30fdb-126">CommonParameters</span></span>
<span data-ttu-id="30fdb-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30fdb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30fdb-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30fdb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30fdb-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="30fdb-129">INPUTS</span></span>

### <span data-ttu-id="30fdb-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="30fdb-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="30fdb-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="30fdb-131">OUTPUTS</span></span>

### <span data-ttu-id="30fdb-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="30fdb-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="30fdb-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="30fdb-133">NOTES</span></span>

## <span data-ttu-id="30fdb-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="30fdb-134">RELATED LINKS</span></span>

[<span data-ttu-id="30fdb-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="30fdb-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="30fdb-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="30fdb-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="30fdb-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="30fdb-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="30fdb-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="30fdb-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
