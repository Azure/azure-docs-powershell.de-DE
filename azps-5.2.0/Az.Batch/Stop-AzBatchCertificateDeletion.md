---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
ms.openlocfilehash: 53c4f4c24e0a5b1c868facd0fed8d3754fda7a41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305936"
---
# <span data-ttu-id="9c2eb-101">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="9c2eb-101">Stop-AzBatchCertificateDeletion</span></span>

## <span data-ttu-id="9c2eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c2eb-102">SYNOPSIS</span></span>
<span data-ttu-id="9c2eb-103">Ein fehlgeschlagenes Löschen eines Zertifikats wird abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="9c2eb-103">Cancels a failed deletion of a certificate.</span></span>

## <span data-ttu-id="9c2eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c2eb-104">SYNTAX</span></span>

```
Stop-AzBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c2eb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9c2eb-105">DESCRIPTION</span></span>
<span data-ttu-id="9c2eb-106">Das **Cmdlet "Stop-AzBatchCertificateDeletion"** bricht ein fehlgeschlagenes Löschen eines Zertifikats im Azure -Batchdienst ab.</span><span class="sxs-lookup"><span data-stu-id="9c2eb-106">The **Stop-AzBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="9c2eb-107">Sie können ein Löschen nur beenden, wenn sich das Zertifikat im Zustand **"DeleteFailed"** befindet.</span><span class="sxs-lookup"><span data-stu-id="9c2eb-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="9c2eb-108">Mit diesem Cmdlet wird das Zertifikat im Status **"Aktiv" wiederhergestellt.**</span><span class="sxs-lookup"><span data-stu-id="9c2eb-108">This cmdlet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="9c2eb-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9c2eb-109">EXAMPLES</span></span>

### <span data-ttu-id="9c2eb-110">Beispiel 1: Abbrechen eines Löschvorgangs</span><span class="sxs-lookup"><span data-stu-id="9c2eb-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="9c2eb-111">Mit diesem Befehl wird das Löschen des Zertifikats mit dem angegebenen Fingerabdruck abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="9c2eb-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="9c2eb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c2eb-112">PARAMETERS</span></span>

### <span data-ttu-id="9c2eb-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9c2eb-113">-BatchContext</span></span>
<span data-ttu-id="9c2eb-114">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9c2eb-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9c2eb-115">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="9c2eb-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9c2eb-116">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9c2eb-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9c2eb-117">Bei verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="9c2eb-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9c2eb-118">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c2eb-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9c2eb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c2eb-119">-DefaultProfile</span></span>
<span data-ttu-id="9c2eb-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9c2eb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c2eb-121">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="9c2eb-121">-Thumbprint</span></span>
<span data-ttu-id="9c2eb-122">Gibt den Fingerabdruck des Zertifikats an, das von diesem Cmdlet im Status **"Aktiv" wiederhergestellt** wird.</span><span class="sxs-lookup"><span data-stu-id="9c2eb-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="9c2eb-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="9c2eb-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="9c2eb-124">Gibt den Algorithmus an, der zum Ableitung des Parameters *"Thumbprint" verwendet* wird.</span><span class="sxs-lookup"><span data-stu-id="9c2eb-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="9c2eb-125">Derzeit ist der einzige gültige Wert "sha1".</span><span class="sxs-lookup"><span data-stu-id="9c2eb-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="9c2eb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c2eb-126">CommonParameters</span></span>
<span data-ttu-id="9c2eb-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c2eb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c2eb-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c2eb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c2eb-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9c2eb-129">INPUTS</span></span>

### <span data-ttu-id="9c2eb-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9c2eb-130">System.String</span></span>

### <span data-ttu-id="9c2eb-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9c2eb-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9c2eb-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9c2eb-132">OUTPUTS</span></span>

### <span data-ttu-id="9c2eb-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="9c2eb-133">System.Void</span></span>

## <span data-ttu-id="9c2eb-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9c2eb-134">NOTES</span></span>

## <span data-ttu-id="9c2eb-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9c2eb-135">RELATED LINKS</span></span>

[<span data-ttu-id="9c2eb-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="9c2eb-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="9c2eb-137">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="9c2eb-137">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="9c2eb-138">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="9c2eb-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
