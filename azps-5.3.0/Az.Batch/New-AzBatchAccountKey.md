---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
ms.openlocfilehash: 121e4b4b2ffe25d9e5ae53cb03e60cb7a1da91b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471149"
---
# <span data-ttu-id="9b092-101">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="9b092-101">New-AzBatchAccountKey</span></span>

## <span data-ttu-id="9b092-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b092-102">SYNOPSIS</span></span>
<span data-ttu-id="9b092-103">Generiert einen Schlüssel eines Batchkontos erneut.</span><span class="sxs-lookup"><span data-stu-id="9b092-103">Regenerates a key of a Batch account.</span></span>

## <span data-ttu-id="9b092-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b092-104">SYNTAX</span></span>

```
New-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b092-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b092-105">DESCRIPTION</span></span>
<span data-ttu-id="9b092-106">Das **Cmdlet "New-AzBatchAccountKey"** generiert den primären oder sekundären Schlüssel eines Azure Batch-Kontos erneut.</span><span class="sxs-lookup"><span data-stu-id="9b092-106">The **New-AzBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="9b092-107">Das Cmdlet gibt ein **BatchAccountContext-Objekt** zurück, das die aktuellen **Eigenschaften "PrimaryAccountKey"** und **"SecondaryAccountKey"** enthält.</span><span class="sxs-lookup"><span data-stu-id="9b092-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="9b092-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9b092-108">EXAMPLES</span></span>

### <span data-ttu-id="9b092-109">Beispiel 1: Erneut erstellen des Primärkontoschlüssels für ein Batchkonto</span><span class="sxs-lookup"><span data-stu-id="9b092-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
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

<span data-ttu-id="9b092-110">Mit diesem Befehl wird der Primärkontoschlüssel für das Batchkonto mit dem Namen "pfuller" erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="9b092-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="9b092-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b092-111">PARAMETERS</span></span>

### <span data-ttu-id="9b092-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9b092-112">-AccountName</span></span>
<span data-ttu-id="9b092-113">Gibt den Namen des Batchkontos an, für das dieses Cmdlet einen Schlüssel erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="9b092-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="9b092-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b092-114">-DefaultProfile</span></span>
<span data-ttu-id="9b092-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b092-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b092-116">-KeyType</span><span class="sxs-lookup"><span data-stu-id="9b092-116">-KeyType</span></span>
<span data-ttu-id="9b092-117">Gibt den Schlüsseltyp an, den dieses Cmdlet erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="9b092-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="9b092-118">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="9b092-118">Valid values are:</span></span>
- <span data-ttu-id="9b092-119">Primär</span><span class="sxs-lookup"><span data-stu-id="9b092-119">Primary</span></span>
- <span data-ttu-id="9b092-120">Sekundär</span><span class="sxs-lookup"><span data-stu-id="9b092-120">Secondary</span></span>

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

### <span data-ttu-id="9b092-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b092-121">-ResourceGroupName</span></span>
<span data-ttu-id="9b092-122">Gibt die Ressourcengruppe des Kontos an, für das dieses Cmdlet einen Schlüssel erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="9b092-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="9b092-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b092-123">CommonParameters</span></span>
<span data-ttu-id="9b092-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b092-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b092-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b092-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b092-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9b092-126">INPUTS</span></span>

### <span data-ttu-id="9b092-127">System.String</span><span class="sxs-lookup"><span data-stu-id="9b092-127">System.String</span></span>

## <span data-ttu-id="9b092-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9b092-128">OUTPUTS</span></span>

### <span data-ttu-id="9b092-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9b092-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9b092-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9b092-130">NOTES</span></span>

## <span data-ttu-id="9b092-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9b092-131">RELATED LINKS</span></span>

[<span data-ttu-id="9b092-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="9b092-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="9b092-133">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="9b092-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
