---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
ms.openlocfilehash: a5e8fd6e6cfba8832365f385cc90357bac59efb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497873"
---
# <span data-ttu-id="0b6b0-101">Set-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="0b6b0-101">Set-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="0b6b0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b6b0-102">SYNOPSIS</span></span>
<span data-ttu-id="0b6b0-103">Ändert die Eigenschaften eines Kontos in einem Batch Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="0b6b0-103">Modifies properties of an account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b6b0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b6b0-104">SYNTAX</span></span>

```
Set-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <String> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b6b0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b6b0-105">DESCRIPTION</span></span>
<span data-ttu-id="0b6b0-106">Das Cmdlet " **Satz-AzureBatchComputeNodeUser** " ändert die Eigenschaften eines Benutzerkontos in einem Azure Batch Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="0b6b0-106">The **Set-AzureBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="0b6b0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b6b0-107">EXAMPLES</span></span>

### <span data-ttu-id="0b6b0-108">Beispiel 1: Aktualisieren eines Benutzerkontos</span><span class="sxs-lookup"><span data-stu-id="0b6b0-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzureBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="0b6b0-109">Mit diesem Befehl wird das Benutzerkonto mit dem Namen PFuller auf dem Compute-Knoten geändert, der die angegebene ID im Pool mit dem Namen ContosoPool aufweist.</span><span class="sxs-lookup"><span data-stu-id="0b6b0-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="0b6b0-110">Der Befehl ändert das Kennwort für das Konto und die Ablaufzeit.</span><span class="sxs-lookup"><span data-stu-id="0b6b0-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="0b6b0-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b6b0-111">PARAMETERS</span></span>

### <span data-ttu-id="0b6b0-112">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="0b6b0-112">-BatchContext</span></span>
<span data-ttu-id="0b6b0-113">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b6b0-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0b6b0-114">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b6b0-114">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="0b6b0-115">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="0b6b0-115">-ComputeNodeId</span></span>
<span data-ttu-id="0b6b0-116">Gibt die ID des Compute-Knotens an, auf dem dieses Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b6b0-116">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="0b6b0-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="0b6b0-117">-ExpiryTime</span></span>
<span data-ttu-id="0b6b0-118">Gibt die Ablaufzeit für das Benutzerkonto an.</span><span class="sxs-lookup"><span data-stu-id="0b6b0-118">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="0b6b0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0b6b0-119">-Name</span></span>
<span data-ttu-id="0b6b0-120">Gibt den Namen des Benutzerkontos an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0b6b0-120">Specifies the name of the user account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0b6b0-121">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="0b6b0-121">-Password</span></span>
<span data-ttu-id="0b6b0-122">Gibt das Kennwort für das Benutzerkonto an.</span><span class="sxs-lookup"><span data-stu-id="0b6b0-122">Specifies the password for the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b6b0-123">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="0b6b0-123">-PoolId</span></span>
<span data-ttu-id="0b6b0-124">Gibt die ID des Pools an, der den Compute-Knoten enthält, auf dem dieses Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b6b0-124">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="0b6b0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b6b0-125">-DefaultProfile</span></span>
<span data-ttu-id="0b6b0-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b6b0-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b6b0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b6b0-127">CommonParameters</span></span>
<span data-ttu-id="0b6b0-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b6b0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b6b0-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b6b0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b6b0-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b6b0-130">INPUTS</span></span>

### <span data-ttu-id="0b6b0-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0b6b0-131">BatchAccountContext</span></span>
<span data-ttu-id="0b6b0-132">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0b6b0-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="0b6b0-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b6b0-133">OUTPUTS</span></span>

## <span data-ttu-id="0b6b0-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b6b0-134">NOTES</span></span>

## <span data-ttu-id="0b6b0-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b6b0-135">RELATED LINKS</span></span>

[<span data-ttu-id="0b6b0-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0b6b0-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="0b6b0-137">Neu – AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="0b6b0-137">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="0b6b0-138">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="0b6b0-138">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="0b6b0-139">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0b6b0-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


