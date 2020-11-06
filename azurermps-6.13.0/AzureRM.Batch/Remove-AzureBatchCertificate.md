---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
ms.openlocfilehash: 7e8159a7a17276d749adb89ea4e1b82118f9b2bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498426"
---
# <span data-ttu-id="a2926-101">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="a2926-101">Remove-AzureBatchCertificate</span></span>

## <span data-ttu-id="a2926-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a2926-102">SYNOPSIS</span></span>
<span data-ttu-id="a2926-103">Löscht ein Zertifikat von einem Konto.</span><span class="sxs-lookup"><span data-stu-id="a2926-103">Deletes a certificate from an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2926-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2926-104">SYNTAX</span></span>

```
Remove-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a2926-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2926-105">DESCRIPTION</span></span>
<span data-ttu-id="a2926-106">Das Cmdlet **Remove-AzureBatchCertificate** entfernt ein Zertifikat aus dem angegebenen Azure-Batch Konto.</span><span class="sxs-lookup"><span data-stu-id="a2926-106">The **Remove-AzureBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="a2926-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2926-107">EXAMPLES</span></span>

### <span data-ttu-id="a2926-108">Beispiel 1: Entfernen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="a2926-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="a2926-109">Mit diesem Befehl wird das Zertifikat entfernt, das den angegebenen Fingerabdruck aufweist.</span><span class="sxs-lookup"><span data-stu-id="a2926-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="a2926-110">Beispiel 2: Entfernen aller aktiven Zertifikate</span><span class="sxs-lookup"><span data-stu-id="a2926-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzureBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="a2926-111">Dieser Befehl ruft alle Zertifikate ab, die mithilfe des Get-AzureBatchCertificate-Cmdlets aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="a2926-111">This command gets all certificates that are active by using the Get-AzureBatchCertificate cmdlet.</span></span>
<span data-ttu-id="a2926-112">Der Befehl übergibt die aktiven Zertifikate mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2926-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a2926-113">Mit diesem Cmdlet werden die einzelnen Zertifikate entfernt.</span><span class="sxs-lookup"><span data-stu-id="a2926-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="a2926-114">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="a2926-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a2926-115">Daher werden Sie vom Befehl nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="a2926-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a2926-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2926-116">PARAMETERS</span></span>

### <span data-ttu-id="a2926-117">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="a2926-117">-BatchContext</span></span>
<span data-ttu-id="a2926-118">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="a2926-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a2926-119">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="a2926-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a2926-120">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a2926-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a2926-121">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="a2926-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a2926-122">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="a2926-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a2926-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2926-123">-DefaultProfile</span></span>
<span data-ttu-id="a2926-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a2926-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2926-125">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="a2926-125">-Thumbprint</span></span>
<span data-ttu-id="a2926-126">Gibt den Fingerabdruck des vom Cmdlet gelöschten Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="a2926-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="a2926-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="a2926-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="a2926-128">Gibt den Algorithmus an, der zum Ableiten des Parameters *Fingerabdruck* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a2926-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="a2926-129">Derzeit ist der einzige gültige Wert SHA1.</span><span class="sxs-lookup"><span data-stu-id="a2926-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="a2926-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a2926-130">-Confirm</span></span>
<span data-ttu-id="a2926-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2926-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2926-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2926-132">-WhatIf</span></span>
<span data-ttu-id="a2926-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2926-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2926-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2926-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2926-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2926-135">CommonParameters</span></span>
<span data-ttu-id="a2926-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2926-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2926-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2926-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2926-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a2926-138">INPUTS</span></span>

### <span data-ttu-id="a2926-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a2926-139">System.String</span></span>

### <span data-ttu-id="a2926-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a2926-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="a2926-141">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a2926-141">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="a2926-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a2926-142">OUTPUTS</span></span>

### <span data-ttu-id="a2926-143">System. void</span><span class="sxs-lookup"><span data-stu-id="a2926-143">System.Void</span></span>

## <span data-ttu-id="a2926-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="a2926-144">NOTES</span></span>

## <span data-ttu-id="a2926-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a2926-145">RELATED LINKS</span></span>

[<span data-ttu-id="a2926-146">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="a2926-146">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="a2926-147">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a2926-147">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a2926-148">Neu – AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="a2926-148">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="a2926-149">Stopp-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="a2926-149">Stop-AzureBatchCertificateDeletion</span></span>](./Stop-AzureBatchCertificateDeletion.md)

[<span data-ttu-id="a2926-150">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a2926-150">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


