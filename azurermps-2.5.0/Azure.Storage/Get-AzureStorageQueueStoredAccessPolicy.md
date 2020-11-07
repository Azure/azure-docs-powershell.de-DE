---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 9ef4be8331c1de38789d25903db9e98f4e2d8cd1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848576"
---
# <span data-ttu-id="4a1b2-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4a1b2-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="4a1b2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4a1b2-102">SYNOPSIS</span></span>
<span data-ttu-id="4a1b2-103">Ruft die gespeicherte Zugriffsrichtlinie oder Richtlinien für eine Azure Storage-Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="4a1b2-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a1b2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a1b2-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a1b2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a1b2-105">DESCRIPTION</span></span>
<span data-ttu-id="4a1b2-106">Das Cmdlet " **Get-AzureStorageQueueStoredAccessPolicy** " listet die gespeicherten Zugriffsrichtlinien oder Richtlinien für eine Azure-Speicherwarteschlange auf.</span><span class="sxs-lookup"><span data-stu-id="4a1b2-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="4a1b2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a1b2-107">EXAMPLES</span></span>

### <span data-ttu-id="4a1b2-108">Beispiel 1: Abrufen einer gespeicherten Zugriffsrichtlinie in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="4a1b2-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="4a1b2-109">Dieser Befehl ruft die Access-Richtlinie mit dem Namen Policy12 in der Speicherwarteschlange mit dem Namen myQueue ab.</span><span class="sxs-lookup"><span data-stu-id="4a1b2-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="4a1b2-110">Beispiel 2: Abrufen aller gespeicherten Zugriffsrichtlinien in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="4a1b2-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="4a1b2-111">Dieser Befehl ruft alle gespeicherten Zugriffsrichtlinien in der Warteschlange mit dem Namen myQueue ab.</span><span class="sxs-lookup"><span data-stu-id="4a1b2-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="4a1b2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a1b2-112">PARAMETERS</span></span>

### <span data-ttu-id="4a1b2-113">-Context</span><span class="sxs-lookup"><span data-stu-id="4a1b2-113">-Context</span></span>
<span data-ttu-id="4a1b2-114">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="4a1b2-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="4a1b2-115">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4a1b2-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a1b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a1b2-116">-DefaultProfile</span></span>
<span data-ttu-id="4a1b2-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4a1b2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a1b2-118">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="4a1b2-118">-Policy</span></span>
<span data-ttu-id="4a1b2-119">Gibt eine Richtlinie für den gespeicherten Zugriff an, die die Berechtigungen für dieses SAS-Token (Shared Access Signature) enthält.</span><span class="sxs-lookup"><span data-stu-id="4a1b2-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="4a1b2-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="4a1b2-120">-Queue</span></span>
<span data-ttu-id="4a1b2-121">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="4a1b2-121">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a1b2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a1b2-122">CommonParameters</span></span>
<span data-ttu-id="4a1b2-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a1b2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a1b2-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a1b2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a1b2-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4a1b2-125">INPUTS</span></span>

### <span data-ttu-id="4a1b2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4a1b2-126">System.String</span></span>

### <span data-ttu-id="4a1b2-127">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4a1b2-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4a1b2-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4a1b2-128">OUTPUTS</span></span>

### <span data-ttu-id="4a1b2-129">Microsoft. WindowsAzure. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="4a1b2-129">Microsoft.WindowsAzure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="4a1b2-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="4a1b2-130">NOTES</span></span>

## <span data-ttu-id="4a1b2-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4a1b2-131">RELATED LINKS</span></span>

[<span data-ttu-id="4a1b2-132">Neu – AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4a1b2-132">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="4a1b2-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4a1b2-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="4a1b2-134">Satz-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4a1b2-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="4a1b2-135">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="4a1b2-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


