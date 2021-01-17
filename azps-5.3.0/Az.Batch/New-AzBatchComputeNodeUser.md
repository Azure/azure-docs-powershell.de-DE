---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
ms.openlocfilehash: 5695f0bf0a7cc65b1eb032be33116cc40ec0618e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471143"
---
# <span data-ttu-id="73799-101">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="73799-101">New-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="73799-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73799-102">SYNOPSIS</span></span>
<span data-ttu-id="73799-103">Erstellt ein Benutzerkonto auf einem Batchberechnungsknoten.</span><span class="sxs-lookup"><span data-stu-id="73799-103">Creates a user account on a Batch compute node.</span></span>

## <span data-ttu-id="73799-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73799-104">SYNTAX</span></span>

### <span data-ttu-id="73799-105">ID</span><span class="sxs-lookup"><span data-stu-id="73799-105">Id</span></span>
```
New-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73799-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="73799-106">ParentObject</span></span>
```
New-AzBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73799-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73799-107">DESCRIPTION</span></span>
<span data-ttu-id="73799-108">Das **Cmdlet "New-AzBatchComputeNodeUser"** erstellt ein Benutzerkonto für einen Azure Batch-Rechenknoten.</span><span class="sxs-lookup"><span data-stu-id="73799-108">The **New-AzBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="73799-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="73799-109">EXAMPLES</span></span>

### <span data-ttu-id="73799-110">Beispiel 1: Erstellen eines Benutzerkontos mit Administratoranmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="73799-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="73799-111">Mit diesem Befehl wird ein Benutzerkonto für den Rechenknoten erstellt, der die ID ComputeNode01 besitzt.</span><span class="sxs-lookup"><span data-stu-id="73799-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="73799-112">Der Knoten befindet sich in dem Pool mit der ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="73799-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="73799-113">Der Benutzername ist "TestUser", das Kennwort ist "Password", das Konto läuft in sieben Tagen ab, und das Konto verfügt über Administratoranmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="73799-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="73799-114">Beispiel 2: Erstellen eines Benutzerkontos auf einem Rechenknoten mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="73799-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="73799-115">Dieser Befehl ruft den Computeknoten "ComputeNode01" mit dem **Cmdlet "Get-AzBatchComputeNode"** ab.</span><span class="sxs-lookup"><span data-stu-id="73799-115">This command gets the compute node named ComputeNode01 by using the **Get-AzBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="73799-116">Dieser Knoten befindet sich in dem Pool mit der ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="73799-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="73799-117">Der Befehl übergibt diesen Rechenknoten mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73799-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="73799-118">Mit dem Befehl wird ein Benutzerkonto erstellt, das den Benutzernamen "TestUser" und das Kennwort "Password" hat.</span><span class="sxs-lookup"><span data-stu-id="73799-118">The command creates a user account that has the user name TestUser and the password Password.</span></span>

## <span data-ttu-id="73799-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73799-119">PARAMETERS</span></span>

### <span data-ttu-id="73799-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="73799-120">-BatchContext</span></span>
<span data-ttu-id="73799-121">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="73799-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="73799-122">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="73799-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="73799-123">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="73799-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="73799-124">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="73799-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="73799-125">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="73799-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="73799-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="73799-126">-ComputeNode</span></span>
<span data-ttu-id="73799-127">Gibt den Rechenknoten als ein **PSComputeNode-Objekt** an, für das dieses Cmdlet ein Benutzerkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="73799-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="73799-128">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="73799-128">-ComputeNodeId</span></span>
<span data-ttu-id="73799-129">Gibt die ID des Rechenknotens an, für den dieses Cmdlet ein Benutzerkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="73799-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="73799-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73799-130">-DefaultProfile</span></span>
<span data-ttu-id="73799-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="73799-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73799-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="73799-132">-ExpiryTime</span></span>
<span data-ttu-id="73799-133">Gibt die Ablaufzeit für das neue Benutzerkonto an.</span><span class="sxs-lookup"><span data-stu-id="73799-133">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="73799-134">-IsAdmin</span><span class="sxs-lookup"><span data-stu-id="73799-134">-IsAdmin</span></span>
<span data-ttu-id="73799-135">Gibt an, dass das Cmdlet ein Benutzerkonto mit Administratoranmeldeinformationen erstellt.</span><span class="sxs-lookup"><span data-stu-id="73799-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="73799-136">-Name</span><span class="sxs-lookup"><span data-stu-id="73799-136">-Name</span></span>
<span data-ttu-id="73799-137">Gibt den Namen des neuen lokalen Windows-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="73799-137">Specifies the name of the new local Windows account.</span></span>

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

### <span data-ttu-id="73799-138">-Password</span><span class="sxs-lookup"><span data-stu-id="73799-138">-Password</span></span>
<span data-ttu-id="73799-139">Gibt das Kennwort für das Benutzerkonto an.</span><span class="sxs-lookup"><span data-stu-id="73799-139">Specifies the user account password.</span></span>

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

### <span data-ttu-id="73799-140">-PoolId</span><span class="sxs-lookup"><span data-stu-id="73799-140">-PoolId</span></span>
<span data-ttu-id="73799-141">Gibt die ID des Pools an, der den Rechenknoten enthält, für den das Benutzerkonto erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="73799-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

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

### <span data-ttu-id="73799-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73799-142">CommonParameters</span></span>
<span data-ttu-id="73799-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73799-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73799-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73799-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73799-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="73799-145">INPUTS</span></span>

### <span data-ttu-id="73799-146">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="73799-146">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="73799-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="73799-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="73799-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="73799-148">OUTPUTS</span></span>

### <span data-ttu-id="73799-149">System.Void</span><span class="sxs-lookup"><span data-stu-id="73799-149">System.Void</span></span>

## <span data-ttu-id="73799-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="73799-150">NOTES</span></span>

## <span data-ttu-id="73799-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="73799-151">RELATED LINKS</span></span>

[<span data-ttu-id="73799-152">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="73799-152">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="73799-153">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="73799-153">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="73799-154">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="73799-154">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="73799-155">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="73799-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
