---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 2e474462983f15c0d58f8ada60b907c100508c6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483166"
---
# <span data-ttu-id="326fa-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="326fa-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="326fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="326fa-102">SYNOPSIS</span></span>
<span data-ttu-id="326fa-103">Entfernt einen stapelverarbeitungsauftrags Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="326fa-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="326fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="326fa-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="326fa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="326fa-105">DESCRIPTION</span></span>
<span data-ttu-id="326fa-106">Das Cmdlet **Remove-AzureBatchJobSchedule** entfernt einen Azure-Batch Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="326fa-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="326fa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="326fa-107">EXAMPLES</span></span>

## <span data-ttu-id="326fa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="326fa-108">PARAMETERS</span></span>

### <span data-ttu-id="326fa-109">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="326fa-109">-BatchContext</span></span>
<span data-ttu-id="326fa-110">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="326fa-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="326fa-111">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="326fa-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="326fa-112">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="326fa-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="326fa-113">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="326fa-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="326fa-114">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="326fa-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="326fa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="326fa-115">-DefaultProfile</span></span>
<span data-ttu-id="326fa-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="326fa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="326fa-117">-Force</span><span class="sxs-lookup"><span data-stu-id="326fa-117">-Force</span></span>
<span data-ttu-id="326fa-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="326fa-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="326fa-119">-ID</span><span class="sxs-lookup"><span data-stu-id="326fa-119">-Id</span></span>
<span data-ttu-id="326fa-120">Gibt die ID des Auftragszeitplans an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="326fa-120">Specifies the ID of the job schedule to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="326fa-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="326fa-121">-Confirm</span></span>
<span data-ttu-id="326fa-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="326fa-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="326fa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="326fa-123">-WhatIf</span></span>
<span data-ttu-id="326fa-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="326fa-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="326fa-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="326fa-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="326fa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="326fa-126">CommonParameters</span></span>
<span data-ttu-id="326fa-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="326fa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="326fa-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="326fa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="326fa-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="326fa-129">INPUTS</span></span>

### <span data-ttu-id="326fa-130">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="326fa-130">BatchAccountContext</span></span>
<span data-ttu-id="326fa-131">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="326fa-131">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="326fa-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="326fa-132">OUTPUTS</span></span>

## <span data-ttu-id="326fa-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="326fa-133">NOTES</span></span>

## <span data-ttu-id="326fa-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="326fa-134">RELATED LINKS</span></span>

[<span data-ttu-id="326fa-135">Deaktivieren-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="326fa-135">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="326fa-136">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="326fa-136">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="326fa-137">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="326fa-137">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="326fa-138">Neu – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="326fa-138">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="326fa-139">Satz-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="326fa-139">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="326fa-140">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="326fa-140">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


