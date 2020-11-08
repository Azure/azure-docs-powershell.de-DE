---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restart-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: cf8b2617e01e472de32f128d4907d68edaebb2e6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178227"
---
# <span data-ttu-id="7325b-101">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="7325b-101">Restart-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="7325b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7325b-102">SYNOPSIS</span></span>
<span data-ttu-id="7325b-103">Startet einen Azure Site Recovery-Auftrag neu.</span><span class="sxs-lookup"><span data-stu-id="7325b-103">Restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="7325b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7325b-104">SYNTAX</span></span>

### <span data-ttu-id="7325b-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="7325b-105">ByObject (Default)</span></span>
```
Restart-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7325b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7325b-106">ByName</span></span>
```
Restart-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7325b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7325b-107">DESCRIPTION</span></span>
<span data-ttu-id="7325b-108">Mit dem Cmdlet " **Restart-AzRecoveryServicesAsrJob** " wird ein Azure Site Recovery-Auftrag neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="7325b-108">The **Restart-AzRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="7325b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7325b-109">EXAMPLES</span></span>

### <span data-ttu-id="7325b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7325b-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="7325b-111">Startet den angegebenen ASR-Auftrag neu und gibt das aktualisierte ASR-Auftragsobjekt des ASR-Auftrags zurück.</span><span class="sxs-lookup"><span data-stu-id="7325b-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="7325b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7325b-112">PARAMETERS</span></span>

### <span data-ttu-id="7325b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7325b-113">-DefaultProfile</span></span>
<span data-ttu-id="7325b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7325b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7325b-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7325b-115">-InputObject</span></span>
<span data-ttu-id="7325b-116">Das Eingabeobjekt für das Cmdlet: das ASR-Auftragsobjekt, das dem ASR-Auftrag entspricht, der neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7325b-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


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

### <span data-ttu-id="7325b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7325b-117">-Name</span></span>
<span data-ttu-id="7325b-118">Geben Sie den Auftrag über den Namen an.</span><span class="sxs-lookup"><span data-stu-id="7325b-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="7325b-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7325b-119">-Confirm</span></span>
<span data-ttu-id="7325b-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7325b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7325b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7325b-121">-WhatIf</span></span>
<span data-ttu-id="7325b-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7325b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7325b-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7325b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7325b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7325b-124">CommonParameters</span></span>
<span data-ttu-id="7325b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7325b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7325b-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7325b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7325b-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7325b-127">INPUTS</span></span>

### <span data-ttu-id="7325b-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7325b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7325b-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7325b-129">OUTPUTS</span></span>

### <span data-ttu-id="7325b-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7325b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7325b-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="7325b-131">NOTES</span></span>

## <span data-ttu-id="7325b-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7325b-132">RELATED LINKS</span></span>

[<span data-ttu-id="7325b-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="7325b-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="7325b-134">Lebenslauf-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="7325b-134">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="7325b-135">Stopp-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="7325b-135">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
