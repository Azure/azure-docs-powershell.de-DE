---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
ms.openlocfilehash: 124000fdf11b3fa5b90253fc3b9a75c040725ba8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499221"
---
# <span data-ttu-id="09ec3-101">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="09ec3-101">Disable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="09ec3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09ec3-102">SYNOPSIS</span></span>
<span data-ttu-id="09ec3-103">Deaktiviert die automatische Skalierung eines Pools.</span><span class="sxs-lookup"><span data-stu-id="09ec3-103">Disables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09ec3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09ec3-104">SYNTAX</span></span>

```
Disable-AzureBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09ec3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09ec3-105">DESCRIPTION</span></span>
<span data-ttu-id="09ec3-106">Das Cmdlet **Disable-AzureBatchAutoScale** deaktiviert die automatische Skalierung des angegebenen Pools.</span><span class="sxs-lookup"><span data-stu-id="09ec3-106">The **Disable-AzureBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="09ec3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09ec3-107">EXAMPLES</span></span>

### <span data-ttu-id="09ec3-108">Beispiel 1: Deaktivieren der automatischen Skalierung eines Pools</span><span class="sxs-lookup"><span data-stu-id="09ec3-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzureBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="09ec3-109">Mit diesem Befehl wird die automatische Skalierung für den Pool mit dem Namen MyPool deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="09ec3-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="09ec3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="09ec3-110">PARAMETERS</span></span>

### <span data-ttu-id="09ec3-111">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="09ec3-111">-BatchContext</span></span>
<span data-ttu-id="09ec3-112">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="09ec3-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="09ec3-113">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09ec3-113">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="09ec3-114">-ID</span><span class="sxs-lookup"><span data-stu-id="09ec3-114">-Id</span></span>
<span data-ttu-id="09ec3-115">Gibt die Objekt-ID des Pools an.</span><span class="sxs-lookup"><span data-stu-id="09ec3-115">Specifies the object ID of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09ec3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09ec3-116">-DefaultProfile</span></span>
<span data-ttu-id="09ec3-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="09ec3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09ec3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09ec3-118">CommonParameters</span></span>
<span data-ttu-id="09ec3-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09ec3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09ec3-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09ec3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09ec3-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09ec3-121">INPUTS</span></span>

### <span data-ttu-id="09ec3-122">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="09ec3-122">BatchAccountContext</span></span>
<span data-ttu-id="09ec3-123">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="09ec3-123">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="09ec3-124">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="09ec3-124">String</span></span>
<span data-ttu-id="09ec3-125">Der Parameter "ID" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="09ec3-125">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="09ec3-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09ec3-126">OUTPUTS</span></span>

## <span data-ttu-id="09ec3-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="09ec3-127">NOTES</span></span>

## <span data-ttu-id="09ec3-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09ec3-128">RELATED LINKS</span></span>

[<span data-ttu-id="09ec3-129">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="09ec3-129">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="09ec3-130">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="09ec3-130">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="09ec3-131">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="09ec3-131">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


