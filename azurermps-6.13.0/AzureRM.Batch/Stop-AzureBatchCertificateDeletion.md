---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
ms.openlocfilehash: d43754e1b04dadc447de3d727769902f5454f79a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498398"
---
# <span data-ttu-id="093b9-101">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="093b9-101">Stop-AzureBatchCertificateDeletion</span></span>

## <span data-ttu-id="093b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="093b9-102">SYNOPSIS</span></span>
<span data-ttu-id="093b9-103">Bricht einen Fehler beim Löschen eines Zertifikats ab.</span><span class="sxs-lookup"><span data-stu-id="093b9-103">Cancels a failed deletion of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="093b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="093b9-104">SYNTAX</span></span>

```
Stop-AzureBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="093b9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="093b9-105">DESCRIPTION</span></span>
<span data-ttu-id="093b9-106">Mit dem Cmdlet " **Stop-AzureBatchCertificateDeletion** " wird ein Fehler beim Löschen eines Zertifikats im Azure-Batch Dienst abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="093b9-106">The **Stop-AzureBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="093b9-107">Sie können einen Löschvorgang nur beenden, wenn sich das Zertifikat im **DeleteFailed** -Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="093b9-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="093b9-108">Mit diesem cmldet wird das Zertifikat im **aktiven** Zustand wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="093b9-108">This cmldet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="093b9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="093b9-109">EXAMPLES</span></span>

### <span data-ttu-id="093b9-110">Beispiel 1: Löschen eines Löschvorgangs</span><span class="sxs-lookup"><span data-stu-id="093b9-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzureBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="093b9-111">Mit diesem Befehl wird das Löschen des Zertifikats mit dem angegebenen Fingerabdruck abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="093b9-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="093b9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="093b9-112">PARAMETERS</span></span>

### <span data-ttu-id="093b9-113">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="093b9-113">-BatchContext</span></span>
<span data-ttu-id="093b9-114">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="093b9-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="093b9-115">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="093b9-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="093b9-116">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="093b9-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="093b9-117">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="093b9-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="093b9-118">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="093b9-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="093b9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="093b9-119">-DefaultProfile</span></span>
<span data-ttu-id="093b9-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="093b9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="093b9-121">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="093b9-121">-Thumbprint</span></span>
<span data-ttu-id="093b9-122">Gibt den Fingerabdruck des Zertifikats an, das von diesem Cmdlet wieder im **aktiven** Zustand wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="093b9-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="093b9-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="093b9-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="093b9-124">Gibt den Algorithmus an, der zum Ableiten des Parameters *Fingerabdruck* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="093b9-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="093b9-125">Derzeit ist der einzige gültige Wert SHA1.</span><span class="sxs-lookup"><span data-stu-id="093b9-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="093b9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="093b9-126">CommonParameters</span></span>
<span data-ttu-id="093b9-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="093b9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="093b9-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="093b9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="093b9-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="093b9-129">INPUTS</span></span>

### <span data-ttu-id="093b9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="093b9-130">System.String</span></span>

### <span data-ttu-id="093b9-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="093b9-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="093b9-132">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="093b9-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="093b9-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="093b9-133">OUTPUTS</span></span>

### <span data-ttu-id="093b9-134">System. void</span><span class="sxs-lookup"><span data-stu-id="093b9-134">System.Void</span></span>

## <span data-ttu-id="093b9-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="093b9-135">NOTES</span></span>

## <span data-ttu-id="093b9-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="093b9-136">RELATED LINKS</span></span>

[<span data-ttu-id="093b9-137">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="093b9-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="093b9-138">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="093b9-138">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="093b9-139">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="093b9-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


