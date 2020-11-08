---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C85576C1-182B-467E-9620-A475728E20D2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3715b07c66d76c824e684976f18de4ecea64cdb1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006242"
---
# <span data-ttu-id="d285f-101">Set-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="d285f-101">Set-AzureVNetGatewayIPsecParameters</span></span>

## <span data-ttu-id="d285f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d285f-102">SYNOPSIS</span></span>
<span data-ttu-id="d285f-103">Legt IPSec-Parameter für die Verbindung zwischen einem virtuellen Netzwerkgateway und einer lokalen Netzwerk Website fest.</span><span class="sxs-lookup"><span data-stu-id="d285f-103">Sets IPsec parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="d285f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d285f-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayIPsecParameters -VNetName <String> -LocalNetworkSiteName <String>
 [-EncryptionType <String>] [-PfsGroup <String>] [-SADataSizeKilobytes <Int32>] [-SALifetimeSeconds <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d285f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d285f-105">DESCRIPTION</span></span>
<span data-ttu-id="d285f-106">Das Cmdlet **Set-AzureVNetGatewayIPsecParameters** legt IPSec (Internet Protocol Security) und IKE-Parameter für die Verbindung zwischen einem virtuellen Netzwerkgateway und einer lokalen Netzwerk Website fest.</span><span class="sxs-lookup"><span data-stu-id="d285f-106">The **Set-AzureVNetGatewayIPsecParameters** cmdlet sets Internet Protocol security (IPsec) and Internet Key Exchange (IKE) parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="d285f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d285f-107">EXAMPLES</span></span>

## <span data-ttu-id="d285f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d285f-108">PARAMETERS</span></span>

### <span data-ttu-id="d285f-109">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="d285f-109">-EncryptionType</span></span>
<span data-ttu-id="d285f-110">Gibt den Verschlüsselungstyp für das virtuelle Netzwerkgateway an.</span><span class="sxs-lookup"><span data-stu-id="d285f-110">Specifies the encryption type for the virtual network gateway.</span></span>
<span data-ttu-id="d285f-111">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="d285f-111">Valid values are:</span></span> 

- <span data-ttu-id="d285f-112">NoEncryption</span><span class="sxs-lookup"><span data-stu-id="d285f-112">NoEncryption</span></span> 
- <span data-ttu-id="d285f-113">RequireEncryption</span><span class="sxs-lookup"><span data-stu-id="d285f-113">RequireEncryption</span></span>

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

### <span data-ttu-id="d285f-114">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="d285f-114">-LocalNetworkSiteName</span></span>
<span data-ttu-id="d285f-115">Gibt den Namen der lokalen Netzwerkstandort Verbindung an, auf der dieses Cmdlet die IPSec-und IKE-Parameter konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="d285f-115">Specifies the name of the local network site connection on which this cmdlet configures the IPsec and IKE parameters.</span></span>

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

### <span data-ttu-id="d285f-116">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="d285f-116">-PfsGroup</span></span>
<span data-ttu-id="d285f-117">Gibt die Gruppe "Perfect Forward Heimlichkeit (PFS)" an.</span><span class="sxs-lookup"><span data-stu-id="d285f-117">Specifies the perfect forward secrecy (PFS) group.</span></span>
<span data-ttu-id="d285f-118">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="d285f-118">Valid values are:</span></span> 

- <span data-ttu-id="d285f-119">PFS1</span><span class="sxs-lookup"><span data-stu-id="d285f-119">PFS1</span></span> 
- <span data-ttu-id="d285f-120">Keine</span><span class="sxs-lookup"><span data-stu-id="d285f-120">None</span></span>

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

### <span data-ttu-id="d285f-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="d285f-121">-Profile</span></span>
<span data-ttu-id="d285f-122">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="d285f-122">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d285f-123">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="d285f-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d285f-124">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="d285f-124">-SADataSizeKilobytes</span></span>
<span data-ttu-id="d285f-125">Gibt die Größe der Sicherheitszuordnung (SA) in Kilobyte an.</span><span class="sxs-lookup"><span data-stu-id="d285f-125">Specifies the size, in kilobytes, of the security association (SA).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d285f-126">-SALifetimeSeconds</span><span class="sxs-lookup"><span data-stu-id="d285f-126">-SALifetimeSeconds</span></span>
<span data-ttu-id="d285f-127">Gibt den Zeitraum (in Sekunden) der Sicherheitszuordnung an.</span><span class="sxs-lookup"><span data-stu-id="d285f-127">Specifies the period, in seconds, of the security association.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d285f-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="d285f-128">-VNetName</span></span>
<span data-ttu-id="d285f-129">Gibt das virtuelle Netzwerk an, für das dieses Cmdlet IPSec-Parameter für die Verbindung festlegt.</span><span class="sxs-lookup"><span data-stu-id="d285f-129">Specifies the virtual network for which this cmdlet sets IPsec parameters for the connection.</span></span>

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

### <span data-ttu-id="d285f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d285f-130">CommonParameters</span></span>
<span data-ttu-id="d285f-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d285f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d285f-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d285f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d285f-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d285f-133">INPUTS</span></span>

## <span data-ttu-id="d285f-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d285f-134">OUTPUTS</span></span>

## <span data-ttu-id="d285f-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="d285f-135">NOTES</span></span>

## <span data-ttu-id="d285f-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d285f-136">RELATED LINKS</span></span>

[<span data-ttu-id="d285f-137">Get-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="d285f-137">Get-AzureVNetGatewayIPsecParameters</span></span>](./Get-AzureVNetGatewayIPsecParameters.md)


