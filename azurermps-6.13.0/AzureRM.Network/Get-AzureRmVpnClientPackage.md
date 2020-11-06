---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientPackage.md
ms.openlocfilehash: fc94bb7de5663995e75f0c4f1fed05fb36b35f40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482349"
---
# <span data-ttu-id="f2e78-101">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="f2e78-101">Get-AzureRmVpnClientPackage</span></span>

## <span data-ttu-id="f2e78-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f2e78-102">SYNOPSIS</span></span>
<span data-ttu-id="f2e78-103">Ruft Informationen zu einem VPN-Clientpaket ab.</span><span class="sxs-lookup"><span data-stu-id="f2e78-103">Gets information about a VPN client package.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2e78-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2e78-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2e78-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2e78-105">DESCRIPTION</span></span>
<span data-ttu-id="f2e78-106">Das Cmdlet " **Get-AzureRmVpnClientPackage** " Ruft Informationen zu den VPN-Client Paketen ab, die von einem virtuellen Netzwerkgateway zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="f2e78-106">The **Get-AzureRmVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="f2e78-107">Clientpakete enthalten Konfigurationsdaten, die es einem Clientcomputer ermöglichen, eine VPN-Verbindung mit einem virtuellen Azure-Netzwerk herzustellen. auf Clientcomputern muss das richtige Konfigurationspaket installiert sein, um eine VPN-Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="f2e78-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="f2e78-108">Unterschiedliche Konfigurationspakete sind basierend auf der Windows-Version des Clientcomputers (beispielsweise Windows 7 oder Windows 10) und auf der Prozessorarchitektur des Clientcomputers verfügbar (amd64 oder x86).</span><span class="sxs-lookup"><span data-stu-id="f2e78-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="f2e78-109">Sie müssen den Architekturtyp angeben, wenn Sie **Get-AzureRmVpnClientPackage** ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2e78-109">You must specify the architecture type when running **Get-AzureRmVpnClientPackage**.</span></span>

## <span data-ttu-id="f2e78-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f2e78-110">EXAMPLES</span></span>

### <span data-ttu-id="f2e78-111">Beispiel 1: Abrufen von Informationen zu einem VPN-Clientpaket für die Prozessorarchitektur</span><span class="sxs-lookup"><span data-stu-id="f2e78-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzureRmVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="f2e78-112">Dieser Befehl ruft Informationen zu den amd64-VPN-Client Paketen ab, die auf dem virtuellen Netzwerkgateway mit dem Namen ContosoVirtualNetworkGateway gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="f2e78-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="f2e78-113">Wenn Sie Informationen zu den x86-Client Paketen erhalten möchten, setzen Sie den Wert des *ProcessorArchitecture* -Parameters auf x86.</span><span class="sxs-lookup"><span data-stu-id="f2e78-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="f2e78-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2e78-114">PARAMETERS</span></span>

### <span data-ttu-id="f2e78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2e78-115">-DefaultProfile</span></span>
<span data-ttu-id="f2e78-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f2e78-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e78-117">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="f2e78-117">-ProcessorArchitecture</span></span>
<span data-ttu-id="f2e78-118">Gibt den Typ der CPU-Architektur an, für die das Clientpaket vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="f2e78-118">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="f2e78-119">Gültige Werte sind amd64 und x86.</span><span class="sxs-lookup"><span data-stu-id="f2e78-119">Valid values are Amd64 and X86.</span></span>

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

### <span data-ttu-id="f2e78-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2e78-120">-ResourceGroupName</span></span>
<span data-ttu-id="f2e78-121">Gibt den Namen der Ressourcengruppe an, der das virtuelle Netzwerkgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="f2e78-121">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="f2e78-122">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="f2e78-122">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="f2e78-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="f2e78-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="f2e78-124">Gibt den Namen des virtuellen Netzwerkgateways an, in dem die Clientpaket Informationen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="f2e78-124">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

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

### <span data-ttu-id="f2e78-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2e78-125">CommonParameters</span></span>
<span data-ttu-id="f2e78-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2e78-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2e78-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2e78-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2e78-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f2e78-128">INPUTS</span></span>

### <span data-ttu-id="f2e78-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f2e78-129">System.String</span></span>
<span data-ttu-id="f2e78-130">Parameter: ResourceGroupName (ByValue), VirtualNetworkGatewayName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f2e78-130">Parameters: ResourceGroupName (ByValue), VirtualNetworkGatewayName (ByValue)</span></span>

## <span data-ttu-id="f2e78-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f2e78-131">OUTPUTS</span></span>

### <span data-ttu-id="f2e78-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f2e78-132">System.String</span></span>

## <span data-ttu-id="f2e78-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="f2e78-133">NOTES</span></span>

## <span data-ttu-id="f2e78-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f2e78-134">RELATED LINKS</span></span>

[<span data-ttu-id="f2e78-135">Größe ändern – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f2e78-135">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="f2e78-136">Satz-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="f2e78-136">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


