---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
ms.openlocfilehash: ee5ae846ed83065b797f1389827d7d53ae1988d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950376"
---
# <span data-ttu-id="eb4b4-101">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="eb4b4-101">New-AzBatchAccountKey</span></span>

## <span data-ttu-id="eb4b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb4b4-102">SYNOPSIS</span></span>
<span data-ttu-id="eb4b4-103">Generiert einen Schlüssel eines Batchkontos neu.</span><span class="sxs-lookup"><span data-stu-id="eb4b4-103">Regenerates a key of a Batch account.</span></span>

## <span data-ttu-id="eb4b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb4b4-104">SYNTAX</span></span>

```
New-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb4b4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb4b4-105">DESCRIPTION</span></span>
<span data-ttu-id="eb4b4-106">Das **Cmdlet New-AzBatchAccountKey** regeneriert den Primär- oder Sekundärschlüssel eines Azure Batch-Kontos.</span><span class="sxs-lookup"><span data-stu-id="eb4b4-106">The **New-AzBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="eb4b4-107">Das Cmdlet gibt ein **BatchAccountContext-Objekt zurück,** das über die aktuellen **Eigenschaften PrimaryAccountKey** und **SecondaryAccountKey** verfügt.</span><span class="sxs-lookup"><span data-stu-id="eb4b4-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="eb4b4-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eb4b4-108">EXAMPLES</span></span>

### <span data-ttu-id="eb4b4-109">Beispiel 1: Regenerieren des Primärkontoschlüssels für ein Batchkonto</span><span class="sxs-lookup"><span data-stu-id="eb4b4-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
```
PS C:\>New-AzBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="eb4b4-110">Mit diesem Befehl wird der Primärkontoschlüssel im Batchkonto mit dem Namen "pfuller" neu generiert.</span><span class="sxs-lookup"><span data-stu-id="eb4b4-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="eb4b4-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="eb4b4-111">PARAMETERS</span></span>

### <span data-ttu-id="eb4b4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eb4b4-112">-AccountName</span></span>
<span data-ttu-id="eb4b4-113">Gibt den Namen des Batchkontos an, für das dieses Cmdlet einen Schlüssel neu generiert.</span><span class="sxs-lookup"><span data-stu-id="eb4b4-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="eb4b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb4b4-114">-DefaultProfile</span></span>
<span data-ttu-id="eb4b4-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb4b4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb4b4-116">-KeyType</span><span class="sxs-lookup"><span data-stu-id="eb4b4-116">-KeyType</span></span>
<span data-ttu-id="eb4b4-117">Gibt den Schlüsseltyp an, den dieses Cmdlet neu generiert.</span><span class="sxs-lookup"><span data-stu-id="eb4b4-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="eb4b4-118">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="eb4b4-118">Valid values are:</span></span>
- <span data-ttu-id="eb4b4-119">Primär</span><span class="sxs-lookup"><span data-stu-id="eb4b4-119">Primary</span></span>
- <span data-ttu-id="eb4b4-120">Sekundär</span><span class="sxs-lookup"><span data-stu-id="eb4b4-120">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb4b4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb4b4-121">-ResourceGroupName</span></span>
<span data-ttu-id="eb4b4-122">Gibt die Ressourcengruppe des Kontos an, für das dieses Cmdlet einen Schlüssel neu generiert.</span><span class="sxs-lookup"><span data-stu-id="eb4b4-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="eb4b4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb4b4-123">CommonParameters</span></span>
<span data-ttu-id="eb4b4-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb4b4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb4b4-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb4b4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb4b4-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eb4b4-126">INPUTS</span></span>

### <span data-ttu-id="eb4b4-127">System.String</span><span class="sxs-lookup"><span data-stu-id="eb4b4-127">System.String</span></span>

## <span data-ttu-id="eb4b4-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eb4b4-128">OUTPUTS</span></span>

### <span data-ttu-id="eb4b4-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="eb4b4-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="eb4b4-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="eb4b4-130">NOTES</span></span>

## <span data-ttu-id="eb4b4-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="eb4b4-131">RELATED LINKS</span></span>

[<span data-ttu-id="eb4b4-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="eb4b4-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="eb4b4-133">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="eb4b4-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
