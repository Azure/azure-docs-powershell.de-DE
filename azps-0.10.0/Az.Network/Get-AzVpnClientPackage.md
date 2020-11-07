---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: d08f91029940d60440d50be406dbdfe3652934a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841475"
---
# <span data-ttu-id="5b0f7-101">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="5b0f7-101">Get-AzVpnClientPackage</span></span>

## <span data-ttu-id="5b0f7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b0f7-102">SYNOPSIS</span></span>
<span data-ttu-id="5b0f7-103">Ruft Informationen zu einem VPN-Clientpaket ab.</span><span class="sxs-lookup"><span data-stu-id="5b0f7-103">Gets information about a VPN client package.</span></span>

## <span data-ttu-id="5b0f7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b0f7-104">SYNTAX</span></span>

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b0f7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b0f7-105">DESCRIPTION</span></span>
<span data-ttu-id="5b0f7-106">Das Cmdlet " **Get-AzVpnClientPackage** " Ruft Informationen zu den VPN-Client Paketen ab, die von einem virtuellen Netzwerkgateway zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="5b0f7-106">The **Get-AzVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="5b0f7-107">Clientpakete enthalten Konfigurationsdaten, die es einem Clientcomputer ermöglichen, eine VPN-Verbindung mit einem virtuellen Azure-Netzwerk herzustellen. auf Clientcomputern muss das richtige Konfigurationspaket installiert sein, um eine VPN-Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="5b0f7-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="5b0f7-108">Unterschiedliche Konfigurationspakete sind basierend auf der Windows-Version des Clientcomputers (beispielsweise Windows 7 oder Windows 10) und auf der Prozessorarchitektur des Clientcomputers verfügbar (amd64 oder x86).</span><span class="sxs-lookup"><span data-stu-id="5b0f7-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="5b0f7-109">Sie müssen den Architekturtyp angeben, wenn Sie **Get-AzVpnClientPackage** ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b0f7-109">You must specify the architecture type when running **Get-AzVpnClientPackage**.</span></span>

## <span data-ttu-id="5b0f7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b0f7-110">EXAMPLES</span></span>

### <span data-ttu-id="5b0f7-111">Beispiel 1: Abrufen von Informationen zu einem VPN-Clientpaket für die Prozessorarchitektur</span><span class="sxs-lookup"><span data-stu-id="5b0f7-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="5b0f7-112">Dieser Befehl ruft Informationen zu den amd64-VPN-Client Paketen ab, die auf dem virtuellen Netzwerkgateway mit dem Namen ContosoVirtualNetworkGateway gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="5b0f7-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="5b0f7-113">Wenn Sie Informationen zu den x86-Client Paketen erhalten möchten, setzen Sie den Wert des *ProcessorArchitecture* -Parameters auf x86.</span><span class="sxs-lookup"><span data-stu-id="5b0f7-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="5b0f7-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b0f7-114">PARAMETERS</span></span>

### <span data-ttu-id="5b0f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b0f7-115">-DefaultProfile</span></span>
<span data-ttu-id="5b0f7-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5b0f7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b0f7-117">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="5b0f7-117">-ProcessorArchitecture</span></span>
<span data-ttu-id="5b0f7-118">Gibt den Typ der CPU-Architektur an, für die das Clientpaket vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="5b0f7-118">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="5b0f7-119">Gültige Werte sind amd64 und x86.</span><span class="sxs-lookup"><span data-stu-id="5b0f7-119">Valid values are Amd64 and X86.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b0f7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b0f7-120">-ResourceGroupName</span></span>
<span data-ttu-id="5b0f7-121">Gibt den Namen der Ressourcengruppe an, der das virtuelle Netzwerkgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="5b0f7-121">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="5b0f7-122">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="5b0f7-122">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b0f7-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="5b0f7-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="5b0f7-124">Gibt den Namen des virtuellen Netzwerkgateways an, in dem die Clientpaket Informationen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="5b0f7-124">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b0f7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b0f7-125">CommonParameters</span></span>
<span data-ttu-id="5b0f7-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b0f7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b0f7-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b0f7-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b0f7-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b0f7-128">INPUTS</span></span>

### <span data-ttu-id="5b0f7-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5b0f7-129">String</span></span>
<span data-ttu-id="5b0f7-130">Der Parameter "ResourceGroupName" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5b0f7-130">Parameter 'ResourceGroupName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="5b0f7-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5b0f7-131">String</span></span>
<span data-ttu-id="5b0f7-132">Der Parameter "VirtualNetworkGatewayName" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5b0f7-132">Parameter 'VirtualNetworkGatewayName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5b0f7-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b0f7-133">OUTPUTS</span></span>

###  
<span data-ttu-id="5b0f7-134">**Get-AzVpnClientPackage** gibt Instanzen des System. String-Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="5b0f7-134">**Get-AzVpnClientPackage** returns instances of the System.String object.</span></span>

## <span data-ttu-id="5b0f7-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b0f7-135">NOTES</span></span>

## <span data-ttu-id="5b0f7-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b0f7-136">RELATED LINKS</span></span>

[<span data-ttu-id="5b0f7-137">Größe ändern – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5b0f7-137">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="5b0f7-138">Satz-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="5b0f7-138">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


