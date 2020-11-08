---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
ms.openlocfilehash: 39b37f6f81a849e7ea3fc59dde6c99bebc3bfd1d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94007444"
---
# <span data-ttu-id="eccb2-101">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="eccb2-101">Stop-AzBatchCertificateDeletion</span></span>

## <span data-ttu-id="eccb2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eccb2-102">SYNOPSIS</span></span>
<span data-ttu-id="eccb2-103">Bricht einen Fehler beim Löschen eines Zertifikats ab.</span><span class="sxs-lookup"><span data-stu-id="eccb2-103">Cancels a failed deletion of a certificate.</span></span>

## <span data-ttu-id="eccb2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eccb2-104">SYNTAX</span></span>

```
Stop-AzBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eccb2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eccb2-105">DESCRIPTION</span></span>
<span data-ttu-id="eccb2-106">Mit dem Cmdlet " **Stop-AzBatchCertificateDeletion** " wird ein Fehler beim Löschen eines Zertifikats im Azure-Batch Dienst abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="eccb2-106">The **Stop-AzBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="eccb2-107">Sie können einen Löschvorgang nur beenden, wenn sich das Zertifikat im **DeleteFailed** -Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="eccb2-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="eccb2-108">Mit diesem Cmdlet wird das Zertifikat im **aktiven** Zustand wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="eccb2-108">This cmdlet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="eccb2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eccb2-109">EXAMPLES</span></span>

### <span data-ttu-id="eccb2-110">Beispiel 1: Löschen eines Löschvorgangs</span><span class="sxs-lookup"><span data-stu-id="eccb2-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="eccb2-111">Mit diesem Befehl wird das Löschen des Zertifikats mit dem angegebenen Fingerabdruck abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="eccb2-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="eccb2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="eccb2-112">PARAMETERS</span></span>

### <span data-ttu-id="eccb2-113">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="eccb2-113">-BatchContext</span></span>
<span data-ttu-id="eccb2-114">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="eccb2-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="eccb2-115">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="eccb2-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="eccb2-116">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="eccb2-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="eccb2-117">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="eccb2-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="eccb2-118">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="eccb2-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="eccb2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eccb2-119">-DefaultProfile</span></span>
<span data-ttu-id="eccb2-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eccb2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eccb2-121">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="eccb2-121">-Thumbprint</span></span>
<span data-ttu-id="eccb2-122">Gibt den Fingerabdruck des Zertifikats an, das von diesem Cmdlet wieder im **aktiven** Zustand wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="eccb2-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="eccb2-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="eccb2-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="eccb2-124">Gibt den Algorithmus an, der zum Ableiten des Parameters *Fingerabdruck* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eccb2-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="eccb2-125">Derzeit ist der einzige gültige Wert SHA1.</span><span class="sxs-lookup"><span data-stu-id="eccb2-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="eccb2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eccb2-126">CommonParameters</span></span>
<span data-ttu-id="eccb2-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eccb2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eccb2-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eccb2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eccb2-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eccb2-129">INPUTS</span></span>

### <span data-ttu-id="eccb2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="eccb2-130">System.String</span></span>

### <span data-ttu-id="eccb2-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="eccb2-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="eccb2-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eccb2-132">OUTPUTS</span></span>

### <span data-ttu-id="eccb2-133">System. void</span><span class="sxs-lookup"><span data-stu-id="eccb2-133">System.Void</span></span>

## <span data-ttu-id="eccb2-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="eccb2-134">NOTES</span></span>

## <span data-ttu-id="eccb2-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eccb2-135">RELATED LINKS</span></span>

[<span data-ttu-id="eccb2-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="eccb2-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="eccb2-137">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="eccb2-137">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="eccb2-138">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="eccb2-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


