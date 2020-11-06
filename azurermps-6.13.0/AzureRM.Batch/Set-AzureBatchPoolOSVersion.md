---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpoolosversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
ms.openlocfilehash: d85e0ca61b86e523c6d73ea8d2349d7d692aafb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501198"
---
# <span data-ttu-id="19e54-101">Set-AzureBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="19e54-101">Set-AzureBatchPoolOSVersion</span></span>

## <span data-ttu-id="19e54-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19e54-102">SYNOPSIS</span></span>
<span data-ttu-id="19e54-103">Ändert die Betriebssystemversion des angegebenen Pools.</span><span class="sxs-lookup"><span data-stu-id="19e54-103">Changes the operating system version of the specified pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19e54-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19e54-104">SYNTAX</span></span>

```
Set-AzureBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19e54-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19e54-105">DESCRIPTION</span></span>
<span data-ttu-id="19e54-106">Das Cmdlet " **Satz-AzureBatchPoolOSVersion** " ändert die Betriebssystemversion des angegebenen Pools.</span><span class="sxs-lookup"><span data-stu-id="19e54-106">The **Set-AzureBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="19e54-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19e54-107">EXAMPLES</span></span>

### <span data-ttu-id="19e54-108">Beispiel 1: Einrichten der Zielbetriebssystem-Version eines Pools</span><span class="sxs-lookup"><span data-stu-id="19e54-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzureBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="19e54-109">Mit diesem Befehl wird die Zielbetriebssystem-Version des Pools MyPool auf WA-Guest-OS-4.20 _201505-01 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="19e54-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="19e54-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="19e54-110">PARAMETERS</span></span>

### <span data-ttu-id="19e54-111">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="19e54-111">-BatchContext</span></span>
<span data-ttu-id="19e54-112">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="19e54-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="19e54-113">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="19e54-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="19e54-114">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="19e54-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="19e54-115">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="19e54-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="19e54-116">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="19e54-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="19e54-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19e54-117">-DefaultProfile</span></span>
<span data-ttu-id="19e54-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="19e54-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19e54-119">-ID</span><span class="sxs-lookup"><span data-stu-id="19e54-119">-Id</span></span>
<span data-ttu-id="19e54-120">Gibt die ID des Pools an.</span><span class="sxs-lookup"><span data-stu-id="19e54-120">Specifies the ID of the pool.</span></span>

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

### <span data-ttu-id="19e54-121">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="19e54-121">-TargetOSVersion</span></span>
<span data-ttu-id="19e54-122">Gibt die Azure Guest-Betriebssystemversion an, die auf den virtuellen Computern im Pool installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="19e54-122">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="19e54-123">Weitere Informationen zu Azure Guest-Betriebssystemversionen finden Sie unter Azure Guest OS Releases und SDK Compatibility Matrix https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ ( https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="19e54-123">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

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

### <span data-ttu-id="19e54-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19e54-124">CommonParameters</span></span>
<span data-ttu-id="19e54-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19e54-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19e54-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19e54-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19e54-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19e54-127">INPUTS</span></span>

### <span data-ttu-id="19e54-128">System. String</span><span class="sxs-lookup"><span data-stu-id="19e54-128">System.String</span></span>

### <span data-ttu-id="19e54-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="19e54-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="19e54-130">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="19e54-130">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="19e54-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19e54-131">OUTPUTS</span></span>

### <span data-ttu-id="19e54-132">System. void</span><span class="sxs-lookup"><span data-stu-id="19e54-132">System.Void</span></span>

## <span data-ttu-id="19e54-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="19e54-133">NOTES</span></span>

## <span data-ttu-id="19e54-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19e54-134">RELATED LINKS</span></span>

[<span data-ttu-id="19e54-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="19e54-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


