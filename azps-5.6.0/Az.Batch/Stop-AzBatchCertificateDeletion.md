---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/powershell/module/az.batch/stop-azbatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
ms.openlocfilehash: 099f6a1ea19e9810745715dbc90ea0e0b1962285
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940592"
---
# <span data-ttu-id="284d2-101">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="284d2-101">Stop-AzBatchCertificateDeletion</span></span>

## <span data-ttu-id="284d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="284d2-102">SYNOPSIS</span></span>
<span data-ttu-id="284d2-103">Bricht ein fehlgeschlagenes Löschen eines Zertifikats ab.</span><span class="sxs-lookup"><span data-stu-id="284d2-103">Cancels a failed deletion of a certificate.</span></span>

## <span data-ttu-id="284d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="284d2-104">SYNTAX</span></span>

```
Stop-AzBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="284d2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="284d2-105">DESCRIPTION</span></span>
<span data-ttu-id="284d2-106">Das **Cmdlet Stop-AzBatchCertificateDeletion** bricht ein fehlgeschlagenes Löschen eines Zertifikats im Azure Batch-Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="284d2-106">The **Stop-AzBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="284d2-107">Sie können einen Löschvorgang nur beenden, wenn sich das Zertifikat im **DeleteFailed-Zustand** befindet.</span><span class="sxs-lookup"><span data-stu-id="284d2-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="284d2-108">Mit diesem Cmdlet wird das Zertifikat in den Status **Aktiv wiederhergestellt.**</span><span class="sxs-lookup"><span data-stu-id="284d2-108">This cmdlet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="284d2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="284d2-109">EXAMPLES</span></span>

### <span data-ttu-id="284d2-110">Beispiel 1: Abbrechen eines Löschvorgangs</span><span class="sxs-lookup"><span data-stu-id="284d2-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="284d2-111">Mit diesem Befehl wird das Löschen des Zertifikats abgebrochen, das den angegebenen Fingerabdruck hat.</span><span class="sxs-lookup"><span data-stu-id="284d2-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="284d2-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="284d2-112">PARAMETERS</span></span>

### <span data-ttu-id="284d2-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="284d2-113">-BatchContext</span></span>
<span data-ttu-id="284d2-114">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="284d2-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="284d2-115">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="284d2-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="284d2-116">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="284d2-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="284d2-117">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="284d2-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="284d2-118">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="284d2-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="284d2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="284d2-119">-DefaultProfile</span></span>
<span data-ttu-id="284d2-120">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="284d2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="284d2-121">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="284d2-121">-Thumbprint</span></span>
<span data-ttu-id="284d2-122">Gibt den Fingerabdruck des Zertifikats an, das von diesem Cmdlet im Status **Aktiv wiederhergestellt** wird.</span><span class="sxs-lookup"><span data-stu-id="284d2-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="284d2-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="284d2-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="284d2-124">Gibt den Algorithmus an, der zum Ableitung des *Thumbprint-Parameters verwendet* wird.</span><span class="sxs-lookup"><span data-stu-id="284d2-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="284d2-125">Derzeit ist der einzige gültige Wert sha1.</span><span class="sxs-lookup"><span data-stu-id="284d2-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="284d2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="284d2-126">CommonParameters</span></span>
<span data-ttu-id="284d2-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="284d2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="284d2-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="284d2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="284d2-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="284d2-129">INPUTS</span></span>

### <span data-ttu-id="284d2-130">System.String</span><span class="sxs-lookup"><span data-stu-id="284d2-130">System.String</span></span>

### <span data-ttu-id="284d2-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="284d2-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="284d2-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="284d2-132">OUTPUTS</span></span>

### <span data-ttu-id="284d2-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="284d2-133">System.Void</span></span>

## <span data-ttu-id="284d2-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="284d2-134">NOTES</span></span>

## <span data-ttu-id="284d2-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="284d2-135">RELATED LINKS</span></span>

[<span data-ttu-id="284d2-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="284d2-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="284d2-137">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="284d2-137">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="284d2-138">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="284d2-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
