---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 615D2C5D-AB31-45DB-9535-9B9C8E957322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 96b51b49d76093be96eeab26417f4a70f70c4627
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005798"
---
# <span data-ttu-id="b6d90-101">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="b6d90-101">Get-AzureSiteRecoveryNetwork</span></span>

## <span data-ttu-id="b6d90-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b6d90-102">SYNOPSIS</span></span>
<span data-ttu-id="b6d90-103">Ruft Informationen zu den Netzwerken ab, die von der Websitewiederherstellung für den aktuellen Tresor verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="b6d90-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="b6d90-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6d90-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryNetwork -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b6d90-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6d90-105">DESCRIPTION</span></span>
<span data-ttu-id="b6d90-106">Das Cmdlet " **Get-AzureSiteRecoveryNetwork** " Ruft Informationen zu Azure Site Recovery Networks für das aktuelle Standort Wiederherstellungs Depot ab.</span><span class="sxs-lookup"><span data-stu-id="b6d90-106">The **Get-AzureSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Site Recovery vault.</span></span>

## <span data-ttu-id="b6d90-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6d90-107">EXAMPLES</span></span>

### <span data-ttu-id="b6d90-108">Beispiel 1: Abrufen von Website Wiederherstellungs Netzwerken</span><span class="sxs-lookup"><span data-stu-id="b6d90-108">Example 1: Get site recovery networks</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetwork -Server $Servers[0]
Name                : phase2RecoveryVMNetwork
ID                  : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
FabricObjectID      : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}

Name                : phase2PrimaryVMNetwork
ID                  : d903e2c6-3141-4cef-bfe1-04616cd43cbb
FabricObjectID      : d903e2c6-3141-4cef-bfe1-04616cd43cbb
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}
```

<span data-ttu-id="b6d90-109">Das Cmdlet "erster Befehl" Ruft Server für das aktuelle Azure Site Recovery Vault mit dem Cmdlet **Get-AzureSiteRecoveryServer** ab.</span><span class="sxs-lookup"><span data-stu-id="b6d90-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="b6d90-110">Der Befehl speichert die Website Wiederherstellungsserver in der $Servers-Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="b6d90-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="b6d90-111">Der zweite Befehl ruft das Standort Wiederherstellungs Netzwerk für den ersten Server im $Servers-Array ab.</span><span class="sxs-lookup"><span data-stu-id="b6d90-111">The second command gets the site recovery network for the first server in the $Servers array.</span></span>

## <span data-ttu-id="b6d90-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6d90-112">PARAMETERS</span></span>

### <span data-ttu-id="b6d90-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="b6d90-113">-Profile</span></span>
<span data-ttu-id="b6d90-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b6d90-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b6d90-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b6d90-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b6d90-116">-Server</span><span class="sxs-lookup"><span data-stu-id="b6d90-116">-Server</span></span>
<span data-ttu-id="b6d90-117">Gibt einen Standort Wiederherstellungsserver an.</span><span class="sxs-lookup"><span data-stu-id="b6d90-117">Specifies a Site Recovery server.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6d90-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6d90-118">CommonParameters</span></span>
<span data-ttu-id="b6d90-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6d90-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6d90-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6d90-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6d90-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b6d90-121">INPUTS</span></span>

## <span data-ttu-id="b6d90-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b6d90-122">OUTPUTS</span></span>

## <span data-ttu-id="b6d90-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="b6d90-123">NOTES</span></span>

## <span data-ttu-id="b6d90-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b6d90-124">RELATED LINKS</span></span>

[<span data-ttu-id="b6d90-125">Azure Site Recovery Services-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="b6d90-125">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


