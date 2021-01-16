---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
ms.openlocfilehash: 636ceb216c7bb6aec2016bdd047a26f707108c9b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301520"
---
# <span data-ttu-id="9e0e3-101">Set-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="9e0e3-101">Set-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="9e0e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e0e3-102">SYNOPSIS</span></span>
<span data-ttu-id="9e0e3-103">Ändert die Eigenschaften eines Kontos auf einem Batchverarbeitungsknoten.</span><span class="sxs-lookup"><span data-stu-id="9e0e3-103">Modifies properties of an account on a Batch compute node.</span></span>

## <span data-ttu-id="9e0e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e0e3-104">SYNTAX</span></span>

```
Set-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e0e3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e0e3-105">DESCRIPTION</span></span>
<span data-ttu-id="9e0e3-106">Das **Cmdlet "Set-AzBatchComputeNodeUser"** ändert die Eigenschaften eines Benutzerkontos für einen Azure Batch-Rechenknoten.</span><span class="sxs-lookup"><span data-stu-id="9e0e3-106">The **Set-AzBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="9e0e3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9e0e3-107">EXAMPLES</span></span>

### <span data-ttu-id="9e0e3-108">Beispiel 1: Aktualisieren eines Benutzerkontos</span><span class="sxs-lookup"><span data-stu-id="9e0e3-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="9e0e3-109">Mit diesem Befehl wird das Benutzerkonto "PFuller" für den Rechenknoten geändert, der die angegebene ID im Pool "ContosoPool" hat.</span><span class="sxs-lookup"><span data-stu-id="9e0e3-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="9e0e3-110">Der Befehl ändert das Kontokennwort und die Ablaufzeit.</span><span class="sxs-lookup"><span data-stu-id="9e0e3-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="9e0e3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e0e3-111">PARAMETERS</span></span>

### <span data-ttu-id="9e0e3-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9e0e3-112">-BatchContext</span></span>
<span data-ttu-id="9e0e3-113">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9e0e3-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9e0e3-114">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e0e3-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9e0e3-115">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9e0e3-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9e0e3-116">Bei verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e0e3-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9e0e3-117">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9e0e3-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9e0e3-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="9e0e3-118">-ComputeNodeId</span></span>
<span data-ttu-id="9e0e3-119">Gibt die ID des Rechenknotens an, für den dieses Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e0e3-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9e0e3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e0e3-120">-DefaultProfile</span></span>
<span data-ttu-id="9e0e3-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e0e3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e0e3-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="9e0e3-122">-ExpiryTime</span></span>
<span data-ttu-id="9e0e3-123">Gibt die Ablaufzeit für das Benutzerkonto an.</span><span class="sxs-lookup"><span data-stu-id="9e0e3-123">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="9e0e3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9e0e3-124">-Name</span></span>
<span data-ttu-id="9e0e3-125">Gibt den Namen des Benutzerkontos an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9e0e3-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9e0e3-126">-Password</span><span class="sxs-lookup"><span data-stu-id="9e0e3-126">-Password</span></span>
<span data-ttu-id="9e0e3-127">Gibt das Kennwort für das Benutzerkonto an.</span><span class="sxs-lookup"><span data-stu-id="9e0e3-127">Specifies the password for the user account.</span></span>

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

### <span data-ttu-id="9e0e3-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="9e0e3-128">-PoolId</span></span>
<span data-ttu-id="9e0e3-129">Gibt die ID des Pools an, der den Rechenknoten enthält, für den dieses Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e0e3-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9e0e3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e0e3-130">CommonParameters</span></span>
<span data-ttu-id="9e0e3-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e0e3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e0e3-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e0e3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e0e3-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9e0e3-133">INPUTS</span></span>

### <span data-ttu-id="9e0e3-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9e0e3-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9e0e3-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9e0e3-135">OUTPUTS</span></span>

### <span data-ttu-id="9e0e3-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="9e0e3-136">System.Void</span></span>

## <span data-ttu-id="9e0e3-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9e0e3-137">NOTES</span></span>

## <span data-ttu-id="9e0e3-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9e0e3-138">RELATED LINKS</span></span>

[<span data-ttu-id="9e0e3-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="9e0e3-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="9e0e3-140">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="9e0e3-140">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="9e0e3-141">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="9e0e3-141">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="9e0e3-142">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="9e0e3-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
