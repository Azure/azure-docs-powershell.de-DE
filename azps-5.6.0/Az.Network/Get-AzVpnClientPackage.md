---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: 69fcd4ee3cdcd2692c242a366c7d88545f9641b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945929"
---
# <span data-ttu-id="424a2-101">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="424a2-101">Get-AzVpnClientPackage</span></span>

## <span data-ttu-id="424a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="424a2-102">SYNOPSIS</span></span>
<span data-ttu-id="424a2-103">Ruft Informationen zu einem VPN-Clientpaket ab.</span><span class="sxs-lookup"><span data-stu-id="424a2-103">Gets information about a VPN client package.</span></span>

## <span data-ttu-id="424a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="424a2-104">SYNTAX</span></span>

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="424a2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="424a2-105">DESCRIPTION</span></span>
<span data-ttu-id="424a2-106">Das **Get-AzVpnClientPackage-Cmdlet** ruft Informationen zu den VPN-Clientpaketen ab, die über ein Gateway für virtuelle Netzwerke verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="424a2-106">The **Get-AzVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="424a2-107">Clientpakete enthalten Konfigurationsdaten, die es einem Clientcomputer ermöglichen, eine #A0 mit einem virtuellen Azure-Netzwerk herzustellen. Auf Clientcomputern muss das richtige Konfigurationspaket installiert sein, um eine VPN-Verbindung herstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="424a2-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="424a2-108">Unterschiedliche Konfigurationspakete sind basierend auf der Windows-Version des Clientcomputers (z. B. Windows 7 oder Windows 10) und der Prozessorarchitektur des Clientcomputers (AMD64 oder x86) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="424a2-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="424a2-109">Sie müssen den Architekturtyp angeben, wenn **Sie Get-AzVpnClientPackage ausführen.**</span><span class="sxs-lookup"><span data-stu-id="424a2-109">You must specify the architecture type when running **Get-AzVpnClientPackage**.</span></span>

## <span data-ttu-id="424a2-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="424a2-110">EXAMPLES</span></span>

### <span data-ttu-id="424a2-111">Beispiel 1: Informationen zu einem VPN-Clientpaket der Prozessorarchitektur</span><span class="sxs-lookup"><span data-stu-id="424a2-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="424a2-112">Dieser Befehl ruft Informationen zu den AMD64-VPN-Clientpaketen ab, die auf dem Virtuellen Netzwerkgateway namens ContosoVirtualNetworkGateway gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="424a2-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="424a2-113">Um Informationen zu den x86-Clientpaketen zu erhalten, legen Sie den Wert des *Parameters ProcessorArchitecture* auf x86.</span><span class="sxs-lookup"><span data-stu-id="424a2-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="424a2-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="424a2-114">PARAMETERS</span></span>

### <span data-ttu-id="424a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="424a2-115">-DefaultProfile</span></span>
<span data-ttu-id="424a2-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="424a2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="424a2-117">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="424a2-117">-ProcessorArchitecture</span></span>
<span data-ttu-id="424a2-118">Gibt den Typ der CPU-Architektur an, für den das Clientpaket entwickelt wurde.</span><span class="sxs-lookup"><span data-stu-id="424a2-118">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="424a2-119">Gültige Werte sind Amd64 und X86.</span><span class="sxs-lookup"><span data-stu-id="424a2-119">Valid values are Amd64 and X86.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="424a2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="424a2-120">-ResourceGroupName</span></span>
<span data-ttu-id="424a2-121">Gibt den Namen der Ressourcengruppe an, der das Virtuelle Netzwerkgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="424a2-121">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="424a2-122">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="424a2-122">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="424a2-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="424a2-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="424a2-124">Gibt den Namen des Virtuellen Netzwerkgateways an, in dem die Clientpaketinformationen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="424a2-124">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="424a2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="424a2-125">CommonParameters</span></span>
<span data-ttu-id="424a2-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="424a2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="424a2-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="424a2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="424a2-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="424a2-128">INPUTS</span></span>

### <span data-ttu-id="424a2-129">System.String</span><span class="sxs-lookup"><span data-stu-id="424a2-129">System.String</span></span>

## <span data-ttu-id="424a2-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="424a2-130">OUTPUTS</span></span>

### <span data-ttu-id="424a2-131">System.String</span><span class="sxs-lookup"><span data-stu-id="424a2-131">System.String</span></span>

## <span data-ttu-id="424a2-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="424a2-132">NOTES</span></span>

## <span data-ttu-id="424a2-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="424a2-133">RELATED LINKS</span></span>

[<span data-ttu-id="424a2-134">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="424a2-134">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="424a2-135">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="424a2-135">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


