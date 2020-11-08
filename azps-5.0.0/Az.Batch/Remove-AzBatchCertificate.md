---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
ms.openlocfilehash: 2f751a6efcf4b798c69bb0dfd9ecd38c33a65d01
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177281"
---
# <span data-ttu-id="6381a-101">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="6381a-101">Remove-AzBatchCertificate</span></span>

## <span data-ttu-id="6381a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6381a-102">SYNOPSIS</span></span>
<span data-ttu-id="6381a-103">Löscht ein Zertifikat von einem Konto.</span><span class="sxs-lookup"><span data-stu-id="6381a-103">Deletes a certificate from an account.</span></span>

## <span data-ttu-id="6381a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6381a-104">SYNTAX</span></span>

```
Remove-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6381a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6381a-105">DESCRIPTION</span></span>
<span data-ttu-id="6381a-106">Das Cmdlet **Remove-AzBatchCertificate** entfernt ein Zertifikat aus dem angegebenen Azure-Batch Konto.</span><span class="sxs-lookup"><span data-stu-id="6381a-106">The **Remove-AzBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="6381a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6381a-107">EXAMPLES</span></span>

### <span data-ttu-id="6381a-108">Beispiel 1: Entfernen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="6381a-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="6381a-109">Mit diesem Befehl wird das Zertifikat entfernt, das den angegebenen Fingerabdruck aufweist.</span><span class="sxs-lookup"><span data-stu-id="6381a-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="6381a-110">Beispiel 2: Entfernen aller aktiven Zertifikate</span><span class="sxs-lookup"><span data-stu-id="6381a-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="6381a-111">Dieser Befehl ruft alle Zertifikate ab, die mithilfe des Get-AzBatchCertificate-Cmdlets aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="6381a-111">This command gets all certificates that are active by using the Get-AzBatchCertificate cmdlet.</span></span>
<span data-ttu-id="6381a-112">Der Befehl übergibt die aktiven Zertifikate mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6381a-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6381a-113">Mit diesem Cmdlet werden die einzelnen Zertifikate entfernt.</span><span class="sxs-lookup"><span data-stu-id="6381a-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="6381a-114">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="6381a-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="6381a-115">Daher werden Sie vom Befehl nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="6381a-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6381a-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="6381a-116">PARAMETERS</span></span>

### <span data-ttu-id="6381a-117">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="6381a-117">-BatchContext</span></span>
<span data-ttu-id="6381a-118">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="6381a-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6381a-119">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="6381a-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6381a-120">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6381a-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6381a-121">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="6381a-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6381a-122">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="6381a-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6381a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6381a-123">-DefaultProfile</span></span>
<span data-ttu-id="6381a-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6381a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6381a-125">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="6381a-125">-Thumbprint</span></span>
<span data-ttu-id="6381a-126">Gibt den Fingerabdruck des vom Cmdlet gelöschten Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="6381a-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="6381a-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="6381a-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="6381a-128">Gibt den Algorithmus an, der zum Ableiten des Parameters *Fingerabdruck* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6381a-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="6381a-129">Derzeit ist der einzige gültige Wert SHA1.</span><span class="sxs-lookup"><span data-stu-id="6381a-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="6381a-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6381a-130">-Confirm</span></span>
<span data-ttu-id="6381a-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6381a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6381a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6381a-132">-WhatIf</span></span>
<span data-ttu-id="6381a-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6381a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6381a-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6381a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6381a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6381a-135">CommonParameters</span></span>
<span data-ttu-id="6381a-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6381a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6381a-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6381a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6381a-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6381a-138">INPUTS</span></span>

### <span data-ttu-id="6381a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6381a-139">System.String</span></span>

### <span data-ttu-id="6381a-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6381a-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6381a-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6381a-141">OUTPUTS</span></span>

### <span data-ttu-id="6381a-142">System. void</span><span class="sxs-lookup"><span data-stu-id="6381a-142">System.Void</span></span>

## <span data-ttu-id="6381a-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="6381a-143">NOTES</span></span>

## <span data-ttu-id="6381a-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6381a-144">RELATED LINKS</span></span>

[<span data-ttu-id="6381a-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="6381a-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="6381a-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="6381a-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6381a-147">Neu – AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="6381a-147">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="6381a-148">Stopp-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="6381a-148">Stop-AzBatchCertificateDeletion</span></span>](./Stop-AzBatchCertificateDeletion.md)

[<span data-ttu-id="6381a-149">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6381a-149">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
