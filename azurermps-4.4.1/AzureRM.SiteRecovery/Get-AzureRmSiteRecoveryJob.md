---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B5CA6FD9-49EE-4115-8477-551CE5D8E6CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 2365b806bd274bb9cc18f84c83a29423408780d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662607"
---
# <span data-ttu-id="a5e0c-101">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="a5e0c-101">Get-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="a5e0c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e0c-103">Ruft die Vorgangsinformationen für den aktuellen Standort Wiederherstellungs Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="a5e0c-103">Gets the operation information for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5e0c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5e0c-104">SYNTAX</span></span>

### <span data-ttu-id="a5e0c-105">ByParam (Standard)</span><span class="sxs-lookup"><span data-stu-id="a5e0c-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5e0c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a5e0c-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5e0c-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="a5e0c-107">ByObject</span></span>
```
Get-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5e0c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5e0c-108">DESCRIPTION</span></span>
<span data-ttu-id="a5e0c-109">Das Cmdlet " **Get-AzureRmSiteRecoveryJob** " ruft Azure Site Recovery-Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="a5e0c-109">The **Get-AzureRmSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="a5e0c-110">Sie können dieses Cmdlet verwenden, um die Vorgangsinformationen für das aktuelle Standort Wiederherstellungs Depot anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a5e0c-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="a5e0c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5e0c-111">EXAMPLES</span></span>

## <span data-ttu-id="a5e0c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5e0c-112">PARAMETERS</span></span>

### <span data-ttu-id="a5e0c-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="a5e0c-113">-EndTime</span></span>
<span data-ttu-id="a5e0c-114">Gibt die Endzeit für die Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="a5e0c-114">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="a5e0c-115">Dieses Cmdlet ruft alle Aufträge ab, die vor der angegebenen Zeit gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="a5e0c-115">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="a5e0c-116">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt für diesen Parameter abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a5e0c-116">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="a5e0c-117">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="a5e0c-117">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e0c-118">-Job</span><span class="sxs-lookup"><span data-stu-id="a5e0c-118">-Job</span></span>
<span data-ttu-id="a5e0c-119">Gibt den Standort Wiederherstellungsauftrag an.</span><span class="sxs-lookup"><span data-stu-id="a5e0c-119">Specifies the Site Recovery job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5e0c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a5e0c-120">-Name</span></span>
<span data-ttu-id="a5e0c-121">Gibt einen eindeutigen Namen an, der den Auftrag identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a5e0c-121">Specifies a unique name that identifies the job.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e0c-122">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="a5e0c-122">-StartTime</span></span>
<span data-ttu-id="a5e0c-123">Gibt die Startzeit für die Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="a5e0c-123">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="a5e0c-124">Dieses Cmdlet ruft alle Aufträge ab, die nach der angegebenen Zeit gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="a5e0c-124">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e0c-125">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="a5e0c-125">-State</span></span>
<span data-ttu-id="a5e0c-126">Gibt den Eingabestatus für einen Standort Wiederherstellungsauftrag an.</span><span class="sxs-lookup"><span data-stu-id="a5e0c-126">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="a5e0c-127">Dieses Cmdlet ruft alle Aufträge ab, die dem angegebenen Zustand entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a5e0c-127">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="a5e0c-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a5e0c-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a5e0c-129">NotStarted</span><span class="sxs-lookup"><span data-stu-id="a5e0c-129">NotStarted</span></span>
- <span data-ttu-id="a5e0c-130">InProgress</span><span class="sxs-lookup"><span data-stu-id="a5e0c-130">InProgress</span></span>
- <span data-ttu-id="a5e0c-131">Erfolgreich</span><span class="sxs-lookup"><span data-stu-id="a5e0c-131">Succeeded</span></span>
- <span data-ttu-id="a5e0c-132">Anderen</span><span class="sxs-lookup"><span data-stu-id="a5e0c-132">Other</span></span>
- <span data-ttu-id="a5e0c-133">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="a5e0c-133">Failed</span></span>
- <span data-ttu-id="a5e0c-134">Storniert</span><span class="sxs-lookup"><span data-stu-id="a5e0c-134">Cancelled</span></span>
- <span data-ttu-id="a5e0c-135">Ausgesetzt</span><span class="sxs-lookup"><span data-stu-id="a5e0c-135">Suspended</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases: 
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e0c-136">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="a5e0c-136">-TargetObjectId</span></span>
<span data-ttu-id="a5e0c-137">Gibt die ID des Objekts an, das für den Auftrag vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="a5e0c-137">Specifies the ID of the object targeted by the job.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e0c-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e0c-138">-DefaultProfile</span></span>
<span data-ttu-id="a5e0c-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a5e0c-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e0c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e0c-140">CommonParameters</span></span>
<span data-ttu-id="a5e0c-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5e0c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e0c-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5e0c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e0c-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5e0c-143">INPUTS</span></span>

### <span data-ttu-id="a5e0c-144">ASRJob</span><span class="sxs-lookup"><span data-stu-id="a5e0c-144">ASRJob</span></span>
<span data-ttu-id="a5e0c-145">Der Parameter ' Job ' akzeptiert den Wert vom Typ ' ASRJob ' aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a5e0c-145">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="a5e0c-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5e0c-146">OUTPUTS</span></span>

### <span data-ttu-id="a5e0c-147">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRJob]</span><span class="sxs-lookup"><span data-stu-id="a5e0c-147">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRJob]</span></span>

## <span data-ttu-id="a5e0c-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5e0c-148">NOTES</span></span>

## <span data-ttu-id="a5e0c-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5e0c-149">RELATED LINKS</span></span>

[<span data-ttu-id="a5e0c-150">Neustart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="a5e0c-150">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="a5e0c-151">Lebenslauf-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="a5e0c-151">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="a5e0c-152">Stopp-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="a5e0c-152">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
