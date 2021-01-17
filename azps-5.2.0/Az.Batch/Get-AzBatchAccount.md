---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
ms.openlocfilehash: 66bab11ab5632464eed8ee160df527b0e44f053d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373007"
---
# <span data-ttu-id="7c69d-101">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7c69d-101">Get-AzBatchAccount</span></span>

## <span data-ttu-id="7c69d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c69d-102">SYNOPSIS</span></span>
<span data-ttu-id="7c69d-103">Ruft ein Batchkonto im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="7c69d-103">Gets a Batch account in the current subscription.</span></span>

## <span data-ttu-id="7c69d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c69d-104">SYNTAX</span></span>

```
Get-AzBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c69d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c69d-105">DESCRIPTION</span></span>
<span data-ttu-id="7c69d-106">Das **Get-AzBatchAccount-Cmdlet** erhält im aktuellen Abonnement ein Azure-Batch-Konto.</span><span class="sxs-lookup"><span data-stu-id="7c69d-106">The **Get-AzBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="7c69d-107">Sie können den Parameter *"AccountName"* verwenden, um ein einzelnes Konto zu erhalten, oder Sie können den Parameter *"ResourceGroupName"* verwenden, um Konten unter dieser Ressourcengruppe zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7c69d-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="7c69d-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7c69d-108">EXAMPLES</span></span>

### <span data-ttu-id="7c69d-109">Beispiel 1: Erhalten eines Batchkontos nach Name</span><span class="sxs-lookup"><span data-stu-id="7c69d-109">Example 1: Get a batch account by name</span></span>
```
PS C:\>Get-AzBatchAccount -AccountName "pfuller"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://pfuller.westus.batch.azure.com
```

<span data-ttu-id="7c69d-110">Dieser Befehl ruft das Batchkonto namens "pfuller" ab.</span><span class="sxs-lookup"><span data-stu-id="7c69d-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="7c69d-111">Beispiel 2: Erhalten der einer Ressourcengruppe zugeordneten Batchkonten</span><span class="sxs-lookup"><span data-stu-id="7c69d-111">Example 2: Get the batch accounts associated with a resource group</span></span>
```
PS C:\>Get-AzBatchAccount -ResourceGroupName "CmdletExampleRG"
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
AccountName                  : cmdletexample2
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="7c69d-112">Dieser Befehl ruft die Batchkonten ab, die der Ressourcengruppe "CmdletExampleRG" zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7c69d-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="7c69d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c69d-113">PARAMETERS</span></span>

### <span data-ttu-id="7c69d-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7c69d-114">-AccountName</span></span>
<span data-ttu-id="7c69d-115">Gibt den Namen eines Kontos an.</span><span class="sxs-lookup"><span data-stu-id="7c69d-115">Specifies the name of an account.</span></span>
<span data-ttu-id="7c69d-116">Wenn Sie einen Kontonamen angeben, gibt dieses Cmdlet nur dieses Konto zurück.</span><span class="sxs-lookup"><span data-stu-id="7c69d-116">If you specify an account name, this cmdlet only returns that account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c69d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c69d-117">-DefaultProfile</span></span>
<span data-ttu-id="7c69d-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c69d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c69d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c69d-119">-ResourceGroupName</span></span>
<span data-ttu-id="7c69d-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7c69d-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="7c69d-121">Wenn Sie eine Ressourcengruppe angeben, ruft dieses Cmdlet die Konten unter der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="7c69d-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c69d-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="7c69d-122">-Tag</span></span>
<span data-ttu-id="7c69d-123">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7c69d-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7c69d-124">Beispiel: @{key0="value0";key1=$null;key2="value2"} Dieses Cmdlet ruft Konten ab, die die von diesem Parameter angegebenen Tags enthalten.</span><span class="sxs-lookup"><span data-stu-id="7c69d-124">For example: @{key0="value0";key1=$null;key2="value2"} This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c69d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c69d-125">CommonParameters</span></span>
<span data-ttu-id="7c69d-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c69d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c69d-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c69d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c69d-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7c69d-128">INPUTS</span></span>

### <span data-ttu-id="7c69d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="7c69d-129">System.String</span></span>

### <span data-ttu-id="7c69d-130">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7c69d-130">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7c69d-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7c69d-131">OUTPUTS</span></span>

### <span data-ttu-id="7c69d-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7c69d-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7c69d-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7c69d-133">NOTES</span></span>

## <span data-ttu-id="7c69d-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7c69d-134">RELATED LINKS</span></span>

[<span data-ttu-id="7c69d-135">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7c69d-135">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="7c69d-136">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7c69d-136">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="7c69d-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7c69d-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="7c69d-138">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7c69d-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
