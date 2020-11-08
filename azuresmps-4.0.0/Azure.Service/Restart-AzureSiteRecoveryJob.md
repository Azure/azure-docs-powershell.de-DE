---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AE26EA0F-9D92-4FDF-92EF-CA33BF06C0DB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68a97359e5181bbc27183c0c1dbb6f526fa2e529
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006282"
---
# <span data-ttu-id="318f7-101">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="318f7-101">Restart-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="318f7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="318f7-102">SYNOPSIS</span></span>
<span data-ttu-id="318f7-103">Startet einen Standort Wiederherstellungsauftrag neu.</span><span class="sxs-lookup"><span data-stu-id="318f7-103">Restarts a Site Recovery job.</span></span>

## <span data-ttu-id="318f7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="318f7-104">SYNTAX</span></span>

### <span data-ttu-id="318f7-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="318f7-105">ByObject (Default)</span></span>
```
Restart-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="318f7-106">ById</span><span class="sxs-lookup"><span data-stu-id="318f7-106">ById</span></span>
```
Restart-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="318f7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="318f7-107">DESCRIPTION</span></span>
<span data-ttu-id="318f7-108">Mit dem Cmdlet " **Restart-AzureSiteRecoveryJob** " wird ein Azure Site Recovery-Auftrag neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="318f7-108">The **Restart-AzureSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="318f7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="318f7-109">EXAMPLES</span></span>

### <span data-ttu-id="318f7-110">Beispiel 1: einen Auftrag neu starten</span><span class="sxs-lookup"><span data-stu-id="318f7-110">Example 1: Restart a job</span></span>
```
PS C:\> Restart-AzureSiteRecoveryJob -Id "bbf0b839-9aaa-49e1-8354-601c9145966d"
ID               : bbf0b839-9aaa-49e1-8354-601c9145966d
ClientRequestId  : ef42c8b0-640c-4442-960b-349f83d161a5-2014-24-06 14:24:04Z-P
State            : Failed
StateDescription : Failed
StartTime        : 10/6/2014 9:41:08 AM
EndTime          : 10/6/2014 9:41:21 AM
AllowedActions   : {Cancel, Restart}
Name             : Enable protection
Tasks            : {Prerequisites check for enabling protection , Identifying replication target, Enable replication, 
                   Starting initial replication...} 
Errors           : {CreateProtectionTargetTask}
```

<span data-ttu-id="318f7-111">Mit diesem Befehl wird der Auftrag mit der angegebenen ID neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="318f7-111">This command restarts the job that has the specified ID.</span></span>

## <span data-ttu-id="318f7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="318f7-112">PARAMETERS</span></span>

### <span data-ttu-id="318f7-113">-ID</span><span class="sxs-lookup"><span data-stu-id="318f7-113">-Id</span></span>
<span data-ttu-id="318f7-114">Gibt die ID des Auftrags an, der neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="318f7-114">Specifies the ID of the job to restart.</span></span>

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

### <span data-ttu-id="318f7-115">-Job</span><span class="sxs-lookup"><span data-stu-id="318f7-115">-Job</span></span>
<span data-ttu-id="318f7-116">Gibt den Auftrag an, der neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="318f7-116">Specifies the job to restart.</span></span>

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

### <span data-ttu-id="318f7-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="318f7-117">-Profile</span></span>
<span data-ttu-id="318f7-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="318f7-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="318f7-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="318f7-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="318f7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="318f7-120">CommonParameters</span></span>
<span data-ttu-id="318f7-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="318f7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="318f7-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="318f7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="318f7-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="318f7-123">INPUTS</span></span>

## <span data-ttu-id="318f7-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="318f7-124">OUTPUTS</span></span>

## <span data-ttu-id="318f7-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="318f7-125">NOTES</span></span>

## <span data-ttu-id="318f7-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="318f7-126">RELATED LINKS</span></span>

[<span data-ttu-id="318f7-127">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="318f7-127">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="318f7-128">Lebenslauf-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="318f7-128">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="318f7-129">Stopp-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="318f7-129">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


