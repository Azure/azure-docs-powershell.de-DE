---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: C5126E20-0A93-4ACE-8297-F1E8E17BEF53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
ms.openlocfilehash: 6ee1319881b200b3fcae56e433f81460bfc90274
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502790"
---
# <span data-ttu-id="87850-101">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="87850-101">Wait-AzureRmBackupJob</span></span>

## <span data-ttu-id="87850-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="87850-102">SYNOPSIS</span></span>
<span data-ttu-id="87850-103">Wartet, bis ein Backup-Auftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="87850-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87850-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="87850-104">SYNTAX</span></span>

```
Wait-AzureRmBackupJob -Job <Object> [-TimeOut <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87850-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87850-105">DESCRIPTION</span></span>
<span data-ttu-id="87850-106">Das **Wait-AzureRmBackupJob-** Cmdlet wartet darauf, dass ein Azure Backup-Auftrag abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="87850-106">The **Wait-AzureRmBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="87850-107">Backup-Aufträge können viel Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="87850-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="87850-108">Wenn Sie einen Sicherungsauftrag als Teil eines Skripts ausführen, möchten Sie möglicherweise erzwingen, dass das Skript auf den Abschluss des Auftrags wartet, bevor es mit anderen Aufgaben fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="87850-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>

<span data-ttu-id="87850-109">Ein Skript, das dieses Cmdlet enthält, kann einfacher als eins sein, das den Sicherungsdienst für den Auftragsstatus abruft.</span><span class="sxs-lookup"><span data-stu-id="87850-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>

## <span data-ttu-id="87850-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="87850-110">EXAMPLES</span></span>

## <span data-ttu-id="87850-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="87850-111">PARAMETERS</span></span>

### <span data-ttu-id="87850-112">-Job</span><span class="sxs-lookup"><span data-stu-id="87850-112">-Job</span></span>
<span data-ttu-id="87850-113">Gibt einen Auftrag an, den dieses Cmdlet abbricht.</span><span class="sxs-lookup"><span data-stu-id="87850-113">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="87850-114">Verwenden Sie das Get-AzureRmBackupJob-Cmdlet, um ein **AzureRmBackupJob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="87850-114">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87850-115">-Timeout</span><span class="sxs-lookup"><span data-stu-id="87850-115">-TimeOut</span></span>
<span data-ttu-id="87850-116">Gibt die maximale Zeitdauer in Sekunden an, die dieses Cmdlet auf den Abschluss des Auftrags wartet.</span><span class="sxs-lookup"><span data-stu-id="87850-116">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="87850-117">Wir empfehlen, dass Sie einen Timeoutwert angeben.</span><span class="sxs-lookup"><span data-stu-id="87850-117">We recommend that you specify a time-out value.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87850-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87850-118">-DefaultProfile</span></span>
<span data-ttu-id="87850-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="87850-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87850-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87850-120">CommonParameters</span></span>
<span data-ttu-id="87850-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87850-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87850-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87850-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87850-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="87850-123">INPUTS</span></span>

### <span data-ttu-id="87850-124">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="87850-124">AzureRmBackupJob</span></span>

## <span data-ttu-id="87850-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="87850-125">OUTPUTS</span></span>

### <span data-ttu-id="87850-126">AzureRmBackupJob[]</span><span class="sxs-lookup"><span data-stu-id="87850-126">AzureRmBackupJob[]</span></span>

## <span data-ttu-id="87850-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="87850-127">NOTES</span></span>

## <span data-ttu-id="87850-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="87850-128">RELATED LINKS</span></span>

[<span data-ttu-id="87850-129">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="87850-129">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="87850-130">Stopp-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="87850-130">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)


