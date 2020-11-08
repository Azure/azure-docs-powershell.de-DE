---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8FF1362B-C7AB-4769-A88B-D1B6E214A006
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf8275b8dfec4263c5ab7a8022dcb65edccb1171
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006613"
---
# <span data-ttu-id="29331-101">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="29331-101">Stop-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="29331-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29331-102">SYNOPSIS</span></span>
<span data-ttu-id="29331-103">Beendet einen Wiederherstellungsauftrag für die Website.</span><span class="sxs-lookup"><span data-stu-id="29331-103">Stops a Site Recovery job.</span></span>

## <span data-ttu-id="29331-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29331-104">SYNTAX</span></span>

### <span data-ttu-id="29331-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="29331-105">ByObject (Default)</span></span>
```
Stop-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="29331-106">ById</span><span class="sxs-lookup"><span data-stu-id="29331-106">ById</span></span>
```
Stop-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="29331-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29331-107">DESCRIPTION</span></span>
<span data-ttu-id="29331-108">Das Cmdlet " **Stop-AzureSiteRecoveryJob** " beendet einen Azure Site Recovery-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="29331-108">The **Stop-AzureSiteRecoveryJob** cmdlet stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="29331-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29331-109">EXAMPLES</span></span>

### <span data-ttu-id="29331-110">Beispiel 1: Beenden aller Aufträge</span><span class="sxs-lookup"><span data-stu-id="29331-110">Example 1: Stop all jobs</span></span>
```
PS C:\>$Jobs = Get-AzureSiteRecoveryJob 
PS C:\> Stop-AzureSiteRecoveryJob -Job $Jobs
```

<span data-ttu-id="29331-111">Der erste Befehl ruft die Azure Site Recovery-Aufträge für das aktuelle Azure Site Recovery Vault mit dem Cmdlet **Get-AzureSiteRecoveryJob** ab und speichert die Ergebnisse dann in der $Jobs-Variablen.</span><span class="sxs-lookup"><span data-stu-id="29331-111">The first command gets the Azure Site Recovery jobs for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryJob** cmdlet, and then stores the results in the $Jobs variable.</span></span>

<span data-ttu-id="29331-112">Mit dem zweiten Befehl werden die von $Jobs angegebenen Aufträge angehalten.</span><span class="sxs-lookup"><span data-stu-id="29331-112">The second command stops the jobs specified by $Jobs.</span></span>

## <span data-ttu-id="29331-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="29331-113">PARAMETERS</span></span>

### <span data-ttu-id="29331-114">-ID</span><span class="sxs-lookup"><span data-stu-id="29331-114">-Id</span></span>
<span data-ttu-id="29331-115">Gibt die ID des Auftrags an, der beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="29331-115">Specifies the ID of the job to stop.</span></span>

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

### <span data-ttu-id="29331-116">-Job</span><span class="sxs-lookup"><span data-stu-id="29331-116">-Job</span></span>
<span data-ttu-id="29331-117">Gibt den Auftrag an, der beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="29331-117">Specifies the job to stop.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29331-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="29331-118">-Profile</span></span>
<span data-ttu-id="29331-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="29331-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="29331-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="29331-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="29331-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29331-121">CommonParameters</span></span>
<span data-ttu-id="29331-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29331-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29331-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29331-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29331-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29331-124">INPUTS</span></span>

## <span data-ttu-id="29331-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29331-125">OUTPUTS</span></span>

## <span data-ttu-id="29331-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="29331-126">NOTES</span></span>

## <span data-ttu-id="29331-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29331-127">RELATED LINKS</span></span>

[<span data-ttu-id="29331-128">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="29331-128">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="29331-129">Neustart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="29331-129">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="29331-130">Lebenslauf-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="29331-130">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)


