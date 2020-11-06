---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
ms.openlocfilehash: 820e94b75c19d49f4e49ee8419f7807a839f925b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499198"
---
# <span data-ttu-id="b7781-101">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="b7781-101">Stop-AzureBatchCertificateDeletion</span></span>

## <span data-ttu-id="b7781-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7781-102">SYNOPSIS</span></span>
<span data-ttu-id="b7781-103">Bricht einen Fehler beim Löschen eines Zertifikats ab.</span><span class="sxs-lookup"><span data-stu-id="b7781-103">Cancels a failed deletion of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7781-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7781-104">SYNTAX</span></span>

```
Stop-AzureBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7781-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7781-105">DESCRIPTION</span></span>
<span data-ttu-id="b7781-106">Mit dem Cmdlet " **Stop-AzureBatchCertificateDeletion** " wird ein Fehler beim Löschen eines Zertifikats im Azure-Batch Dienst abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="b7781-106">The **Stop-AzureBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="b7781-107">Sie können einen Löschvorgang nur beenden, wenn sich das Zertifikat im **DeleteFailed** -Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="b7781-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="b7781-108">Mit diesem cmldet wird das Zertifikat im **aktiven** Zustand wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="b7781-108">This cmldet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="b7781-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7781-109">EXAMPLES</span></span>

### <span data-ttu-id="b7781-110">Beispiel 1: Löschen eines Löschvorgangs</span><span class="sxs-lookup"><span data-stu-id="b7781-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzureBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="b7781-111">Mit diesem Befehl wird das Löschen des Zertifikats mit dem angegebenen Fingerabdruck abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="b7781-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="b7781-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7781-112">PARAMETERS</span></span>

### <span data-ttu-id="b7781-113">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="b7781-113">-BatchContext</span></span>
<span data-ttu-id="b7781-114">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="b7781-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b7781-115">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7781-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="b7781-116">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="b7781-116">-Thumbprint</span></span>
<span data-ttu-id="b7781-117">Gibt den Fingerabdruck des Zertifikats an, das von diesem Cmdlet wieder im **aktiven** Zustand wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b7781-117">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="b7781-118">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="b7781-118">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="b7781-119">Gibt den Algorithmus an, der zum Ableiten des Parameters *Fingerabdruck* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b7781-119">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="b7781-120">Derzeit ist der einzige gültige Wert SHA1.</span><span class="sxs-lookup"><span data-stu-id="b7781-120">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="b7781-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7781-121">-DefaultProfile</span></span>
<span data-ttu-id="b7781-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b7781-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7781-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7781-123">CommonParameters</span></span>
<span data-ttu-id="b7781-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7781-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7781-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7781-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7781-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7781-126">INPUTS</span></span>

### <span data-ttu-id="b7781-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b7781-127">BatchAccountContext</span></span>
<span data-ttu-id="b7781-128">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b7781-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="b7781-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7781-129">OUTPUTS</span></span>

## <span data-ttu-id="b7781-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7781-130">NOTES</span></span>

## <span data-ttu-id="b7781-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7781-131">RELATED LINKS</span></span>

[<span data-ttu-id="b7781-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b7781-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b7781-133">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="b7781-133">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="b7781-134">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="b7781-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


