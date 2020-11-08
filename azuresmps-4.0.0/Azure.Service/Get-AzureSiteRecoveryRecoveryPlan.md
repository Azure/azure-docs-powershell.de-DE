---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8557B04E-DE35-473E-8F5D-B72B70300AA6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1949d30d6bbea16e1626954bf241df36d81533e1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005791"
---
# <span data-ttu-id="c3fb0-101">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c3fb0-101">Get-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="c3fb0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3fb0-102">SYNOPSIS</span></span>
<span data-ttu-id="c3fb0-103">Ruft einen Wiederherstellungsplan in der Websitewiederherstellung ab.</span><span class="sxs-lookup"><span data-stu-id="c3fb0-103">Gets a recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="c3fb0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3fb0-104">SYNTAX</span></span>

### <span data-ttu-id="c3fb0-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3fb0-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c3fb0-106">ById</span><span class="sxs-lookup"><span data-stu-id="c3fb0-106">ById</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c3fb0-107">ByName</span><span class="sxs-lookup"><span data-stu-id="c3fb0-107">ByName</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c3fb0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3fb0-108">DESCRIPTION</span></span>
<span data-ttu-id="c3fb0-109">Das Cmdlet " **Get-AzureSiteRecoveryRecoveryPlan** " Ruft einen Wiederherstellungsplan in Azure Site Recovery ab.</span><span class="sxs-lookup"><span data-stu-id="c3fb0-109">The **Get-AzureSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="c3fb0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3fb0-110">EXAMPLES</span></span>

### <span data-ttu-id="c3fb0-111">Beispiel 1: Abrufen eines Wiederherstellungsplans</span><span class="sxs-lookup"><span data-stu-id="c3fb0-111">Example 1: Get a recovery plan</span></span>
```
PS C:\> Get-AzureSiteRecoveryRecoveryPlan
ID                            Name                          ServerId                      TargetServerId
--                            ----                          --------                      --------------
71de8ebc-1e9a-4242-aec3-ee... ContosoPlan                   4a94c4a9-c856-4577-afbd-36... 78facf56-b273-4941-82fd-cc...
```

<span data-ttu-id="c3fb0-112">Dieser Befehl ruft Informationen zum Wiederherstellungsplan für das aktuelle Azure Site Recovery Vault ab.</span><span class="sxs-lookup"><span data-stu-id="c3fb0-112">This command gets information about the recovery plan for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="c3fb0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3fb0-113">PARAMETERS</span></span>

### <span data-ttu-id="c3fb0-114">-ID</span><span class="sxs-lookup"><span data-stu-id="c3fb0-114">-Id</span></span>
<span data-ttu-id="c3fb0-115">Gibt die ID des abzurufenden Wiederherstellungsplans an.</span><span class="sxs-lookup"><span data-stu-id="c3fb0-115">Specifies the ID of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3fb0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c3fb0-116">-Name</span></span>
<span data-ttu-id="c3fb0-117">Gibt den Namen des abzurufenden Wiederherstellungsplans an.</span><span class="sxs-lookup"><span data-stu-id="c3fb0-117">Specifies the name of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3fb0-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="c3fb0-118">-Profile</span></span>
<span data-ttu-id="c3fb0-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c3fb0-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c3fb0-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c3fb0-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c3fb0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3fb0-121">CommonParameters</span></span>
<span data-ttu-id="c3fb0-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3fb0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3fb0-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3fb0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3fb0-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3fb0-124">INPUTS</span></span>

## <span data-ttu-id="c3fb0-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3fb0-125">OUTPUTS</span></span>

## <span data-ttu-id="c3fb0-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3fb0-126">NOTES</span></span>

## <span data-ttu-id="c3fb0-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3fb0-127">RELATED LINKS</span></span>

[<span data-ttu-id="c3fb0-128">Neu – AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c3fb0-128">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="c3fb0-129">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c3fb0-129">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="c3fb0-130">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c3fb0-130">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


