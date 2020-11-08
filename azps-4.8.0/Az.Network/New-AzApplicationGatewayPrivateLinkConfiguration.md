---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: df616c0b8e6d2fdb7de3567c921714251093fd60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175080"
---
# <span data-ttu-id="66ebb-101">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="66ebb-101">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="66ebb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66ebb-102">SYNOPSIS</span></span>
<span data-ttu-id="66ebb-103">Erstellt eine private Link Konfiguration für ein Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="66ebb-103">Creates a private link configuration for an application gateway</span></span>

## <span data-ttu-id="66ebb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66ebb-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66ebb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66ebb-105">DESCRIPTION</span></span>
<span data-ttu-id="66ebb-106">Das Cmdlet **New-AzApplicationGatewayPrivateLinkConfiguration** erstellt eine PrivateLink-Konfiguration für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="66ebb-106">The **New-AzApplicationGatewayPrivateLinkConfiguration** cmdlet creates an PrivateLink Configuration for an Azure application gateway.</span></span>
<span data-ttu-id="66ebb-107">Die Konfiguration privater Links muss einer Frontend-IP-Konfiguration zugeordnet sein, um die Funktion privater Link zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="66ebb-107">The private link configuration must be associated to a frontend ip configuration to enable the private link functionality.</span></span>
<span data-ttu-id="66ebb-108">Eine private Link-Konfiguration kann atmost nur einer Frontend-IP-Konfiguration auf dem Application Gateway zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="66ebb-108">One private link configuration can atmost be associated to only one frontend ip configuration on application gateway.</span></span>

## <span data-ttu-id="66ebb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66ebb-109">EXAMPLES</span></span>

### <span data-ttu-id="66ebb-110">Beispiel 1: Erstellen einer privaten Link Konfiguration mit einer einzelnen IP-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="66ebb-110">Example 1: Create an Private Link Configuration with single Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

<span data-ttu-id="66ebb-111">Mit diesem Befehl wird eine PrivateLink-Konfiguration mit dem Namen "privateLinkConfig01" erstellt, und das Ergebnis wird in der Variablen mit dem Namen $PrivateLinkConfiguration gespeichert.</span><span class="sxs-lookup"><span data-stu-id="66ebb-111">This command creates an PrivateLink configuration named 'privateLinkConfig01' and stores the result in the variable named $PrivateLinkConfiguration.</span></span>

### <span data-ttu-id="66ebb-112">Beispiel 2: Erstellen einer privaten Link Konfiguration mit mehreren IP-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="66ebb-112">Example 2: Create an Private Link Configuration with multiple Ip Configurations</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

<span data-ttu-id="66ebb-113">Mit diesem Befehl wird eine PrivateLink-Konfiguration mit dem Namen "privateLinkConfig01" mit zwei ipConfigurations erstellt, und das Ergebnis wird in der Variablen mit dem Namen $PrivateLinkConfiguration gespeichert.</span><span class="sxs-lookup"><span data-stu-id="66ebb-113">This command creates an PrivateLink configuration named 'privateLinkConfig01' with two ipConfigurations and stores the result in the variable named $PrivateLinkConfiguration.</span></span> 

## <span data-ttu-id="66ebb-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="66ebb-114">PARAMETERS</span></span>

### <span data-ttu-id="66ebb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66ebb-115">-DefaultProfile</span></span>
<span data-ttu-id="66ebb-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="66ebb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66ebb-117">-IPKonfigurationsdateiAddress</span><span class="sxs-lookup"><span data-stu-id="66ebb-117">-IpConfiguration</span></span>
<span data-ttu-id="66ebb-118">Die Liste der IPKonfigurationsdateiAddress</span><span class="sxs-lookup"><span data-stu-id="66ebb-118">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="66ebb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="66ebb-119">-Name</span></span>
<span data-ttu-id="66ebb-120">Der Name der privateLink-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="66ebb-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="66ebb-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="66ebb-121">-Confirm</span></span>
<span data-ttu-id="66ebb-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66ebb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66ebb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66ebb-123">-WhatIf</span></span>
<span data-ttu-id="66ebb-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66ebb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66ebb-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66ebb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66ebb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66ebb-126">CommonParameters</span></span>
<span data-ttu-id="66ebb-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66ebb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66ebb-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66ebb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66ebb-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66ebb-129">INPUTS</span></span>

### <span data-ttu-id="66ebb-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPrivateLinkIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="66ebb-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="66ebb-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66ebb-131">OUTPUTS</span></span>

### <span data-ttu-id="66ebb-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="66ebb-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="66ebb-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="66ebb-133">NOTES</span></span>

## <span data-ttu-id="66ebb-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66ebb-134">RELATED LINKS</span></span>

[<span data-ttu-id="66ebb-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="66ebb-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="66ebb-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="66ebb-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="66ebb-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="66ebb-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="66ebb-138">Satz-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="66ebb-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
