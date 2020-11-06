---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
ms.openlocfilehash: c0f1dc4972e3b71dce74bffb7a72e782774a2734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476226"
---
# <span data-ttu-id="8217b-101">Set-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="8217b-101">Set-AzureBatchPool</span></span>

## <span data-ttu-id="8217b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8217b-102">SYNOPSIS</span></span>
<span data-ttu-id="8217b-103">Aktualisiert die Eigenschaften eines Pools.</span><span class="sxs-lookup"><span data-stu-id="8217b-103">Updates the properties of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8217b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8217b-104">SYNTAX</span></span>

```
Set-AzureBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8217b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8217b-105">DESCRIPTION</span></span>
<span data-ttu-id="8217b-106">Das Cmdlet " **Satz-AzureBatchPool** " aktualisiert die Eigenschaften eines Pools im Azure-Stapelverarbeitungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="8217b-106">The **Set-AzureBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="8217b-107">Verwenden Sie das Get-AzureBatchPool-Cmdlet, um ein **PSCloudPool** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8217b-107">Use the Get-AzureBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="8217b-108">Ändern Sie die Eigenschaften des Objekts, und verwenden Sie dann das aktuelle Cmdlet, um Ihre Änderungen an den Stapelverarbeitungs Dienst zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="8217b-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="8217b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8217b-109">EXAMPLES</span></span>

### <span data-ttu-id="8217b-110">Beispiel 1: Aktualisieren eines Pools</span><span class="sxs-lookup"><span data-stu-id="8217b-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzureBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzureBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="8217b-111">Der erste Befehl ruft einen Pool mithilfe von **Get-AzureBatchPool** ab und speichert ihn dann in der $Pool-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8217b-111">The first command gets a pool by using **Get-AzureBatchPool** , and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="8217b-112">Die nächsten drei Befehle ändern die Startaufgaben Spezifikation für das $Pool-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8217b-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="8217b-113">Der endgültige Befehl aktualisiert den Batch Dienst so, dass er dem lokalen Objekt in $Pool entspricht.</span><span class="sxs-lookup"><span data-stu-id="8217b-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="8217b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8217b-114">PARAMETERS</span></span>

### <span data-ttu-id="8217b-115">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="8217b-115">-BatchContext</span></span>
<span data-ttu-id="8217b-116">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="8217b-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8217b-117">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="8217b-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8217b-118">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8217b-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8217b-119">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="8217b-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8217b-120">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="8217b-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8217b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8217b-121">-DefaultProfile</span></span>
<span data-ttu-id="8217b-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8217b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8217b-123">-Pool</span><span class="sxs-lookup"><span data-stu-id="8217b-123">-Pool</span></span>
<span data-ttu-id="8217b-124">Gibt den **PSCloudPool** an, zu dem dieses Cmdlet den Batch Dienst aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8217b-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8217b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8217b-125">CommonParameters</span></span>
<span data-ttu-id="8217b-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8217b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8217b-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8217b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8217b-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8217b-128">INPUTS</span></span>

### <span data-ttu-id="8217b-129">Microsoft.Azure.Commands.Batch. Models. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="8217b-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>
<span data-ttu-id="8217b-130">Parameter: Pool (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8217b-130">Parameters: Pool (ByValue)</span></span>

### <span data-ttu-id="8217b-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8217b-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="8217b-132">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8217b-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="8217b-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8217b-133">OUTPUTS</span></span>

### <span data-ttu-id="8217b-134">System. void</span><span class="sxs-lookup"><span data-stu-id="8217b-134">System.Void</span></span>

## <span data-ttu-id="8217b-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="8217b-135">NOTES</span></span>

## <span data-ttu-id="8217b-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8217b-136">RELATED LINKS</span></span>

[<span data-ttu-id="8217b-137">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="8217b-137">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="8217b-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8217b-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="8217b-139">Neu – AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="8217b-139">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="8217b-140">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="8217b-140">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="8217b-141">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8217b-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


