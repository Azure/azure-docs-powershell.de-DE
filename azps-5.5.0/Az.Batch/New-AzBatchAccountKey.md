---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
ms.openlocfilehash: 121e4b4b2ffe25d9e5ae53cb03e60cb7a1da91b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171474"
---
# <span data-ttu-id="54942-101">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="54942-101">New-AzBatchAccountKey</span></span>

## <span data-ttu-id="54942-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54942-102">SYNOPSIS</span></span>
<span data-ttu-id="54942-103">Generiert einen Schlüssel eines Batchkontos erneut.</span><span class="sxs-lookup"><span data-stu-id="54942-103">Regenerates a key of a Batch account.</span></span>

## <span data-ttu-id="54942-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54942-104">SYNTAX</span></span>

```
New-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54942-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54942-105">DESCRIPTION</span></span>
<span data-ttu-id="54942-106">Das **Cmdlet "New-AzBatchAccountKey"** generiert den primären oder sekundären Schlüssel eines Azure Batch-Kontos erneut.</span><span class="sxs-lookup"><span data-stu-id="54942-106">The **New-AzBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="54942-107">Das Cmdlet gibt ein **BatchAccountContext-Objekt** zurück, das die aktuellen **Eigenschaften "PrimaryAccountKey"** und **"SecondaryAccountKey"** enthält.</span><span class="sxs-lookup"><span data-stu-id="54942-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="54942-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="54942-108">EXAMPLES</span></span>

### <span data-ttu-id="54942-109">Beispiel 1: Erneut erstellen des Primärkontoschlüssels für ein Batchkonto</span><span class="sxs-lookup"><span data-stu-id="54942-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
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

<span data-ttu-id="54942-110">Mit diesem Befehl wird der Primärkontoschlüssel für das Batchkonto mit dem Namen "pfuller" erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="54942-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="54942-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54942-111">PARAMETERS</span></span>

### <span data-ttu-id="54942-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="54942-112">-AccountName</span></span>
<span data-ttu-id="54942-113">Gibt den Namen des Batchkontos an, für das dieses Cmdlet einen Schlüssel erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="54942-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="54942-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54942-114">-DefaultProfile</span></span>
<span data-ttu-id="54942-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54942-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54942-116">-KeyType</span><span class="sxs-lookup"><span data-stu-id="54942-116">-KeyType</span></span>
<span data-ttu-id="54942-117">Gibt den Schlüsseltyp an, den dieses Cmdlet erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="54942-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="54942-118">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="54942-118">Valid values are:</span></span>
- <span data-ttu-id="54942-119">Primär</span><span class="sxs-lookup"><span data-stu-id="54942-119">Primary</span></span>
- <span data-ttu-id="54942-120">Sekundär</span><span class="sxs-lookup"><span data-stu-id="54942-120">Secondary</span></span>

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

### <span data-ttu-id="54942-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54942-121">-ResourceGroupName</span></span>
<span data-ttu-id="54942-122">Gibt die Ressourcengruppe des Kontos an, für das dieses Cmdlet einen Schlüssel erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="54942-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="54942-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54942-123">CommonParameters</span></span>
<span data-ttu-id="54942-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54942-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54942-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54942-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54942-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="54942-126">INPUTS</span></span>

### <span data-ttu-id="54942-127">System.String</span><span class="sxs-lookup"><span data-stu-id="54942-127">System.String</span></span>

## <span data-ttu-id="54942-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="54942-128">OUTPUTS</span></span>

### <span data-ttu-id="54942-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="54942-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="54942-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="54942-130">NOTES</span></span>

## <span data-ttu-id="54942-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="54942-131">RELATED LINKS</span></span>

[<span data-ttu-id="54942-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="54942-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="54942-133">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="54942-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
