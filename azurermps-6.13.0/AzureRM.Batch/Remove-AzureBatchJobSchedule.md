---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 59a906420e2326564e779c9358e07a5003946b28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662524"
---
# <span data-ttu-id="bc063-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bc063-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="bc063-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bc063-102">SYNOPSIS</span></span>
<span data-ttu-id="bc063-103">Entfernt einen stapelverarbeitungsauftrags Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="bc063-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc063-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc063-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc063-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc063-105">DESCRIPTION</span></span>
<span data-ttu-id="bc063-106">Das Cmdlet **Remove-AzureBatchJobSchedule** entfernt einen Azure-Batch Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="bc063-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="bc063-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc063-107">EXAMPLES</span></span>

## <span data-ttu-id="bc063-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc063-108">PARAMETERS</span></span>

### <span data-ttu-id="bc063-109">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="bc063-109">-BatchContext</span></span>
<span data-ttu-id="bc063-110">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="bc063-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bc063-111">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="bc063-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bc063-112">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bc063-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bc063-113">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="bc063-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bc063-114">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="bc063-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc063-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc063-115">-DefaultProfile</span></span>
<span data-ttu-id="bc063-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bc063-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc063-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bc063-117">-Force</span></span>
<span data-ttu-id="bc063-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="bc063-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc063-119">-ID</span><span class="sxs-lookup"><span data-stu-id="bc063-119">-Id</span></span>
<span data-ttu-id="bc063-120">Gibt die ID des Auftragszeitplans an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc063-120">Specifies the ID of the job schedule to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc063-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bc063-121">-Confirm</span></span>
<span data-ttu-id="bc063-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bc063-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc063-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc063-123">-WhatIf</span></span>
<span data-ttu-id="bc063-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bc063-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc063-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bc063-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc063-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc063-126">CommonParameters</span></span>
<span data-ttu-id="bc063-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc063-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc063-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc063-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc063-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bc063-129">INPUTS</span></span>

### <span data-ttu-id="bc063-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bc063-130">System.String</span></span>

### <span data-ttu-id="bc063-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bc063-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="bc063-132">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bc063-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="bc063-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bc063-133">OUTPUTS</span></span>

### <span data-ttu-id="bc063-134">System. void</span><span class="sxs-lookup"><span data-stu-id="bc063-134">System.Void</span></span>

## <span data-ttu-id="bc063-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="bc063-135">NOTES</span></span>

## <span data-ttu-id="bc063-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bc063-136">RELATED LINKS</span></span>

[<span data-ttu-id="bc063-137">Deaktivieren-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bc063-137">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="bc063-138">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bc063-138">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="bc063-139">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bc063-139">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="bc063-140">Neu – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bc063-140">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="bc063-141">Satz-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bc063-141">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="bc063-142">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bc063-142">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


