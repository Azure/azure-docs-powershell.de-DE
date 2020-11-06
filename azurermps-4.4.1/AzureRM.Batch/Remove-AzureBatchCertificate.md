---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
ms.openlocfilehash: c63caed99a10851d6172e0db5dcc33e3404be215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479922"
---
# <span data-ttu-id="eeb6a-101">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="eeb6a-101">Remove-AzureBatchCertificate</span></span>

## <span data-ttu-id="eeb6a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eeb6a-102">SYNOPSIS</span></span>
<span data-ttu-id="eeb6a-103">Löscht ein Zertifikat von einem Konto.</span><span class="sxs-lookup"><span data-stu-id="eeb6a-103">Deletes a certificate from an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eeb6a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eeb6a-104">SYNTAX</span></span>

```
Remove-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eeb6a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eeb6a-105">DESCRIPTION</span></span>
<span data-ttu-id="eeb6a-106">Das Cmdlet **Remove-AzureBatchCertificate** entfernt ein Zertifikat aus dem angegebenen Azure-Batch Konto.</span><span class="sxs-lookup"><span data-stu-id="eeb6a-106">The **Remove-AzureBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="eeb6a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eeb6a-107">EXAMPLES</span></span>

### <span data-ttu-id="eeb6a-108">Beispiel 1: Entfernen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="eeb6a-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="eeb6a-109">Mit diesem Befehl wird das Zertifikat entfernt, das den angegebenen Fingerabdruck aufweist.</span><span class="sxs-lookup"><span data-stu-id="eeb6a-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="eeb6a-110">Beispiel 2: Entfernen aller aktiven Zertifikate</span><span class="sxs-lookup"><span data-stu-id="eeb6a-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzureBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="eeb6a-111">Dieser Befehl ruft alle Zertifikate ab, die mithilfe des Get-AzureBatchCertificate-Cmdlets aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="eeb6a-111">This command gets all certificates that are active by using the Get-AzureBatchCertificate cmdlet.</span></span>
<span data-ttu-id="eeb6a-112">Der Befehl übergibt die aktiven Zertifikate mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeb6a-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="eeb6a-113">Mit diesem Cmdlet werden die einzelnen Zertifikate entfernt.</span><span class="sxs-lookup"><span data-stu-id="eeb6a-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="eeb6a-114">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="eeb6a-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="eeb6a-115">Daher werden Sie vom Befehl nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="eeb6a-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="eeb6a-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="eeb6a-116">PARAMETERS</span></span>

### <span data-ttu-id="eeb6a-117">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="eeb6a-117">-BatchContext</span></span>
<span data-ttu-id="eeb6a-118">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="eeb6a-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="eeb6a-119">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeb6a-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="eeb6a-120">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="eeb6a-120">-Thumbprint</span></span>
<span data-ttu-id="eeb6a-121">Gibt den Fingerabdruck des vom Cmdlet gelöschten Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="eeb6a-121">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="eeb6a-122">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="eeb6a-122">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="eeb6a-123">Gibt den Algorithmus an, der zum Ableiten des Parameters *Fingerabdruck* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eeb6a-123">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="eeb6a-124">Derzeit ist der einzige gültige Wert SHA1.</span><span class="sxs-lookup"><span data-stu-id="eeb6a-124">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="eeb6a-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eeb6a-125">-Confirm</span></span>
<span data-ttu-id="eeb6a-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eeb6a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeb6a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeb6a-127">-WhatIf</span></span>
<span data-ttu-id="eeb6a-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eeb6a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeb6a-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eeb6a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeb6a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeb6a-130">-DefaultProfile</span></span>
<span data-ttu-id="eeb6a-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eeb6a-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eeb6a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeb6a-132">CommonParameters</span></span>
<span data-ttu-id="eeb6a-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeb6a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeb6a-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeb6a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeb6a-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eeb6a-135">INPUTS</span></span>

### <span data-ttu-id="eeb6a-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="eeb6a-136">BatchAccountContext</span></span>
<span data-ttu-id="eeb6a-137">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="eeb6a-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="eeb6a-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eeb6a-138">OUTPUTS</span></span>

## <span data-ttu-id="eeb6a-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="eeb6a-139">NOTES</span></span>

## <span data-ttu-id="eeb6a-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eeb6a-140">RELATED LINKS</span></span>

[<span data-ttu-id="eeb6a-141">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="eeb6a-141">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="eeb6a-142">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="eeb6a-142">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="eeb6a-143">Neu – AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="eeb6a-143">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="eeb6a-144">Stopp-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="eeb6a-144">Stop-AzureBatchCertificateDeletion</span></span>](./Stop-AzureBatchCertificateDeletion.md)

[<span data-ttu-id="eeb6a-145">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="eeb6a-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


