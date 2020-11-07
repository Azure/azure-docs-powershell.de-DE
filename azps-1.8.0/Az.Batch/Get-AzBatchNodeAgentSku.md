---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodeagentsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeAgentSku.md
ms.openlocfilehash: 8f7228a540456e76e4f7a22d70d00969a9ef568c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93662090"
---
# <span data-ttu-id="b4936-101">Get-AzBatchNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="b4936-101">Get-AzBatchNodeAgentSku</span></span>

## <span data-ttu-id="b4936-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4936-102">SYNOPSIS</span></span>
<span data-ttu-id="b4936-103">Ruft Batch-Knoten-Agent-SKUs in einem Batch Konto ab.</span><span class="sxs-lookup"><span data-stu-id="b4936-103">Gets Batch node agent SKUs available in a Batch account.</span></span>

## <span data-ttu-id="b4936-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4936-104">SYNTAX</span></span>

```
Get-AzBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4936-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4936-105">DESCRIPTION</span></span>
<span data-ttu-id="b4936-106">Das Cmdlet " **Get-AzBatchNodeAgentSku** " ruft Knoten-Agent-SKUs ab, die in einem Azure-Batch Konto verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b4936-106">The **Get-AzBatchNodeAgentSku** cmdlet gets node agent SKUs that are available in an Azure Batch account.</span></span>
<span data-ttu-id="b4936-107">Geben Sie das Konto mithilfe des *batchcontext* -Parameters an.</span><span class="sxs-lookup"><span data-stu-id="b4936-107">Specify the account by using the *BatchContext* parameter.</span></span>
<span data-ttu-id="b4936-108">Sie können Ihre Suche auf SKUs einschränken, die einem Open Data Protocol (OData)-Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b4936-108">You can narrow your search to SKUs that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="b4936-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4936-109">EXAMPLES</span></span>

### <span data-ttu-id="b4936-110">Beispiel 1: Abrufen aller verfügbaren Knoten-Agent-SKUs</span><span class="sxs-lookup"><span data-stu-id="b4936-110">Example 1: Get all available node agent SKUs</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchNodeAgentSku -BatchContext $Context 
batch.node.centos 7 Linux {7.0, 7.1, 7.2, OL70} 
batch.node.debian 8 Linux {15.10, 8} 
batch.node.opensuse 13.2 Linux {13.2} 
batch.node.opensuse 42.1 Linux {42.1, 12, 12-SP1, 12} 
batch.node.ubuntu 14.04 Linux {14.04.0-LTS, 14.04.1-LTS, 14.04.2-LTS, 14.04.3-LTS...} 
batch.node.windows amd64 Windows {2008-R2-SP1, 2012-Datacenter, 2012-R2-Datacenter, Windows-Server-Technical-Preview}
```

<span data-ttu-id="b4936-111">Der erste Befehl ruft einen Batch Konto Kontext ab, der Zugriffstasten für Ihr Abonnement enthält, indem **Sie Get-AzBatchAccountKeys** verwenden.</span><span class="sxs-lookup"><span data-stu-id="b4936-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="b4936-112">Der Befehl speichert den Kontext in der $Context Variablen, die im nächsten Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b4936-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="b4936-113">Der zweite Befehl ruft alle verfügbaren Knoten-Agent-SKUs ab, die von Batch unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b4936-113">The second command gets all available node agent SKUs that Batch supports.</span></span>

## <span data-ttu-id="b4936-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4936-114">PARAMETERS</span></span>

### <span data-ttu-id="b4936-115">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="b4936-115">-BatchContext</span></span>
<span data-ttu-id="b4936-116">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="b4936-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b4936-117">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b4936-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b4936-118">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b4936-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b4936-119">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="b4936-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b4936-120">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="b4936-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b4936-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4936-121">-DefaultProfile</span></span>
<span data-ttu-id="b4936-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b4936-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4936-123">-Filter</span><span class="sxs-lookup"><span data-stu-id="b4936-123">-Filter</span></span>
<span data-ttu-id="b4936-124">Gibt eine OData-Filterklausel für Knoten-Agent-SKUs an.</span><span class="sxs-lookup"><span data-stu-id="b4936-124">Specifies an OData filter clause for node agent SKUs.</span></span>
<span data-ttu-id="b4936-125">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle von Batch unterstützten Knoten-Agent-SKUs zurück.</span><span class="sxs-lookup"><span data-stu-id="b4936-125">If you do not specify a filter, this cmdlet returns all node agent SKUs that Batch supports.</span></span>

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

### <span data-ttu-id="b4936-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b4936-126">-MaxCount</span></span>
<span data-ttu-id="b4936-127">Gibt die maximale Anzahl von Knoten-Agent-SKUs an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b4936-127">Specifies the maximum number of node agent SKUs to return.</span></span>

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

### <span data-ttu-id="b4936-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4936-128">CommonParameters</span></span>
<span data-ttu-id="b4936-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4936-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4936-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4936-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4936-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4936-131">INPUTS</span></span>

### <span data-ttu-id="b4936-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b4936-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b4936-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4936-133">OUTPUTS</span></span>

### <span data-ttu-id="b4936-134">Microsoft.Azure.Commands.Batch. Models. PSNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="b4936-134">Microsoft.Azure.Commands.Batch.Models.PSNodeAgentSku</span></span>

## <span data-ttu-id="b4936-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4936-135">NOTES</span></span>

## <span data-ttu-id="b4936-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4936-136">RELATED LINKS</span></span>

[<span data-ttu-id="b4936-137">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b4936-137">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)


