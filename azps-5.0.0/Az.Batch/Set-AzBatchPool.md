---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
ms.openlocfilehash: 423f249a7971883cbe47d8f499fdd780980362f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177019"
---
# <span data-ttu-id="c5abf-101">Set-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="c5abf-101">Set-AzBatchPool</span></span>

## <span data-ttu-id="c5abf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c5abf-102">SYNOPSIS</span></span>
<span data-ttu-id="c5abf-103">Aktualisiert die Eigenschaften eines Pools.</span><span class="sxs-lookup"><span data-stu-id="c5abf-103">Updates the properties of a pool.</span></span>

## <span data-ttu-id="c5abf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5abf-104">SYNTAX</span></span>

```
Set-AzBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5abf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5abf-105">DESCRIPTION</span></span>
<span data-ttu-id="c5abf-106">Das Cmdlet " **Satz-AzBatchPool** " aktualisiert die Eigenschaften eines Pools im Azure-Stapelverarbeitungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="c5abf-106">The **Set-AzBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="c5abf-107">Verwenden Sie das Get-AzBatchPool-Cmdlet, um ein **PSCloudPool** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c5abf-107">Use the Get-AzBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="c5abf-108">Ändern Sie die Eigenschaften des Objekts, und verwenden Sie dann das aktuelle Cmdlet, um Ihre Änderungen an den Stapelverarbeitungs Dienst zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="c5abf-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="c5abf-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5abf-109">EXAMPLES</span></span>

### <span data-ttu-id="c5abf-110">Beispiel 1: Aktualisieren eines Pools</span><span class="sxs-lookup"><span data-stu-id="c5abf-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="c5abf-111">Der erste Befehl ruft einen Pool mithilfe von **Get-AzBatchPool** ab und speichert ihn dann in der $Pool-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c5abf-111">The first command gets a pool by using **Get-AzBatchPool** , and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="c5abf-112">Die nächsten drei Befehle ändern die Startaufgaben Spezifikation für das $Pool-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c5abf-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="c5abf-113">Der endgültige Befehl aktualisiert den Batch Dienst so, dass er dem lokalen Objekt in $Pool entspricht.</span><span class="sxs-lookup"><span data-stu-id="c5abf-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="c5abf-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5abf-114">PARAMETERS</span></span>

### <span data-ttu-id="c5abf-115">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="c5abf-115">-BatchContext</span></span>
<span data-ttu-id="c5abf-116">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="c5abf-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c5abf-117">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c5abf-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c5abf-118">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c5abf-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c5abf-119">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="c5abf-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c5abf-120">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="c5abf-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c5abf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5abf-121">-DefaultProfile</span></span>
<span data-ttu-id="c5abf-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c5abf-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5abf-123">-Pool</span><span class="sxs-lookup"><span data-stu-id="c5abf-123">-Pool</span></span>
<span data-ttu-id="c5abf-124">Gibt den **PSCloudPool** an, zu dem dieses Cmdlet den Batch Dienst aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c5abf-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5abf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5abf-125">CommonParameters</span></span>
<span data-ttu-id="c5abf-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5abf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5abf-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5abf-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5abf-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c5abf-128">INPUTS</span></span>

### <span data-ttu-id="c5abf-129">Microsoft.Azure.Commands.Batch. Models. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="c5abf-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="c5abf-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c5abf-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c5abf-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c5abf-131">OUTPUTS</span></span>

### <span data-ttu-id="c5abf-132">System. void</span><span class="sxs-lookup"><span data-stu-id="c5abf-132">System.Void</span></span>

## <span data-ttu-id="c5abf-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="c5abf-133">NOTES</span></span>

## <span data-ttu-id="c5abf-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c5abf-134">RELATED LINKS</span></span>

[<span data-ttu-id="c5abf-135">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="c5abf-135">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="c5abf-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c5abf-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c5abf-137">Neu – AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="c5abf-137">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="c5abf-138">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="c5abf-138">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="c5abf-139">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="c5abf-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
