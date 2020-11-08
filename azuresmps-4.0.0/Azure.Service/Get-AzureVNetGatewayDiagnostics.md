---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 22E8CB18-8CDD-4992-AB81-E1BB400E6BC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 294e931529b7de939a6a5c20181d48b18da1e892
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006483"
---
# <span data-ttu-id="34cd3-101">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="34cd3-101">Get-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="34cd3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="34cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="34cd3-103">Ruft den aktuellen Status der Diagnose für ein virtuelles Netzwerkgateway ab.</span><span class="sxs-lookup"><span data-stu-id="34cd3-103">Gets the current state of diagnostics for a virtual network gateway.</span></span>

## <span data-ttu-id="34cd3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="34cd3-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="34cd3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34cd3-105">DESCRIPTION</span></span>
<span data-ttu-id="34cd3-106">Das Cmdlet " **Get-AzureVNetGatewayDiagnostics** " Ruft den aktuellen Status der Diagnose für ein virtuelles Netzwerkgateway ab.</span><span class="sxs-lookup"><span data-stu-id="34cd3-106">The **Get-AzureVNetGatewayDiagnostics** cmdlet gets the current state of diagnostics for a virtual network gateway.</span></span>
<span data-ttu-id="34cd3-107">Wenn ein BLOB (Binary Large Object) vorhanden ist, in dem die **Start-AzureVNetGatewayDiagnostics** eine vorherige Diagnosesitzung gespeichert haben, gibt dieses Cmdlet auch die URL des BLOB zurück, in dem dieses Cmdlet diese Diagnosesitzung gespeichert hat.</span><span class="sxs-lookup"><span data-stu-id="34cd3-107">If a binary large object (blob) exists where the **Start-AzureVNetGatewayDiagnostics** saved a previous diagnostics session, this cmdlet also returns the URL of the blob where that cmdlet saved that diagnostics session.</span></span>

## <span data-ttu-id="34cd3-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34cd3-108">EXAMPLES</span></span>

## <span data-ttu-id="34cd3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="34cd3-109">PARAMETERS</span></span>

### <span data-ttu-id="34cd3-110">-Profil</span><span class="sxs-lookup"><span data-stu-id="34cd3-110">-Profile</span></span>
<span data-ttu-id="34cd3-111">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="34cd3-111">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="34cd3-112">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="34cd3-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="34cd3-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="34cd3-113">-VNetName</span></span>
<span data-ttu-id="34cd3-114">Gibt das virtuelle Netzwerk an, das ein virtuelles Netzwerkgateway enthält, für das dieses Cmdlet Diagnosen erhält.</span><span class="sxs-lookup"><span data-stu-id="34cd3-114">Specifies the virtual network that contains a virtual network gateway for which this cmdlet gets diagnostics.</span></span>

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

### <span data-ttu-id="34cd3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34cd3-115">CommonParameters</span></span>
<span data-ttu-id="34cd3-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34cd3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34cd3-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34cd3-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34cd3-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="34cd3-118">INPUTS</span></span>

## <span data-ttu-id="34cd3-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="34cd3-119">OUTPUTS</span></span>

## <span data-ttu-id="34cd3-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="34cd3-120">NOTES</span></span>

## <span data-ttu-id="34cd3-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="34cd3-121">RELATED LINKS</span></span>

[<span data-ttu-id="34cd3-122">Anfang-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="34cd3-122">Start-AzureVNetGatewayDiagnostics</span></span>](./Start-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="34cd3-123">Stopp-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="34cd3-123">Stop-AzureVNetGatewayDiagnostics</span></span>](./Stop-AzureVNetGatewayDiagnostics.md)


