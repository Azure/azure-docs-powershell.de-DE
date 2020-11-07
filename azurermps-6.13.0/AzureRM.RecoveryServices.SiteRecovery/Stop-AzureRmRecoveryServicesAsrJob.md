---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/stop-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 14f24f9b9659b6668041b800462eca422fb67c97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662304"
---
# <span data-ttu-id="58567-101">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="58567-101">Stop-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="58567-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="58567-102">SYNOPSIS</span></span>
<span data-ttu-id="58567-103">Beendet einen Azure Site Recovery-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="58567-103">Stops an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58567-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="58567-104">SYNTAX</span></span>

### <span data-ttu-id="58567-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="58567-105">ByObject (Default)</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58567-106">ByName</span><span class="sxs-lookup"><span data-stu-id="58567-106">ByName</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58567-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58567-107">DESCRIPTION</span></span>
<span data-ttu-id="58567-108">Das Cmdlet **Stop-AzureRmRecoveryServicesAsrJob** beendet den angegebenen Azure Site Recovery-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="58567-108">The **Stop-AzureRmRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="58567-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="58567-109">EXAMPLES</span></span>

### <span data-ttu-id="58567-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="58567-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="58567-111">Versucht, den angegebenen Auftrag zu beenden und gibt ein aktualisiertes ASR-Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="58567-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="58567-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="58567-112">PARAMETERS</span></span>

### <span data-ttu-id="58567-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58567-113">-DefaultProfile</span></span>
<span data-ttu-id="58567-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="58567-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="58567-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="58567-115">-InputObject</span></span>
<span data-ttu-id="58567-116">Eingabeobjekt: Geben Sie das ASR-Auftragsobjekt an, das dem zu beendenden ASR-Auftrag entspricht.</span><span class="sxs-lookup"><span data-stu-id="58567-116">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58567-117">-Name</span><span class="sxs-lookup"><span data-stu-id="58567-117">-Name</span></span>
<span data-ttu-id="58567-118">Geben Sie den ASR-Auftrag an, der vom ASR-Auftragsnamen angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="58567-118">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="58567-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="58567-119">-Confirm</span></span>
<span data-ttu-id="58567-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="58567-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58567-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58567-121">-WhatIf</span></span>
<span data-ttu-id="58567-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="58567-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58567-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="58567-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58567-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58567-124">CommonParameters</span></span>
<span data-ttu-id="58567-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58567-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58567-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58567-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58567-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="58567-127">INPUTS</span></span>

### <span data-ttu-id="58567-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="58567-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="58567-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="58567-129">OUTPUTS</span></span>

### <span data-ttu-id="58567-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="58567-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="58567-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="58567-131">NOTES</span></span>

## <span data-ttu-id="58567-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="58567-132">RELATED LINKS</span></span>

[<span data-ttu-id="58567-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="58567-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="58567-134">Neustart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="58567-134">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="58567-135">Lebenslauf-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="58567-135">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)
