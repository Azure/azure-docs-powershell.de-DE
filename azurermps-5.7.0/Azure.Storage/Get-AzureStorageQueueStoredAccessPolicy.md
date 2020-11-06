---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: ebf5596ba63a86e3865c5a6dc05bdea648dc18c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496766"
---
# <span data-ttu-id="4cc4c-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4cc4c-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="4cc4c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4cc4c-102">SYNOPSIS</span></span>
<span data-ttu-id="4cc4c-103">Ruft die gespeicherte Zugriffsrichtlinie oder Richtlinien für eine Azure Storage-Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="4cc4c-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cc4c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cc4c-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="4cc4c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4cc4c-105">DESCRIPTION</span></span>
<span data-ttu-id="4cc4c-106">Das Cmdlet " **Get-AzureStorageQueueStoredAccessPolicy** " listet die gespeicherten Zugriffsrichtlinien oder Richtlinien für eine Azure-Speicherwarteschlange auf.</span><span class="sxs-lookup"><span data-stu-id="4cc4c-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="4cc4c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4cc4c-107">EXAMPLES</span></span>

### <span data-ttu-id="4cc4c-108">Beispiel 1: Abrufen einer gespeicherten Zugriffsrichtlinie in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="4cc4c-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="4cc4c-109">Dieser Befehl ruft die Access-Richtlinie mit dem Namen Policy12 in der Speicherwarteschlange mit dem Namen myQueue ab.</span><span class="sxs-lookup"><span data-stu-id="4cc4c-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="4cc4c-110">Beispiel 2: Abrufen aller gespeicherten Zugriffsrichtlinien in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="4cc4c-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="4cc4c-111">Dieser Befehl ruft alle gespeicherten Zugriffsrichtlinien in der Warteschlange mit dem Namen myQueue ab.</span><span class="sxs-lookup"><span data-stu-id="4cc4c-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="4cc4c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cc4c-112">PARAMETERS</span></span>

### <span data-ttu-id="4cc4c-113">-Context</span><span class="sxs-lookup"><span data-stu-id="4cc4c-113">-Context</span></span>
<span data-ttu-id="4cc4c-114">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="4cc4c-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="4cc4c-115">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4cc4c-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cc4c-116">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="4cc4c-116">-Policy</span></span>
<span data-ttu-id="4cc4c-117">Gibt eine Richtlinie für den gespeicherten Zugriff an, die die Berechtigungen für dieses SAS-Token (Shared Access Signature) enthält.</span><span class="sxs-lookup"><span data-stu-id="4cc4c-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cc4c-118">-Queue</span><span class="sxs-lookup"><span data-stu-id="4cc4c-118">-Queue</span></span>
<span data-ttu-id="4cc4c-119">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="4cc4c-119">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cc4c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc4c-120">CommonParameters</span></span>
<span data-ttu-id="4cc4c-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cc4c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc4c-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cc4c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc4c-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4cc4c-123">INPUTS</span></span>

### <span data-ttu-id="4cc4c-124">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4cc4c-124">IStorageContext</span></span>

<span data-ttu-id="4cc4c-125">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4cc4c-125">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="4cc4c-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4cc4c-126">String</span></span>

<span data-ttu-id="4cc4c-127">Der Parameter "Queue" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4cc4c-127">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="4cc4c-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4cc4c-128">OUTPUTS</span></span>

### <span data-ttu-id="4cc4c-129">Microsoft. WindowsAzure. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="4cc4c-129">Microsoft.WindowsAzure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="4cc4c-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="4cc4c-130">NOTES</span></span>

## <span data-ttu-id="4cc4c-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4cc4c-131">RELATED LINKS</span></span>

[<span data-ttu-id="4cc4c-132">Neu – AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4cc4c-132">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="4cc4c-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4cc4c-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="4cc4c-134">Satz-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4cc4c-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="4cc4c-135">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="4cc4c-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


