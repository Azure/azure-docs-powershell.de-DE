---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 615D2C5D-AB31-45DB-9535-9B9C8E957322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a5701fc6308f1884bbf0237887a223a62a58669
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411584"
---
# <span data-ttu-id="6ee02-101">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="6ee02-101">Get-AzureSiteRecoveryNetwork</span></span>

## <span data-ttu-id="6ee02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ee02-102">SYNOPSIS</span></span>
<span data-ttu-id="6ee02-103">Ruft Informationen zu den Netzwerken ab, die von der Websitewiederherstellung für den aktuellen Tresor verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="6ee02-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="6ee02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ee02-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryNetwork -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6ee02-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ee02-105">DESCRIPTION</span></span>
<span data-ttu-id="6ee02-106">Das **Cmdlet "Get-AzureSiteRecoveryNetwork"** ruft Informationen zu Azure Site Recovery Networks für den aktuellen Websitewiederherstellungstresor ab.</span><span class="sxs-lookup"><span data-stu-id="6ee02-106">The **Get-AzureSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Site Recovery vault.</span></span>

## <span data-ttu-id="6ee02-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6ee02-107">EXAMPLES</span></span>

### <span data-ttu-id="6ee02-108">Beispiel 1: Websitewiederherstellungsnetzwerke erhalten</span><span class="sxs-lookup"><span data-stu-id="6ee02-108">Example 1: Get site recovery networks</span></span>
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

<span data-ttu-id="6ee02-109">Das erste Befehls-Cmdlet ruft Mithilfe des **Cmdlets "Get-AzureSiteRecoveryServer"** Server für den aktuellen Azure Site Recovery Vault ab.</span><span class="sxs-lookup"><span data-stu-id="6ee02-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="6ee02-110">Der Befehl speichert die Websitewiederherstellungsserver in $Servers Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="6ee02-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="6ee02-111">Der zweite Befehl ruft das Websitewiederherstellungsnetzwerk für den ersten Server im Array $Servers ab.</span><span class="sxs-lookup"><span data-stu-id="6ee02-111">The second command gets the site recovery network for the first server in the $Servers array.</span></span>

## <span data-ttu-id="6ee02-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ee02-112">PARAMETERS</span></span>

### <span data-ttu-id="6ee02-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="6ee02-113">-Profile</span></span>
<span data-ttu-id="6ee02-114">Gibt das Azure-Profil an, aus dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="6ee02-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6ee02-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="6ee02-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6ee02-116">-Server</span><span class="sxs-lookup"><span data-stu-id="6ee02-116">-Server</span></span>
<span data-ttu-id="6ee02-117">Gibt einen Websitewiederherstellungsserver an.</span><span class="sxs-lookup"><span data-stu-id="6ee02-117">Specifies a Site Recovery server.</span></span>

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

### <span data-ttu-id="6ee02-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ee02-118">CommonParameters</span></span>
<span data-ttu-id="6ee02-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ee02-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ee02-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ee02-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ee02-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6ee02-121">INPUTS</span></span>

## <span data-ttu-id="6ee02-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6ee02-122">OUTPUTS</span></span>

## <span data-ttu-id="6ee02-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6ee02-123">NOTES</span></span>

## <span data-ttu-id="6ee02-124">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6ee02-124">RELATED LINKS</span></span>




