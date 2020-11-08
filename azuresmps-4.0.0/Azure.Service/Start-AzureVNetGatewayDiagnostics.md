---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9FCECA04-9855-461C-9470-85312993C4B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bb7bb3e708720b481edc4489d858c70736eac95
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006232"
---
# <span data-ttu-id="5a838-101">Start-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="5a838-101">Start-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="5a838-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a838-102">SYNOPSIS</span></span>
<span data-ttu-id="5a838-103">Startet die Gateway-Diagnose für ein VPN-Gateway.</span><span class="sxs-lookup"><span data-stu-id="5a838-103">Starts gateway diagnostics for a VPN gateway.</span></span>

## <span data-ttu-id="5a838-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a838-104">SYNTAX</span></span>

```
Start-AzureVNetGatewayDiagnostics -VNetName <String> -CaptureDurationInSeconds <Int32>
 [-ContainerName <String>] -StorageContext <AzureStorageContext> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a838-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a838-105">DESCRIPTION</span></span>
<span data-ttu-id="5a838-106">Das Cmdlet **Start-AzureVNetGatewayDiagnostics** startet eine neue Gateway-Diagnosesitzung für ein VPN-Gateway (virtuelles privates Netzwerk).</span><span class="sxs-lookup"><span data-stu-id="5a838-106">The **Start-AzureVNetGatewayDiagnostics** cmdlet starts a new gateway diagnostics session for a virtual private network (VPN) gateway.</span></span>
<span data-ttu-id="5a838-107">Es kann immer nur eine Gateway-Diagnosesitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5a838-107">Only one gateway diagnostics session can run at a time.</span></span>
<span data-ttu-id="5a838-108">Wenn Sie dieses Cmdlet ausführen, während eine Gateway-Diagnosesitzung ausgeführt wird, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="5a838-108">If you run this cmdlet while a gateway diagnostics session is running, this cmdlet returns an error.</span></span>

## <span data-ttu-id="5a838-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a838-109">EXAMPLES</span></span>

## <span data-ttu-id="5a838-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a838-110">PARAMETERS</span></span>

### <span data-ttu-id="5a838-111">-CaptureDurationInSeconds</span><span class="sxs-lookup"><span data-stu-id="5a838-111">-CaptureDurationInSeconds</span></span>
<span data-ttu-id="5a838-112">Gibt die Aufnahmedauer in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="5a838-112">Specifies the capture duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a838-113">-Containername</span><span class="sxs-lookup"><span data-stu-id="5a838-113">-ContainerName</span></span>
<span data-ttu-id="5a838-114">Gibt den Namen eines Azure-Containers an.</span><span class="sxs-lookup"><span data-stu-id="5a838-114">Specifies the name of an Azure container.</span></span>
<span data-ttu-id="5a838-115">Dieses Cmdlet speichert Ergebnisse in dem Container, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5a838-115">This cmdlet stores results in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="5a838-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="5a838-116">-Profile</span></span>
<span data-ttu-id="5a838-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="5a838-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="5a838-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="5a838-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5a838-119">-Storagecontext</span><span class="sxs-lookup"><span data-stu-id="5a838-119">-StorageContext</span></span>
<span data-ttu-id="5a838-120">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="5a838-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5a838-121">Dieses Cmdlet speichert Ergebnisse unter Verwendung des Speicher Kontexts, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5a838-121">This cmdlet stores results by using the storage context that this parameter specifies.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a838-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="5a838-122">-VNetName</span></span>
<span data-ttu-id="5a838-123">Gibt das virtuelle Netzwerk an, das ein virtuelles Netzwerkgateway enthält, für das dieses Cmdlet eine Diagnose ausführt.</span><span class="sxs-lookup"><span data-stu-id="5a838-123">Specifies the virtual network that contains a virtual network gateway for which this cmdlet runs diagnostics.</span></span>

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

### <span data-ttu-id="5a838-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a838-124">CommonParameters</span></span>
<span data-ttu-id="5a838-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a838-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a838-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a838-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a838-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a838-127">INPUTS</span></span>

## <span data-ttu-id="5a838-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a838-128">OUTPUTS</span></span>

## <span data-ttu-id="5a838-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a838-129">NOTES</span></span>

## <span data-ttu-id="5a838-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a838-130">RELATED LINKS</span></span>

[<span data-ttu-id="5a838-131">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="5a838-131">Get-AzureVNetGatewayDiagnostics</span></span>](./Get-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="5a838-132">Stopp-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="5a838-132">Stop-AzureVNetGatewayDiagnostics</span></span>](./Stop-AzureVNetGatewayDiagnostics.md)


