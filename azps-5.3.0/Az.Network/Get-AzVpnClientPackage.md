---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: 8eba8d26bcac5de16be3e2cda5e8ca80356aea11
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379670"
---
# <span data-ttu-id="dfbcd-101">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="dfbcd-101">Get-AzVpnClientPackage</span></span>

## <span data-ttu-id="dfbcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfbcd-102">SYNOPSIS</span></span>
<span data-ttu-id="dfbcd-103">Ruft Informationen zu einem VPN-Clientpaket ab.</span><span class="sxs-lookup"><span data-stu-id="dfbcd-103">Gets information about a VPN client package.</span></span>

## <span data-ttu-id="dfbcd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dfbcd-104">SYNTAX</span></span>

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfbcd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dfbcd-105">DESCRIPTION</span></span>
<span data-ttu-id="dfbcd-106">Das **Cmdlet "Get-AzVpnClientPackage"** ruft Informationen zu den VPN-Clientpaketen ab, die über ein virtuelles Netzwerkgateway verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="dfbcd-106">The **Get-AzVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="dfbcd-107">Clientpakete enthalten Konfigurationsdaten, die einem Clientcomputer das Herstellen einer #A0 mit einem virtuellen #A1 ermöglichen. client computers must have the correct configuration package installed to make a VPN connection.</span><span class="sxs-lookup"><span data-stu-id="dfbcd-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="dfbcd-108">Basierend auf der Version des Clientcomputers von Windows (z. B. Windows 7 oder Windows 10) und der Prozessorarchitektur des Clientcomputers (AMD64 oder x86) stehen verschiedene Konfigurationspakete zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="dfbcd-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="dfbcd-109">Sie müssen den Architekturtyp angeben, wenn **Sie "Get-AzVpnClientPackage" ausführen.**</span><span class="sxs-lookup"><span data-stu-id="dfbcd-109">You must specify the architecture type when running **Get-AzVpnClientPackage**.</span></span>

## <span data-ttu-id="dfbcd-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dfbcd-110">EXAMPLES</span></span>

### <span data-ttu-id="dfbcd-111">Beispiel 1: Informationen zu einem CLIENTpaket für die Prozessorarchitektur von VPN</span><span class="sxs-lookup"><span data-stu-id="dfbcd-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="dfbcd-112">Dieser Befehl ruft Informationen zu den AMD64 VPN-Clientpaketen ab, die auf dem virtuellen Netzwerkgateway namens "ContosoVirtualNetworkGateway" gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="dfbcd-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="dfbcd-113">Um Informationen zu den x86-Clientpaketen zu erhalten, legen Sie den Wert des Parameters *"ProcessorArchitecture"* auf "x86" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dfbcd-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="dfbcd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfbcd-114">PARAMETERS</span></span>

### <span data-ttu-id="dfbcd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfbcd-115">-DefaultProfile</span></span>
<span data-ttu-id="dfbcd-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dfbcd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfbcd-117">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="dfbcd-117">-ProcessorArchitecture</span></span>
<span data-ttu-id="dfbcd-118">Gibt den Typ der CPU-Architektur an, auf den das Clientpaket ausgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dfbcd-118">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="dfbcd-119">Gültige Werte sind Amd64 und X86.</span><span class="sxs-lookup"><span data-stu-id="dfbcd-119">Valid values are Amd64 and X86.</span></span>

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

### <span data-ttu-id="dfbcd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfbcd-120">-ResourceGroupName</span></span>
<span data-ttu-id="dfbcd-121">Gibt den Namen der Ressourcengruppe an, der das virtuelle Netzwerkgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="dfbcd-121">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="dfbcd-122">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Verwaltung von Azure zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="dfbcd-122">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="dfbcd-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="dfbcd-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="dfbcd-124">Gibt den Namen des virtuellen Netzwerkgateways an, in dem die Clientpaketinformationen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="dfbcd-124">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

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

### <span data-ttu-id="dfbcd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfbcd-125">CommonParameters</span></span>
<span data-ttu-id="dfbcd-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfbcd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfbcd-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dfbcd-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfbcd-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dfbcd-128">INPUTS</span></span>

### <span data-ttu-id="dfbcd-129">System.String</span><span class="sxs-lookup"><span data-stu-id="dfbcd-129">System.String</span></span>

## <span data-ttu-id="dfbcd-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dfbcd-130">OUTPUTS</span></span>

### <span data-ttu-id="dfbcd-131">System.String</span><span class="sxs-lookup"><span data-stu-id="dfbcd-131">System.String</span></span>

## <span data-ttu-id="dfbcd-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dfbcd-132">NOTES</span></span>

## <span data-ttu-id="dfbcd-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dfbcd-133">RELATED LINKS</span></span>

[<span data-ttu-id="dfbcd-134">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dfbcd-134">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="dfbcd-135">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="dfbcd-135">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


