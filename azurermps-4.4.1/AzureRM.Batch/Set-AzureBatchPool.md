---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
ms.openlocfilehash: d18a6bdc9a2064e21507c909005692d5d21c63f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499209"
---
# <span data-ttu-id="887de-101">Set-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="887de-101">Set-AzureBatchPool</span></span>

## <span data-ttu-id="887de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="887de-102">SYNOPSIS</span></span>
<span data-ttu-id="887de-103">Aktualisiert die Eigenschaften eines Pools.</span><span class="sxs-lookup"><span data-stu-id="887de-103">Updates the properties of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="887de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="887de-104">SYNTAX</span></span>

```
Set-AzureBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="887de-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="887de-105">DESCRIPTION</span></span>
<span data-ttu-id="887de-106">Das Cmdlet " **Satz-AzureBatchPool** " aktualisiert die Eigenschaften eines Pools im Azure-Stapelverarbeitungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="887de-106">The **Set-AzureBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="887de-107">Verwenden Sie das Get-AzureBatchPool-Cmdlet, um ein **PSCloudPool** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="887de-107">Use the Get-AzureBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="887de-108">Ändern Sie die Eigenschaften des Objekts, und verwenden Sie dann das aktuelle Cmdlet, um Ihre Änderungen an den Stapelverarbeitungs Dienst zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="887de-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="887de-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="887de-109">EXAMPLES</span></span>

### <span data-ttu-id="887de-110">Beispiel 1: Aktualisieren eines Pools</span><span class="sxs-lookup"><span data-stu-id="887de-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzureBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzureBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="887de-111">Der erste Befehl ruft einen Pool mithilfe von **Get-AzureBatchPool** ab und speichert ihn dann in der $Pool-Variablen.</span><span class="sxs-lookup"><span data-stu-id="887de-111">The first command gets a pool by using **Get-AzureBatchPool** , and then stores it in the $Pool variable.</span></span>

<span data-ttu-id="887de-112">Die nächsten drei Befehle ändern die Startaufgaben Spezifikation für das $Pool-Objekt.</span><span class="sxs-lookup"><span data-stu-id="887de-112">The next three commands modify the start task specification on the $Pool object.</span></span>

<span data-ttu-id="887de-113">Der endgültige Befehl aktualisiert den Batch Dienst so, dass er dem lokalen Objekt in $Pool entspricht.</span><span class="sxs-lookup"><span data-stu-id="887de-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="887de-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="887de-114">PARAMETERS</span></span>

### <span data-ttu-id="887de-115">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="887de-115">-BatchContext</span></span>
<span data-ttu-id="887de-116">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="887de-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="887de-117">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="887de-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="887de-118">-Pool</span><span class="sxs-lookup"><span data-stu-id="887de-118">-Pool</span></span>
<span data-ttu-id="887de-119">Gibt den **PSCloudPool** an, zu dem dieses Cmdlet den Batch Dienst aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="887de-119">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="887de-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="887de-120">-DefaultProfile</span></span>
<span data-ttu-id="887de-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="887de-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="887de-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="887de-122">CommonParameters</span></span>
<span data-ttu-id="887de-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="887de-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="887de-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="887de-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="887de-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="887de-125">INPUTS</span></span>

### <span data-ttu-id="887de-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="887de-126">BatchAccountContext</span></span>
<span data-ttu-id="887de-127">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="887de-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="887de-128">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="887de-128">PSCloudPool</span></span>
<span data-ttu-id="887de-129">Der Parameter "Pool" akzeptiert den Wert vom Typ "PSCloudPool" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="887de-129">Parameter 'Pool' accepts value of type 'PSCloudPool' from the pipeline</span></span>

## <span data-ttu-id="887de-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="887de-130">OUTPUTS</span></span>

## <span data-ttu-id="887de-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="887de-131">NOTES</span></span>

## <span data-ttu-id="887de-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="887de-132">RELATED LINKS</span></span>

[<span data-ttu-id="887de-133">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="887de-133">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="887de-134">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="887de-134">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="887de-135">Neu – AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="887de-135">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="887de-136">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="887de-136">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="887de-137">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="887de-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


