---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 6289aa916b4d03559fccb11ea0a8897f4b506b53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497906"
---
# <span data-ttu-id="eb4ce-101">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="eb4ce-101">New-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="eb4ce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eb4ce-102">SYNOPSIS</span></span>
<span data-ttu-id="eb4ce-103">Erstellt ein Benutzerkonto in einem Batch Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="eb4ce-103">Creates a user account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb4ce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb4ce-104">SYNTAX</span></span>

### <span data-ttu-id="eb4ce-105">ID</span><span class="sxs-lookup"><span data-stu-id="eb4ce-105">Id</span></span>
```
New-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <String>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb4ce-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="eb4ce-106">ParentObject</span></span>
```
New-AzureBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <String>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb4ce-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb4ce-107">DESCRIPTION</span></span>
<span data-ttu-id="eb4ce-108">Das Cmdlet **New-AzureBatchComputeNodeUser** erstellt ein Benutzerkonto in einem Azure Batch Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="eb4ce-108">The **New-AzureBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="eb4ce-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb4ce-109">EXAMPLES</span></span>

### <span data-ttu-id="eb4ce-110">Beispiel 1: Erstellen eines Benutzerkontos mit administrativen Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="eb4ce-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzureBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="eb4ce-111">Mit diesem Befehl wird ein Benutzerkonto auf dem Compute-Knoten erstellt, das die ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="eb4ce-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="eb4ce-112">Der Knoten befindet sich im Pool mit der ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="eb4ce-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="eb4ce-113">Der Benutzername lautet testuser, das Kennwort ist Kennwort, das Konto läuft innerhalb von sieben Tagen ab, und das Konto verfügt über Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="eb4ce-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="eb4ce-114">Beispiel 2: Erstellen eines Benutzerkontos auf einem Compute-Knoten mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="eb4ce-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzureBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="eb4ce-115">Dieser Befehl ruft mit dem Cmdlet **Get-AzureBatchComputeNode** den Compute-Knoten mit dem Namen ComputeNode01 ab.</span><span class="sxs-lookup"><span data-stu-id="eb4ce-115">This command gets the compute node named ComputeNode01 by using the **Get-AzureBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="eb4ce-116">Dieser Knoten befindet sich im Pool mit der ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="eb4ce-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="eb4ce-117">Der Befehl übergibt diesen Compute-Knoten mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb4ce-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="eb4ce-118">Der Befehl erstellt ein Benutzerkonto mit dem Benutzernamen TestUserand Kennwort.</span><span class="sxs-lookup"><span data-stu-id="eb4ce-118">The command creates a user account that has the user name TestUserand the password Password.</span></span>

## <span data-ttu-id="eb4ce-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb4ce-119">PARAMETERS</span></span>

### <span data-ttu-id="eb4ce-120">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="eb4ce-120">-BatchContext</span></span>
<span data-ttu-id="eb4ce-121">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="eb4ce-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="eb4ce-122">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb4ce-122">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="eb4ce-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="eb4ce-123">-ComputeNode</span></span>
<span data-ttu-id="eb4ce-124">Gibt den Compute-Knoten als **PSComputeNode** -Objekt an, auf dem dieses Cmdlet ein Benutzerkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="eb4ce-124">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="eb4ce-125">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="eb4ce-125">-ComputeNodeId</span></span>
<span data-ttu-id="eb4ce-126">Gibt die ID des Compute-Knotens an, auf dem dieses Cmdlet ein Benutzerkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="eb4ce-126">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="eb4ce-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="eb4ce-127">-ExpiryTime</span></span>
<span data-ttu-id="eb4ce-128">Gibt die Ablaufzeit für das neue Benutzerkonto an.</span><span class="sxs-lookup"><span data-stu-id="eb4ce-128">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="eb4ce-129">-IsAdmin</span><span class="sxs-lookup"><span data-stu-id="eb4ce-129">-IsAdmin</span></span>
<span data-ttu-id="eb4ce-130">Gibt an, dass das Cmdlet ein Benutzerkonto erstellt, das über Administratorberechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="eb4ce-130">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="eb4ce-131">-Name</span><span class="sxs-lookup"><span data-stu-id="eb4ce-131">-Name</span></span>
<span data-ttu-id="eb4ce-132">Gibt den Namen des neuen lokalen Windows-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="eb4ce-132">Specifies the name of the new local Windows account.</span></span>

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

### <span data-ttu-id="eb4ce-133">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="eb4ce-133">-Password</span></span>
<span data-ttu-id="eb4ce-134">Gibt das Kennwort für das Benutzerkonto an.</span><span class="sxs-lookup"><span data-stu-id="eb4ce-134">Specifies the user account password.</span></span>

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

### <span data-ttu-id="eb4ce-135">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="eb4ce-135">-PoolId</span></span>
<span data-ttu-id="eb4ce-136">Gibt die ID des Pools an, der den Compute-Knoten enthält, für den das Benutzerkonto erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb4ce-136">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

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

### <span data-ttu-id="eb4ce-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb4ce-137">-DefaultProfile</span></span>
<span data-ttu-id="eb4ce-138">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eb4ce-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb4ce-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb4ce-139">CommonParameters</span></span>
<span data-ttu-id="eb4ce-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb4ce-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb4ce-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb4ce-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb4ce-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eb4ce-142">INPUTS</span></span>

### <span data-ttu-id="eb4ce-143">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="eb4ce-143">BatchAccountContext</span></span>
<span data-ttu-id="eb4ce-144">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="eb4ce-144">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="eb4ce-145">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="eb4ce-145">PSComputeNode</span></span>
<span data-ttu-id="eb4ce-146">Der Parameter "ComputeNode" akzeptiert den Wert vom Typ "PSComputeNode" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="eb4ce-146">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="eb4ce-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eb4ce-147">OUTPUTS</span></span>

## <span data-ttu-id="eb4ce-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="eb4ce-148">NOTES</span></span>

## <span data-ttu-id="eb4ce-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eb4ce-149">RELATED LINKS</span></span>

[<span data-ttu-id="eb4ce-150">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="eb4ce-150">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="eb4ce-151">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="eb4ce-151">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="eb4ce-152">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="eb4ce-152">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="eb4ce-153">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="eb4ce-153">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


