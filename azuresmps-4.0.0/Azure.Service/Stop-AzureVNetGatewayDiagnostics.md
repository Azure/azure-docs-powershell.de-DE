---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 706CBF65-C796-4525-BAEB-AAFAD44C0464
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37c2ce3b32d23f7c5bb682d2116de84cc90f047
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006225"
---
# <span data-ttu-id="1e422-101">Stop-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1e422-101">Stop-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="1e422-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e422-102">SYNOPSIS</span></span>
<span data-ttu-id="1e422-103">Beendet eine ausgeführte VPN-Gateway-Diagnosesitzung.</span><span class="sxs-lookup"><span data-stu-id="1e422-103">Stops a running VPN gateway diagnostics session.</span></span>

## <span data-ttu-id="1e422-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e422-104">SYNTAX</span></span>

```
Stop-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1e422-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e422-105">DESCRIPTION</span></span>
<span data-ttu-id="1e422-106">Das Cmdlet **Stop-AzureVNetGatewayDiagnostics** beendet eine ausgeführte VPN-Gateway-Diagnosesitzung (virtuelles privates Netzwerk).</span><span class="sxs-lookup"><span data-stu-id="1e422-106">The **Stop-AzureVNetGatewayDiagnostics** cmdlet stops a running virtual private network (VPN) gateway diagnostics session.</span></span>
<span data-ttu-id="1e422-107">Dieser Befehl speichert die Ergebnisse der Diagnosesitzung auf dem Speicherkonto, das vom Cmdlet **Start-AzureVNetGatewayDiagnostics** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1e422-107">This command saves the results of the diagnostics session to the storage account that the **Start-AzureVNetGatewayDiagnostics** cmdlet specifies.</span></span>

## <span data-ttu-id="1e422-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e422-108">EXAMPLES</span></span>

## <span data-ttu-id="1e422-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e422-109">PARAMETERS</span></span>

### <span data-ttu-id="1e422-110">-Profil</span><span class="sxs-lookup"><span data-stu-id="1e422-110">-Profile</span></span>
<span data-ttu-id="1e422-111">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="1e422-111">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1e422-112">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="1e422-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1e422-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="1e422-113">-VNetName</span></span>
<span data-ttu-id="1e422-114">Gibt das virtuelle Netzwerk an, das ein virtuelles Netzwerkgateway enthält, für das dieses Cmdlet die Diagnose beendet.</span><span class="sxs-lookup"><span data-stu-id="1e422-114">Specifies the virtual network that contains a virtual network gateway for which this cmdlet stops diagnostics.</span></span>

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

### <span data-ttu-id="1e422-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e422-115">CommonParameters</span></span>
<span data-ttu-id="1e422-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e422-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e422-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e422-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e422-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e422-118">INPUTS</span></span>

## <span data-ttu-id="1e422-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e422-119">OUTPUTS</span></span>

## <span data-ttu-id="1e422-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e422-120">NOTES</span></span>

## <span data-ttu-id="1e422-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e422-121">RELATED LINKS</span></span>

[<span data-ttu-id="1e422-122">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1e422-122">Get-AzureVNetGatewayDiagnostics</span></span>](./Get-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="1e422-123">Anfang-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1e422-123">Start-AzureVNetGatewayDiagnostics</span></span>](./Start-AzureVNetGatewayDiagnostics.md)


