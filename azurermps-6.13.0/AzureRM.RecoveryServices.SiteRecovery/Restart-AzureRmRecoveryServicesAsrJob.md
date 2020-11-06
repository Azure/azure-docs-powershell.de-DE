---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/restart-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 94f4f44da8da4b2ad16db6dff86ad22908847a62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502913"
---
# <span data-ttu-id="f6a8d-101">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f6a8d-101">Restart-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="f6a8d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f6a8d-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a8d-103">Startet einen Azure Site Recovery-Auftrag neu.</span><span class="sxs-lookup"><span data-stu-id="f6a8d-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6a8d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6a8d-104">SYNTAX</span></span>

### <span data-ttu-id="f6a8d-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="f6a8d-105">ByObject (Default)</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6a8d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f6a8d-106">ByName</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6a8d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6a8d-107">DESCRIPTION</span></span>
<span data-ttu-id="f6a8d-108">Mit dem Cmdlet " **Restart-AzureRmRecoveryServicesAsrJob** " wird ein Azure Site Recovery-Auftrag neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="f6a8d-108">The **Restart-AzureRmRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="f6a8d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6a8d-109">EXAMPLES</span></span>

### <span data-ttu-id="f6a8d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f6a8d-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="f6a8d-111">Startet den angegebenen ASR-Auftrag neu und gibt das aktualisierte ASR-Auftragsobjekt des ASR-Auftrags zurück.</span><span class="sxs-lookup"><span data-stu-id="f6a8d-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="f6a8d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6a8d-112">PARAMETERS</span></span>

### <span data-ttu-id="f6a8d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a8d-113">-DefaultProfile</span></span>
<span data-ttu-id="f6a8d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f6a8d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f6a8d-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f6a8d-115">-InputObject</span></span>
<span data-ttu-id="f6a8d-116">Das Eingabeobjekt für das Cmdlet: das ASR-Auftragsobjekt, das dem ASR-Auftrag entspricht, der neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f6a8d-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


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

### <span data-ttu-id="f6a8d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f6a8d-117">-Name</span></span>
<span data-ttu-id="f6a8d-118">Geben Sie den Auftrag über den Namen an.</span><span class="sxs-lookup"><span data-stu-id="f6a8d-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="f6a8d-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f6a8d-119">-Confirm</span></span>
<span data-ttu-id="f6a8d-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6a8d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6a8d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6a8d-121">-WhatIf</span></span>
<span data-ttu-id="f6a8d-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6a8d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6a8d-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f6a8d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6a8d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a8d-124">CommonParameters</span></span>
<span data-ttu-id="f6a8d-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6a8d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a8d-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6a8d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a8d-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f6a8d-127">INPUTS</span></span>

### <span data-ttu-id="f6a8d-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f6a8d-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f6a8d-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f6a8d-129">OUTPUTS</span></span>

### <span data-ttu-id="f6a8d-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f6a8d-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f6a8d-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="f6a8d-131">NOTES</span></span>

## <span data-ttu-id="f6a8d-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f6a8d-132">RELATED LINKS</span></span>

[<span data-ttu-id="f6a8d-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f6a8d-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="f6a8d-134">Lebenslauf-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f6a8d-134">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="f6a8d-135">Stopp-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f6a8d-135">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
