---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: E214AFEB-90A6-4553-94D4-FBEA6ADE572E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ee340c2302670628bb8a3893567d7f8a2da754f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006646"
---
# <span data-ttu-id="3d068-101">Resume-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="3d068-101">Resume-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="3d068-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d068-102">SYNOPSIS</span></span>
<span data-ttu-id="3d068-103">Setzt einen angehaltene Website Wiederherstellungsauftrag fort.</span><span class="sxs-lookup"><span data-stu-id="3d068-103">Resumes a suspended Site Recovery job.</span></span>

## <span data-ttu-id="3d068-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d068-104">SYNTAX</span></span>

### <span data-ttu-id="3d068-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="3d068-105">ByObject (Default)</span></span>
```
Resume-AzureSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3d068-106">ById</span><span class="sxs-lookup"><span data-stu-id="3d068-106">ById</span></span>
```
Resume-AzureSiteRecoveryJob -Id <String> [-Comments <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3d068-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d068-107">DESCRIPTION</span></span>
<span data-ttu-id="3d068-108">Mit dem Cmdlet **Resume-AzureSiteRecoveryJob** wird ein angehaltene Azure Site Recovery-Auftrag fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="3d068-108">The **Resume-AzureSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="3d068-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d068-109">EXAMPLES</span></span>

### <span data-ttu-id="3d068-110">Beispiel 1: Fortsetzen aller Aufträge</span><span class="sxs-lookup"><span data-stu-id="3d068-110">Example 1: Resume all jobs</span></span>
```
PS C:\> $Jobs = Get-AzureSiteRecoveryJob  
PS C:\> Resume-AzureSiteRecoveryJob -Job $Jobs
ID               : d16397fb-cdf1-4972-b677-c333f3c557b4
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : Suspended
StateDescription : WaitingForManualAction
StartTime        : 10/6/2014 10:19:28 AM
EndTime          : 10/6/2014 10:19:31 AM
AllowedActions   : {Cancel, RestartTestFailoverCleanup}
Name             : Test failover
Tasks            : {Recovery plan preflight checks, Create test environment, All groups failover: Pre steps (1), 
                   Recovery plan failover...} 
Errors           : {}
```

<span data-ttu-id="3d068-111">Der erste Befehl ruft alle Azure Site Recovery-Aufträge für den aktuellen Standort Wiederherstellungs Speicher mit dem Cmdlet **Get-AzureSiteRecoveryJob** ab und speichert die Ergebnisse dann in der $Jobs Variablen.</span><span class="sxs-lookup"><span data-stu-id="3d068-111">The first command gets all the Azure Site Recovery jobs for the current Site Recovery vault by using the **Get-AzureSiteRecoveryJob** cmdlet, and then stores the results in the $Jobs variable.</span></span>

<span data-ttu-id="3d068-112">Mit dem zweiten Befehl wird der durch $Jobs angegebene Auftrag fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="3d068-112">The second command resumes the job specified by $Jobs.</span></span>

## <span data-ttu-id="3d068-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d068-113">PARAMETERS</span></span>

### <span data-ttu-id="3d068-114">-Kommentare</span><span class="sxs-lookup"><span data-stu-id="3d068-114">-Comments</span></span>
<span data-ttu-id="3d068-115">Gibt die Kommentare für das Auftragsprotokoll an.</span><span class="sxs-lookup"><span data-stu-id="3d068-115">Specifies the comments for the job log.</span></span>

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

### <span data-ttu-id="3d068-116">-ID</span><span class="sxs-lookup"><span data-stu-id="3d068-116">-Id</span></span>
<span data-ttu-id="3d068-117">Gibt die ID eines Auftrags an, der fortgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d068-117">Specifies the ID of a job to resume.</span></span>

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

### <span data-ttu-id="3d068-118">-Job</span><span class="sxs-lookup"><span data-stu-id="3d068-118">-Job</span></span>
<span data-ttu-id="3d068-119">Gibt den Auftrag an, der fortgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d068-119">Specifies the job to resume.</span></span>

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

### <span data-ttu-id="3d068-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="3d068-120">-Profile</span></span>
<span data-ttu-id="3d068-121">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="3d068-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3d068-122">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="3d068-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3d068-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d068-123">CommonParameters</span></span>
<span data-ttu-id="3d068-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d068-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d068-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d068-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d068-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d068-126">INPUTS</span></span>

## <span data-ttu-id="3d068-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d068-127">OUTPUTS</span></span>

## <span data-ttu-id="3d068-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d068-128">NOTES</span></span>

## <span data-ttu-id="3d068-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d068-129">RELATED LINKS</span></span>

[<span data-ttu-id="3d068-130">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="3d068-130">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="3d068-131">Neustart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="3d068-131">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="3d068-132">Stopp-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="3d068-132">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


