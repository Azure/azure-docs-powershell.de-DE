---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
ms.openlocfilehash: 2f751a6efcf4b798c69bb0dfd9ecd38c33a65d01
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471125"
---
# <span data-ttu-id="ce401-101">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="ce401-101">Remove-AzBatchCertificate</span></span>

## <span data-ttu-id="ce401-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce401-102">SYNOPSIS</span></span>
<span data-ttu-id="ce401-103">Löscht ein Zertifikat aus einem Konto.</span><span class="sxs-lookup"><span data-stu-id="ce401-103">Deletes a certificate from an account.</span></span>

## <span data-ttu-id="ce401-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce401-104">SYNTAX</span></span>

```
Remove-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce401-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce401-105">DESCRIPTION</span></span>
<span data-ttu-id="ce401-106">Das **Cmdlet "Remove-AzBatchCertificate"** entfernt ein Zertifikat aus dem angegebenen Azure Batch-Konto.</span><span class="sxs-lookup"><span data-stu-id="ce401-106">The **Remove-AzBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="ce401-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ce401-107">EXAMPLES</span></span>

### <span data-ttu-id="ce401-108">Beispiel 1: Entfernen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="ce401-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="ce401-109">Mit diesem Befehl wird das Zertifikat mit dem angegebenen Druckabdruck entfernt.</span><span class="sxs-lookup"><span data-stu-id="ce401-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="ce401-110">Beispiel 2: Entfernen aller aktiven Zertifikate</span><span class="sxs-lookup"><span data-stu-id="ce401-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="ce401-111">Dieser Befehl ruft alle aktiven Zertifikate mithilfe des cmdlets Get-AzBatchCertificate ab.</span><span class="sxs-lookup"><span data-stu-id="ce401-111">This command gets all certificates that are active by using the Get-AzBatchCertificate cmdlet.</span></span>
<span data-ttu-id="ce401-112">Der Befehl übergibt die aktiven Zertifikate mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce401-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ce401-113">Mit diesem Cmdlet wird jedes Zertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="ce401-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="ce401-114">Der Befehl gibt den Parameter *"Force"* an.</span><span class="sxs-lookup"><span data-stu-id="ce401-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="ce401-115">Daher fordert Sie der Befehl nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="ce401-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ce401-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce401-116">PARAMETERS</span></span>

### <span data-ttu-id="ce401-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ce401-117">-BatchContext</span></span>
<span data-ttu-id="ce401-118">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ce401-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ce401-119">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce401-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ce401-120">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ce401-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ce401-121">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce401-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ce401-122">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ce401-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ce401-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce401-123">-DefaultProfile</span></span>
<span data-ttu-id="ce401-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce401-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce401-125">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="ce401-125">-Thumbprint</span></span>
<span data-ttu-id="ce401-126">Gibt den Fingerabdruck des Zertifikats an, das von diesem Cmdlet gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="ce401-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="ce401-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="ce401-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="ce401-128">Gibt den Algorithmus an, der zum Ableitung des Parameters *"Thumbprint" verwendet* wird.</span><span class="sxs-lookup"><span data-stu-id="ce401-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="ce401-129">Derzeit ist der einzige gültige Wert "sha1".</span><span class="sxs-lookup"><span data-stu-id="ce401-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="ce401-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce401-130">-Confirm</span></span>
<span data-ttu-id="ce401-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ce401-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce401-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ce401-132">-WhatIf</span></span>
<span data-ttu-id="ce401-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ce401-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce401-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce401-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce401-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce401-135">CommonParameters</span></span>
<span data-ttu-id="ce401-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce401-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce401-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce401-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce401-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ce401-138">INPUTS</span></span>

### <span data-ttu-id="ce401-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ce401-139">System.String</span></span>

### <span data-ttu-id="ce401-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ce401-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ce401-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ce401-141">OUTPUTS</span></span>

### <span data-ttu-id="ce401-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="ce401-142">System.Void</span></span>

## <span data-ttu-id="ce401-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ce401-143">NOTES</span></span>

## <span data-ttu-id="ce401-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ce401-144">RELATED LINKS</span></span>

[<span data-ttu-id="ce401-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="ce401-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="ce401-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ce401-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ce401-147">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="ce401-147">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="ce401-148">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="ce401-148">Stop-AzBatchCertificateDeletion</span></span>](./Stop-AzBatchCertificateDeletion.md)

[<span data-ttu-id="ce401-149">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="ce401-149">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
