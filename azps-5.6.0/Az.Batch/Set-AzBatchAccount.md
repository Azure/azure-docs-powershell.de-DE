---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
ms.openlocfilehash: bbbe4c9b6a9832df490fee1668e953354b0c6d7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934339"
---
# <span data-ttu-id="52e1b-101">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="52e1b-101">Set-AzBatchAccount</span></span>

## <span data-ttu-id="52e1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52e1b-102">SYNOPSIS</span></span>
<span data-ttu-id="52e1b-103">Aktualisiert ein Batchkonto.</span><span class="sxs-lookup"><span data-stu-id="52e1b-103">Updates a Batch account.</span></span>

## <span data-ttu-id="52e1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52e1b-104">SYNTAX</span></span>

```
Set-AzBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52e1b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52e1b-105">DESCRIPTION</span></span>
<span data-ttu-id="52e1b-106">Das **Cmdlet Set-AzBatchAccount** aktualisiert ein Azure Batch-Konto.</span><span class="sxs-lookup"><span data-stu-id="52e1b-106">The **Set-AzBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="52e1b-107">Derzeit kann dieses Cmdlet nur Tags aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="52e1b-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="52e1b-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="52e1b-108">EXAMPLES</span></span>

### <span data-ttu-id="52e1b-109">Beispiel 1: Aktualisieren der Tags für ein Batchkonto</span><span class="sxs-lookup"><span data-stu-id="52e1b-109">Example 1: Update the tags on a Batch account</span></span>
```
PS C:\>Set-AzBatchAccount -AccountName "cmdletexample" -Tag @{key0="value0";key1=$null;key2="value2"}
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
                               Name  Value
                               ====  ======
                               key0  value0
                               key1
                               key2  value2
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="52e1b-110">Mit diesem Befehl werden die Tags für das Konto mit dem Namen "pfuller" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="52e1b-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="52e1b-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="52e1b-111">PARAMETERS</span></span>

### <span data-ttu-id="52e1b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="52e1b-112">-AccountName</span></span>
<span data-ttu-id="52e1b-113">Gibt den Namen des Batchkontos an, das dieses Cmdlet aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="52e1b-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52e1b-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="52e1b-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="52e1b-115">Gibt die Ressourcen-ID des Speicherkontos an, das für den automatischen Speicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="52e1b-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52e1b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52e1b-116">-DefaultProfile</span></span>
<span data-ttu-id="52e1b-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="52e1b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52e1b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52e1b-118">-ResourceGroupName</span></span>
<span data-ttu-id="52e1b-119">Gibt die Ressourcengruppe des Kontos an, das von diesem Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="52e1b-119">Specifies the resource group of the account that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52e1b-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="52e1b-120">-Tag</span></span>
<span data-ttu-id="52e1b-121">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="52e1b-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="52e1b-122">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="52e1b-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52e1b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52e1b-123">CommonParameters</span></span>
<span data-ttu-id="52e1b-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52e1b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52e1b-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52e1b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52e1b-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="52e1b-126">INPUTS</span></span>

### <span data-ttu-id="52e1b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="52e1b-127">System.String</span></span>

### <span data-ttu-id="52e1b-128">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="52e1b-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="52e1b-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="52e1b-129">OUTPUTS</span></span>

### <span data-ttu-id="52e1b-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="52e1b-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="52e1b-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="52e1b-131">NOTES</span></span>

## <span data-ttu-id="52e1b-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="52e1b-132">RELATED LINKS</span></span>

[<span data-ttu-id="52e1b-133">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="52e1b-133">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="52e1b-134">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="52e1b-134">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="52e1b-135">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="52e1b-135">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="52e1b-136">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="52e1b-136">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
