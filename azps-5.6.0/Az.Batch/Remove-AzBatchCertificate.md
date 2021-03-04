---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
ms.openlocfilehash: 62858f37a7444e052c3d0a192a346a2284f232c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928707"
---
# <span data-ttu-id="b7d28-101">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="b7d28-101">Remove-AzBatchCertificate</span></span>

## <span data-ttu-id="b7d28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7d28-102">SYNOPSIS</span></span>
<span data-ttu-id="b7d28-103">Löscht ein Zertifikat aus einem Konto.</span><span class="sxs-lookup"><span data-stu-id="b7d28-103">Deletes a certificate from an account.</span></span>

## <span data-ttu-id="b7d28-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7d28-104">SYNTAX</span></span>

```
Remove-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7d28-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b7d28-105">DESCRIPTION</span></span>
<span data-ttu-id="b7d28-106">Das **Cmdlet Remove-AzBatchCertificate** entfernt ein Zertifikat aus dem angegebenen Azure Batch-Konto.</span><span class="sxs-lookup"><span data-stu-id="b7d28-106">The **Remove-AzBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="b7d28-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b7d28-107">EXAMPLES</span></span>

### <span data-ttu-id="b7d28-108">Beispiel 1: Entfernen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="b7d28-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="b7d28-109">Mit diesem Befehl wird das Zertifikat entfernt, das den angegebenen Fingerabdruck hat.</span><span class="sxs-lookup"><span data-stu-id="b7d28-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="b7d28-110">Beispiel 2:Entfernen aller aktiven Zertifikate</span><span class="sxs-lookup"><span data-stu-id="b7d28-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="b7d28-111">Dieser Befehl ruft alle Zertifikate ab, die mit dem cmdlet Get-AzBatchCertificate sind.</span><span class="sxs-lookup"><span data-stu-id="b7d28-111">This command gets all certificates that are active by using the Get-AzBatchCertificate cmdlet.</span></span>
<span data-ttu-id="b7d28-112">Der Befehl übergibt die aktiven Zertifikate mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7d28-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b7d28-113">Dieses Cmdlet entfernt jedes Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="b7d28-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="b7d28-114">Der Befehl gibt den Parameter *"Erzwingen"* an.</span><span class="sxs-lookup"><span data-stu-id="b7d28-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="b7d28-115">Daher werden Sie mit dem Befehl nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="b7d28-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b7d28-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b7d28-116">PARAMETERS</span></span>

### <span data-ttu-id="b7d28-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b7d28-117">-BatchContext</span></span>
<span data-ttu-id="b7d28-118">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b7d28-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b7d28-119">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="b7d28-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b7d28-120">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b7d28-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b7d28-121">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="b7d28-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b7d28-122">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="b7d28-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b7d28-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7d28-123">-DefaultProfile</span></span>
<span data-ttu-id="b7d28-124">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7d28-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7d28-125">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="b7d28-125">-Thumbprint</span></span>
<span data-ttu-id="b7d28-126">Gibt den Fingerabdruck des Zertifikats an, das von diesem Cmdlet gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="b7d28-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="b7d28-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="b7d28-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="b7d28-128">Gibt den Algorithmus an, der zum Ableitung des *Thumbprint-Parameters verwendet* wird.</span><span class="sxs-lookup"><span data-stu-id="b7d28-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="b7d28-129">Derzeit ist der einzige gültige Wert sha1.</span><span class="sxs-lookup"><span data-stu-id="b7d28-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="b7d28-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b7d28-130">-Confirm</span></span>
<span data-ttu-id="b7d28-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b7d28-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7d28-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7d28-132">-WhatIf</span></span>
<span data-ttu-id="b7d28-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b7d28-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7d28-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7d28-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7d28-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7d28-135">CommonParameters</span></span>
<span data-ttu-id="b7d28-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7d28-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7d28-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7d28-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7d28-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b7d28-138">INPUTS</span></span>

### <span data-ttu-id="b7d28-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b7d28-139">System.String</span></span>

### <span data-ttu-id="b7d28-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b7d28-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b7d28-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b7d28-141">OUTPUTS</span></span>

### <span data-ttu-id="b7d28-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="b7d28-142">System.Void</span></span>

## <span data-ttu-id="b7d28-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b7d28-143">NOTES</span></span>

## <span data-ttu-id="b7d28-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b7d28-144">RELATED LINKS</span></span>

[<span data-ttu-id="b7d28-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="b7d28-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="b7d28-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b7d28-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b7d28-147">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="b7d28-147">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="b7d28-148">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="b7d28-148">Stop-AzBatchCertificateDeletion</span></span>](./Stop-AzBatchCertificateDeletion.md)

[<span data-ttu-id="b7d28-149">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="b7d28-149">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
