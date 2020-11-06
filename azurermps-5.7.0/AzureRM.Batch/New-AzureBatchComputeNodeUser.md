---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 3e52b2f3c9bddb2039b87b373d0963d51827f293
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497765"
---
# <span data-ttu-id="de76b-101">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="de76b-101">New-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="de76b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="de76b-102">SYNOPSIS</span></span>
<span data-ttu-id="de76b-103">Erstellt ein Benutzerkonto in einem Batch Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="de76b-103">Creates a user account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de76b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="de76b-104">SYNTAX</span></span>

### <span data-ttu-id="de76b-105">ID</span><span class="sxs-lookup"><span data-stu-id="de76b-105">Id</span></span>
```
New-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String>
 -Password <SecureString> [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de76b-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="de76b-106">ParentObject</span></span>
```
New-AzureBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de76b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de76b-107">DESCRIPTION</span></span>
<span data-ttu-id="de76b-108">Das Cmdlet **New-AzureBatchComputeNodeUser** erstellt ein Benutzerkonto in einem Azure Batch Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="de76b-108">The **New-AzureBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="de76b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de76b-109">EXAMPLES</span></span>

### <span data-ttu-id="de76b-110">Beispiel 1: Erstellen eines Benutzerkontos mit administrativen Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="de76b-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzureBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="de76b-111">Mit diesem Befehl wird ein Benutzerkonto auf dem Compute-Knoten erstellt, das die ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="de76b-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="de76b-112">Der Knoten befindet sich im Pool mit der ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="de76b-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="de76b-113">Der Benutzername lautet testuser, das Kennwort ist Kennwort, das Konto läuft innerhalb von sieben Tagen ab, und das Konto verfügt über Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="de76b-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="de76b-114">Beispiel 2: Erstellen eines Benutzerkontos auf einem Compute-Knoten mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="de76b-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzureBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="de76b-115">Dieser Befehl ruft mit dem Cmdlet **Get-AzureBatchComputeNode** den Compute-Knoten mit dem Namen ComputeNode01 ab.</span><span class="sxs-lookup"><span data-stu-id="de76b-115">This command gets the compute node named ComputeNode01 by using the **Get-AzureBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="de76b-116">Dieser Knoten befindet sich im Pool mit der ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="de76b-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="de76b-117">Der Befehl übergibt diesen Compute-Knoten mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de76b-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="de76b-118">Der Befehl erstellt ein Benutzerkonto mit dem Benutzernamen TestUserand Kennwort.</span><span class="sxs-lookup"><span data-stu-id="de76b-118">The command creates a user account that has the user name TestUserand the password Password.</span></span>

## <span data-ttu-id="de76b-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="de76b-119">PARAMETERS</span></span>

### <span data-ttu-id="de76b-120">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="de76b-120">-BatchContext</span></span>
<span data-ttu-id="de76b-121">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="de76b-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="de76b-122">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="de76b-122">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="de76b-123">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="de76b-123">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="de76b-124">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="de76b-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="de76b-125">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="de76b-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de76b-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="de76b-126">-ComputeNode</span></span>
<span data-ttu-id="de76b-127">Gibt den Compute-Knoten als **PSComputeNode** -Objekt an, auf dem dieses Cmdlet ein Benutzerkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="de76b-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de76b-128">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="de76b-128">-ComputeNodeId</span></span>
<span data-ttu-id="de76b-129">Gibt die ID des Compute-Knotens an, auf dem dieses Cmdlet ein Benutzerkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="de76b-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de76b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de76b-130">-DefaultProfile</span></span>
<span data-ttu-id="de76b-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="de76b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de76b-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="de76b-132">-ExpiryTime</span></span>
<span data-ttu-id="de76b-133">Gibt die Ablaufzeit für das neue Benutzerkonto an.</span><span class="sxs-lookup"><span data-stu-id="de76b-133">Specifies the expiry time for the new user account.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de76b-134">-IsAdmin</span><span class="sxs-lookup"><span data-stu-id="de76b-134">-IsAdmin</span></span>
<span data-ttu-id="de76b-135">Gibt an, dass das Cmdlet ein Benutzerkonto erstellt, das über Administratorberechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="de76b-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de76b-136">-Name</span><span class="sxs-lookup"><span data-stu-id="de76b-136">-Name</span></span>
<span data-ttu-id="de76b-137">Gibt den Namen des neuen lokalen Windows-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="de76b-137">Specifies the name of the new local Windows account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de76b-138">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="de76b-138">-Password</span></span>
<span data-ttu-id="de76b-139">Gibt das Kennwort für das Benutzerkonto an.</span><span class="sxs-lookup"><span data-stu-id="de76b-139">Specifies the user account password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de76b-140">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="de76b-140">-PoolId</span></span>
<span data-ttu-id="de76b-141">Gibt die ID des Pools an, der den Compute-Knoten enthält, für den das Benutzerkonto erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="de76b-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de76b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de76b-142">CommonParameters</span></span>
<span data-ttu-id="de76b-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de76b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de76b-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de76b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de76b-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="de76b-145">INPUTS</span></span>

### <span data-ttu-id="de76b-146">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="de76b-146">BatchAccountContext</span></span>
<span data-ttu-id="de76b-147">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="de76b-147">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="de76b-148">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="de76b-148">PSComputeNode</span></span>
<span data-ttu-id="de76b-149">Der Parameter "ComputeNode" akzeptiert den Wert vom Typ "PSComputeNode" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="de76b-149">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="de76b-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="de76b-150">OUTPUTS</span></span>

## <span data-ttu-id="de76b-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="de76b-151">NOTES</span></span>

## <span data-ttu-id="de76b-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="de76b-152">RELATED LINKS</span></span>

[<span data-ttu-id="de76b-153">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="de76b-153">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="de76b-154">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="de76b-154">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="de76b-155">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="de76b-155">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="de76b-156">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="de76b-156">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


