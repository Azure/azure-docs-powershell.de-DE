---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
ms.openlocfilehash: 5695f0bf0a7cc65b1eb032be33116cc40ec0618e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009403"
---
# <span data-ttu-id="8a973-101">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="8a973-101">New-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="8a973-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a973-102">SYNOPSIS</span></span>
<span data-ttu-id="8a973-103">Erstellt ein Benutzerkonto in einem Batch Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="8a973-103">Creates a user account on a Batch compute node.</span></span>

## <span data-ttu-id="8a973-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a973-104">SYNTAX</span></span>

### <span data-ttu-id="8a973-105">ID</span><span class="sxs-lookup"><span data-stu-id="8a973-105">Id</span></span>
```
New-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a973-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="8a973-106">ParentObject</span></span>
```
New-AzBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a973-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a973-107">DESCRIPTION</span></span>
<span data-ttu-id="8a973-108">Das Cmdlet **New-AzBatchComputeNodeUser** erstellt ein Benutzerkonto in einem Azure Batch Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="8a973-108">The **New-AzBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="8a973-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a973-109">EXAMPLES</span></span>

### <span data-ttu-id="8a973-110">Beispiel 1: Erstellen eines Benutzerkontos mit administrativen Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="8a973-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="8a973-111">Mit diesem Befehl wird ein Benutzerkonto auf dem Compute-Knoten erstellt, das die ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="8a973-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="8a973-112">Der Knoten befindet sich im Pool mit der ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="8a973-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="8a973-113">Der Benutzername lautet testuser, das Kennwort ist Kennwort, das Konto läuft innerhalb von sieben Tagen ab, und das Konto verfügt über Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="8a973-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="8a973-114">Beispiel 2: Erstellen eines Benutzerkontos auf einem Compute-Knoten mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="8a973-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="8a973-115">Dieser Befehl ruft mit dem Cmdlet **Get-AzBatchComputeNode** den Compute-Knoten mit dem Namen ComputeNode01 ab.</span><span class="sxs-lookup"><span data-stu-id="8a973-115">This command gets the compute node named ComputeNode01 by using the **Get-AzBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="8a973-116">Dieser Knoten befindet sich im Pool mit der ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="8a973-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="8a973-117">Der Befehl übergibt diesen Compute-Knoten mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a973-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8a973-118">Der Befehl erstellt ein Benutzerkonto mit dem Benutzernamen testuser und dem Kennwort-Kennwort.</span><span class="sxs-lookup"><span data-stu-id="8a973-118">The command creates a user account that has the user name TestUser and the password Password.</span></span>

## <span data-ttu-id="8a973-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a973-119">PARAMETERS</span></span>

### <span data-ttu-id="8a973-120">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="8a973-120">-BatchContext</span></span>
<span data-ttu-id="8a973-121">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="8a973-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8a973-122">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="8a973-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8a973-123">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8a973-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8a973-124">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="8a973-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8a973-125">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="8a973-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8a973-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="8a973-126">-ComputeNode</span></span>
<span data-ttu-id="8a973-127">Gibt den Compute-Knoten als **PSComputeNode** -Objekt an, auf dem dieses Cmdlet ein Benutzerkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="8a973-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a973-128">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="8a973-128">-ComputeNodeId</span></span>
<span data-ttu-id="8a973-129">Gibt die ID des Compute-Knotens an, auf dem dieses Cmdlet ein Benutzerkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="8a973-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a973-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a973-130">-DefaultProfile</span></span>
<span data-ttu-id="8a973-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a973-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a973-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8a973-132">-ExpiryTime</span></span>
<span data-ttu-id="8a973-133">Gibt die Ablaufzeit für das neue Benutzerkonto an.</span><span class="sxs-lookup"><span data-stu-id="8a973-133">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="8a973-134">-IsAdmin</span><span class="sxs-lookup"><span data-stu-id="8a973-134">-IsAdmin</span></span>
<span data-ttu-id="8a973-135">Gibt an, dass das Cmdlet ein Benutzerkonto erstellt, das über Administratorberechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="8a973-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a973-136">-Name</span><span class="sxs-lookup"><span data-stu-id="8a973-136">-Name</span></span>
<span data-ttu-id="8a973-137">Gibt den Namen des neuen lokalen Windows-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="8a973-137">Specifies the name of the new local Windows account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a973-138">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="8a973-138">-Password</span></span>
<span data-ttu-id="8a973-139">Gibt das Kennwort für das Benutzerkonto an.</span><span class="sxs-lookup"><span data-stu-id="8a973-139">Specifies the user account password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a973-140">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="8a973-140">-PoolId</span></span>
<span data-ttu-id="8a973-141">Gibt die ID des Pools an, der den Compute-Knoten enthält, für den das Benutzerkonto erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a973-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a973-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a973-142">CommonParameters</span></span>
<span data-ttu-id="8a973-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a973-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a973-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a973-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a973-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a973-145">INPUTS</span></span>

### <span data-ttu-id="8a973-146">Microsoft.Azure.Commands.Batch. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="8a973-146">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="8a973-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8a973-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8a973-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a973-148">OUTPUTS</span></span>

### <span data-ttu-id="8a973-149">System. void</span><span class="sxs-lookup"><span data-stu-id="8a973-149">System.Void</span></span>

## <span data-ttu-id="8a973-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a973-150">NOTES</span></span>

## <span data-ttu-id="8a973-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a973-151">RELATED LINKS</span></span>

[<span data-ttu-id="8a973-152">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8a973-152">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8a973-153">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="8a973-153">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="8a973-154">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="8a973-154">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="8a973-155">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8a973-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
