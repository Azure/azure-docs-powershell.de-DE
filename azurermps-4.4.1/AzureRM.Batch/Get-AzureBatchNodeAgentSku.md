---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
ms.openlocfilehash: e29b5df4a72ff21dbacb0928b298306eb585b493
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502786"
---
# <span data-ttu-id="6cbd8-101">Get-AzureBatchNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="6cbd8-101">Get-AzureBatchNodeAgentSku</span></span>

## <span data-ttu-id="6cbd8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6cbd8-102">SYNOPSIS</span></span>
<span data-ttu-id="6cbd8-103">Ruft Batch-Knoten-Agent-SKUs in einem Batch Konto ab.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-103">Gets Batch node agent SKUs available in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cbd8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cbd8-104">SYNTAX</span></span>

```
Get-AzureBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cbd8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6cbd8-105">DESCRIPTION</span></span>
<span data-ttu-id="6cbd8-106">Das Cmdlet " **Get-AzureBatchNodeAgentSku** " ruft Knoten-Agent-SKUs ab, die in einem Azure-Batch Konto verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-106">The **Get-AzureBatchNodeAgentSku** cmdlet gets node agent SKUs that are available in an Azure Batch account.</span></span>
<span data-ttu-id="6cbd8-107">Geben Sie das Konto mithilfe des *batchcontext* -Parameters an.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-107">Specify the account by using the *BatchContext* parameter.</span></span>
<span data-ttu-id="6cbd8-108">Sie können Ihre Suche auf SKUs einschränken, die einem Open Data Protocol (OData)-Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-108">You can narrow your search to SKUs that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="6cbd8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6cbd8-109">EXAMPLES</span></span>

### <span data-ttu-id="6cbd8-110">Beispiel 1: Abrufen aller verfügbaren Knoten-Agent-SKUs</span><span class="sxs-lookup"><span data-stu-id="6cbd8-110">Example 1: Get all available node agent SKUs</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchNodeAgentSku -BatchContext $Context 
batch.node.centos 7 Linux {7.0, 7.1, 7.2, OL70} 
batch.node.debian 8 Linux {15.10, 8} 
batch.node.opensuse 13.2 Linux {13.2} 
batch.node.opensuse 42.1 Linux {42.1, 12, 12-SP1, 12} 
batch.node.ubuntu 14.04 Linux {14.04.0-LTS, 14.04.1-LTS, 14.04.2-LTS, 14.04.3-LTS...} 
batch.node.windows amd64 Windows {2008-R2-SP1, 2012-Datacenter, 2012-R2-Datacenter, Windows-Server-Technical-Preview}
```

<span data-ttu-id="6cbd8-111">Der erste Befehl ruft einen Batch Konto Kontext ab, der Zugriffstasten für Ihr Abonnement enthält, indem **Sie Get-AzureRmBatchAccountKeys** verwenden.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="6cbd8-112">Der Befehl speichert den Kontext in der $Context Variablen, die im nächsten Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-112">The command stores the context in the $Context variable to use in the next command.</span></span>

<span data-ttu-id="6cbd8-113">Der zweite Befehl ruft alle verfügbaren Knoten-Agent-SKUs ab, die von Batch unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-113">The second command gets all available node agent SKUs that Batch supports.</span></span>

## <span data-ttu-id="6cbd8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cbd8-114">PARAMETERS</span></span>

### <span data-ttu-id="6cbd8-115">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="6cbd8-115">-BatchContext</span></span>
<span data-ttu-id="6cbd8-116">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6cbd8-117">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="6cbd8-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="6cbd8-118">-Filter</span></span>
<span data-ttu-id="6cbd8-119">Gibt eine OData-Filterklausel für Knoten-Agent-SKUs an.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-119">Specifies an OData filter clause for node agent SKUs.</span></span>
<span data-ttu-id="6cbd8-120">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle von Batch unterstützten Knoten-Agent-SKUs zurück.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-120">If you do not specify a filter, this cmdlet returns all node agent SKUs that Batch supports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cbd8-121">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="6cbd8-121">-MaxCount</span></span>
<span data-ttu-id="6cbd8-122">Gibt die maximale Anzahl von Knoten-Agent-SKUs an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-122">Specifies the maximum number of node agent SKUs to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cbd8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cbd8-123">-DefaultProfile</span></span>
<span data-ttu-id="6cbd8-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cbd8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cbd8-125">CommonParameters</span></span>
<span data-ttu-id="6cbd8-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cbd8-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cbd8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cbd8-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6cbd8-128">INPUTS</span></span>

### <span data-ttu-id="6cbd8-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6cbd8-129">BatchAccountContext</span></span>
<span data-ttu-id="6cbd8-130">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="6cbd8-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="6cbd8-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6cbd8-131">OUTPUTS</span></span>

### <span data-ttu-id="6cbd8-132">Microsoft.Azure.Commands.Batch. Models. PSNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="6cbd8-132">Microsoft.Azure.Commands.Batch.Models.PSNodeAgentSku</span></span>

## <span data-ttu-id="6cbd8-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="6cbd8-133">NOTES</span></span>

## <span data-ttu-id="6cbd8-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6cbd8-134">RELATED LINKS</span></span>

[<span data-ttu-id="6cbd8-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6cbd8-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


