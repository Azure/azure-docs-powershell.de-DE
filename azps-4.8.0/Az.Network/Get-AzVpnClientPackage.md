---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: 8eba8d26bcac5de16be3e2cda5e8ca80356aea11
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010131"
---
# <span data-ttu-id="f2e7e-101">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="f2e7e-101">Get-AzVpnClientPackage</span></span>

## <span data-ttu-id="f2e7e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f2e7e-102">SYNOPSIS</span></span>
<span data-ttu-id="f2e7e-103">Ruft Informationen zu einem VPN-Clientpaket ab.</span><span class="sxs-lookup"><span data-stu-id="f2e7e-103">Gets information about a VPN client package.</span></span>

## <span data-ttu-id="f2e7e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2e7e-104">SYNTAX</span></span>

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2e7e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2e7e-105">DESCRIPTION</span></span>
<span data-ttu-id="f2e7e-106">Das Cmdlet " **Get-AzVpnClientPackage** " Ruft Informationen zu den VPN-Client Paketen ab, die von einem virtuellen Netzwerkgateway zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="f2e7e-106">The **Get-AzVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="f2e7e-107">Clientpakete enthalten Konfigurationsdaten, die es einem Clientcomputer ermöglichen, eine VPN-Verbindung mit einem virtuellen Azure-Netzwerk herzustellen. auf Clientcomputern muss das richtige Konfigurationspaket installiert sein, um eine VPN-Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="f2e7e-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="f2e7e-108">Unterschiedliche Konfigurationspakete sind basierend auf der Windows-Version des Clientcomputers (beispielsweise Windows 7 oder Windows 10) und auf der Prozessorarchitektur des Clientcomputers verfügbar (amd64 oder x86).</span><span class="sxs-lookup"><span data-stu-id="f2e7e-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="f2e7e-109">Sie müssen den Architekturtyp angeben, wenn Sie **Get-AzVpnClientPackage** ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2e7e-109">You must specify the architecture type when running **Get-AzVpnClientPackage**.</span></span>

## <span data-ttu-id="f2e7e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f2e7e-110">EXAMPLES</span></span>

### <span data-ttu-id="f2e7e-111">Beispiel 1: Abrufen von Informationen zu einem VPN-Clientpaket für die Prozessorarchitektur</span><span class="sxs-lookup"><span data-stu-id="f2e7e-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="f2e7e-112">Dieser Befehl ruft Informationen zu den amd64-VPN-Client Paketen ab, die auf dem virtuellen Netzwerkgateway mit dem Namen ContosoVirtualNetworkGateway gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="f2e7e-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="f2e7e-113">Wenn Sie Informationen zu den x86-Client Paketen erhalten möchten, setzen Sie den Wert des *ProcessorArchitecture* -Parameters auf x86.</span><span class="sxs-lookup"><span data-stu-id="f2e7e-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="f2e7e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2e7e-114">PARAMETERS</span></span>

### <span data-ttu-id="f2e7e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2e7e-115">-DefaultProfile</span></span>
<span data-ttu-id="f2e7e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f2e7e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2e7e-117">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="f2e7e-117">-ProcessorArchitecture</span></span>
<span data-ttu-id="f2e7e-118">Gibt den Typ der CPU-Architektur an, für die das Clientpaket vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="f2e7e-118">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="f2e7e-119">Gültige Werte sind amd64 und x86.</span><span class="sxs-lookup"><span data-stu-id="f2e7e-119">Valid values are Amd64 and X86.</span></span>

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

### <span data-ttu-id="f2e7e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2e7e-120">-ResourceGroupName</span></span>
<span data-ttu-id="f2e7e-121">Gibt den Namen der Ressourcengruppe an, der das virtuelle Netzwerkgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="f2e7e-121">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="f2e7e-122">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="f2e7e-122">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="f2e7e-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="f2e7e-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="f2e7e-124">Gibt den Namen des virtuellen Netzwerkgateways an, in dem die Clientpaket Informationen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="f2e7e-124">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

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

### <span data-ttu-id="f2e7e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2e7e-125">CommonParameters</span></span>
<span data-ttu-id="f2e7e-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2e7e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2e7e-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2e7e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2e7e-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f2e7e-128">INPUTS</span></span>

### <span data-ttu-id="f2e7e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f2e7e-129">System.String</span></span>

## <span data-ttu-id="f2e7e-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f2e7e-130">OUTPUTS</span></span>

### <span data-ttu-id="f2e7e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f2e7e-131">System.String</span></span>

## <span data-ttu-id="f2e7e-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="f2e7e-132">NOTES</span></span>

## <span data-ttu-id="f2e7e-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f2e7e-133">RELATED LINKS</span></span>

[<span data-ttu-id="f2e7e-134">Größe ändern – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f2e7e-134">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="f2e7e-135">Satz-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="f2e7e-135">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


