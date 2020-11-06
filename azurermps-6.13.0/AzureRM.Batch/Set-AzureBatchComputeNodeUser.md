---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
ms.openlocfilehash: c6a89a5c42daea7991711dfa0c96953856949aed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477934"
---
# <span data-ttu-id="cee4a-101">Set-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="cee4a-101">Set-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="cee4a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cee4a-102">SYNOPSIS</span></span>
<span data-ttu-id="cee4a-103">Ändert die Eigenschaften eines Kontos in einem Batch Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="cee4a-103">Modifies properties of an account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cee4a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cee4a-104">SYNTAX</span></span>

```
Set-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cee4a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cee4a-105">DESCRIPTION</span></span>
<span data-ttu-id="cee4a-106">Das Cmdlet " **Satz-AzureBatchComputeNodeUser** " ändert die Eigenschaften eines Benutzerkontos in einem Azure Batch Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="cee4a-106">The **Set-AzureBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="cee4a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cee4a-107">EXAMPLES</span></span>

### <span data-ttu-id="cee4a-108">Beispiel 1: Aktualisieren eines Benutzerkontos</span><span class="sxs-lookup"><span data-stu-id="cee4a-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzureBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="cee4a-109">Mit diesem Befehl wird das Benutzerkonto mit dem Namen PFuller auf dem Compute-Knoten geändert, der die angegebene ID im Pool mit dem Namen ContosoPool aufweist.</span><span class="sxs-lookup"><span data-stu-id="cee4a-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="cee4a-110">Der Befehl ändert das Kennwort für das Konto und die Ablaufzeit.</span><span class="sxs-lookup"><span data-stu-id="cee4a-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="cee4a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="cee4a-111">PARAMETERS</span></span>

### <span data-ttu-id="cee4a-112">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="cee4a-112">-BatchContext</span></span>
<span data-ttu-id="cee4a-113">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="cee4a-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cee4a-114">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="cee4a-114">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cee4a-115">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cee4a-115">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cee4a-116">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="cee4a-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cee4a-117">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="cee4a-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cee4a-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="cee4a-118">-ComputeNodeId</span></span>
<span data-ttu-id="cee4a-119">Gibt die ID des Compute-Knotens an, auf dem dieses Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cee4a-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cee4a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cee4a-120">-DefaultProfile</span></span>
<span data-ttu-id="cee4a-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cee4a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cee4a-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="cee4a-122">-ExpiryTime</span></span>
<span data-ttu-id="cee4a-123">Gibt die Ablaufzeit für das Benutzerkonto an.</span><span class="sxs-lookup"><span data-stu-id="cee4a-123">Specifies the expiry time for the user account.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cee4a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="cee4a-124">-Name</span></span>
<span data-ttu-id="cee4a-125">Gibt den Namen des Benutzerkontos an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="cee4a-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cee4a-126">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="cee4a-126">-Password</span></span>
<span data-ttu-id="cee4a-127">Gibt das Kennwort für das Benutzerkonto an.</span><span class="sxs-lookup"><span data-stu-id="cee4a-127">Specifies the password for the user account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cee4a-128">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="cee4a-128">-PoolId</span></span>
<span data-ttu-id="cee4a-129">Gibt die ID des Pools an, der den Compute-Knoten enthält, auf dem dieses Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cee4a-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cee4a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cee4a-130">CommonParameters</span></span>
<span data-ttu-id="cee4a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cee4a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cee4a-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cee4a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cee4a-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cee4a-133">INPUTS</span></span>

### <span data-ttu-id="cee4a-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cee4a-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="cee4a-135">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cee4a-135">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="cee4a-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cee4a-136">OUTPUTS</span></span>

### <span data-ttu-id="cee4a-137">System. void</span><span class="sxs-lookup"><span data-stu-id="cee4a-137">System.Void</span></span>

## <span data-ttu-id="cee4a-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="cee4a-138">NOTES</span></span>

## <span data-ttu-id="cee4a-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cee4a-139">RELATED LINKS</span></span>

[<span data-ttu-id="cee4a-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="cee4a-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="cee4a-141">Neu – AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="cee4a-141">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="cee4a-142">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="cee4a-142">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="cee4a-143">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cee4a-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


