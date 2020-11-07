---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 673d9e5034b1e7c97d3b6b7cfdd6f89e9a79a34f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662976"
---
# <span data-ttu-id="a7f34-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a7f34-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="a7f34-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a7f34-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f34-103">Entfernt einen stapelverarbeitungsauftrags Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="a7f34-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7f34-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7f34-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7f34-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7f34-105">DESCRIPTION</span></span>
<span data-ttu-id="a7f34-106">Das Cmdlet **Remove-AzureBatchJobSchedule** entfernt einen Azure-Batch Auftragszeitplan.</span><span class="sxs-lookup"><span data-stu-id="a7f34-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="a7f34-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7f34-107">EXAMPLES</span></span>

## <span data-ttu-id="a7f34-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7f34-108">PARAMETERS</span></span>

### <span data-ttu-id="a7f34-109">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="a7f34-109">-BatchContext</span></span>
<span data-ttu-id="a7f34-110">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7f34-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a7f34-111">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7f34-111">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="a7f34-112">-Force</span><span class="sxs-lookup"><span data-stu-id="a7f34-112">-Force</span></span>
<span data-ttu-id="a7f34-113">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="a7f34-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a7f34-114">-ID</span><span class="sxs-lookup"><span data-stu-id="a7f34-114">-Id</span></span>
<span data-ttu-id="a7f34-115">Gibt die ID des Auftragszeitplans an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a7f34-115">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="a7f34-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a7f34-116">-Confirm</span></span>
<span data-ttu-id="a7f34-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a7f34-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7f34-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7f34-118">-WhatIf</span></span>
<span data-ttu-id="a7f34-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a7f34-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7f34-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7f34-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7f34-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f34-121">-DefaultProfile</span></span>
<span data-ttu-id="a7f34-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a7f34-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7f34-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f34-123">CommonParameters</span></span>
<span data-ttu-id="a7f34-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7f34-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f34-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7f34-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f34-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a7f34-126">INPUTS</span></span>

### <span data-ttu-id="a7f34-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a7f34-127">BatchAccountContext</span></span>
<span data-ttu-id="a7f34-128">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a7f34-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="a7f34-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a7f34-129">OUTPUTS</span></span>

## <span data-ttu-id="a7f34-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="a7f34-130">NOTES</span></span>

## <span data-ttu-id="a7f34-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a7f34-131">RELATED LINKS</span></span>

[<span data-ttu-id="a7f34-132">Deaktivieren-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a7f34-132">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="a7f34-133">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a7f34-133">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="a7f34-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a7f34-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="a7f34-135">Neu – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a7f34-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="a7f34-136">Satz-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a7f34-136">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="a7f34-137">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a7f34-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


