---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: fbd5adc202886ae987f7739ac24d1dadbc0d41d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933331"
---
# <span data-ttu-id="efa1a-101">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="efa1a-101">Get-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="efa1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efa1a-102">SYNOPSIS</span></span>
<span data-ttu-id="efa1a-103">Ruft die Richtlinie für den gespeicherten Zugriff oder die Richtlinien für eine Azure-Speicherwarteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="efa1a-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="efa1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="efa1a-104">SYNTAX</span></span>

```
Get-AzStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efa1a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="efa1a-105">DESCRIPTION</span></span>
<span data-ttu-id="efa1a-106">Im **Cmdlet Get-AzStorageQueueStoredAccessPolicy** werden die gespeicherten Zugriffsrichtlinien oder Richtlinien für eine Azure-Speicherwarteschlange aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="efa1a-106">The **Get-AzStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="efa1a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="efa1a-107">EXAMPLES</span></span>

### <span data-ttu-id="efa1a-108">Beispiel 1: Erhalten einer gespeicherten Zugriffsrichtlinie in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="efa1a-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="efa1a-109">Dieser Befehl ruft die Zugriffsrichtlinie mit dem Namen Policy12 in der Speicherwarteschlange mit dem Namen MyQueue ab.</span><span class="sxs-lookup"><span data-stu-id="efa1a-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="efa1a-110">Beispiel 2: Alle gespeicherten Zugriffsrichtlinien in der Warteschlange erhalten</span><span class="sxs-lookup"><span data-stu-id="efa1a-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="efa1a-111">Dieser Befehl ruft alle gespeicherten Zugriffsrichtlinien in der Warteschlange mit dem Namen MyQueue ab.</span><span class="sxs-lookup"><span data-stu-id="efa1a-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="efa1a-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="efa1a-112">PARAMETERS</span></span>

### <span data-ttu-id="efa1a-113">-Context</span><span class="sxs-lookup"><span data-stu-id="efa1a-113">-Context</span></span>
<span data-ttu-id="efa1a-114">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="efa1a-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="efa1a-115">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efa1a-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="efa1a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efa1a-116">-DefaultProfile</span></span>
<span data-ttu-id="efa1a-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="efa1a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa1a-118">-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="efa1a-118">-Policy</span></span>
<span data-ttu-id="efa1a-119">Gibt eine Richtlinie für den gespeicherten Zugriff an, die die Berechtigungen für dieses SAS-Token (Shared Access Signature) enthält.</span><span class="sxs-lookup"><span data-stu-id="efa1a-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="efa1a-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="efa1a-120">-Queue</span></span>
<span data-ttu-id="efa1a-121">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="efa1a-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="efa1a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efa1a-122">CommonParameters</span></span>
<span data-ttu-id="efa1a-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efa1a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efa1a-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efa1a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efa1a-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="efa1a-125">INPUTS</span></span>

### <span data-ttu-id="efa1a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="efa1a-126">System.String</span></span>

### <span data-ttu-id="efa1a-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="efa1a-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="efa1a-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="efa1a-128">OUTPUTS</span></span>

### <span data-ttu-id="efa1a-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="efa1a-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="efa1a-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="efa1a-130">NOTES</span></span>

## <span data-ttu-id="efa1a-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="efa1a-131">RELATED LINKS</span></span>

[<span data-ttu-id="efa1a-132">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="efa1a-132">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="efa1a-133">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="efa1a-133">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="efa1a-134">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="efa1a-134">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="efa1a-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="efa1a-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


