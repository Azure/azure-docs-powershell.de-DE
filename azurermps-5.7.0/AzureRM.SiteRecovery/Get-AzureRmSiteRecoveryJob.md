---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B5CA6FD9-49EE-4115-8477-551CE5D8E6CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: dc8a1e6cfe8c3d68af0f8c413a0e96cac9feaee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498781"
---
# <span data-ttu-id="632de-101">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="632de-101">Get-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="632de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="632de-102">SYNOPSIS</span></span>
<span data-ttu-id="632de-103">Ruft die Vorgangsinformationen für den aktuellen Standort Wiederherstellungs Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="632de-103">Gets the operation information for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="632de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="632de-104">SYNTAX</span></span>

### <span data-ttu-id="632de-105">ByParam (Standard)</span><span class="sxs-lookup"><span data-stu-id="632de-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="632de-106">ByName</span><span class="sxs-lookup"><span data-stu-id="632de-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="632de-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="632de-107">ByObject</span></span>
```
Get-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="632de-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="632de-108">DESCRIPTION</span></span>
<span data-ttu-id="632de-109">Das Cmdlet " **Get-AzureRmSiteRecoveryJob** " ruft Azure Site Recovery-Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="632de-109">The **Get-AzureRmSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="632de-110">Sie können dieses Cmdlet verwenden, um die Vorgangsinformationen für das aktuelle Standort Wiederherstellungs Depot anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="632de-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="632de-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="632de-111">EXAMPLES</span></span>

## <span data-ttu-id="632de-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="632de-112">PARAMETERS</span></span>

### <span data-ttu-id="632de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="632de-113">-DefaultProfile</span></span>
<span data-ttu-id="632de-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="632de-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632de-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="632de-115">-EndTime</span></span>
<span data-ttu-id="632de-116">Gibt die Endzeit für die Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="632de-116">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="632de-117">Dieses Cmdlet ruft alle Aufträge ab, die vor der angegebenen Zeit gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="632de-117">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="632de-118">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt für diesen Parameter abzurufen.</span><span class="sxs-lookup"><span data-stu-id="632de-118">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="632de-119">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="632de-119">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632de-120">-Job</span><span class="sxs-lookup"><span data-stu-id="632de-120">-Job</span></span>
<span data-ttu-id="632de-121">Gibt den Standort Wiederherstellungsauftrag an.</span><span class="sxs-lookup"><span data-stu-id="632de-121">Specifies the Site Recovery job.</span></span>

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

### <span data-ttu-id="632de-122">-Name</span><span class="sxs-lookup"><span data-stu-id="632de-122">-Name</span></span>
<span data-ttu-id="632de-123">Gibt einen eindeutigen Namen an, der den Auftrag identifiziert.</span><span class="sxs-lookup"><span data-stu-id="632de-123">Specifies a unique name that identifies the job.</span></span>

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

### <span data-ttu-id="632de-124">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="632de-124">-StartTime</span></span>
<span data-ttu-id="632de-125">Gibt die Startzeit für die Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="632de-125">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="632de-126">Dieses Cmdlet ruft alle Aufträge ab, die nach der angegebenen Zeit gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="632de-126">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632de-127">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="632de-127">-State</span></span>
<span data-ttu-id="632de-128">Gibt den Eingabestatus für einen Standort Wiederherstellungsauftrag an.</span><span class="sxs-lookup"><span data-stu-id="632de-128">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="632de-129">Dieses Cmdlet ruft alle Aufträge ab, die dem angegebenen Zustand entsprechen.</span><span class="sxs-lookup"><span data-stu-id="632de-129">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="632de-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="632de-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="632de-131">NotStarted</span><span class="sxs-lookup"><span data-stu-id="632de-131">NotStarted</span></span>
- <span data-ttu-id="632de-132">InProgress</span><span class="sxs-lookup"><span data-stu-id="632de-132">InProgress</span></span>
- <span data-ttu-id="632de-133">Erfolgreich</span><span class="sxs-lookup"><span data-stu-id="632de-133">Succeeded</span></span>
- <span data-ttu-id="632de-134">Anderen</span><span class="sxs-lookup"><span data-stu-id="632de-134">Other</span></span>
- <span data-ttu-id="632de-135">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="632de-135">Failed</span></span>
- <span data-ttu-id="632de-136">Storniert</span><span class="sxs-lookup"><span data-stu-id="632de-136">Cancelled</span></span>
- <span data-ttu-id="632de-137">Ausgesetzt</span><span class="sxs-lookup"><span data-stu-id="632de-137">Suspended</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632de-138">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="632de-138">-TargetObjectId</span></span>
<span data-ttu-id="632de-139">Gibt die ID des Objekts an, das für den Auftrag vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="632de-139">Specifies the ID of the object targeted by the job.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632de-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="632de-140">CommonParameters</span></span>
<span data-ttu-id="632de-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="632de-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="632de-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="632de-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="632de-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="632de-143">INPUTS</span></span>

### <span data-ttu-id="632de-144">ASRJob</span><span class="sxs-lookup"><span data-stu-id="632de-144">ASRJob</span></span>
<span data-ttu-id="632de-145">Der Parameter ' Job ' akzeptiert den Wert vom Typ ' ASRJob ' aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="632de-145">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="632de-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="632de-146">OUTPUTS</span></span>

### <span data-ttu-id="632de-147">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRJob]</span><span class="sxs-lookup"><span data-stu-id="632de-147">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRJob]</span></span>

## <span data-ttu-id="632de-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="632de-148">NOTES</span></span>

## <span data-ttu-id="632de-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="632de-149">RELATED LINKS</span></span>

[<span data-ttu-id="632de-150">Neustart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="632de-150">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="632de-151">Lebenslauf-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="632de-151">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="632de-152">Stopp-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="632de-152">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
