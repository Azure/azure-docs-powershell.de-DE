---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
ms.openlocfilehash: 52fea755708645173a5f0f3429591a384ec63b01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164236"
---
# <span data-ttu-id="34059-101">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="34059-101">Remove-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="34059-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34059-102">SYNOPSIS</span></span>
<span data-ttu-id="34059-103">Löscht ein Benutzerkonto aus einem Batchverarbeitungsknoten.</span><span class="sxs-lookup"><span data-stu-id="34059-103">Deletes a user account from a Batch compute node.</span></span>

## <span data-ttu-id="34059-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34059-104">SYNTAX</span></span>

```
Remove-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34059-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34059-105">DESCRIPTION</span></span>
<span data-ttu-id="34059-106">Das **Cmdlet "Remove-AzBatchComputeNodeUser"** löscht ein Benutzerkonto aus einem Azure Batch-Computeknoten.</span><span class="sxs-lookup"><span data-stu-id="34059-106">The **Remove-AzBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="34059-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="34059-107">EXAMPLES</span></span>

### <span data-ttu-id="34059-108">Beispiel 1: Löschen eines Benutzers aus einem Rechenknoten ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="34059-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="34059-109">Mit diesem Befehl wird der Benutzer "User14" aus dem Computeknoten "ComputeNode01" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="34059-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="34059-110">Der Rechenknoten befindet sich im Pool namens "Pool01".</span><span class="sxs-lookup"><span data-stu-id="34059-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="34059-111">Dieser Befehl gibt den Parameter *"Force"* an.</span><span class="sxs-lookup"><span data-stu-id="34059-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="34059-112">Daher fordert Sie der Befehl nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="34059-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="34059-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34059-113">PARAMETERS</span></span>

### <span data-ttu-id="34059-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="34059-114">-BatchContext</span></span>
<span data-ttu-id="34059-115">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34059-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="34059-116">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="34059-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="34059-117">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="34059-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="34059-118">Bei verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="34059-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="34059-119">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="34059-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="34059-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="34059-120">-ComputeNodeId</span></span>
<span data-ttu-id="34059-121">Gibt die ID des Rechenknotens an, für den dieses Cmdlet das Benutzerkonto löscht.</span><span class="sxs-lookup"><span data-stu-id="34059-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

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

### <span data-ttu-id="34059-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34059-122">-DefaultProfile</span></span>
<span data-ttu-id="34059-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="34059-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34059-124">-Name</span><span class="sxs-lookup"><span data-stu-id="34059-124">-Name</span></span>
<span data-ttu-id="34059-125">Gibt den Namen des zu löschenden Benutzerkontos an.</span><span class="sxs-lookup"><span data-stu-id="34059-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="34059-126">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="34059-126">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34059-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="34059-127">-PoolId</span></span>
<span data-ttu-id="34059-128">Gibt die ID des Pools an, der den Rechenknoten enthält, für den das Benutzerkonto gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="34059-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="34059-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34059-129">-Confirm</span></span>
<span data-ttu-id="34059-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="34059-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34059-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="34059-131">-WhatIf</span></span>
<span data-ttu-id="34059-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34059-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34059-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34059-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34059-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34059-134">CommonParameters</span></span>
<span data-ttu-id="34059-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34059-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34059-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34059-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34059-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="34059-137">INPUTS</span></span>

### <span data-ttu-id="34059-138">System.String</span><span class="sxs-lookup"><span data-stu-id="34059-138">System.String</span></span>

### <span data-ttu-id="34059-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="34059-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="34059-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="34059-140">OUTPUTS</span></span>

### <span data-ttu-id="34059-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="34059-141">System.Void</span></span>

## <span data-ttu-id="34059-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="34059-142">NOTES</span></span>

## <span data-ttu-id="34059-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="34059-143">RELATED LINKS</span></span>

[<span data-ttu-id="34059-144">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="34059-144">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="34059-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="34059-145">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="34059-146">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="34059-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
