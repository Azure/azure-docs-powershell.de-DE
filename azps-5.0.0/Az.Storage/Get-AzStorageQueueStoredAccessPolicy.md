---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: b1e7f305b571c5b40c12dacadf520f9637e076f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176547"
---
# <span data-ttu-id="72db2-101">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="72db2-101">Get-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="72db2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72db2-102">SYNOPSIS</span></span>
<span data-ttu-id="72db2-103">Ruft die gespeicherte Zugriffsrichtlinie oder Richtlinien für eine Azure Storage-Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="72db2-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="72db2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72db2-104">SYNTAX</span></span>

```
Get-AzStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72db2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72db2-105">DESCRIPTION</span></span>
<span data-ttu-id="72db2-106">Das Cmdlet " **Get-AzStorageQueueStoredAccessPolicy** " listet die gespeicherten Zugriffsrichtlinien oder Richtlinien für eine Azure-Speicherwarteschlange auf.</span><span class="sxs-lookup"><span data-stu-id="72db2-106">The **Get-AzStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="72db2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72db2-107">EXAMPLES</span></span>

### <span data-ttu-id="72db2-108">Beispiel 1: Abrufen einer gespeicherten Zugriffsrichtlinie in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="72db2-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="72db2-109">Dieser Befehl ruft die Access-Richtlinie mit dem Namen Policy12 in der Speicherwarteschlange mit dem Namen myQueue ab.</span><span class="sxs-lookup"><span data-stu-id="72db2-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="72db2-110">Beispiel 2: Abrufen aller gespeicherten Zugriffsrichtlinien in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="72db2-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="72db2-111">Dieser Befehl ruft alle gespeicherten Zugriffsrichtlinien in der Warteschlange mit dem Namen myQueue ab.</span><span class="sxs-lookup"><span data-stu-id="72db2-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="72db2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="72db2-112">PARAMETERS</span></span>

### <span data-ttu-id="72db2-113">-Context</span><span class="sxs-lookup"><span data-stu-id="72db2-113">-Context</span></span>
<span data-ttu-id="72db2-114">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="72db2-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="72db2-115">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="72db2-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="72db2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72db2-116">-DefaultProfile</span></span>
<span data-ttu-id="72db2-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="72db2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72db2-118">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="72db2-118">-Policy</span></span>
<span data-ttu-id="72db2-119">Gibt eine Richtlinie für den gespeicherten Zugriff an, die die Berechtigungen für dieses SAS-Token (Shared Access Signature) enthält.</span><span class="sxs-lookup"><span data-stu-id="72db2-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="72db2-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="72db2-120">-Queue</span></span>
<span data-ttu-id="72db2-121">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="72db2-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="72db2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72db2-122">CommonParameters</span></span>
<span data-ttu-id="72db2-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72db2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72db2-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72db2-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72db2-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72db2-125">INPUTS</span></span>

### <span data-ttu-id="72db2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="72db2-126">System.String</span></span>

### <span data-ttu-id="72db2-127">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="72db2-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="72db2-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72db2-128">OUTPUTS</span></span>

### <span data-ttu-id="72db2-129">Microsoft. Azure. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="72db2-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="72db2-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="72db2-130">NOTES</span></span>

## <span data-ttu-id="72db2-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72db2-131">RELATED LINKS</span></span>

[<span data-ttu-id="72db2-132">Neu – AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="72db2-132">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="72db2-133">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="72db2-133">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="72db2-134">Satz-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="72db2-134">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="72db2-135">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="72db2-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


